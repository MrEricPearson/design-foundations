# M365 Peer Review System — Build Guide
## Design Foundations Library

**Last updated:** 2026-08-26
**Estimated build time:** 6–8 hours across multiple sessions
**License requirement:** Microsoft 365 E1/E3/E5 (all connectors used are standard — no premium Power Automate license required)

This guide builds the complete peer review infrastructure described in `meta/peer-review-policy.md`. Read that document first — it defines the thresholds, slot mechanics, and funneling strategy this guide implements.

---

## Architecture overview

```
SharePoint List (Library Review Tracker)
    ↑ writes          ↓ reads
Power Automate     Article pages      Eric's dashboard
  Claim Flow       (List web part     (List rollup view)
  Feedback Flow     + claim button)
  Weekly Digest
  Topic Alerts
    ↓ posts
  Teams channels
    ↑ triggers
  Microsoft Forms
  (Claim + Feedback)
```

**Data flows in one direction:** Forms → Power Automate → SharePoint List. Everything else reads from the List. The List is the single source of truth.

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

Before building anything, create a spreadsheet with every article that needs peer review. Columns: Article ID (e.g., 103), Title, Tier (T100/T200/T300), Topic Tag, Goal Line (your subtitle text — this appears in the Adaptive Card and slot widget), SharePoint page URL (leave blank until pages are built), Minimum reviews required (1/2/3), Ceiling (2/3/4).

This list must be complete before building the SharePoint List, because article IDs and tags become the schema.

### Step 1.2 — Confirm your topic taxonomy

Decide your topic tags now. They cannot change later without cascading updates to the List, Forms dropdown, and Adaptive Card flow filters. Based on the current library: Prototyping, Research, Facilitation, AI, Assumptions, Personas, Story Mapping. Confirm this is the complete set before proceeding.

### Step 1.3 — Confirm license access

Everything in this guide uses standard connectors. Verify your M365 tenant has:
- Power Automate (included in E1/E3/E5 — confirm with IT admin if unsure)
- Microsoft Forms (included in all M365 plans)
- SharePoint Online (included in all M365 plans)

**✓ Verify:** sign into make.powerautomate.com and confirm you can create a new flow. Sign into forms.office.com and confirm you can create a new form. Resolve any access issues with IT before continuing.

---

## Phase 2 — SharePoint List (45 minutes)

This is the data layer. Everything else reads from and writes to this List.

### Step 2.1 — Create the List

Navigate to your SharePoint site → New → List. Name it: `Library Review Tracker`. If SharePoint auto-generates internal name with spaces, rename immediately under List Settings → List name.

### Step 2.2 — Rename the default Title column

Go to List Settings → Columns → Title → rename to `Article Title`. You cannot delete the Title column, but renaming prevents confusion with your own columns.

### Step 2.3 — Add all columns in this exact order

Use names without spaces — this avoids the `_x0020_` encoding problem in Power Automate expressions and OData filter queries. Set display names separately if needed.

| Column name (internal) | Type | Settings |
|---|---|---|
| ArticleID | Number | Required. No decimal places. |
| Tier | Choice | T100 / T200 / T300. Required. |
| TopicTag | Choice | Your confirmed taxonomy. Required. Single value only. |
| GoalLine | Multiple lines of text | Plain text. The subtitle — appears in Adaptive Cards. |
| MinReviews | Number | Required. Default: 1. |
| Ceiling | Number | Required. Default: 2. |
| Reviewer1Name | Single line of text | |
| Reviewer1Email | Single line of text | |
| Reviewer1Claimed | Date and Time | Date only. |
| Reviewer1Submitted | Yes/No | Default: No. |
| Reviewer2Name | Single line of text | |
| Reviewer2Email | Single line of text | |
| Reviewer2Claimed | Date and Time | Date only. |
| Reviewer2Submitted | Yes/No | Default: No. |
| Reviewer3Name | Single line of text | |
| Reviewer3Email | Single line of text | |
| Reviewer3Claimed | Date and Time | Date only. |
| Reviewer3Submitted | Yes/No | Default: No. |
| Reviewer4Name | Single line of text | (T300 ceiling only) |
| Reviewer4Email | Single line of text | |
| Reviewer4Claimed | Date and Time | Date only. |
| Reviewer4Submitted | Yes/No | Default: No. |
| ReviewCount | Calculated | `=IF(Reviewer1Submitted,1,0)+IF(Reviewer2Submitted,1,0)+IF(Reviewer3Submitted,1,0)+IF(Reviewer4Submitted,1,0)` |
| SlotsClaimed | Calculated | `=IF(LEN(Reviewer1Email)>0,1,0)+IF(LEN(Reviewer2Email)>0,1,0)+IF(LEN(Reviewer3Email)>0,1,0)+IF(LEN(Reviewer4Email)>0,1,0)` |
| Status | Calculated | `=IF(ReviewCount>=Ceiling,"Closed",IF(ReviewCount>=MinReviews,"Ready to Publish","Needs Review"))` |
| ArticlePageURL | Hyperlink | Populate in Phase 9 after pages exist. |
| ClaimFormURL | Single line of text | Populate in Phase 4 after forms exist. |
| FeedbackFormURL | Single line of text | Populate in Phase 4 after forms exist. |
| Notes | Multiple lines of text | Eric's use only. |

⚠ **Gotcha — calculated column internal names:** SharePoint uses internal names in formulas. If you named columns without spaces, the formula uses the name directly (e.g., `Reviewer1Submitted`). If you used spaces, the internal name encodes them (e.g., `Reviewer_x0020_1_x0020_Submitted`). Check the actual internal name under List Settings → column → inspect the URL. Using no-space column names from the start avoids this entirely.

### Step 2.4 — Populate the List with all articles

Add one row per article. Fill ArticleID, Article Title, Tier, TopicTag, GoalLine, MinReviews, Ceiling. Leave reviewer columns and URL columns blank.

**✓ Verify:** Status calculated column shows "Needs Review" for every row. ReviewCount shows 0. If calculated columns show errors, the formula references a wrong internal name — fix the formula before proceeding.

### Step 2.5 — Create named views

Create four named views (List → All Items dropdown → Create new view):

- **Eric's Dashboard** — all columns, grouped by Status, sorted by ArticleID. Your management view.
- **Needs Review** — filter: Status equals "Needs Review." Show: Article Title, Tier, TopicTag, GoalLine, SlotsClaimed, ReviewCount. Feeds the weekly Adaptive Card digest.
- **Ready to Publish** — filter: Status equals "Ready to Publish." Shows what's cleared for publication.
- **By Topic** — no filter, grouped by TopicTag. Browse by subject area.

Also create one view per article for the article page web parts (see Phase 9). Name them `Article-[ID]` (e.g., `Article-103`). Each filters to ArticleID equals [number]. This is the only way to show a filtered List on a modern SharePoint page — URL-based filtering is not supported on modern pages.

⚠ **Gotcha — named view limit:** SharePoint Lists support up to 50 public views. With 20+ articles plus 4 management views you'll be around 25 views — within limits, but worth monitoring if the library grows.

**✓ Verify:** Needs Review view shows all articles. Ready to Publish view is empty. Both correct.

---

## Phase 3 — Microsoft Forms (1 hour)

You need two forms: one for claiming a slot, one for submitting feedback. Build both before generating pre-fill URLs.

### Step 3.1 — Create the Claim Form

Go to forms.office.com → New Form. Title: `Claim a Review Slot — Design Foundations Library`.

| Question | Type | Settings |
|---|---|---|
| Which article are you claiming a slot for? | Dropdown | Every article as "ID — Title" (e.g., "103 — Attachment Is the Real Risk"). Required. This field will be pre-filled via URL. |
| Your name | Text | Required. |
| Your email | Text | Required. Add input validation: Must be email address. |
| Your role | Choice | PM / Custom Dev / Non-Custom Dev / UX / Other. Required. Single answer. |
| Any topics you'd especially like to review in future? (optional) | Checkboxes | Your full topic taxonomy. Not required. This is passive interest capture for topic notifications. |

Under Settings: enable Require sign-in (captures AAD email, reduces manual entry friction). Set One response per person to OFF — same person may claim slots on different articles.

### Step 3.2 — Create the Feedback Form

New Form. Title: `Peer Review — Design Foundations Library`.

| Question | Type | Settings |
|---|---|---|
| Which article are you reviewing? | Dropdown | Same article list as claim form. Required. Pre-fillable. |
| Your role | Choice | PM / Custom Dev / Non-Custom Dev / UX / Other. Required. |
| What worked — what landed clearly and why | Paragraph | Required. |
| What didn't work — what confused you, made you want to skip, or felt off | Paragraph | Required. |
| Comprehension check: in your own words, what is the main thing this piece is saying? | Paragraph | Required. |
| Would you forward this to a colleague? Who, and why? | Paragraph | Not required. |

Under Settings: enable Require sign-in. Set One response per person to OFF. Enable Show progress bar.

The comprehension check (question 5) is the most diagnostic. A wrong answer means the concept didn't transfer regardless of how engaging the piece felt.

**✓ Verify:** preview both forms. All questions appear in order, required fields are marked, dropdowns include every article.

---

## Phase 4 — Pre-fill URLs (45 minutes)

Generates per-article URLs that pre-select the correct article in both forms. Must be done manually via the Microsoft Forms GUI — programmatic URL construction is not officially supported and the encoding format is fragile.

### Step 4.1 — How pre-fill URLs work

Microsoft Forms pre-fill uses a base64-encoded JSON payload in the URL's `r=` parameter. The only supported way to generate these is the GUI. Do not attempt to construct or edit them manually.

### Step 4.2 — Generate pre-filled Claim Form URLs

Open the Claim Form. Click the three-dot menu (…) at top right → Get pre-filled link. The form opens in an authoring mode where you fill in answers.

For each article:
1. Select that article in the "Which article" dropdown
2. Leave all other fields blank
3. Click Copy link at the bottom
4. Paste the URL into your spreadsheet in the ClaimFormURL column
5. Clear the selection and repeat for the next article

⚠ **Gotcha — URL integrity:** do not edit the generated URL manually. Do not run it through a URL shortener. Test each URL in an incognito window before storing it.

### Step 4.3 — Generate pre-filled Feedback Form URLs

Same process for the Feedback Form. Generate one URL per article with the article pre-selected. Paste into FeedbackFormURL column of your spreadsheet.

### Step 4.4 — Update the SharePoint List

For each article row in Library Review Tracker, paste the ClaimFormURL and FeedbackFormURL values into their columns.

**✓ Verify:** open three pre-fill URLs from the List across different tiers. Confirm each pre-selects the correct article.

---

## Phase 5 — Power Automate: Claim Flow (45 minutes)

Listens for Claim Form submissions and writes reviewer data into the next available slot.

### Step 5.1 — Create the flow

Automated cloud flow. Name: `Library Review — Claim Slot`. Trigger: "When a new response is submitted" (Microsoft Forms). Select your Claim Form.

### Step 5.2 — Get response details (mandatory)

Add action: "Get response details" (Microsoft Forms). Form ID: Claim Form. Response ID: dynamic `Response Id` from trigger.

⚠ **Gotcha — the trigger alone contains no answer data.** The trigger fires with a Response ID only. You must always follow it with "Get response details" to access the actual answers. Skipping this step is the most common Power Automate + Forms error.

### Step 5.3 — Get the matching List item

Add action: "Get items" (SharePoint). Site: [SP Site]. List: Library Review Tracker. Filter Query:

```
ArticleID eq [dynamic: answer to "Which article" question — extract the number from the string]
```

⚠ **Gotcha — extracting ArticleID from the dropdown answer:** the dropdown answer returns a string like "103 — Attachment Is the Real Risk." You need to extract just the number. Use the expression: `int(first(split(outputs('Get_response_details')?['body/r[question_id]'], ' ')))`. Find the question ID in the dynamic content schema output by running the flow once and inspecting the "Get response details" output. Alternatively, add ArticleID as a hidden question in the form and use its value directly — simpler and more reliable.

Top Count: 1.

### Step 5.4 — Determine the next available slot

Add nested Condition actions checking which reviewer email slots are empty. For each empty slot found, add "Update item" (SharePoint) setting Name, Email, and Claimed date for that slot. For the ceiling-exceeded case, send the reviewer an email: "This article has reached its review ceiling and is no longer accepting claims."

Slot check order:
1. Is Reviewer1Email empty? → fill slot 1
2. Else: is Reviewer2Email empty? → fill slot 2
3. Else: is Reviewer3Email empty? → fill slot 3
4. Else: is Reviewer4Email empty? → fill slot 4
5. Else: send ceiling-exceeded email

### Step 5.5 — Notify Eric

After each Update item action, send email to Eric: article title, reviewer name, email, role, slots now filled.

### Step 5.6 — Send confirmation to reviewer

Send email to reviewer with their article's pre-filled Feedback Form URL. Use a Compose action to look up the FeedbackFormURL from the List item retrieved in Step 5.3, then reference it in the email body.

**✓ Verify:** submit a test claim. Confirm List updates correctly, Eric's notification arrives, reviewer confirmation arrives with the correct feedback link.

---

## Phase 6 — Power Automate: Feedback Flow (30 minutes)

Listens for Feedback Form submissions and marks the reviewer's slot as Submitted.

### Step 6.1 — Create the flow

Automated cloud flow. Name: `Library Review — Feedback Submitted`. Trigger: "When a new response is submitted." Select Feedback Form.

### Step 6.2 — Get response details

Same mandatory two-step pattern: trigger → Get response details.

### Step 6.3 — Find the reviewer's slot and mark Submitted

Get items with OData filter on ArticleID. Add nested conditions checking which reviewer email slot matches the form responder's email. On match, Update item setting that slot's Submitted column to Yes.

Add a final else branch: if no slot matches, send Eric a notification — "A feedback submission didn't match any claimed slot for [article]. Manual review needed."

### Step 6.4 — Notify Eric with full response

Send email to Eric immediately with: article title, reviewer name, role, all four substantive answers, and the comprehension check response verbatim.

**✓ Verify:** submit test feedback after claiming. Confirm slot shows Submitted = Yes, ReviewCount increments, Eric receives full response email.

---

## Phase 7 — Power Automate: Weekly Teams Digest (1 hour)

Posts Adaptive Cards to Teams channels for articles still needing reviewers. Runs automatically. Requires no ongoing manual action.

### Step 7.1 — Create the flow

Scheduled cloud flow. Name: `Library Review — Weekly Digest`. Recurrence: weekly, Monday, 9:00 AM.

### Step 7.2 — Get articles needing reviewers

"Get items" (SharePoint). List: Library Review Tracker. Filter Query: `Status eq 'Needs Review'`. Order by ArticleID ascending.

### Step 7.3 — Loop and post one card per article

"Apply to each" on the Get items output. Inside the loop, add action: **"Post your own adaptive card as the Flow bot to a channel"** (Microsoft Teams connector).

⚠ **Critical — do NOT use "Post and wait for a response":** the "wait" variant pauses the entire flow after the first card is submitted. For a digest posting 15+ cards, this halts all subsequent posts after the first claim. Use the non-waiting variant. Claiming happens on the article page, not in the card. The card's button is Action.OpenUrl only.

⚠ **Gotcha — Workflows app required:** the Adaptive Card post action requires the Microsoft Workflows app to be installed in the target Teams channel. Confirm this with your Teams admin before testing.

### Step 7.4 — Adaptive Card JSON

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
      "color": "Accent",
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
        { "title": "Tier", "value": "@{items('Apply_to_each')?['Tier']?['Value']}" },
        { "title": "Topic", "value": "@{items('Apply_to_each')?['TopicTag']?['Value']}" },
        {
          "title": "Slots remaining",
          "value": "@{sub(items('Apply_to_each')?['Ceiling'], items('Apply_to_each')?['SlotsClaimed'])}"
        }
      ]
    }
  ],
  "actions": [
    {
      "type": "Action.OpenUrl",
      "title": "Read the article & claim a slot",
      "url": "@{items('Apply_to_each')?['ArticlePageURL']}"
    }
  ]
}
```

⚠ **Gotcha — dynamic expressions in JSON:** Power Automate expressions inside JSON strings use `@{expression}` syntax. Column references use the display name (for simple names) or internal name. Test by running the flow once with a single article and inspecting the card output before running on all articles.

### Step 7.5 — Route cards to correct channels

Add a Switch or Condition action inside the loop to post to the topic-relevant Teams channel based on TopicTag. Also post all cards to a general library channel. Hardcode channel names in the flow — there is no dynamic channel lookup without premium connectors.

### Step 7.6 — Skip closed articles

Add a Condition before the card post: if Status equals "Closed" then do nothing (empty branch). Safety net for timing gaps between Get items and card post.

**✓ Verify:** run the flow manually. Cards appear in correct channels. Button opens correct SharePoint page. Closed articles do not appear.

---

## Phase 8 — Power Automate: Topic Interest Notifications (30 minutes)

Replaces the retired SharePoint Alerts feature (fully retired July 2026 — alert creation is no longer possible). Sends personalized notifications when articles matching a reviewer's interests need reviewers.

### Step 8.1 — Create Reviewer Interests List

New SharePoint List: `Reviewer Interests`. Columns: ReviewerName (text), ReviewerEmail (text), Topics (choice, multi-select, same taxonomy as Library Review Tracker).

Populate by adding a Power Automate action to the Claim Flow (Phase 5): after writing the reviewer's slot, also "Create item" in Reviewer Interests with their name, email, and topic interests from the form's last question.

### Step 8.2 — Add topic notification to the weekly digest flow

Inside the Apply to each loop (Phase 7, Step 7.3), after posting the card, add:

1. "Get items" from Reviewer Interests (get all rows — no OData filter, because multi-select choice column filtering is not supported in OData)
2. "Filter array" (Data Operations) — filter the array where the Topics field contains the current article's TopicTag value
3. "Apply to each" on the filtered array — send each matching reviewer a Teams message or email with article title, goal line, and article page URL

⚠ **Gotcha — multi-select OData filter not supported:** you cannot filter a multi-value choice column server-side via OData in SharePoint. You must retrieve all rows and filter client-side using Power Automate's "Filter array" action. For large reviewer pools this is fine; at 100+ reviewers with many topic interests it remains within Power Automate's processing limits.

**✓ Verify:** add yourself to Reviewer Interests with a topic tag. Run the digest flow. Confirm you receive a notification for an article with that tag.

---

## Phase 9 — SharePoint Article Pages (1 hour)

Each article page needs a slot widget and a claim link.

### Step 9.1 — Add the List web part

Edit the article's SharePoint page. Add web part → List. Select Library Review Tracker.

In the web part properties: select the named view for this article (`Article-103`, etc.). The view was created in Phase 2 Step 2.5, filtered to ArticleID equals [number]. Show columns: SlotsClaimed, ReviewCount, Reviewer1Name, Reviewer2Name, Reviewer3Name, Status.

⚠ **Gotcha — no URL-based filtering on modern pages:** it is not possible to pass a filter via URL query string to a List web part on a modern SharePoint page. Microsoft has confirmed this is unsupported. Named views are the only viable approach without custom SPFx development.

### Step 9.2 — Add the Claim button

Below the List web part, add a Button web part. Label: "Claim a Review Slot." Link: the pre-filled ClaimFormURL for this article (from Phase 4). Open in new tab.

Add a Text web part above the button: "If you read this and have thoughts, claim a slot below. Takes 5–10 minutes. We're looking for [N] reviewer(s) for this piece."

### Step 9.3 — Update ArticlePageURL in the List

Once pages exist, paste each page URL into the ArticlePageURL column. The Adaptive Card digest (Phase 7) uses this for the button link.

**✓ Verify:** open an article page. List web part shows only that article's row. Claim button opens the correct pre-filled form with the right article pre-selected.

---

## Phase 10 — Eric's Rollup Dashboard (15 minutes)

### Step 10.1 — Create a dashboard page

New SharePoint page: "Library Review Dashboard." Add the List web part using the "Eric's Dashboard" view. This is your management view — not linked from article pages, not public-facing.

### Step 10.2 — Optional chart

Add a Quick Chart web part for review count by article. Gives at-a-glance coverage without reading rows.

**✓ Verify:** dashboard shows all articles grouped by Status with ReviewCount visible.

---

## Phase 11 — Recognition Layer (15 minutes)

### Step 11.1 — Reserve space on each article page

Add a Text web part at the bottom of each article page with placeholder text: "Reviewed by: [names will appear here after review is complete]." Update manually when a piece reaches its ceiling.

### Step 11.2 — Add ceiling notification to Feedback Flow

In the Feedback Flow (Phase 6), after marking a slot Submitted, add a condition: if ReviewCount now equals Ceiling, send Eric an email: "[Article Title] has reached its ceiling. Update the 'Reviewed by' section on the article page."

---

## Phase 12 — Kickoff Message (15 minutes)

One message. Posted once to each relevant Teams community. Never repeated — the weekly digest handles all ongoing recruitment automatically.

> **The Design Foundations Library is live.**
>
> It's a microlearning library for practitioners — short pieces on research, prototyping, facilitation, and AI-assisted design. Each piece is under 5 minutes.
>
> We're running peer review before publishing each piece, and we need practitioners to help. If you read something and have thoughts, there's a 5-minute review form right on the page. Slots are first-come, first-served, and close once filled — so the same piece won't get over-reviewed while others sit waiting.
>
> [Link to article index or library home page]
>
> If you want to be notified when pieces on a specific topic need reviewers, claim any slot and check your topic interests at the end of the claim form.

---

## Phase 13 — Testing Checklist (1 hour)

Run every path before the kickoff message goes out.

| Test | Steps | Pass condition |
|---|---|---|
| Claim form pre-fill | Open ClaimFormURL for article 103 | Dropdown shows "103 — Attachment Is the Real Risk" pre-selected |
| Claim flow end-to-end | Submit claim for article 103 | List updates Reviewer1Name/Email/Claimed; Eric gets notification; reviewer gets confirmation with feedback link |
| Feedback form pre-fill | Open FeedbackFormURL for article 103 | Dropdown pre-selected |
| Feedback flow end-to-end | Submit feedback for article 103 | List shows Reviewer1Submitted = Yes, ReviewCount = 1; Eric gets email with full response |
| Status: Needs Review → Ready to Publish | Set Reviewer1Submitted = Yes on a T100 article | Status changes to "Ready to Publish" |
| Status: Ready to Publish → Closed | Set Reviewer2Submitted = Yes on that T100 article | Status changes to "Closed" |
| Ceiling lock | Attempt a third claim on the T100 article | Claim flow sends ceiling-exceeded email; List does not update |
| Weekly digest | Trigger digest flow manually | Adaptive Cards appear in correct Teams channels; links work; closed articles absent |
| Article page widget | Open any article page | List web part shows correct row; Claim button opens correct pre-filled form |
| Topic notifications | Add self to Reviewer Interests with a tag; run digest | Receive notification for matching article |
| Blind end-to-end | Ask one other person to run full claim-to-feedback on a real article with no instructions | They complete it without asking for help |

---

## What this guide does not cover

These topics require separate decisions or build work beyond this guide's scope:

### Article index / browse page
A public-facing page listing all library pieces so readers can discover articles organically without relying on the Teams digest. Options: a SharePoint page with a filtered List web part (all articles, by tier or topic), a Viva Connections dashboard card, or a static manually-maintained links page. Build this before the kickoff message if you want organic discovery to work on day one.

### Power BI analytics dashboard
If you want richer analytics than the List views provide — review velocity over time, topic coverage trends, reviewer participation rates, comprehension score patterns — connect Power BI to the SharePoint List as a data source. Build after the system is running and you have at least 2–3 weeks of data. A premature analytics build on an empty dataset wastes setup time.

### Feedback synthesis workflow
The Feedback Flow delivers review submissions to Eric's inbox and stores them in the List. What happens next — reading submissions, deciding what to revise, writing the revision — is human work. The process for this is documented in `meta/peer-review-policy.md` and the per-piece feedback files at `meta/piece-feedback/`. No automation covers it.

### Automated "Reviewed by" recognition on article pages
Currently a manual step (Phase 11). Automating it would require a Power Automate flow that edits a SharePoint page's web part content via the SharePoint REST API or Graph API — technically possible but complex, requiring app registration and admin consent. Not worth the build time at this library's scale. Revisit if the library grows beyond 50 pieces.

### User testing phase infrastructure
Peer review (expert feedback) and user testing (behavioral, with PMs and devs) are separate phases with different tooling needs. User testing is typically run as moderated sessions (video call + screen share) or unmoderated sessions (using a tool like Maze, Lookback, or simply a structured Teams meeting). This guide covers peer review only. The user testing protocol, participant recruitment, task design, and metrics definition are separate work — documented separately when that phase begins.

### Viva Engage (Yammer) integration
If your company uses Viva Engage communities in addition to Teams, the Adaptive Card digest could be extended to post there as well. Power Automate has a Viva Engage connector. The card format differs (Viva Engage doesn't support Adaptive Cards — plain post with link only). Add this after the Teams digest is proven and stable.

### Reviewer onboarding for non-power users
The system assumes reviewers can follow a claim link, fill a form, and use Teams. If any reviewer population needs a walkthrough, a short 2-minute video recording (using Teams or Clipchamp) of the claim-to-submission flow would serve as async onboarding. Record after the system is built and tested — using the live system, not a mockup.

### Localization
All form text, card content, and email notifications are in English. If your reviewer pool includes non-native English speakers (see Carolina Louro's note in `meta/piece-feedback/103.feedback.md` about this being a real factor), consider whether any review prompts need simplification. The comprehension check question in particular should use plain language — "in your own words, what is this piece mainly about?" over more formal academic phrasing.

### Archiving and expiry
Once the library stabilizes post-publication, closed review slots don't need to remain in the active tracker. A quarterly archiving pass — moving closed rows to an Archive List — keeps the tracker clean and the digest fast. Power Automate can automate this with a monthly scheduled flow that moves rows where Status = Closed and ReviewCount >= Ceiling to the Archive List.

---

## Related files

- `meta/peer-review-policy.md` — thresholds, slot mechanics, funneling strategy, capacity planning
- `meta/piece-feedback/` — per-piece reviewer notes and revision priorities
- `meta/quality-benchmarks.html` — the 81-benchmark evaluation rubric reviewers are implicitly testing against
