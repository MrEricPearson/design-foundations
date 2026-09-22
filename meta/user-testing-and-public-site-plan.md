# Phase 3 — Public Site & User Testing Plan

**Status:** Draft content/architecture plan for Eric to build. No SharePoint access from this session — everything below is a spec to build from, not a build log.
**Fills the gap** flagged in `meta/peer-review-m365-build-guide.md` under "What this guide does not cover → User testing phase infrastructure" and "→ Article index / browse page." That phase begins now.
**Sequencing (per Eric's decision, 2026-09-02):** the new public site gets built first. The 2-user test runs on it directly — not on the interim `DesignatBayer` review site. Pilot content was originally 103 and 105 because those were the first finished `.publish.md` maps. As of 2026-09-22, **27 pieces** have publish docs (including forwarding scenarios). 106 / 147 / 157 / 177 are the expert-review ready-to-publish set; use those plus 103/105 when the public site is provisioned.

---

## Part A — New Public Site: Content & Architecture Plan

### Purpose and distinction from the existing site

`DesignatBayer` is the internal peer-review workspace — reviewers, Gallery view, Feedback Form. It stays exactly as-is; nothing here replaces it. The new site is the actual reader destination: where a PM, custom dev, or non-custom-dev practitioner lands to read a published piece. Two different audiences, two different jobs. Don't merge them onto one site — the review site's Gallery/dashboard machinery would just be noise for a general reader.

### Open decisions (yours to make, not mine)

- **Site name.** Suggest something that reads as a destination, not a project — e.g. "Design Foundations" or "Design Foundations Library." Avoid "DesignatBayer" (already claimed by the review site) and avoid naming the Product Fulfillment team per `CLAUDE.md`.
- **Permission scope for "public to the Bayer network."** In SharePoint terms this is almost certainly a Communication Site shared with "Everyone except external users," not a Team Site. Confirm with IT/governance before provisioning — tenant-wide sharing policies vary and this is the kind of thing that's much easier to set correctly at creation than to widen later.

### Site structure

```
Home  (browsable index — the "article index page" the review guide deferred)
  └─ filtered, grouped list of published pieces, read-only, no review chrome
Article pages (one per published piece, built from its .publish.md layout map)
```

Keep it to these two page types for the pilot. Don't build tier-browse pages, topic-browse pages, or the PM/Custom-Dev/Non-Custom-Dev "Start Here" entry points (`meta/16-start-here-pm.md` etc.) yet — those pages assume a library deep enough to need routing. At 2 published pieces, a single flat list on Home does that job with no extra construction, and the Start Here docs already exist as content whenever the site has enough behind it to justify their own nav entries.

### Home page content

- Short intro, first-person peer voice, same register as the pieces themselves. States what this is (practical, under-5-minute reads on design fundamentals) and who it's for. No mention of the AI-adoption mandate, no leadership framing, no org-structure detail — same silence rules that govern the articles themselves apply to this page.
- Below the intro: a List web part in Gallery or standard layout, one row per published piece, showing Title, Tier, Subtitle/Goal line, and a link. This is a read-only mirror of published rows — no ReviewCount, no Status, no reviewer-facing columns.

**Reuse the existing data instead of duplicating it.** Add one column to the existing `Library Review Tracker` List (the one built in `meta/peer-review-m365-build-guide.md` Phase 2): `PublicPageURL` (Hyperlink, blank by default). Populate it only when a piece's public page goes live. Point the new site's Home list web part at this same List, filtered to `PublicPageURL is not blank`. One source of truth, no second tracker to keep in sync, and the act of filling in that column is your actual "go live" switch.

### Article pages

Nothing new to design here — `meta/layout-system.md` (patterns P1–P12) and each piece's own `.publish.md` (see `100-foundations/103.publish.md`, `100-foundations/105.publish.md`) are the complete build spec: web part sequence, spacer schedule, image specs, sources block formatting. Build 103's and 105's public pages directly from those two files. No review callout, no "Submit Review" button — that chrome belongs to the review site only.

---

## Part B — Phase 3 User Testing

This is the "Audience Sample Testing" phase already defined in `content-strategy-spec.html` (Quality Benchmark module) — this section operationalizes it for the first real cohort.

### Scope check, stated plainly

Two participants is a pilot, not a sample. Treat every metric below as a directional signal to act on, not a statistic to trust. A single "no" or a confused comprehension answer from either participant is worth investigating before wider distribution — don't wait for a pattern across two data points that will never repeat itself the same way twice.

### Participants and task

Recruit 2 readers per Eric's plan (reuse Alberto/Michael/whoever hasn't already reviewed 103 or 105 as a peer reviewer — a fresh, non-reviewer read is the point of this phase; someone who already reviewed the piece has seen it revised once and isn't a clean read). Send each participant the live public-page link for 103 and 105, plus the Phase 3 form link below. No task script beyond "read it, do the Try This exercise for real with something you're currently working on, then fill out the form" — the pieces are already built to be self-contained five-minute reads, so the "task" is just the intended reading experience.

### New Microsoft Form: `User Testing — Design Foundations Library`

A separate form from the peer-review Feedback Form — different questions, different purpose (behavioral response, not content-accuracy critique).

| # | Question | Type | Maps to spec metric |
|---|---|---|---|
| 1 | Which article did you read? | Dropdown (103 / 105) — pre-filled via URL, same mechanism as the review form | — |
| 2 | Your role | Choice: PM / Custom Dev / Non-Custom Dev / Other | — |
| 3 | Did you read it all the way to the end? | Choice: Yes / No, stopped partway / Skimmed the back half | Completion rate |
| 4 | About how long did it take? | Choice: Under 3 min / 3–5 min / 5–7 min / Over 7 min | Time on page |
| 5 | Did you do the Try This exercise? | Choice: Yes, with something I'm actually working on / Yes, but hypothetically / No | Try This completion |
| 6 | In one sentence: what is this piece asking you to be able to do? | Paragraph, required | Comprehension |
| 7 | Would you send this to a colleague? Who, and why (or why not)? | Paragraph, required | Forward signal |
| 8 | What was most useful? | Paragraph | Open feedback |
| 9 | What was confusing, felt off, or made you want to skip? | Paragraph | Open feedback |

Settings: require sign-in (same rationale as the review form — reduces friction, captures identity automatically). One response per person: off (each participant fills it out twice, once per article).

**Pre-fill URLs:** same manual process as `meta/peer-review-m365-build-guide.md` Phase 5 — generate one pre-filled link per article via the Forms GUI "Get pre-filled link," test each in an incognito window before sending.

### Reading the results — what counts as "working"

Map each answer back to the spec's Phase 3 table (`content-strategy-spec.html`, Quality Benchmark module):

| Signal | Working | Needs another pass |
|---|---|---|
| Q3 completion | Both read to the end | Either stopped or skimmed → check tone consistency and length against the ~1000-word target |
| Q4 time | Both land in 3–5 min | Both readings feel too fast to be true (skimming) or run long → audit density |
| Q5 Try This | At least one did it "for real" | Both only hypothetical or skipped → the prompt is too vague or needs setup the piece didn't name |
| Q6 comprehension | Answer restates the piece's actual Goal line in the participant's own words | Answer names a different concept, or is vague ("something about feedback") → Concept or Goal isn't precise enough |
| Q7 forward signal | Names a specific colleague and a specific reason | "Maybe" or no one named → check title, quotability, recognition precision |
| Q8/Q9 open feedback | — | Read every answer regardless of the other metrics — this is where the next revision's priorities come from, same synthesis process as peer review (`meta/piece-feedback/`) |

No numeric pass/fail threshold at n=2. If both participants clear every signal, that's a green light to move toward the next iteration and wider distribution. If either misses on Q3, Q5, or Q6, revise before broadening the audience — those three are the ones that mean the piece isn't doing its actual job, not just a style preference.

### After the pilot

1. Synthesize both responses into `meta/piece-feedback/103.feedback.md` and `105.feedback.md` under a new "Phase 3 — User Testing" section, same format as the existing peer-review synthesis.
2. Revise per the priorities that fall out.
3. Widen distribution (Teams post, wider SharePoint visibility) only after that revision pass — not before.
4. If a craft-level pattern shows up here that also showed up in peer review (see `meta/craft-learnings-pending.md`), that's independent-phase corroboration — enough to promote straight to `content-strategy-spec.html`.

---

## Next steps checklist (Eric)

1. Decide the site name and confirm the "public to Bayer network" permission scope with IT.
2. Provision the Communication Site; build Home per the content plan above.
3. Add `PublicPageURL` to the existing `Library Review Tracker` List.
4. Build 103 and 105 article pages from their `.publish.md` files; populate `PublicPageURL` for each when live.
5. Build the `User Testing — Design Foundations Library` Form from the question table above; generate the two pre-filled links.
6. Recruit 2 non-reviewer participants; send links.
7. Collect responses, apply the signal table, synthesize into the per-piece feedback files, revise, then distribute.
