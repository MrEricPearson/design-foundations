# Peer Review Policy — Design Foundations Library

## Purpose

Every published piece in the library is reviewed by practitioners before publication. Reviews serve two goals: catching content problems before they reach the full audience, and building confidence that the library teaches what it claims to teach. This policy defines who reviews what, how many reviews are required, and how the system closes slots to distribute coverage fairly.

---

## Review thresholds by tier

| Tier | Publish gate | Slot ceiling | Logic |
|------|-------------|--------------|-------|
| T100 — Recognize | 1 review | 2 reviews | One reviewer confirms or flags. Second is a bonus. Closes at 2 so capacity flows to uncovered pieces. |
| T200 — Practice | 2 reviews | 3 reviews | Two reviewers needed before publication — one may miss what another catches at the method level. Closes at 3. |
| T300 — Orchestrate | 3 reviews | 4 reviews | Full panel before publication. Arc-level judgment errors require multiple perspectives to surface. Closes at 4. |

**Ceiling rule:** once a piece reaches its ceiling, the claim slot locks permanently. No additional reviews are accepted. This prevents popular topics from absorbing disproportionate reviewer capacity while lower-profile pieces sit uncovered.

**Publish gate:** a piece may publish as soon as it hits its minimum threshold — it does not need to reach the ceiling first. A T100 piece with 1 review is ready to publish. A T200 piece with 2 reviews is ready to publish.

---

## Who reviews what

Reviews are **opt-in by topic relevance**, not assigned. Reviewers self-select based on whether an article's subject matches their work. This produces better feedback than assigned reviews — someone who chose to review a piece on assumption mapping is already the right person to review it.

**Expert review panel** (peer review phase, before user testing):
- Behavioral/psychology expertise — validates that research citations are accurately represented and claims are appropriately scoped
- UX practitioner voice — validates that the piece reads as a peer, not a lecture; catches tone and flow issues
- Instructional design / learning science — validates that the piece actually teaches (not just informs), that Try This produces real behavior change, and that the spaced practice arc holds

**User testing phase** (after expert review and revision):
- Product Managers — audience-fit validation for PM-targeted pieces
- Developers (custom and non-custom) — audience-fit validation for dev-targeted pieces

Expert reviewers and user testers serve different functions and are recruited separately. Expert reviewers evaluate craft, accuracy, and structure. User testers evaluate whether the piece changes behavior.

---

## Review form

All reviews use a single Microsoft Form. Six questions, 5–10 minutes to complete:

1. **Which article?** (pre-filled from article page, locked)
2. **Your role** — PM / Custom Dev / Non-Custom Dev / UX / Other
3. **What worked** — what landed clearly, what you'd keep
4. **What didn't work** — what confused you, made you want to skip, or felt off
5. **Comprehension check** — in your own words, what's the main thing this piece is saying?
6. **Forward intent** — would you send this to a colleague? Who and why?

Question 5 is the most diagnostic. A wrong answer means the concept didn't transfer regardless of how engaging the piece felt. Role field allows filtering by audience segment in the response dashboard.

---

## Slot mechanics

**Claiming a slot:**
Reviewers claim a slot before submitting feedback. Claiming is a separate step — it makes coverage visible to others and prevents five people from reviewing the same piece while three others sit at zero. The claim button appears on the article page and in the weekly Teams digest. Once claimed, the reviewer's name appears in the slot widget on the article page.

**Slot states:**
- **Open** — slot available, claim button visible
- **Claimed** — reviewer name shown, awaiting submission
- **Submitted** — review received, slot filled
- **Locked** — ceiling reached, no further claims accepted

**Social proof:** claimed slots display reviewer first names and avatars. Seeing that one person has already claimed makes it easier to be the second. Seeing two claimed creates urgency to be the third. An empty slot panel is a harder ask than a partially filled one.

---

## Status definitions

| Status | Meaning | Action |
|--------|---------|--------|
| Needs Review | Below publish gate | Active in weekly Teams digest |
| Ready to Publish | At or above publish gate, below ceiling | Can publish; additional slot(s) still open |
| Closed | At ceiling | Slot locked; removed from digest |
| Published | Live on SharePoint | Review complete |

---

## Funneling and recruitment

**Weekly Adaptive Card digest (automated):** Power Automate posts one Adaptive Card per article needing reviewers to relevant Teams communities each week. Cards show title, goal line, topic tag, slots remaining, and existing reviewer names. Includes a one-click claim button. Runs automatically — no manual action required from the library owner. Posts only pieces below ceiling; stops posting a piece once it closes.

**In-article widget:** Every article page embeds a slot count widget and claim button. Captures reviewers at the highest-intent moment — when they're already reading and already have opinions.

**Topic subscriptions:** Reviewers can subscribe to SharePoint List alerts for specific topic tags. They're notified automatically when new pieces in their area need reviewers. Set once, runs indefinitely.

**Direct outreach:** After two weeks, any piece with zero claims receives a short personalized email to 2–3 practitioners whose role matches the topic. Targeted, not broadcast. Used as a fallback only.

**Kickoff message:** One post to each relevant Teams community at library launch. Announces the library, explains the review program in two sentences, links to the review dashboard, explains how to subscribe to topic alerts. Never repeated.

---

## After review

**Revision:** piece author (Eric) reads all submissions for a piece once minimum threshold is hit, synthesizes findings, and revises before publication. The [meta/piece-feedback/](piece-feedback/) folder stores reviewer notes and revision priorities per piece.

**Recognition:** after publication, reviewer names appear in a "Reviewed by" section on the article page. Visible to all future readers. Makes reviewer contribution real and public.

**Feedback summary:** a brief synthesis of what reviewers found — themes only, not individual responses — is added to the article page or the feedback file after review is complete. Closes the loop publicly and signals that reviews produce changes.

---

## Capacity planning

Realistic participation rate from a 100-person pool: ~15 active reviewers over 2 months, producing ~25–35 total submissions. Tiered thresholds map to this reality:

- ~15 T100 pieces × 1 minimum = 15 submissions needed
- ~11 T200 pieces × 2 minimum = 22 submissions needed
- ~4 T300 pieces × 3 minimum = 12 submissions needed
- **Total minimum: ~49 submissions**

Priority order when capacity is constrained: T300 arcs first (highest stakes, smallest count), then T200 methods, then T100 atoms. T100 atoms benefit most from user testing anyway — recognition is a behavioral outcome observable directly, where expert review adds less marginal value than it does at higher tiers.
