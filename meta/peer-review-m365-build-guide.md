# M365 Peer Review System — Build Guide
## Design Foundations Library

**Last updated:** 2026-08-26
**Estimated build time:** 3–4 hours across multiple sessions
**License requirement:** Microsoft 365 E1/E3/E5 (all connectors used are standard — no premium Power Automate license required)

This guide builds the peer review infrastructure described in `meta/peer-review-policy.md`. Read that document first — it defines the thresholds, phased recruitment strategy, and review flow this guide implements.

---

## Architecture overview

```
SharePoint List (Library Review Tracker)
        ↑ writes              ↓ reads
 Power Automate          Review Gallery         Eric's Dashboard
   Feedback Flow         (Gallery view —        (List rollup view)
   Weekly Digest         direct link to list)
        ↓ posts
   Teams channels
        ↑ triggers
 Microsoft Forms
  (Feedback Form only)
```

**Data flows in one direction:** Form → Power Automate → SharePoint List. Everything else reads from the List. The List is the single source of truth. No claiming step — reviews are first-come-first-served. Submit the form, the counter increments, the status updates.

---

## Conventions used in this guide

- **[SP Site]** = your SharePoint site URL
- **[PA]** = Power Automate (make.powerautomate.com)
- **[Form]** = Microsoft Forms (forms.office.com)
- **✓ Verify** = checkpoint — confirm this before proceeding to the next step
- **⚠ Gotcha** = known failure mode confirmed in M365 documentation

---

## Phase 1 — Preparation (30 minutes)

### Step 1.1 — Inventory your articles

Before building anything, create a spreadsheet with every article that needs peer review. Columns: Article ID (e.g., 103), Title, Tier (T100/T200/T300), Topic Tag, Goal Line (your subtitle text — appears on Gallery cards and in Teams digest), SharePoint page URL (leave blank until pages are built), Minimum reviews required (1/2/3), Ceiling (2/3/4).

This list must be complete before building the SharePoint List, because article IDs and topic tags become the schema.

### Step 1.2 — Confirm your topic taxonomy

Decide your topic tags now. They cannot change later without cascading updates to the List and Forms dropdown. Based on the current library: Prototyping, Research, Facilitation, AI, Assumptions, Personas, Story Mapping. Confirm this is the complete set before proceeding.

### Step 1.3 — Confirm license access

Everything in this guide uses standard connectors. Verify your M365 tenant has:
- Power Automate (included in E1/E3/E5 — confirm with IT admin if unsure)
- Microsoft Forms (included in all M365 plans)
- SharePoint Online (included in all M365 plans)

**✓ Verify:** sign into make.powerautomate.com and confirm you can create a new flow. Sign into forms.office.com and confirm you can create a new form. Resolve any access issues with IT before continuing.

---

## Phase 2 — SharePoint List (30 minutes)

This is the data layer. Everything reads from and writes to this List.

### Step 2.1 — Create the List

Navigate to your SharePoint site → New → List. Name it: `Library Review Tracker`. If SharePoint auto-generates an internal name with spaces, rename immediately under List Settings → List name.

### Step 2.2 — Rename the default Title column

Go to List Settings → Columns → Title → rename to `Article Title`. You cannot delete the Title column, but renaming prevents confusion with your other columns.

### Step 2.3 — Add all columns in this exact order

Use names without spaces — this avoids the `_x0020_` encoding problem in Power Automate OData filter expressions.

| Column name (internal) | Type | Settings |
|---|---|---|
| ArticleID | Number | Required. No decimal places. |
| Tier | Choice | T100 / T200 / T300. Required. |
| TopicTag | Choice | Your confirmed taxonomy. Required. Single value only. |
| GoalLine | Single line of text | The subtitle — appears on Gallery cards and in Adaptive Cards. Must be single line; multi-line text columns do not display in Gallery view. |
| MinReviews | Number | Required. Default: 1. |
| Ceiling | Number | Required. Default: 2. |
| ReviewCount | Number | Default: 0. Updated by Power Automate Feedback Flow on each submission. |
| Status | Calculated | `=IF(ReviewCount>=Ceiling,"Closed",IF(ReviewCount>=MinReviews,"Ready to Publish","Needs Review"))` — recalculates automatically each time Power Automate updates ReviewCount. |
| ArticlePageURL | Hyperlink | Populate after article pages exist. |
| FeedbackFormURL | Single line of text | Populate in Phase 5 after form pre-fill URLs exist. |
| Notes | Multiple lines of text | Eric's use only. Does not appear on Gallery cards. |

⚠ **Gotcha — calculated column internal names:** SharePoint uses internal names in formulas. If you named columns without spaces, the formula uses the name directly (e.g., `ReviewCount`). If you used spaces, the internal name encodes them. Using no-space column names from the start avoids this entirely.

⚠ **Gotcha — GoalLine must be single line:** SharePoint Gallery view does not display multi-line text columns on cards — they are invisible regardless of configuration. Keep GoalLine as single line of text and write short subtitles (under 120 characters).

### Step 2.4 — Populate the List with all articles

Add one row per article. Fill ArticleID, Article Title, Tier, TopicTag, GoalLine, MinReviews, Ceiling. Leave ReviewCount at 0. Leave URL columns blank.

**✓ Verify:** Status calculated column shows "Needs Review" for every row. ReviewCount shows 0. If Status shows an error, the formula references a wrong internal column name — inspect the column's internal name under List Settings → column → URL, and fix the formula.

### Step 2.5 — Create named views

Create these named views (List → All Items dropdown → Create new view):

- **Gallery** — Gallery layout. Filter: Status does not equal "Closed" and Status does not equal "Published." This is the public-facing review gallery. See Phase 3 for formatting.
- **Eric's Dashboard** — Standard layout, all columns, grouped by Status, sorted by ArticleID. Your management view.
- **Needs Review** — Standard layout, filter: Status equals "Needs Review." Feeds the Power Automate weekly digest.
- **Ready to Publish** — Standard layout, filter: Status equals "Ready to Publish." Shows what's cleared for publication.

**✓ Verify:** Gallery view shows all articles. Needs Review view shows all articles. Ready to Publish view is empty. All correct.

---

## Phase 3 — Gallery View Formatting (45 minutes)

The Gallery view is the public-facing review page. Reviewers land here, scan open articles, and click through to the one they want to read and review. The card formatting makes the slot count and urgency visible at a glance.

### Step 3.1 — Access the Gallery view formatter

Open the Library Review Tracker list. Switch to the Gallery view you created in Phase 2. Click **View options** (top right) → **Format current view**. In the formatting panel, select **Advanced mode**.

⚠ **Gotcha — different schema from column formatting:** Gallery view uses the tile-formatting schema, not the standard column-formatting schema. The root-level structure differs. Do not copy column formatting JSON directly — use the template below.

### Step 3.2 — Apply the card JSON

Paste this JSON into the Advanced mode panel. It renders each card with a color-coded left border by Status, shows tier, topic, goal line, slots remaining, and a direct link to the article page and feedback form.

```json
{
  "$schema": "https://developer.microsoft.com/json-schemas/sp/v2/tile-formatting.schema.json",
  "height": 220,
  "hideSelection": true,
  "formatter": {
    "elmType": "div",
    "style": {
      "display": "flex",
      "flex-direction": "row",
      "border-radius": "4px",
      "overflow": "hidden",
      "border": "1px solid #e5e7eb",
      "height": "100%"
    },
    "children": [
      {
        "elmType": "div",
        "style": {
          "width": "6px",
          "flex-shrink": "0",
          "background-color": "=if([$Status] == 'Needs Review', '#f59e0b', if([$Status] == 'Ready to Publish', '#22c55e', '#9ca3af'))"
        }
      },
      {
        "elmType": "div",
        "style": {
          "padding": "12px 14px",
          "display": "flex",
          "flex-direction": "column",
          "gap": "6px",
          "flex": "1",
          "overflow": "hidden"
        },
        "children": [
          {
            "elmType": "div",
            "style": {
              "font-size": "11px",
              "font-weight": "600",
              "color": "#6b7280",
              "text-transform": "uppercase",
              "letter-spacing": "0.05em"
            },
            "txtContent": "=[$Tier] + ' · ' + [$TopicTag]"
          },
          {
            "elmType": "div",
            "style": {
              "font-size": "15px",
              "font-weight": "600",
              "color": "#111827",
              "line-height": "1.3"
            },
            "txtContent": "[$Article Title]"
          },
          {
            "elmType": "div",
            "style": {
              "font-size": "13px",
              "color": "#4b5563",
              "line-height": "1.4",
              "overflow": "hidden",
              "text-overflow": "ellipsis"
            },
            "txtContent": "[$GoalLine]"
          },
          {
            "elmType": "div",
            "style": {
              "margin-top": "auto",
              "font-size": "12px",
              "font-weight": "600",
              "color": "=if(sub([$Ceiling], [$ReviewCount]) <= 1, '#dc2626', '#374151')"
            },
            "txtContent": "=if(sub([$Ceiling], [$ReviewCount]) == 1, '1 slot remaining', toString(sub([$Ceiling], [$ReviewCount])) + ' slots remaining')"
          },
          {
            "elmType": "a",
            "style": {
              "font-size": "12px",
              "color": "#2563eb",
              "text-decoration": "none"
            },
            "attributes": {
              "href": "[$ArticlePageURL.URL]",
              "target": "_blank"
            },
            "txtContent": "Read & review →"
          }
        ]
      }
    ]
  }
}
```

**Color key:** amber left border = Needs Review, green = Ready to Publish (still accepting reviews). Slot count turns red when only 1 slot remains.

⚠ **Gotcha — web part embed bug:** do NOT embed the Gallery view as a List web part on a SharePoint page. A confirmed SharePoint bug causes Title and date fields to display twice per card when Gallery view is embedded as a web part. Instead, link directly to the list's Gallery view URL. Copy the URL of the Gallery view from the browser address bar after switching to it — this is your review gallery link.

**✓ Verify:** Gallery view cards show tier, topic tag, title, goal line, and slots remaining. Border colors reflect Status correctly. "Read & review" link opens the article page.

---

## Phase 4 — Microsoft Forms: Feedback Form (30 minutes)

One form. Reviewers fill this out after reading an article. No claiming step — this is the only form in the system.

### Step 4.1 — Create the Feedback Form

Go to forms.office.com → New Form. Title: `Peer Review — Design Foundations Library`.

| Question | Type | Settings |
|---|---|---|
| Which article are you reviewing? | Dropdown | Every article as "ID — Title" (e.g., "103 — Attachment Is the Real Risk"). Required. This field will be pre-filled via URL. |
| Your role | Choice | PM / Custom Dev / Non-Custom Dev / UX / Other. Required. Single answer. |
| What worked — what landed clearly and why | Paragraph | Required. |
| What didn't work — what confused you, made you want to skip, or felt off | Paragraph | Required. |
| Comprehension check: in your own words, what is the main thing this piece is saying? | Paragraph | Required. |
| Would you forward this to a colleague? Who, and why? | Paragraph | Not required. |
| Any topics you'd especially like to review in future? | Checkboxes | Your full topic taxonomy. Not required. Passive interest capture for topic notifications — populated in the Reviewer Interests List by the Feedback Flow. |

Under Settings: enable **Require sign-in** (captures AAD email automatically, reduces entry friction). Set **One response per person** to OFF — same person may review multiple articles. Enable **Show progress bar**.

The comprehension check (question 5) is the most diagnostic. A wrong answer means the concept didn't transfer regardless of how engaging the piece felt.

**✓ Verify:** preview the form. All questions appear in order, required fields marked, article dropdown includes every article.

---

## Phase 5 — Pre-fill URLs (30 minutes)

Generates per-article form URLs that pre-select the correct article in the feedback form. Must be done manually via the Microsoft Forms GUI — programmatic URL construction is not officially supported and the encoding format is fragile.

### Step 5.1 — How pre-fill URLs work

Microsoft Forms pre-fill uses a base64-encoded JSON payload in the URL's `r=` parameter. The only supported way to generate these is the GUI.

### Step 5.2 — Generate pre-filled Feedback Form URLs

Open the Feedback Form. Click the three-dot menu (…) at top right → **Get pre-filled link**. The form opens in an authoring mode where you fill in answers.

For each article:
1. Select that article in the "Which article" dropdown
2. Leave all other fields blank
3. Click **Copy link** at the bottom
4. Paste the URL into your spreadsheet in the FeedbackFormURL column
5. Clear the selection and repeat for the next article

⚠ **Gotcha — URL integrity:** do not edit the generated URL manually. Do not run it through a URL shortener. Test each URL in an incognito window before storing it.

### Step 5.3 — Update the SharePoint List

For each article row in Library Review Tracker, paste the FeedbackFormURL value into the FeedbackFormURL column.

**✓ Verify:** open three pre-fill URLs from different tiers. Each pre-selects the correct article in the form.

---

## Phase 6 — Power Automate: Feedback Flow (30 minutes)

Listens for Feedback Form submissions. Increments the review count, updates status, notifies Eric, and captures the reviewer's topic interests.

### Step 6.1 — Create the flow

Automated cloud flow. Name: `Library Review — Feedback Submitted`. Trigger: **"When a new response is submitted"** (Microsoft Forms). Select your Feedback Form.

### Step 6.2 — Get response details (mandatory)

Add action: **"Get response details"** (Microsoft Forms). Form ID: Feedback Form. Response ID: dynamic `Response Id` from trigger.

⚠ **Gotcha — trigger contains no answer data:** the trigger fires with a Response ID only. You must always follow it with "Get response details" to access the actual answers. This is the most common Power Automate + Forms error.

### Step 6.3 — Get the matching List item

Add action: **"Get items"** (SharePoint). Site: [SP Site]. List: Library Review Tracker. Filter Query:

```
ArticleID eq [number extracted from the article dropdown answer]
```

The dropdown answer returns a string like "103 — Attachment Is the Real Risk." Extract just the number with the expression: `int(first(split(body('Get_response_details')?['r[question_id]'], ' ')))` — find the question ID by running the flow once and inspecting Get response details output. Alternatively, add ArticleID as a hidden question and use its value directly — simpler and more reliable.

Top Count: 1.

### Step 6.4 — Increment ReviewCount

Add action: **"Update item"** (SharePoint). Site: [SP Site]. List: Library Review Tracker. ID: the item ID from Get items. Set ReviewCount to:

```
add(first(outputs('Get_items')?['body/value'])?['ReviewCount'], 1)
```

This reads the current ReviewCount from the item and adds 1. SharePoint recalculates the Status column automatically when the item is saved.

### Step 6.5 — Check if ceiling is hit

Add a **Get item** action after the update to read the refreshed Status value. Add a Condition: if Status equals "Closed," send Eric an email: "[Article Title] has reached its review ceiling. Update the 'Reviewed by' section on the article page."

### Step 6.6 — Send Eric the full response

Send email to Eric with: article title, reviewer name, reviewer role, all four substantive answers verbatim, and the comprehension check response highlighted. Eric reads this immediately — no dashboard required for individual responses.

### Step 6.7 — Capture topic interests (optional but recommended)

If the reviewer selected any topics in question 7, create an item in a Reviewer Interests List (two columns: ReviewerEmail, Topics choice multi-select). First check whether a row already exists for this email using Get items with filter `ReviewerEmail eq '[email]'` — if yes, update the existing row; if no, create a new one.

This list feeds the topic notification logic in Phase 8.

**✓ Verify:** submit a test feedback response. Confirm ReviewCount increments in the List, Status updates correctly, Eric receives the full response email.

---

## Phase 7 — Power Automate: Weekly Teams Digest (45 minutes)

Posts Adaptive Cards to Teams channels for articles still needing reviewers. Runs automatically on a schedule. **Most useful in weeks 5–8 when the open inventory is small enough for the list to feel actionable** — see phased recruitment strategy in the policy doc.

### Step 7.1 — Create the flow

Scheduled cloud flow. Name: `Library Review — Weekly Digest`. Recurrence: weekly, Monday, 9:00 AM.

### Step 7.2 — Get articles needing reviewers

**"Get items"** (SharePoint). List: Library Review Tracker. Filter Query: `Status eq 'Needs Review'`. Order by ArticleID ascending.

### Step 7.3 — Get count of open pieces

Add a **Compose** action to count the items: `length(outputs('Get_items')?['body/value'])`. This count drives the card format switch.

### Step 7.4 — Conditional card format (traffic management)

Add a **Condition**: if the open piece count is less than or equal to 10.

- **If yes (tail phase — ≤10 pieces):** post a single summary card listing all remaining pieces by name. Format: one card with a bulleted list of open article titles, slot counts, and links. Makes the short list feel urgent and closeable.
- **If no (early/mid phase — >10 pieces):** post one card per article in an **Apply to each** loop (see Step 7.5).

### Step 7.5 — Per-article card (early/mid phase)

Inside the Apply to each on the Get items output, add: **"Post your own adaptive card as the Flow bot to a channel"** (Microsoft Teams connector).

⚠ **Critical — do NOT use "Post and wait for a response":** the "wait" variant pauses the entire flow after the first card is submitted. For a digest posting multiple cards, this halts all subsequent posts. Use the non-waiting variant. Linking to the feedback form happens in the card via Action.OpenUrl only.

⚠ **Gotcha — Workflows app required:** the Adaptive Card post action requires the Microsoft Workflows app installed in the target Teams channel. Confirm with your Teams admin before testing.

**Per-article Adaptive Card JSON:**

```json
{
  "type": "AdaptiveCard",
  "version": "1.4",
  "body": [
    {
      "type": "TextBlock",
      "text": "PEER REVIEW NEEDED",
      "size": "Small",
      "weight": "Bolder",
      "color": "Warning",
      "spacing": "None"
    },
    {
      "type": "TextBlock",
      "text": "@{items('Apply_to_each')?['Article Title']}",
      "size": "Large",
      "weight": "Bolder",
      "wrap": true
    },
    {
      "type": "TextBlock",
      "text": "@{items('Apply_to_each')?['GoalLine']}",
      "wrap": true,
      "spacing": "Small"
    },
    {
      "type": "FactSet",
      "facts": [
        {
          "title": "Tier",
          "value": "@{items('Apply_to_each')?['Tier']?['Value']}"
        },
        {
          "title": "Topic",
          "value": "@{items('Apply_to_each')?['TopicTag']?['Value']}"
        },
        {
          "title": "Slots remaining",
          "value": "@{sub(items('Apply_to_each')?['Ceiling'], items('Apply_to_each')?['ReviewCount'])}"
        }
      ]
    }
  ],
  "actions": [
    {
      "type": "Action.OpenUrl",
      "title": "Read & review →",
      "url": "@{items('Apply_to_each')?['ArticlePageURL']?['Url']}"
    }
  ]
}
```

### Step 7.6 — Route cards to correct channels

Add a Switch action inside the loop to post to the topic-relevant Teams channel based on TopicTag. Also post all cards to a general library channel. Hardcode channel names in the flow — there is no dynamic channel lookup without premium connectors.

**✓ Verify:** run the flow manually. Cards appear in correct channels. Button opens the correct article page. When open count is ≤10, a single summary card appears instead of per-article cards.

---

## Phase 8 — Power Automate: Topic Interest Notifications (30 minutes)

Sends personalized notifications when articles matching a reviewer's interests need reviewers. Replaces the retired SharePoint Alerts feature (fully retired July 2026).

### Step 8.1 — Create the Reviewer Interests List

New SharePoint List: `Reviewer Interests`. Columns: ReviewerEmail (single line of text, required), Topics (choice, multi-select, same taxonomy as Library Review Tracker).

This list is populated by the Feedback Flow (Phase 6, Step 6.7) when reviewers select topic interests in the form.

### Step 8.2 — Add topic notification inside the weekly digest flow

Inside the Apply to each loop (Phase 7, Step 7.5), after posting the Adaptive Card, add:

1. **"Get items"** from Reviewer Interests — retrieve all rows (no OData filter — see gotcha below)
2. **"Filter array"** (Data Operations) — filter where the Topics field contains the current article's TopicTag value
3. **"Apply to each"** on the filtered array — send each matching reviewer a Teams direct message or email with article title, goal line, and article page URL

⚠ **Gotcha — multi-select OData filter not supported:** you cannot filter a multi-value choice column server-side via OData in SharePoint. Retrieve all rows and filter client-side with Power Automate's "Filter array" action. At 100-person scale this is well within processing limits.

**✓ Verify:** add yourself to Reviewer Interests with a topic tag. Run the digest flow manually. Confirm you receive a notification for an open article with that tag.

---

## Phase 9 — Review Gallery and Article Pages (30 minutes)

### Step 9.1 — The review gallery page

The review gallery is the Gallery view of the Library Review Tracker list — linked directly, not embedded as a web part.

After completing Phase 3 (Gallery view formatting), copy the URL of the Gallery view from your browser address bar. This is the review gallery link. Use it everywhere: kickoff message, Teams channel descriptions, article pages. It opens the live, filtered gallery of open articles.

⚠ **Do not embed Gallery view as a List web part on a SharePoint page.** A confirmed SharePoint bug causes Title and date fields to display twice per card when Gallery view is embedded in a page. Linking directly to the list URL avoids this.

### Step 9.2 — Article page review callout

On each article's SharePoint page, add a brief callout above the footer with:

- A Text web part: "Read this? Share your feedback — takes 5 minutes, helps us make it better."
- A Button web part linked to the pre-filled FeedbackFormURL for this article (from Phase 5)

Keep it minimal — one sentence, one button. Reviewers who land here have already read the article.

### Step 9.3 — Update ArticlePageURL in the List

Once article pages exist, paste each page URL into the ArticlePageURL column. The Adaptive Card digest (Phase 7) and the Gallery card (Phase 3) both use this for their links.

**✓ Verify:** open an article page. Feedback button opens the correct pre-filled form. Feedback form shows the correct article pre-selected.

---

## Phase 10 — Eric's Rollup Dashboard (15 minutes)

### Step 10.1 — Create a dashboard page

New SharePoint page: "Library Review Dashboard." Add the List web part using the **Eric's Dashboard** view (standard list layout — not Gallery, to avoid the web part embed bug). Group by Status, show ReviewCount and Ceiling per row. This is your management view — not linked from article pages, not public-facing.

**✓ Verify:** dashboard shows all articles grouped by Status with ReviewCount visible.

---

## Phase 11 — Recognition Layer (15 minutes)

### Step 11.1 — Reserve space on each article page

Add a Text web part at the bottom of each article page with placeholder text: "Reviewed by: [names will appear here after review is complete]." Update manually when a piece reaches its ceiling and the ceiling notification email arrives.

### Step 11.2 — Ceiling notification already covered

The Feedback Flow (Phase 6, Step 6.5) sends Eric an email when a piece hits its ceiling. That email is the trigger to update the "Reviewed by" text on the article page.

---

## Phase 12 — Kickoff Message (15 minutes)

One message. Posted once to each relevant Teams community at library launch. Never repeated.

> **The Design Foundations Library is live.**
>
> It's a microlearning library for practitioners — short pieces on research, prototyping, facilitation, and AI-assisted design. Each piece is under 5 minutes.
>
> We're running peer review before publishing each piece, and we need practitioners to help. Read something, have thoughts? There's a 5-minute review form right on the page. First-come, first-served — a piece closes once it's been reviewed enough times, so the same piece won't get over-reviewed while others sit waiting.
>
> [Link to the review gallery — the Gallery view URL from Phase 9]
>
> If you want to be notified when pieces on a specific topic need reviewers, fill in your interests at the end of the review form after you submit one.

---

## Phase 13 — Testing Checklist (45 minutes)

Run every path before the kickoff message goes out.

| Test | Steps | Pass condition |
|---|---|---|
| Gallery view cards | Open the Gallery view URL | Cards show title, tier, topic, goal line, slots remaining. Amber/green/grey border by status. |
| Feedback form pre-fill | Open FeedbackFormURL for article 103 | Dropdown shows "103 — Attachment Is the Real Risk" pre-selected |
| Feedback flow end-to-end | Submit feedback for article 103 | ReviewCount increments to 1, Status updates if threshold hit, Eric receives full response email |
| Status: Needs Review → Ready to Publish | Manually set ReviewCount to MinReviews value on a T100 article | Status changes to "Ready to Publish" |
| Status: Ready to Publish → Closed | Manually set ReviewCount to Ceiling value | Status changes to "Closed" |
| Closed article removed from gallery | Article with Status = Closed | Not visible in Gallery view (filtered out) |
| Ceiling notification | Trigger Feedback Flow that pushes ReviewCount to Ceiling | Eric receives ceiling notification email |
| Weekly digest — high inventory | Trigger digest flow manually with >10 open pieces | Per-article Adaptive Cards appear in correct Teams channels |
| Weekly digest — low inventory | Temporarily set all but 5 articles to Closed, run digest | Single summary card listing remaining pieces appears instead |
| Topic notifications | Add self to Reviewer Interests with a tag; run digest | Receive notification for matching open article |
| Blind end-to-end | Ask one person to find and submit a review with no instructions | They complete it without asking for help |

---

## What this guide does not cover

### Article index / browse page
A page listing all published library pieces for discovery beyond the review gallery. The review gallery only shows open pieces — it disappears once review is complete. Options: a SharePoint page with a filtered standard-layout List web part (all articles, all statuses), grouped by tier or topic. Build this separately once the article inventory is stable.

### Power BI analytics dashboard
For richer analytics — review velocity, topic coverage trends, reviewer participation rates, comprehension score patterns — connect Power BI to the SharePoint List as a data source. Build after 2–3 weeks of live data. A premature build on an empty dataset wastes setup time.

### Feedback synthesis workflow
The Feedback Flow delivers submissions to Eric's inbox. What happens next — reading, deciding revisions, writing them — is human work. Process documented in `meta/peer-review-policy.md` and per-piece feedback files at `meta/piece-feedback/`.

### Automated "Reviewed by" on article pages
Currently manual (Phase 11). Automating requires a Power Automate flow that edits a SharePoint page's web part content via the SharePoint REST API or Graph API — technically possible but requires app registration and admin consent. Not worth it at this scale.

### User testing phase infrastructure
Peer review (expert feedback) and user testing (behavioral, with PMs and devs) are separate phases. This guide covers peer review only. The user testing protocol, participant recruitment, task design, and metrics are separate work, documented when that phase begins.

### Viva Engage integration
If your company uses Viva Engage communities, the digest could post there too. Power Automate has a Viva Engage connector, but the format differs — Viva Engage doesn't support Adaptive Cards, so it's a plain post with a link. Add after Teams digest is proven.

### Reviewer onboarding for non-power users
If any reviewer population needs a walkthrough, a short 2-minute Clipchamp recording of the find-to-submit flow would serve as async onboarding. Record after the system is built and tested — using the live system.

### Localization
All form text, card content, and email notifications are in English. If your reviewer pool includes non-native English speakers (see `meta/piece-feedback/103.feedback.md`), simplify the comprehension check question: "in your own words, what is this piece mainly about?" over more formal phrasing.

### Archiving and expiry
Once the library stabilizes post-publication, a quarterly archiving pass — moving Closed rows to an Archive List — keeps the tracker clean and the digest fast.

---

## Related files

- `meta/peer-review-policy.md` — thresholds, phased recruitment strategy, review flow, capacity planning
- `meta/piece-feedback/` — per-piece reviewer notes and revision priorities
- `meta/quality-benchmarks.html` — the 81-benchmark evaluation rubric reviewers are implicitly testing against
