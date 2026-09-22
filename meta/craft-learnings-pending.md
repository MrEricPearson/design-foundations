# Pending Craft Learnings — Not Yet Spec-Worthy

Single-source or unresolved signals from piece reviews. None of these have cleared the bar for a
`content-strategy-spec.html` change (2+ independent reviewers converging on the same underlying
issue). Tracked here so they aren't lost, and so a second independent hit on any of them gets
noticed instead of re-discovered from scratch.

**Promotion rule:** when a second, independent reviewer (not the same person, not the same piece)
flags the same underlying issue, promote it to `content-strategy-spec.html` and move the entry
below into a "resolved" note referencing the spec change. Until then, treat these as open
questions, not rules — don't act on them unilaterally when revising a piece.

**Survey batch logged 2026-09-22:** Library Review Feedback IDs 1–13. IDs 1–3 are Eric Pearson
proxy entries for the Carolina Louro / Dr. Magdalena Dybas-Stronkowska notes already in
`103.feedback.md`. IDs 4–8 were already in piece-feedback files. IDs 9–13 are the new reviews
(106 Magda, 270h Alberto, 123 Magda, 270i Alberto, 157 Magda).

---

## 1. Readers keep asking for a concrete/worked example, despite the no-anecdote rule

**Source:** Alberto Zamarron, independently on pieces 105, 147, 177 (concrete example) and 219
(worked example, start to finish). Four requests, but all from one reviewer — a real reading
preference, not yet independent corroboration.

**Not corroboration (same batch):** Dr. Dybas-Stronkowska on 123 asked to *swap* the search-bar /
click-data parenthetical for a usability-test-shaped instance. That is "this pattern is the wrong
kind of evidence," not "invent a story." It supports the existing "sharpen the pattern" workaround,
not a lift of the no-anecdote rule.

**Tension:** The project's core rule (`CLAUDE.md`, Voice; `content-strategy-spec.html`,
Recognition Mechanism module) is that pattern description outperforms invented anecdotes because
the reader's self-supplied instance is more vivid and carries no risk of feeling called out. That
rule was a deliberate design choice, not an oversight — it shouldn't flip on one reviewer's
pattern, however consistent.

**What to watch for:** If a second reviewer (Dybas-Stronkowska, Carolina Louro, or a new one)
independently asks for a concrete example on any future piece, that's real corroboration — revisit
whether the Recognition Mechanism module needs a caveat (e.g., "sharpen the pattern description
further" as the fix before "add an example" is ever the answer).

**In the meantime:** where a piece can satisfy this instinct through *sharper pattern description*
instead of an anecdote (see 177.feedback.md item 2; 123.feedback.md Magda #7), do that — it may
resolve the underlying gap without touching the rule.

---

## 2. Reader-facing subtitles / section headers for scan-reading

**Source:** Michael Calvillo, single review on piece 123.

**Still single-source after this batch.** Magda's 123 review asked for stronger distinction
language, not headers. Alberto's 270h review praised the five-step method without asking for
labels.

**Tension:** Directly contradicts the narrative-over-template rule — template section elements are
author checklists, never reader-facing headers (`CLAUDE.md`, Structure; `content-strategy-spec.html`,
Voice Profile). The project's position is that the SharePoint publish layer (blue panel, amber
block) does the navigation work visually, so the source markdown shouldn't need labels.

**What to watch for:** If this recurs, the real question isn't whether to add headers to markdown —
it's whether the *publish-layer* visual treatment is actually landing for readers, or whether
scan-support needs to happen at that layer rather than in prose. Check with whoever owns the
SharePoint publish templates before concluding the markdown needs to change.

---

## 3. Standardized Tier 200 structure — is it legible without labels?

**Source:** Alberto Zamarron, single review on piece 219 (full detail in `219.feedback.md`).

**Counter-signal in the same reviewer, later piece:** on 270h he said the five-step method was
clear, actionable, and "appropriate for Tier 200," with no request for labeled sections. That
points at 219's execution (too much 147-rationale before the method) more than at a library-wide
need for visible templates.

**Note:** This one may not need a second reviewer so much as a self-check — the Tier 200 template
already mandates the structure Alberto is asking for (Trigger, Concept, Method, Artifact, Watchout,
Try This, Proof). Before treating this as a corroboration-pending item, verify 219 is actually
executing the template correctly in narrative form. If it is and the structure still didn't read as
present, that's a genuine signal that narrative-only structure isn't surviving contact with readers
skimming for reference use — which would be a much bigger finding than a single-piece fix.

---

## 4. Researcher-name context and research-vs-extrapolation framing

**Source:** Dr. Magdalena Dybas-Stronkowska, piece 103 (2026-08-26) and again on piece 157
(2026-09-22): "academic and research-focused," simplify methodological language. Same reviewer,
second piece. Still not independent corroboration.

Already captured in full in project memory (`feedback-sourcing-citations.md`) — not re-derived here.

**Status:** Apply on 157 when that piece is revised (Bronfenbrenner / ecological validity is the
obvious target). Don't write it into the spec as a hard rule until a second reviewer raises it.

---

## 5. Audience specificity — name actual work contexts, not generic "building/designing"

**Source:** Dr. Magdalena Dybas-Stronkowska, piece 103 and again on 157 ("more accessible for PMs,
devs, and other not UX audience"; connect helping-during-testing to false confidence in a product
decision). Same reviewer, second piece.

**Status:** Same disposition as #4 — apply judgment on a case-by-case basis for now, especially on
ready-to-publish pieces aimed at mixed practitioner audiences. Don't treat as settled spec.

---

## 6. Length / density — independent reviewers asking to shorten

**Source:** Michael Calvillo on 123 ("edit this down so it's a bit faster read") and Dr.
Dybas-Stronkowska on 157 (shorten a few sections 20–30%). Two independent reviewers, two pieces.

**Not clean promotion yet:** Magda's 123 review asked for *additions* on the same piece Michael
wanted shorter, so "shorter is always better" is false. The shared underlying issue is closer to:
academic or definitional setup that isn't earning its keep for a PM/dev reader.

**What to watch for:** A third hit, especially if someone other than Magda flags 157 or 106-adjacent
pieces as long. If it recurs, the spec change is not a word-count cap (the project already targets
~1000 words and warns against over-compression). It would be: methodological scaffolding belongs
in Sources, not in the Concept pass.

**In the meantime:** on 157, cut jargon before cutting voice. On 123, do not add Magda's full list
and do not gut the piece to satisfy Michael — see `123.feedback.md` synthesis.

---

## 7. Standalone pieces still have to carry their own "when to use this artifact"

**Source:** Alberto Zamarron, piece 270i. He warned non-designers could read "just build it," and
said we cannot count on readers having other articles in mind.

**Status:** This is compliance with an existing rule (`CLAUDE.md` sequencing philosophy: every
piece stands alone), not a new craft rule. Logged so 270i's revision doesn't get filed as "title
preference" only. The fix is an in-piece comparison of sketch / prototype / working-code, not a
What Next dump.

---

## Resolved and promoted to spec

- **Experiential bridge for research citations** — corroborated by two independent reviewers
  (Carolina Louro and Dr. Dybas-Stronkowska) both flagging the Staw (1976) paragraph in piece 103
  for the same underlying reason. Promoted to `content-strategy-spec.html`, Earned Authority module
  ("The Experiential Bridge (research citations)"), 2026-09-02.

---

## Editorial backlog (not craft-spec)

Work that came out of review logging, not a writing-rule question.

- [x] **Contributors block — started 2026-09-22.** Pattern locked as P13 (Contributors) in
  `meta/layout-system.md` and `.claude/agents/write-piece.md` Step 12: after Sources,
  heading `**Contributors**`, then names only, one per line. Distinct from APA Sources.
  Excluded from body word count. Not an author byline (P1 still has no author/date).

  Applied to every piece that currently has a named expert review:
  103 (Carolina Louro, Dr. Magdalena Dybas-Stronkowska), 105 (Alberto Zamarron), 106 (Carolina
  Louro, Dr. Magdalena Dybas-Stronkowska), 123 (Michael Calvillo, Dr. Magdalena Dybas-Stronkowska),
  147 (Alberto Zamarron), 157 (Dr. Magdalena Dybas-Stronkowska), 177 (Alberto Zamarron), 219
  (Alberto Zamarron), 270h (Alberto Zamarron), 270i (Alberto Zamarron).

  Remaining pieces have no named reviewer yet. Add the block when a review lands, not as a
  placeholder.

- [x] **Backfill "Forwarding scenario" into all legacy publish docs — DONE 2026-09-22.** Root
  cause found and fixed: `meta/layout-system.md`'s companion publish doc template and
  `.claude/agents/write-piece.md` Step 12 never included a slot for the forwarding scenario, even
  though write-piece's own Test H computes it during drafting and Phase 9 requires reporting it
  back — it just never had a home in the persisted file. Confirmed via grep that **zero of the 27
  existing `.publish.md` files** had a real forwarding-scenario section (the 4 files matching
  "forward" were incidental word usage — "forward reference," "carried forward," "forwardable
  insight" — not the actual field). Fixed at the template level (both files now specify the field
  and a checklist line) and backfilled a one-sentence scenario ("I sent this to [role/person]
  because [reason]") into **all 27** publish docs, confirmed by grep count after the pass:
  103, 105, 106, 113, 123, 132, 139, 147, 157, 158, 159, 174, 177, 178, 215a, 215b, 219,
  270a–270i, 309. Three files (215b, 270g, 270h) use non-standard section headers from an older
  publish-doc format (no "## Publishing checklist" heading) — inserted the field before their
  closest equivalent (Publishing Checklist / Post-Publication Checklist / Phase 1 QA Notes). Worth
  a follow-up pass to normalize those three onto the current template structure, but not blocking.

- [ ] **Stale duplicate-content bug pattern, worth a systemic check.** While backfilling the above,
  found that `147.publish.md` and `177.publish.md` both carry a *second, independent copy* of
  content that also exists in the article body (147's publish doc has its own Source Attribution
  block with full citation text; 177's publish doc quotes the goal line twice). In both cases, an
  eval-and-repair pass had corrected the article body but missed the duplicate copy living in the
  publish doc, leaving the two files inconsistent with each other. This is a real gap in the
  eval-and-repair skill's D9 checks — it should be diffing publish-doc-embedded content (source
  blocks, quoted goal lines, quoted pull quotes) against the current article body, not just
  checking that the *sections* exist. Worth adding an explicit D9 benchmark for this before the
  next batch eval run, rather than relying on manual catches like this one.
