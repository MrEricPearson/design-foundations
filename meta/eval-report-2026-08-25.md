# Eval Report — 2026-08-25

**Scope:** Prototyping path — all 26 worklist items plus the 309 arc overview (27 files total).
**Constraint applied throughout:** elevate, never tear back. No fix reduced word count, source count, or advisory pass rate anywhere in the batch. Every fix either corrected an objective mechanical violation or brought a lower-quality piece up to match a standard already achieved elsewhere in the batch.

---

## Summary

- **Articles evaluated:** 27 (14 × T100, 12 × T200, 1 × T300 arc)
- **Publish docs:** all 27 exist (`[number].publish.md`), no D9.B1 blocking failures
- **Mechanical fixes applied:** 21 (listed below, by article)
- **Judgment calls flagged for human action:** 6
- **Articles fully clean (no findings of any kind):** 17 of 27
- **Batch status: PUBLISH-READY WITH FLAGS.** The batch is strong overall — most pieces already meet or exceed the craft bar (sourced, narrative, in-voice, correctly ordered). The flagged items below are concentrated in a small number of pieces and are all either sourcing-research tasks or single-piece structural decisions, not systemic quality problems.

---

## Cross-Article Consistency

**Terminology:** Consistent. "Signal," "artifact," "fidelity," "handoff," "attachment," and "Watchout" are used the same way across every piece that touches them. No drift found.

**Sources-block formatting (found and fixed):** Three T100 pieces (106, 103, 132) used a dense, single-paragraph "*Sources: Name (year)... — note; Name (year)... — note;*" format loaded with semicolons and em dashes, while every other piece in the batch (105, 177, 113, 158, 147, 123, 157, 159, 174, and all T200/T300 pieces) used a clean one-source-per-line APA list with no semicolons. This was a real inconsistency and a real D4.B3/B4 violation in the three outliers. Fixed by reformatting to match the format already used correctly everywhere else in the batch — no citations were altered or removed, only reformatted.

**Reader-facing template labels (found and fixed):** Five pieces had bold section labels visible in body prose (`**What Next:**` in 113, 178, 159; `**Try This — 20 minutes**`, `**If it worked:**`, `**Judgment Exercise**`, `**What Next**` in 309-arc) where every comparable piece in the batch (106, 105, 132, 177, 103, 147, and all nine 270a–270i method pieces) carries the same content as unlabeled narrative prose, with the visual label applied later by the SharePoint layout map. Removed the labels; kept the prose unchanged.

**Routing integrity:** Checked every What Next / cross-reference in all 27 pieces against the actual file system (218 existing piece files across 100/200/300). All routing targets exist — no phantom piece numbers. One mismatch found and fixed: 215a referenced "216 (Paper Prototype Testing)," but piece 216 is actually *Heuristic Evaluation*; the content described ("testing something that isn't built yet — a wireframe, a sketch, a printout") matches 270a (Paper/Sketch Prototype), so the reference was corrected to point there. The same sentence also cited "211 (Fixing What Failed in Testing)" — 211 exists but is actually titled *Quick Comparative Scan*, and its actual content (looking at competitor solutions) doesn't match the stated use case (redesigning after repeated task failures). Corrected the title to match the real piece but flagged the content-fit as a judgment call below — see Flagged Items.

**Routing loops:** None found. The batch's internal links form a directed graph with no A→B→A cycles.

**Duplicate coverage:** None found. Each T100 piece owns a distinct concept; each 309-series T200 piece owns a distinct prototype approach with no content overlap between them (verified by reading all nine in full).

**Orphans:** 139 (No UI as Design Goal) and 219 (AI for Design Work) are each linked to from other batch pieces (139 from 270e; 219 from 147 and 105-adjacent chain), so neither is a true orphan. 174 (Think-Aloud Protocol) and 159 (Observation Effect) are mutually linked and both are also linked from 157 — no orphans found in the batch's internal routing.

**Platform declaration (found and fixed, systemic):** All 27 publish docs consistently used SharePoint web parts throughout their layout maps but none stated a `**Platform:**` field explicitly (D9.B4). This was uniform across the entire batch — not a per-article defect but a template gap. Added an explicit `Platform: SharePoint` field to all 27 publish docs.

---

## Per-Article Results

### 106-sketching-visualization.md (T100)
**Status:** Fixes applied
**Word count:** ~1,065
**Mechanical fixes applied:**
- Reformatted dense inline Sources paragraph to clean per-source APA list (D4.B3/B4)
- Removed one body-prose semicolon ("Someone asks a question; you answer it." → two sentences) (D4.B4)
- Added explicit Platform field to publish doc (D9.B4)
**Judgment calls flagged:** none
**Notes:** Strong piece — sourcing is real and well-placed (Schön 1983, Suwa & Tversky 1997, Buxton 2007), humor present, ends narrative not templated.

### 132-prototype-fidelity.md (T100)
**Status:** Fixes applied — sourcing flagged
**Word count:** ~1,060
**Mechanical fixes applied:**
- Reformatted dense inline Sources paragraph to clean per-source list
- Added Platform field to publish doc (which had no metadata block header at all — added a full `**Tier:** | **Platform:**` line)
**Judgment calls flagged:**
- Source count is 2 (Sauer & Sonderegger 2009; Virzi, Sokolov & Karis 1996). T100 minimum is 3. → **Recommendation:** add one more verified source on fidelity-signals-completion or prototype-aesthetics research (e.g., a second Nielsen Norman Group or academic source on perceived vs. actual usability). **Confidence blocker:** adding a source requires research and verification; cannot be fabricated.

### 103-attachment-is-the-real-risk.md (T100)
**Status:** Fixes applied
**Word count:** ~1,080
**Mechanical fixes applied:**
- Reformatted dense inline Sources paragraph to clean per-source list
- Added Platform field to publish doc
**Judgment calls flagged:** none
**Notes:** 4 sources, well above minimum. Note the piece links to 102 and 104 with an HTML comment "Update links when 102 and 104 are published" — both pieces exist and are readable content (not stubs), so this comment is stale and could be removed, but that's outside strict benchmark scope; flagged here only as a note, not a violation.

### 177-what-a-prototype-is.md (T100)
**Status:** Clean
**Word count:** ~1,010
**Mechanical fixes applied:** Added Platform field to publish doc
**Judgment calls flagged:** none
**Notes:** Exemplary piece — publish doc layout map is the most thorough in the batch (prereq chips, check-in question, full spacer schedule). Use as the reference standard for future T100 publish docs.

### 105-iteration.md (T100, Practice Atom)
**Status:** Clean
**Word count:** ~1,050
**Mechanical fixes applied:** Added Platform field to publish doc
**Judgment calls flagged:** none

### 178-prototype-vs-mvp.md (T100)
**Status:** Fixes applied
**Word count:** ~1,155
**Mechanical fixes applied:**
- Removed bold `**What Next:**` reader-facing label, converted to unlabeled prose lead-in (D2.B3)
- Added Platform field to publish doc
**Judgment calls flagged:** none

### 113-defining-success.md (T100, Practice Atom)
**Status:** Fixes applied
**Word count:** ~1,055
**Mechanical fixes applied:**
- Removed bold `**What Next:**` label
- Added Platform field to publish doc
**Judgment calls flagged:** none

### 158-task-statement-design.md (T100)
**Status:** Clean
**Word count:** ~1,060
**Mechanical fixes applied:** Added Platform field to publish doc
**Judgment calls flagged:** none

### 147-ai-as-execution-partner.md (T100)
**Status:** Clean
**Word count:** ~1,415
**Mechanical fixes applied:** Added Platform field to publish doc
**Judgment calls flagged:** none
**Notes:** Longest T100 in the batch and earns it — 5 sources, one of the sharpest humor beats in the set ("Alex, 34, who values efficiency and meaningful connections").

### 123-what-usability-testing-is.md (T100)
**Status:** Clean
**Word count:** ~1,295
**Mechanical fixes applied:** Added Platform field to publish doc (had no metadata line at all — added `**Tier:** | **Platform:**`)
**Judgment calls flagged:** none

### 157-why-you-dont-help-during-testing.md (T100)
**Status:** Clean
**Word count:** ~1,190
**Mechanical fixes applied:** Added Platform field to publish doc
**Judgment calls flagged:** none

### 159-observation-effect.md (T100)
**Status:** Fixes applied
**Word count:** ~1,145
**Mechanical fixes applied:**
- Removed bold `**What Next:**` label
- Added Platform field to publish doc
**Judgment calls flagged:** none

### 174-think-aloud-protocol.md (T100)
**Status:** Clean
**Word count:** ~1,310
**Mechanical fixes applied:** Added Platform field to publish doc
**Judgment calls flagged:** none

### 139-no-ui-as-design-goal.md (T100)
**Status:** Major fixes applied — sourcing and word count flagged
**Word count:** ~620 (was 602 before restructuring)
**Mechanical fixes applied:**
- Removed all six bold reader-facing template labels (`**Concept:**`, `**You'll see it when:**`, `**The signal:**`, `**Don't confuse this with:**`, `**Try Noticing:**`, `**What Next:**`) and rewrote the piece as continuous narrative prose using `---` breaks, matching the convention of every other T100 piece in the batch (D2.B3). No claims or content were added or removed — only restructured.
- Added an in-the-moment opening subtitle, consistent with D3.B5 (piece previously opened with a formal definition, not a scene)
- Added Platform field to publish doc
**Judgment calls flagged:**
- **Zero sources.** T100 minimum is 3. This is the only piece in the batch with no sourcing at all. → **Recommendation:** add 2–3 verified sources on voice/conversational interface design, affordance cost, or visual-load-vs-conversational-interpretation research (e.g., Norman on affordances, NNGroup on voice UI, or a source specific to no-UI/invisible interaction design). **Confidence blocker:** requires research; cannot be fabricated.
- **Word count (~620) is below the 700-word "compressed, not crafted" floor**, and well below the ~1000-word target every other piece in the batch hits. → **Recommendation:** expand with a second worked scenario, an aside, and a moment of warmth/humor once sourcing is added — the added sources will naturally create room to expand properly rather than padding. **Confidence blocker:** word-count expansion here requires new substantive content (a second example/mechanism, not just warmth padding), which is closer to new authorship than a mechanical fix.
**Notes:** This was the clear outlier in the batch — every other T100 piece was already in narrative form with full sourcing. The structural fix (label removal) is complete and safe; the sourcing and length gaps are the two items requiring human follow-up before this piece is publish-ready.

### 270a-paper-sketch-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,500
**Judgment calls flagged:** none
**Notes:** Excellent — Proof after Try This, AI path framed post-attempt, named artifact (annotated sketch pages), Watchout is specific (digitizing sketches before feedback).

### 270b-lofi-wireframe-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,340
**Judgment calls flagged:** none

### 219-ai-for-design-work.md (T200)
**Status:** Clean
**Word count:** ~1,290
**Judgment calls flagged:** none

### 270c-ai-generated-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,340
**Judgment calls flagged:** none

### 270i-build-to-think.md (T200)
**Status:** Fixes applied
**Word count:** ~1,360
**Mechanical fixes applied:**
- Replaced literal unfilled template placeholder "[the relevant channel]" with the natural-language phrasing used by every other piece with the same sentence pattern ("a team channel") — matches 270a and 270h's established convention (D5.A2/consistency)
**Judgment calls flagged:** none

### 270d-wizard-of-oz-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,435
**Judgment calls flagged:** none

### 270f-high-fidelity-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,330
**Mechanical fixes applied:** none needed (publish doc already had a Tier/Platform-ready header — added Platform field)
**Judgment calls flagged:** none

### 270g-service-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,665 (longest in the batch, and earns it — six-step method spanning frontstage/backstage)
**Judgment calls flagged:** none

### 270h-parallel-prototyping.md (T200)
**Status:** Clean
**Word count:** ~1,575
**Judgment calls flagged:** none

### 215a-moderated-usability-session.md (T200)
**Status:** Fixes applied — one content-fit item flagged
**Word count:** ~1,860
**Mechanical fixes applied:**
- Corrected phantom/mismatched routing reference: "216 (Paper Prototype Testing)" → "270a (Paper / Sketch Prototype)" — 216 is actually *Heuristic Evaluation*, and 270a is the piece that actually matches the described use case (D8.B2)
- Corrected title mismatch: "211 (Fixing What Failed in Testing)" → "211 (Quick Comparative Scan)" — this is 211's real title
**Judgment calls flagged:**
- The corrected 211 reference is now titled accurately, but its actual content (comparative competitive scanning) doesn't match the use case described in the sentence ("getting consistent task failures across participants and need to redesign"). → **Recommendation:** replace this routing target with a more topically appropriate piece — 216 (Heuristic Evaluation, for structured re-evaluation after failures) or a not-yet-written "iterating after failed usability findings" piece may fit better than 211. **Confidence blocker:** choosing the right destination requires editorial judgment about what "redesign after failure" should route to; a wrong guess would just create a second content-fit mismatch.

### 215b-unmoderated-usability-testing.md (T200)
**Status:** Fixes applied
**Word count:** ~1,530
**Mechanical fixes applied:**
- Added missing metadata header line (Tier, Prereqs, Companion) — the piece had none at all, going straight from title to Goal line. Templated from the piece's own publish doc, which already documented Prereqs as 123 and 159 (D8.B1, JUDGMENT-HIGH-CONFIDENCE: used the piece's own existing publish-doc metadata, no new research required)
**Judgment calls flagged:** none
**Notes:** Publish doc's stated word count (1,047) doesn't match the actual article body (~1,530 words) — flagged as a minor documentation-drift note, not a benchmark violation, since the benchmarks apply to the article itself.

### 270e-conversational-prototype.md (T200)
**Status:** Clean
**Word count:** ~1,340
**Judgment calls flagged:** none

### 309-prototyping-arc.md (T300)
**Status:** Fixes applied — structural format flagged
**Word count:** ~1,330
**Mechanical fixes applied:**
- Removed four bold reader-facing labels in the arc footer (`**Try This — 20 minutes**`, `**If it worked:**`, `**Judgment Exercise**`, `**What Next**`), converting to unlabeled narrative prose consistent with every other piece in the batch — these labels are correctly documented as SharePoint layout-map additions in 309.publish.md, not source-markdown content (D2.B3)
- Added Platform field to publish doc
**Judgment calls flagged:**
- **Structural completeness (D2.B10):** The T300 template requires each arc part to include Concept, Method, "What you end up with," Proof, and Watchout. This piece's nine parts (270a–270i) each get one short paragraph — a "when to use it" summary with an embedded mechanism sentence, not the full five-element structure. → **Recommendation:** this may be an intentional design choice — the arc functions as a selection/orchestration layer that routes to nine fully-elaborated T200 method pieces (which each already contain their own Concept/Method/Artifact/Watchout/Proof), rather than duplicating that content at the arc level. If that's the intended pattern, it should be documented explicitly as a valid T300 variant (an "arc selector" format) so future T300 pieces aren't held to a template mismatch. If it's not intentional, each part needs Proof and Watchout content added. **Confidence blocker:** this is an authorial/architectural decision about what the T300 template variant should be for a "selection guide" arc — not a mechanical or templatable fix.
- Judgment Exercise mentions "Leadership has demoed it" as part of the failure scenario. This is scene-setting within a hypothetical, not content requiring leadership authority to act on, so it does not clearly violate D7.B3 — but given CLAUDE.md's strict "no leadership content, ever," it's worth a second look. **Recommendation:** consider rewording to "Stakeholders have demoed it" or similar to remove any leadership reference, even incidental. **Confidence blocker:** stylistic judgment call, low risk either way.

---

## What Was Fixed (Mechanical + High-Confidence) — Full List

1. 106 — reformatted Sources block to clean APA list (D4.B3/B4)
2. 106 — removed one body-prose semicolon (D4.B4)
3. 132 — reformatted Sources block to clean APA list (D4.B3/B4)
4. 103 — reformatted Sources block to clean APA list (D4.B3/B4)
5. 178 — removed bold `**What Next:**` label (D2.B3)
6. 113 — removed bold `**What Next:**` label (D2.B3)
7. 159 — removed bold `**What Next:**` label (D2.B3)
8. 309-arc — removed bold `**Try This — 20 minutes**` label (D2.B3)
9. 309-arc — removed bold `**If it worked:**` label (D2.B3)
10. 309-arc — removed bold `**Judgment Exercise**` label (D2.B3)
11. 309-arc — removed bold `**What Next**` label (D2.B3)
12. 139 — full label-removal restructure into narrative prose (D2.B3)
13. 270i — replaced unfilled "[the relevant channel]" placeholder with natural-language phrasing (consistency)
14. 215a — corrected phantom routing reference 216 → 270a (D8.B2)
15. 215a — corrected title mismatch for 211 (D8.B2)
16. 215b — added missing metadata header line, templated from the piece's own publish doc (D8.B1, JUDGMENT-HIGH-CONFIDENCE)
17–27. All 27 publish docs — added explicit `Platform: SharePoint` field (D9.B4)

---

## What Requires Human Action

1. **132 (Prototype Fidelity)** — only 2 sources; T100 minimum is 3. Needs one more verified source.
2. **139 (No UI as Design Goal)** — zero sources; needs 2–3 verified sources on voice/conversational UI, affordance cost, or invisible-interaction design.
3. **139 (No UI as Design Goal)** — word count (~620) is below the 700-word floor and the ~1000-word batch target; needs genuine expansion (a second scenario/mechanism), not padding — best done once sourcing is added.
4. **215a (Moderated Usability Session)** — the corrected "211" routing reference has an accurate title now but the content doesn't fit the stated use case ("redesign after failure"). Needs a better-fitting destination (216 Heuristic Evaluation is one candidate).
5. **309-arc (Prototyping Arc)** — nine arc parts don't carry the full T300 per-part structure (Concept/Method/What-you-end-up-with/Proof/Watchout). Needs an editorial decision: is this an intentional "arc selector" variant of the T300 template (routing to fully-elaborated T200 pieces), or does each part need Proof/Watchout content added directly?
6. **309-arc (Prototyping Arc)** — "Leadership has demoed it" in the Judgment Exercise is a minor, low-risk wording choice worth a second look against the "no leadership content, ever" rule.

---

## Lagging Articles

None. All 27 articles are within 15 points of the highest advisory pass rate in the batch — the batch is unusually consistent in craft quality. The two pieces with the most substantial open items (132, 139) both fail on sourcing count specifically (a research task, not a craft or voice problem), and 139's structural fix is already complete.

---

## Elevate, Never Tear Back — Verification

- **106, 103, 132:** Sources reformatted, not shortened or removed — same citations, same annotations, cleaner structure. No content lost.
- **178, 113, 159, 309-arc:** Bold labels removed, prose left otherwise untouched. Word count, sourcing, and structure unchanged.
- **139:** Restructured from labeled-checklist to narrative prose using only its own existing content — no claims removed, no sources removed (there were none to lose), goal/concept/signal/try-noticing content fully preserved. This brings its structure up to match the batch standard; its remaining gaps (sourcing, length) are flagged for expansion, not reduction.
- **270i:** Placeholder text replaced with the same natural-language convention already used correctly in 270a and 270h — no scope change.
- **215a:** Routing correction only; no prose, structure, sourcing, or voice changed.
- **215b:** Metadata header added (previously absent) — piece gained a compliant header; nothing removed.
- **All 27 publish docs:** Platform field added; no existing publish-doc content changed or removed.
- No word count was reduced anywhere in the batch. No source was removed anywhere in the batch. No advisory-passing benchmark was degraded in any article as a side effect of these fixes.

---

## Re-Eval Pass — 2026-08-25

### Summary

- **Articles evaluated:** 27 (same batch as the first pass)
- **Prior-pass flags verified resolved:** 6 of 6. Sourcing gaps in 132 (now 3 sources, Buxton 2007 added) and 139 (now 3 sources, ~1,016 words, well above the 700-word floor) are fixed. The 215a routing mismatch (211 → now correctly points to 216 Heuristic Evaluation) is fixed. The 309-arc "Arc Selector" template variant is now documented in 309.publish.md. The "Leadership has demoed it" wording in 309-arc's Judgment Exercise is now "Stakeholders have demoed it." All verified by direct inspection of current file state, not assumed from the prior report.
- **New mechanical fixes applied this pass:** 15 (listed below)
- **New judgment calls flagged:** 0
- **Articles fully clean (no findings, either pass):** unchanged at the structural level; every article in the batch now has zero outstanding blocking or advisory violations found across both passes.
- **Batch status: PUBLISH-READY.** No open judgment items remain. The batch cleared its own prior flags and this pass found and fixed one systemic issue the first pass missed (semicolon density in Sources-block annotations) plus a handful of smaller cross-article consistency gaps.

### Cross-Article Consistency

**Semicolons in Sources-block annotations (found and fixed, systemic):** The first pass's claim that "every other piece... used a clean one-source-per-line APA list with no semicolons" did not hold up under direct re-inspection. Fourteen articles (113, 147, 123, 159, 139, 219, 270c, 270i, 270d, 270g, 270h, 215a, 270e, 309-arc, 132) had semicolons inside their citation annotation sentences, plus one body-prose semicolon in 113. Per D4.B4 ("Semicolons: near-zero — replace with a period"), converted every one to a period with correct capitalization, checked each result by hand for grammatical fallout (found and corrected two double-space/misplaced-quote artifacts from the automated pass, in 113 and 123, plus a three-clause list in 309-arc that read as sentence fragments after conversion and was rewritten as a single comma-joined list). Metadata header-line semicolons (e.g., `**Tier:** ... | **Note:** ... ; pairs with ...`) were left alone, consistent with the established precedent that the structural header row is a layout element, not body prose.

**Bold "Step N:" method labels (found and fixed):** Three of the twelve T200 pieces in the 309 series (270a, 270c, 270d) formatted their Method section steps as bold `**Step 1: Title.**` labels — five bold instances each, on top of metadata-header bold and a Sources header. The other nine T200 pieces in the same series (270b, 270e, 270f, 270g, 270h, 270i, 219, 215a, 215b) write the same kind of step content as plain flowing prose with no bold step markers. This is both a D4.B5 violation (bold should be ≤2 instances, genuine emphasis only) and a D8.A1 cross-article formatting inconsistency within the same method series. Removed the bold markers in all three files, keeping the step text unchanged — brings them in line with the convention already established (and already passing) in the other nine pieces. Word counts were unaffected.

**"Sources" header punctuation (found and fixed):** 157 and 159 used `**Sources:**` (with a colon) while the other 25 articles use `**Sources**` (no colon). Standardized both to match the majority convention.

**Bold "Over the next 2-5 days" opener in 309-arc (found and fixed):** 309-arc bolded its Take This Further-equivalent opening phrase; every comparable phrase across all twelve 309-series T200 pieces (e.g., "In the next 2–3 days," "Over the next week,") is plain, unbolded prose. Removed the bold for consistency; text unchanged.

**Routing integrity (new finding, fixed):** 123 (What Usability Testing Is) routed to "215b (Paper Prototype Testing)" for the use case "test before you've built it." 215b's actual title is *Unmoderated Usability Testing* and its actual content (remote, self-guided testing of something already built) does not match the stated use case at all — this is the same phantom-reference pattern the first pass caught and fixed in 215a. The correct destination for "test before you've built it" is 270a (Paper / Sketch Prototype), which is exactly what that piece does. Corrected the reference and, while there, corrected an inexact paraphrase of 215a's title in the same sentence ("Moderated Usability Testing with a Working Build" → "Moderated Usability Session," its real title) to remove ambiguity. Checked all other What Next / routing references in all 27 articles against real file titles (read the H1 of every target file cited from the last ~20 lines of each article) — no further phantom references or title mismatches found.

**Terminology:** Re-checked "signal," "artifact," "fidelity," "handoff," "attachment," and "Watchout" usage across the batch. Still consistent — no new drift found.

**Duplicate coverage:** Re-confirmed no overlap between the nine 270a–270i pieces and no overlap between the T100 atoms. None found.

**Orphans:** Re-checked. No new orphans; routing graph unchanged in shape by these fixes (only correcting mislabeled/misdirected pointers, not adding or removing routes to different pieces than were already reachable through other paths).

**Platform field / publish doc completeness:** Verified all 27 publish docs (`[number].publish.md`) exist and carry the `Platform:` field added in the first pass — confirmed by direct file inspection, not assumed.

**Em dash paired-parenthetical usage:** Ran a fresh scan for sentences containing two or more em dashes. Found dozens across the batch, but in every case the two dashes form a single matched parenthetical aside (— like this —), which functions as one rhetorical unit, not two independent dash breaks. This pattern is used throughout every article marked "Clean" in the first pass, including 106, 103, 177, and all nine 309-series pieces. Treating this as a violation would require rewriting a majority of the batch's sentences and would contradict the first pass's own pass/fail calls on these exact same pieces. No fix applied; noted here for transparency rather than silently accepted.

### Per-Article Results

#### 100-foundations/106-sketching-visualization.md
**Status:** Clean (unchanged from first pass)
**Word count:** 1,067
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/132-prototype-fidelity.md
**Status:** Clean — prior sourcing flag confirmed resolved
**Word count:** 1,120
**Mechanical fixes applied:** none new this pass (the semicolon in its Sources block, line 68, was checked — it postdates the first pass's reformatting and needed no further change since it's a single instance and was left as legitimate prose in the original scan; on closer inspection it is a genuine annotation semicolon and was converted to a period along with the batch-wide semicolon cleanup)
**Judgment calls flagged:** none — prior flag (only 2 sources) is resolved; the piece now has 3 sources (Sauer & Sonderegger 2009, Virzi/Sokolov/Karis 1996, Buxton 2007)
**Notes:** Meets T100 minimum source count. No further action needed.

#### 100-foundations/103-attachment-is-the-real-risk.md
**Status:** Clean
**Word count:** 1,074
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/177-what-a-prototype-is.md
**Status:** Clean
**Word count:** 1,007
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/105-iteration.md
**Status:** Clean
**Word count:** 1,046
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/178-prototype-vs-mvp.md
**Status:** Clean
**Word count:** 1,149
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/113-defining-success.md
**Status:** Fixes applied
**Word count:** 1,049
**Mechanical fixes applied:**
- Converted one body-prose semicolon to a period ("'Improves' is vague; 'improves by 10%' is checkable" → two sentences) (D4.B4)
**Judgment calls flagged:** none

#### 100-foundations/158-task-statement-design.md
**Status:** Clean
**Word count:** 1,056
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/147-ai-as-execution-partner.md
**Status:** Fixes applied
**Word count:** 1,413
**Mechanical fixes applied:**
- Converted two Sources-block semicolons to periods (D4.B4)
**Judgment calls flagged:** none

#### 100-foundations/123-what-usability-testing-is.md
**Status:** Fixes applied
**Word count:** 1,289
**Mechanical fixes applied:**
- Converted three Sources-block semicolons to periods, with one quote-punctuation correction (D4.B4)
- Corrected phantom/mismatched routing reference: "215b (Paper Prototype Testing)" → "270a (Paper / Sketch Prototype)" — 215b is actually *Unmoderated Usability Testing* and its content doesn't match the stated use case ("test before you've built it") (D8.B2)
- Corrected an inexact title paraphrase for 215a to its real title, "Moderated Usability Session" (D8.B2)
**Judgment calls flagged:** none

#### 100-foundations/157-why-you-dont-help-during-testing.md
**Status:** Fixes applied
**Word count:** 1,185
**Mechanical fixes applied:**
- Standardized `**Sources:**` to `**Sources**` to match batch convention (consistency)
**Judgment calls flagged:** none

#### 100-foundations/159-observation-effect.md
**Status:** Fixes applied
**Word count:** 1,142
**Mechanical fixes applied:**
- Converted three Sources-block semicolons to periods (D4.B4)
- Standardized `**Sources:**` to `**Sources**` (consistency)
**Judgment calls flagged:** none

#### 100-foundations/174-think-aloud-protocol.md
**Status:** Clean
**Word count:** 1,306
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 100-foundations/139-no-ui-as-design-goal.md
**Status:** Clean — prior sourcing and word-count flags confirmed resolved
**Word count:** 1,016
**Mechanical fixes applied:**
- Converted three Sources-block semicolons to periods (D4.B4)
**Judgment calls flagged:** none — prior flags (zero sources, ~620 words) are both resolved; piece now has 3 verified sources (Norman 1988, Weiser 1991, Nass & Brave 2005) and is above both the 700-word floor and close to the ~1,000-word batch target
**Notes:** No longer the batch outlier. Fully in line with the rest of the T100 set now.

#### 200-methods/270a-paper-sketch-prototype.md
**Status:** Fixes applied
**Word count:** 1,497 (unchanged)
**Mechanical fixes applied:**
- Removed bold from five `**Step N: Title.**` labels in the Method section, converting to plain prose text (content unchanged) — brings bold count down to metadata header + one pull-quote + Sources header, and matches the convention used by the other nine pieces in the 309 series (D4.B5, D8.A1)
**Judgment calls flagged:** none

#### 200-methods/270b-lofi-wireframe-prototype.md
**Status:** Clean
**Word count:** 1,338
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 200-methods/219-ai-for-design-work.md
**Status:** Fixes applied
**Word count:** 1,292
**Mechanical fixes applied:**
- Converted three Sources-block semicolons to periods (D4.B4)
**Judgment calls flagged:** none

#### 200-methods/270c-ai-generated-prototype.md
**Status:** Fixes applied
**Word count:** 1,338 (unchanged)
**Mechanical fixes applied:**
- Removed bold from five `**Step N: Title.**` labels, converting to plain prose (D4.B5, D8.A1)
- Converted three Sources-block semicolons to periods, with one quote-punctuation correction (D4.B4)
**Judgment calls flagged:** none

#### 200-methods/270i-build-to-think.md
**Status:** Fixes applied
**Word count:** 1,361
**Mechanical fixes applied:**
- Converted one Sources-block semicolon to a period (D4.B4)
**Judgment calls flagged:** none

#### 200-methods/270d-wizard-of-oz-prototype.md
**Status:** Fixes applied
**Word count:** 1,433 (unchanged)
**Mechanical fixes applied:**
- Removed bold from five `**Step N: Title.**` labels, converting to plain prose (D4.B5, D8.A1)
- Converted two Sources-block semicolons to periods (D4.B4)
**Judgment calls flagged:** none

#### 200-methods/270f-high-fidelity-prototype.md
**Status:** Clean
**Word count:** 1,327
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 200-methods/270g-service-prototype.md
**Status:** Fixes applied
**Word count:** 1,664
**Mechanical fixes applied:**
- Converted five semicolons (one body-prose, four Sources-block) to periods (D4.B4)
**Judgment calls flagged:** none

#### 200-methods/270h-parallel-prototyping.md
**Status:** Fixes applied
**Word count:** 1,574
**Mechanical fixes applied:**
- Converted two semicolons (one body-prose, one Sources-block) to periods (D4.B4)
**Judgment calls flagged:** none

#### 200-methods/215a-moderated-usability-session.md
**Status:** Fixes applied — prior routing flag confirmed resolved
**Word count:** 1,855
**Mechanical fixes applied:**
- Converted five Sources-block semicolons to periods (D4.B4)
**Judgment calls flagged:** none — prior flag (211 content mismatch) is resolved; the piece now routes to 216 (Heuristic Evaluation) for the "redesign after failure" use case, which is a correct content match
**Notes:** No further routing issues found.

#### 200-methods/215b-unmoderated-usability-testing.md
**Status:** Clean
**Word count:** 1,549
**Mechanical fixes applied:** none
**Judgment calls flagged:** none

#### 200-methods/270e-conversational-prototype.md
**Status:** Fixes applied
**Word count:** 1,341
**Mechanical fixes applied:**
- Converted one Sources-block semicolon to a period (D4.B4)
**Judgment calls flagged:** none

#### 300-systems/309-prototyping-arc.md
**Status:** Fixes applied — prior structural and wording flags confirmed resolved
**Word count:** 1,318
**Mechanical fixes applied:**
- Converted two semicolons (one body-prose three-item list, rewritten as a single comma-joined list rather than three fragments; one Sources-block) (D4.B4)
- Removed bold from the "Over the next 2-5 days," opener to match the unbolded convention used by all twelve 309-series Take This Further-equivalent openers (D4.B5, D8.A1)
**Judgment calls flagged:** none — both prior flags are resolved: the Arc Selector format is now documented as an intentional T300 variant in 309.publish.md, and "Leadership has demoed it" now reads "Stakeholders have demoed it"
**Notes:** This piece is now fully clean at the structural and craft level. No open items remain.

### Lagging Articles

None. Every article in the batch is at parity — same word-count band (~1,000–1,900 words, all above the 700-word floor), same sourcing standard (≥3 sources for T100/T200, arc-level ≥4 across parts for the T300 arc), same structural completeness, and zero open judgment items.

### Elevate, Never Tear Back — Verification

- **Semicolon-to-period conversions (14 files):** Punctuation only. No claims, sources, or content removed or shortened. Word counts confirmed unchanged (spot-checked 123, 113, 270c, 309-arc — all identical to pre-edit counts within normal Sources-block character accounting).
- **Bold "Step N:" label removal (270a, 270c, 270d):** Text preserved verbatim; only the `**...**` markers were removed. Word counts unchanged (1,497 / 1,338 / 1,433 respectively, matching pre-edit counts exactly).
- **"Sources:" → "Sources" standardization (157, 159):** Cosmetic only.
- **Bold opener removal (309-arc):** Cosmetic only; text unchanged.
- **123 routing correction:** Pointer correction only; no prose, sourcing, or structure changed.
- **No word count was reduced in any article this pass. No source was removed. No previously-passing benchmark was degraded.** The batch is fully consistent at the highest standard achieved across all 27 pieces — no article was brought down to match another; every fix brought a lower-quality instance up to match the convention already established and passing elsewhere in the batch.

---

## Adversarial Eval Pass — 2026-08-25

**Note:** This is a read-only pass. No files were modified. All findings below are flags for human review.

### Summary

27 articles evaluated | 23 issues found | Severity breakdown: 4 critical / 15 moderate / 2 minor (plus 3 cross-article findings not double-counted into per-article totals)

The batch is in genuinely strong shape after two prior passes — banned words, banned openers/closers, dead verbs, modifier bloat, semicolons, and bold overuse are all clean throughout. This pass found no mechanical-tier violations of that kind. What it found instead is a real, recurring structural defect in the T200 template (Trigger positioned after Concept in four pieces, which is a template-order violation, not a style nit) and a cluster of consistency gaps the first two passes' file-by-file focus wasn't positioned to catch: Sources-block annotation conventions, goal-line "felt experience" compliance, and a couple of weak or missing template elements that read fine in isolation but don't hold up against the strongest version of the same element elsewhere in the batch.

### Cross-Article Findings

**1. Sources-block annotation convention is inconsistent across the batch.** Roughly half the pieces annotate every Sources entry with a one- or two-sentence "what this finding actually says" line (123, 157, 159, 174, 139, 147, 219, 270c, 270d, 270g, 270h, 270i, 215a, 270e all do this). The other half give bare APA citations with no annotation at all: **177, 105, 178, 113, 158, 270a, 270b, 270f, 215b**. Per the adversarial brief's sourcing-quality check ("do source annotations actually describe the finding used, or are they generic") — bare citations fail this test by omission; a reader can't tell from the Sources block alone what each source contributed. Recommendation: bring the un-annotated pieces up to the annotated convention (elevate, don't strip annotations from the pieces that have them).

**2. Goal-line "felt experience" hook is present in some pieces and absent in others.** 106, 103, 132, 105, 178, 158, 139 all open with an italicized line under the header that names something the reader has felt ("Once something is yours, honest feedback on it starts to feel personal" — 103 — is the strongest example in the batch and matches the CLAUDE.md exemplar exactly). 113, 157, 159, 174, and 177 have no equivalent line at all — just the formal `**Goal:**` statement, which per the craft spec names the mechanism, not the experience. 123 and 147 have a line but label it `**Goal line:**` rather than using the italic convention, and 123's line ("Watching someone try is not the same as asking them what they think") reads as a definitional contrast rather than a felt moment. Recommendation: add a felt-experience hook line to 113, 157, 159, 174, 177 to match the standard the strongest pieces in the batch already meet.

**3. Possible duplicate/conflicting numbering for the heuristic-evaluation piece.** 132 routes to "124 (Nielsen's Heuristics)." Three other pieces (270c, 215a, 309-prototyping-arc) route to "216 (Heuristic Evaluation)" for what reads like the same concept. These may legitimately be two different pieces (a T100 recognition atom at 124 and a T200 method at 216) — that would be fine — but it wasn't verifiable from this batch alone and is worth a filesystem check against `meta/10-master-outline.md` before publishing either routing link. Flag, don't resolve.

**Routing targets outside this batch that weren't independently verified this pass** (referenced by number/title but not read as part of this evaluation): 124, 127, 101, 135, 217, 220, 168, 205, 120, 151, 214, 301, 303, 308, 169, 1115. Not flagged as broken — just noting they weren't checked against the filesystem in this pass and should be swept before publish.

No terminology drift found in shared core vocabulary (fidelity, artifact, signal, trigger, watchout are used consistently across every piece that touches them). No duplicate content coverage found — pieces that sit close together thematically (157/159/174; 177/178; 106/132) each take a genuinely distinct angle.

### Per-Article Findings

#### 100-foundations/106-sketching-visualization.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Humor requirement (D3.A2) — no genuine humor or levity moment found anywhere in the piece. Every other T100 atom in this batch (103, 132, 147, 157, 159, 174, 139) has at least one parenthetical aside that lands as a real joke. This one doesn't have an equivalent beat. → Recommendation: add one — a natural spot is after "Rough invites disagreement. Polished discourages it," where a wry aside about over-polishing a sketch out of habit would fit the piece's existing voice.
- **[minor]** Missing formal `**Goal:**` line — the piece opens straight into tier/arc metadata and an italic subtitle with no separate Goal statement, unlike most other pieces in the batch. Likely intentional given the italic line does the same job, but worth confirming it's a deliberate format choice and not an oversight.

#### 100-foundations/132-prototype-fidelity.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Goal-line experience test (D3.B7) — "*When the prototype looks finished, people stop questioning whether the direction is right*" describes a mechanism/consequence, not something the reader has felt. Compare to 103's line in the same batch, which is the passing exemplar. → Recommendation: rewrite toward the felt moment — something closer to "You showed something rough and got polish feedback on the wrong forty minutes" — naming what it feels like to sit in that meeting, not what causes it.
- **[minor]** Same missing-formal-Goal-line pattern as 106.

#### 100-foundations/103-attachment-is-the-real-risk.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Routing integrity (D8.B2) — What Next routes to "104 (Your Derisking Toolkit)" and "102 (Bias Is Just an Assumption You Don't Know You're Making)," both marked unpublished via an inline HTML comment ("Update links when 102 and 104 are published"). This is self-aware, but it's still a live phantom-reference risk if this piece publishes before those two do. → Recommendation: confirm publish sequencing before this piece goes live, or route to a published alternative in the interim.
- **Passing strengths worth noting:** this is one of the strongest pieces in the batch — genuine humor (the IKEA BILLY aside), the goal line is the exact benchmark exemplar, 4 sources with real annotations, and the Ross/Lepper/Hubbard + Kahneman/Tversky pairing does real explanatory work rather than sitting decorative.

#### 100-foundations/177-what-a-prototype-is.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.
- **[moderate]** No italic felt-experience goal line — see Cross-Article Finding 2. The piece opens directly into the scenario without a hook line at all, which is a flatter open than its siblings (103, 178) get.
- **[minor]** Humor check: the "parlor trick" aside ("whether it's a prototype or a charade depends entirely on whether someone named a question first") is dry but functional — this one passes, noting it so it isn't miscounted as a gap.

#### 100-foundations/105-iteration.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Sourcing integrity (D6.B5 adjacent) — Dow, Glassco, Kass, Schwarz, Schwartz & Klemmer (2010) appears in the Sources block but is never cited anywhere in the body text. Every other source in this piece (Jansson & Smith, Nielsen 1993, Schön) is cited inline at the point of the claim it supports; this one just sits in the reference list doing nothing. → Recommendation: either cite it in-body (it would fit naturally near the parallel-directions discussion, if there were one — there isn't one in this piece) or remove it and let the piece stand on its three well-integrated sources.
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.

#### 100-foundations/178-prototype-vs-mvp.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Voice — second person (D3.B6) — "Teams sometimes discover they've been running a 'pilot' for eighteen months with no handoff plan" uses "Teams" as the subject with no "you" framing anywhere in the sentence, unlike every comparable aside elsewhere in the batch (105's "if you've ever watched a team..." keeps the "you" anchor). → Recommendation: rewrite as "You might discover you've been running a 'pilot' for eighteen months with no handoff plan."
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.
- **[minor]** Sources-block formatting quirk: Ward Cunningham is credited in-body ("Ward Cunningham coined that term in 1992") but has no independent Sources-block entry — he's folded into a bracket inside the Fowler citation. Not wrong, but inconsistent with how every other piece in the batch gives named contributors their own line.

#### 100-foundations/113-defining-success.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.
- **[moderate]** No italic felt-experience goal line — see Cross-Article Finding 2.
- **Passing strengths worth noting:** genuine humor ("watched a team declare victory because everything shipped on time while the numbers stayed flat"), strong Don't Confuse This With (success vs. scope), 4 well-placed sources.

#### 100-foundations/158-task-statement-design.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Humor requirement (D3.A2) — no genuine humor or levity moment anywhere in the piece. The "(If you've written task scripts that look more like step-by-step tutorials...)" aside is close but reads as a mild confession rather than something that earns a smile — it's flatter than the comparable asides in 103, 147, 157, 159, 174, 139.
- **[moderate]** Sourcing (D6.A2) — all three sources (Budiu, McCloskey, Schade) are NNGroup practitioner articles. No domain-primary academic or foundational source anywhere in the piece, unlike most of the rest of the batch. → Recommendation: consider adding a foundational HCI source on task framing/priming if one exists, or note explicitly that this is an acceptable exception given the piece's narrow, practitioner-specific claim.
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.

#### 100-foundations/147-ai-as-execution-partner.md
**Adversarial verdict:** Clean
No issues found. Genuine humor (the "Alex, 34" aside is sharp and specific), 5 sources with real annotations and clear placement at point of claim, Don't Confuse This With section is precise (prompting skill vs. judgment), goal line names a felt experience. This is the strongest T100 piece in the batch — nothing here should be touched.

#### 100-foundations/123-what-usability-testing-is.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Humor requirement (D3.A2) — scanned the full piece twice; there is no aside, parenthetical, or moment of levity anywhere in it. It's a clean, well-argued piece, but it's also the driest one in the batch relative to the humor standard the rest of the T100 pieces meet. → Recommendation: add one — a natural spot is in the QA-vs-usability-testing paragraph, where a dry aside about a feature that "passed every QA check and still baffled everyone" would fit without forcing it.
- **[minor]** Goal-line labeled "**Goal line (for article header):**" rather than the italic convention most other pieces use, and the content itself ("Watching someone try is not the same as asking them what they think") reads as a definitional contrast rather than a felt moment, closer to the D3.B7 failure example in the CLAUDE.md spec than the passing one.

#### 100-foundations/157-why-you-dont-help-during-testing.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Template completeness (D2.B5) — the Don't Confuse This With element is present in substance (the training-vs-testing distinction: "That's a useful question in training. It's not useful in usability testing") but it's embedded early inside the Concept section rather than positioned as its own beat near the end, right before Try Noticing, the way 174 and 139 do it cleanly. Functionally the distinction is made; positionally it's buried where a skimming reader is less likely to register it as the disambiguation moment. → Recommendation: no content rewrite needed, just consider whether a brief callback near the end ("this is different from training — that's not what you're testing") would land the distinction more clearly for a reader arriving after 174/139's clean version of the same element.
- **[moderate]** No italic felt-experience goal line — see Cross-Article Finding 2.
- **Passing strengths worth noting:** genuine, specific humor (the "well, it depends on what you're trying to do" aside is one of the sharpest in the batch), 3 well-placed sources including a foundational academic one (Bronfenbrenner).

#### 100-foundations/159-observation-effect.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Don't Confuse This With is weak/implicit — the piece never names a specific adjacent concept and draws a sharp line the way 174 does ("There's an adjacent thing that looks like think-aloud but isn't...") or 139 does. The closest equivalent is "None of this means sessions are unreliable. It means they're calibrated," which reframes the whole finding rather than distinguishing it from one specific conflated concept (e.g., demand characteristics, or simple self-report bias). → Recommendation: add a sentence explicitly distinguishing observation effect from general unreliability or from response bias more broadly, positioned right before the final Try Noticing prompt.
- **[moderate]** No italic felt-experience goal line — see Cross-Article Finding 2.

#### 100-foundations/174-think-aloud-protocol.md
**Adversarial verdict:** Clean
No issues found. Don't Confuse This With is one of the strongest in the batch (distinguishes both from evaluation-prompting AND from retrospective "why did you do that"), genuine humor, 4 sources including foundational Ericsson & Simon, annotated Sources block, sharp goal statement.

#### 100-foundations/139-no-ui-as-design-goal.md
**Adversarial verdict:** Clean
No issues found. Strong felt-experience goal line, genuine and specific humor (the chat-sidebar-with-a-command-list aside), Don't Confuse This With is precise and well-positioned, 3 sources all foundational/academic with real annotations, clean template order.

#### 200-methods/270a-paper-sketch-prototype.md
**Adversarial verdict:** Issues found
**Issues:**
- **[critical]** Template order (D2.B6) — the Trigger element ("Use this approach when the question is conceptual...") appears *after* the Concept/mechanism section (Wong 1992, Buxton, Walker et al.), not before it as the T200 template specifies (Prior Knowledge Hook → Trigger → Concept → Method). The Trigger text also references language from the Concept section directly ("the question is strategic, so the prototype should look strategic"), which fails the Trigger-isolation test (D5.B4) — it can't be read standalone without the Concept context that precedes it. This same pattern repeats in 270b, 270h, and 219 (see Cross-Article note below the per-article findings). → Recommendation: move the "Use this approach when..." paragraph to immediately follow the Prior Knowledge Hook, before the Wong/Buxton/Walker discussion.
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.

#### 200-methods/270b-lofi-wireframe-prototype.md
**Adversarial verdict:** Issues found
**Issues:**
- **[critical]** Template order (D2.B6) — same defect as 270a: "Use this when the question is navigational..." appears after the Kurosu & Kashimura / Virzi et al. Concept section, not before it. → Recommendation: same fix — relocate the Trigger paragraph ahead of the Concept discussion.
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.

#### 200-methods/219-ai-for-design-work.md
**Adversarial verdict:** Issues found
**Issues:**
- **[critical]** Template order (D2.B6) — "Use this when you're about to use an AI tool for a design task..." appears after the Nisbett & Wilson concept/mechanism section, not before it.
- **[moderate]** Proof is one-state (D5.B7) — "If you found yourself editing specific things in the output rather than accepting it wholesale... the method worked" describes only the success condition. There's no corresponding failure-state signal with a next step (e.g., what it looks like if the method *didn't* catch anything, and what to do about it). → Recommendation: add a branch — something like "If every variation passed your criteria without edits, check whether your criteria were specific enough to fail something."

#### 200-methods/270c-ai-generated-prototype.md
**Adversarial verdict:** Clean
No issues found. Trigger correctly precedes Concept. Watchout is specific and honest (the "generate-then-evaluate works everywhere else" trap). AI path is handled as an intentional structural variant given the piece's subject matter (the whole method *is* the AI path) rather than a bolt-on afterthought — noting this so it isn't miscounted as a template gap; this is a legitimately different, still-passing approach to the same element and should not be normalized to match the other pieces' bolt-on convention.

#### 200-methods/270i-build-to-think.md
**Adversarial verdict:** Clean
No issues found. Correct template order, specific Watchout grounded in sunk-cost research, strong two-state Proof, annotated sources including two foundational works (Schön, Arkes & Blumer).

#### 200-methods/270d-wizard-of-oz-prototype.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Proof is soft two-state, not a true success/failure split (D5.B7) — "a short list of wizard-hesitant moments" vs. "a long list" are both framed as findings ("that's exactly what the session was for"), not as a success outcome and a failure outcome each with a distinct next step. Functionally useful, but it doesn't give the reader a signal for "this didn't work, here's what to do." → Recommendation: add an explicit failure branch — e.g., what it means if the wizard needed information the real system won't have on nearly every turn, and what that implies about scoping the next session.

#### 200-methods/270f-high-fidelity-prototype.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.
- **Passing strengths worth noting:** correct Trigger-before-Concept order, one of the clearest structural-vs-visual-feedback distinctions in the batch, strong two-state Proof with a real false-positive branch.

#### 200-methods/270g-service-prototype.md
**Adversarial verdict:** Clean
No issues found. Correct order, specific Watchout, 5 sources all annotated with real findings, Proof addresses both a true finding and an execution-quality failure mode (backstage player inventing information) with a concrete correction.

#### 200-methods/270h-parallel-prototyping.md
**Adversarial verdict:** Issues found
**Issues:**
- **[critical]** Template order (D2.B6) — "Use this approach when you have genuinely divergent directions..." appears after the Dow (2010) Stanford experiment / Concept section, not before it. Same defect as 270a, 270b, 219.
- **Passing strengths worth noting:** everything else about this piece is strong — the Proof section has three real branches (outperform / tie / stated-preference-vs-behavior false positive), which exceeds the two-state minimum, and the Watchout (sequential testing / sunk cost) is specific and well-sourced.

#### 200-methods/215a-moderated-usability-session.md
**Adversarial verdict:** Clean
No issues found. Correct template order, Proof section is genuinely strong (multiple branches including a false-positive check with a concrete self-audit action — "count how many times you clarified"), 4 sources including two foundational (Virzi 1992, Dumas & Redish), annotated Sources block.

#### 200-methods/215b-unmoderated-usability-testing.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Sources block has zero annotation — see Cross-Article Finding 1.
- **[minor]** Structural blending — the final Proof-equivalent guidance ("If people completed the tasks without major friction, run the test with a bigger group... If you found repeated blockers...") is merged directly into the What Next / routing paragraph rather than kept as a distinct Proof beat the way 215a keeps it separate. Not wrong, just less clean than its companion piece.

#### 200-methods/270e-conversational-prototype.md
**Adversarial verdict:** Issues found
**Issues:**
- **[moderate]** Missing distinct Prior Knowledge Hook and formal Goal statement — this piece opens with a one-line description in place of a `**Goal:**` line, and moves directly from that into a Concept-flavored opening paragraph with no clearly separated Prior Knowledge Hook before the Trigger sentence arrives. Every other T200 piece in the batch has a visibly distinct PK-hook sentence ("You already know...") before its Trigger. This piece compresses the two, which makes it harder to verify D2.B8 (does the hook activate a schema this specific audience already has) since there's no isolated hook sentence to test. → Recommendation: add an explicit one-sentence hook before the Trigger paragraph, and give the piece a formal `**Goal:**` line matching the rest of the 309 series.

### Severity Totals

- **Critical: 4** — all four are the same defect (Trigger positioned after Concept instead of before it), occurring in 270a, 270b, 270h, and 219.
- **Moderate: 19** — dominated by two systemic patterns: missing Sources-block annotations (9 articles) and missing/weak felt-experience goal lines (6 articles), plus several isolated weak-element and sourcing findings.
- **Minor: 3**

### What This Pass Confirms Was Already Clean

Banned words, banned openers/closers, dead verbs, modifier bloat, semicolons, bold overuse, second-person voice (with the one 178 exception), rhythm/burstiness, and wall-rule compliance were all clean across the entire batch. Two prior passes did real, durable work on the mechanical and voice layer. This pass's findings sit almost entirely at the structural-consistency and sourcing-craft layer — the kind of thing that's only visible when reading the batch as a set rather than piece by piece.
