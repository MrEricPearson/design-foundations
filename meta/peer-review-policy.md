# Peer Review Policy — Design Foundations Library

## Purpose

Every published piece in the library is reviewed by practitioners before publication. Reviews serve two goals: catching content problems before they reach the full audience, and building confidence that the library teaches what it claims to teach. This policy defines who reviews what, how many reviews are required, and how the system distributes coverage fairly across the full article inventory.

---

## Review thresholds by tier

| Tier | Publish gate | Slot ceiling | Logic |
|------|-------------|--------------|-------|
| T100 — Recognize | 1 review | 2 reviews | One reviewer confirms or flags. Second is a bonus. Closes at 2 so capacity flows to uncovered pieces. |
| T200 — Practice | 2 reviews | 3 reviews | Two reviewers needed before publication — one may miss what another catches at the method level. Closes at 3. |
| T300 — Orchestrate | 3 reviews | 4 reviews | Full panel before publication. Arc-level judgment errors require multiple perspectives to surface. Closes at 4. |

**Ceiling rule:** once a piece reaches its ceiling, it is marked Closed and removed from the review gallery. No additional reviews are accepted. This prevents popular topics from absorbing disproportionate reviewer capacity while lower-profile pieces sit uncovered.

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

## Review flow

Reviews are **first-come-first-served** up to the ceiling. There is no claiming step — submit the form and you've reviewed the piece. The system tracks how many reviews each piece has received and closes it automatically once the ceiling is hit.

The gallery page shows every piece still accepting reviews, with a live slot count. When a piece closes, it disappears from the gallery. This is the primary coverage signal: once the gallery is empty, review is complete across the library.

**Status definitions:**

| Status | Meaning | Shown in gallery |
|--------|---------|-----------------|
| Needs Review | Below publish gate | Yes |
| Ready to Publish | At or above gate, below ceiling | Yes — still accepting reviews |
| Closed | At ceiling | No — removed from gallery |
| Published | Live on SharePoint | No |

---

## Phased recruitment

The 8-week review window calls for different tactics at different inventory levels. Broadcasting every article from week one produces noise. Concentrating at the end produces urgency. The approach shifts in three phases:

**Phase 1 — Weeks 1–4 (high inventory, 20+ pieces open)**

The single kickoff message goes out once to each relevant Teams community. It explains the library, links to the review gallery, and describes the one-step review process. No per-article posts. Organic traffic to article pages — from the kickoff link, from shares, from Teams conversations — is the primary driver. The gallery captures reviewers at their highest-intent moment: when they've just finished reading.

**Phase 2 — Weeks 5–6 (mid inventory, 10–15 pieces open)**

The weekly Teams digest becomes useful. At this inventory level, the list is short enough to scan, and visible progress (pieces closing) creates momentum. The digest posts an Adaptive Card for every open piece once per week. Reviewers can see the list shrinking. This is when passive interest becomes active participation.

**Phase 3 — Weeks 7–8 (tail, fewer than 10 pieces open)**

The digest switches to highlighting the remaining pieces specifically — a card that names all remaining open pieces in one view rather than per-article cards. Direct outreach to 2–3 named practitioners per remaining piece, matched by topic. At this stage, the ask is concrete: "this is the last piece in your area that needs one more reviewer."

**Direct outreach** (fallback, any phase): any piece with zero reviews after two weeks receives a short personalized message to 2–3 practitioners whose role matches the topic. Targeted, not broadcast.

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
