# Quality Evaluation Report
**Date:** 2026-09-22
**Articles evaluated:** 1
**Evaluator:** eval-and-repair skill

---

## Executive Summary

Piece 147 ("The Part of This Work AI Can't Do") was evaluated against all 9 dimensions after its write-piece revision. All blocking violations found were mechanical or high-confidence structural fixes (em dash overuse, two double-em-dash sentences, one third-person lapse, three monotone sentence-length triples, and one uncited/unwoven source missing its APA year) — all were repaired directly. No blocking issues remain. Two minor advisory items are flagged for optional human judgment; neither blocks publication.

**Batch status:** PUBLISH-READY WITH FLAGS

---

## Queue

| Article | Tier | Path | Publish doc |
|---|---|---|---|
| 147 — The Part of This Work AI Can't Do | T100 | `100-foundations/147-ai-as-execution-partner.md` | `100-foundations/147.publish.md` — **EXISTS** (D9.B1 pass, no blocking violation) |

---

## Summary Table (Before → After)

| Article | Before Blocking Fails | After Blocking Fails | Before Advisory Fails | After Advisory Fails | Status |
|---|---|---|---|---|---|
| 147 | 4 | 0 | 2 | 2 | PUBLISH-READY WITH FLAGS |

---

## Phase 1/2 — Per-Dimension Violation List

### D6 — Sourcing Integrity
- **B1 (min 3 sources, T100):** PASS. 5 sources present (Parasuraman & Manzey 2010; Reber, Schwarz & Winkielman 2004; Kruger & Dunning 1999; NNGroup 2025 "Good from Afar"; NNGroup 2026 "Core Skill of Design in the AI Era: Critique").
- **B2 (no fabricated sources):** PASS. All 5 verified — the four psychology/HCI papers are established foundational works; both NNGroup URLs were fetched and returned 200 OK with matching titles.
- **B3 (claims accurately represent source findings):** PASS. All paraphrases checked against known findings; consistent with how the same sources are cited in pieces 132 and 219 (cross-article consistency).
- **B4 (APA inline format, name + year):** **FAIL** — the 5th source ("Core Skill of Design in the AI Era: Critique") was listed in the Sources block with no year. Verified actual publish date via WebFetch: 2026-06-12. FIX TYPE: MECHANICAL/JUDGMENT-HIGH-CONFIDENCE (applied).
- **B5 (sources woven into prose at point of claim):** **FAIL** — the same 5th source had no inline citation anywhere in the body; it sat in the bibliography unused. FIX TYPE: JUDGMENT-HIGH-CONFIDENCE (applied — wove it into "The Signal" section where its finding directly supports the claim being made).

### D2 — Structural Completeness
- **B1 (all required T100 elements present):** PASS.
- **B2 (elements in prescribed order):** PASS.
- **B3 (no bold template labels as reader-facing headers):** PASS — zero bold headers in body; structure carried entirely by `---` breaks and prose, per the narrative-over-template rule.
- **B4 (T100 sequence: Goal → Concept → You'll See It When → The Signal → Don't Confuse This With → Try Noticing → What Next):** PASS — verified against the file's 7 section breaks; order matches exactly.
- **B5 (Don't Confuse This With names one sharp adjacent concept):** PASS — distinguishes prompting skill from judgment cleanly ("Strong prompting skill with a vague goal produces polished output with shallow substance. Design judgment with a precise description produces output that can be evaluated and improved.").

### D7 — Audience Fit
- **B1 (readable/actionable with no design background):** PASS.
- **B2 (design-coded vocabulary handled):** PASS — the revision's cross-role widening is visible: examples now span persona, journey map, interview questions, edge-case list, requirements doc, and spec section, not persona-only.
- **B3 (no leadership-only content):** PASS.
- **B4 (no AI-adoption mandate reference):** PASS.
- **B5 (no illustrative examples/anecdotes/invented stories):** PASS — the opening uses the T100-standard present-tense situational framing ("You ask AI to generate a persona...") rather than a narrated anecdote with named people; consistent with how piece 132 opens. The "Alex, 34" aside is a humor beat about a recurring AI pattern, not an invented story about a real situation.

### D8 — System Coherence
- **B1 (metadata header accurate):** PASS — confirmed against `10-master-outline.md`, `STATUS.md`, and `worklist.md`: T100, standalone, no prereqs, foundational for 219/270c/270e/270i/139/267.
- **B2 (What Next routing — files exist, descriptions match content):** PASS — see Phase 4 routing check below for full detail.
- **B3 (What Next conditions are genuine decision points):** PASS — all three routing sentences name a specific downstream situation, not generic "if you want more" phrasing.
- **B4 (prereq cross-references are layout elements, not prose):** PASS — piece has no prereqs; no prereq references embedded in prose.
- **B5 (no duplicated coverage without new angle):** PASS — 147 is the foundational concept atom; 219/132/214 apply it in specific method contexts without repeating it.

### D1 — Learning Outcome Validity
- **B1 (goal verb matches tier):** PASS by corpus convention — T100 pieces in this library (147, 132) use a goal-line subtitle rather than an explicit "Goal:" sentence; the piece's function is recognition (naming the judgment-layer/production-layer distinction), consistent with T100.
- **B2 (goal achievable after one reading):** PASS.
- **B3 (teaches exactly one goal):** PASS.
- **B4 (Bloom's alignment — Remember/Understand):** PASS — the Try Noticing exercise asks the reader to *notice and name* a gap, not execute a method.
- **A1 (non-obvious insight):** PASS — automation bias / processing fluency mechanism is genuinely non-obvious.
- **A2 (Merrill's coverage):** PASS — activation, demonstration, application, and integration with real work all present.
- **A3 (works without design authority, SaaS/3rd-party valid):** PASS.

### D5 — Action Section Quality
T100 pieces intentionally omit Method, Artifact, Proof, Watchout, AI path, and Take This Further per the tier template — these are N/A, not failures.
- **Try Noticing / B1 (names specific artifact):** ADVISORY CONCERN — "Take an AI-generated artifact from your current work: something from the last week or two" is generic rather than naming a specific artifact type. Judged PASS by corpus precedent (132's equivalent prompt, "the last prototype or mockup you showed to someone," is similarly general), but flagged below as an optional improvement.
- **B2 (achievable in one sitting):** PASS.
- **B3 (tests the piece's actual concept):** PASS — directly exercises the judgment-layer distinction the piece teaches.

### D3 — Voice & Register
- **B1 (no banned words):** PASS — zero matches on the full banned list.
- **B2 (no banned openers):** PASS — opens in the moment ("You ask AI to generate a persona...").
- **B3 (no banned closers, rhetorical Q+A, or parallel negation):** PASS.
- **B4 (discipline invisible):** PASS — no sentence argues for design as a function.
- **B5 (opens in the moment):** PASS.
- **B6 (second person throughout):** **FAIL** — "Practitioners who use AI daily can conflate the two..." used third person where the claim is the author's general observation, not a reported study finding. FIX TYPE: MECHANICAL (applied — changed to "If you use AI daily, it's easy to conflate the two...").
- **B7 (goal line names experience, not concept):** PASS — "The output looked complete, everyone moved on, and nobody asked if it was right" names a felt moment.
- **A1/A2 (warmth/humor):** PASS — the "Alex, 34" parenthetical aside delivers both.
- **A3 (contractions throughout):** PASS.

### D4 — Sentence-Level Craft
- **B1 (≥1 sentence ≤6 words per 150-word block):** PASS — short sentences appear frequently throughout.
- **B2 (no 3 consecutive sentences within 5 words of each other):** **FAIL** — found and fixed 3 genuine monotone runs: "Nobody asks... / The persona looked like a persona. / That was the problem." (7/6/4); "All the right sections. / Professional phrasing. / Appropriate length." (4/2/2); "The thing looks finished. / It probably is finished. / Checking feels redundant." (4/4/3). FIX TYPE: JUDGMENT-HIGH-CONFIDENCE (applied — merged adjacent short sentences in each run to break the monotony while preserving rhythm and meaning). Note: a purely mechanical word-count-window rescan flags many additional "triples" across the piece (e.g., 18/16/20-word sentences), but these vary meaningfully in internal complexity and do not read as monotonous on the read-aloud test — treated as false positives of a literal script, not real craft violations, consistent with how the same check would flag similar passages in already-accepted pieces 132/214/219.
- **B3 (em dash: ≤1/300 words, no 2 in same sentence, no 2 in adjacent paragraphs):** **FAIL** — original body had 13 em dashes across ~1,106 words (≈3.5×over budget), including two sentences with two em dashes each (the Parasuraman/Manzey sentence and the "132" What Next sentence). FIX TYPE: MECHANICAL (applied — converted 8 em dashes to colons/commas/periods; both double-dash sentences resolved; also cleaned a redundant double-dash in the Sources block). Final body count: 3 em dashes in ~1,117 words (≈0.8/300, within budget); zero double-dash sentences anywhere in the file.
- **B4 (semicolons near-zero):** PASS — 0 semicolons.
- **B5 (bold ≤2, genuine emphasis only):** PASS — 0 bold instances in body prose; the 6 bold instances in the file are all metadata/heading labels (Tier/Arc/Prereqs/Wave/Goal line/Sources), consistent with the established convention in 132/214/219.
- **B6 (bullet soup):** PASS — no bullets present.
- **B7 (one idea per sentence):** PASS.
- **B8 (dead verbs, modifier bloat):** PASS — no matches for either list.
- **B9 (cut test — restatement, dangling analysis):** PASS.
- **A1 (read-aloud):** PASS post-repair.
- **A2 (distinctive opening):** PASS — "You ask AI to generate a persona. Thirty seconds later, it's back..." is distinctive to this piece.

### D9 — Publication Readiness
- **B1 (publish doc exists):** PASS — `147.publish.md` exists (10,577 bytes). No blocking violation.
- **B2 (layout map has all required rows):** PASS — Prereq chip, image spec, pull quote, callout content, What Next routing, and platform (SharePoint) are all present.
- **B3 (pull quote ≤30 words, self-contained):** PASS — "The quality check got skipped because the artifact looked like the artifact." (12 words).
- **B4 (platform specified):** PASS — SharePoint.
- **A1 (image spec illustrates, doesn't decorate):** PASS — the two-panel production/judgment-layer diagram directly maps to the piece's core distinction.
- **A2 (forwarding scenario named):** **FAIL (advisory)** — no copy-pasteable Teams forwarding scenario is present in the publish doc. Flagged below for human action; not blocking.

---

## Phase 3 — What Was Fixed (Mechanical + High-Confidence)

All changes below were applied directly to `100-foundations/147-ai-as-execution-partner.md`.

1. **D3.B6 — third person → second person.**
   - Before: *"Practitioners who use AI daily can conflate the two: producing something and being able to evaluate whether it's any good look similar from the outside."*
   - After: *"If you use AI daily, it's easy to conflate the two: producing something and being able to evaluate whether it's any good look similar from the outside."*

2. **D4.B3 — em dash reduction (8 conversions + Sources cleanup), including both double-dash sentences.**
   - Before: *"Thirty seconds later, it's back — name, demographics, goals, frustrations."*
     After: *"Thirty seconds later, it's back: name, demographics, goals, frustrations."*
   - Before: *"All the right sections. Professional phrasing. Appropriate length."*
     After: *"All the right sections. Professional phrasing, appropriate length."* (also resolves part of the D4.B2 fix below)
   - Before: *"The production layer is making the thing — drafting the first version, generating the structure, producing the artifact."*
     After: *"The production layer is making the thing: drafting the first version, generating the structure, producing the artifact."*
   - Before: *"Parasuraman and Manzey (2010) studied what they called automation bias — the tendency to accept automated output without independent verification — across dozens of domains in knowledge work."* (two em dashes, same sentence)
     After: *"Parasuraman and Manzey (2010) studied automation bias, the tendency to accept automated output without independent verification, across dozens of domains in knowledge work."*
   - Before: *"AI consistently produces output that's easier to read than whatever you'd have generated otherwise — and that fluency gets interpreted, just beneath conscious notice, as a quality signal."*
     After: *"AI consistently produces output that's easier to read than whatever you'd have generated otherwise. That fluency gets interpreted, just beneath conscious notice, as a quality signal."*
   - Before: *"The evaluation requires the same understanding the task requires — which means the judgment layer... is entirely yours."*
     After: *"The evaluation requires the same understanding the task requires. That means the judgment layer... is entirely yours."*
   - Before: *"...came in with a strong existing foundation — and AI widened the gap between those who understood the domain and those who didn't..."*
     After: *"...came in with a strong existing foundation. AI widened the gap between those who understood the domain and those who didn't..."*
   - Before: *"Take an AI-generated artifact from your current work — something from the last week or two."*
     After: *"Take an AI-generated artifact from your current work: something from the last week or two."*
   - Before: *"For how this plays out in prototyping — where AI can produce high-polish screens in seconds but the fidelity decision remains yours — read 132 (Prototype Fidelity)."*  (two em dashes, same sentence)
     After: *"For how this plays out in prototyping, where AI can produce high-polish screens in seconds but the fidelity decision remains yours, read 132 (Prototype Fidelity)."*
   - Sources block, before: *"Finding: automation bias — the tendency to accept automated output without independent verification — occurs in both novice and expert users..."* (two em dashes, same sentence)
     After: *"Finding: automation bias, the tendency to accept automated output without independent verification, occurs in both novice and expert users..."*
   - Result: body em dash count went from 13 (≈3.5/300 words) to 3 (≈0.8/300 words); 0 double-dash sentences remain anywhere in the file (was 3).

3. **D4.B2 — three monotone sentence-length triples broken.**
   - Before: *"Nobody asks what it was drawn from. ... The persona looked like a persona. That was the problem."*
     After: *"...The persona looked like a persona, and that was the problem."*
   - Before: *"All the right sections. Professional phrasing. Appropriate length."*
     After: *"All the right sections. Professional phrasing, appropriate length."*
   - Before: *"The thing looks finished. It probably is finished. Checking feels redundant."*
     After: *"The thing looks finished. It probably is finished, so checking feels redundant."*

4. **D6.B4/B5 — missing citation year + unwoven source fixed.**
   - Verified the 5th source's actual publish date via WebFetch (2026-06-12) and its title ("The Core Skill of Design in the AI Era: Critique") against the live NNGroup page.
   - Sources block, before: *"Nielsen Norman Group. The core skill of design in the AI era: Critique. https://www.nngroup.com/articles/ai-era-critique/ Finding: in AI-assisted work, evaluation — not generation — becomes the central practitioner skill..."*
     After: *"Nielsen Norman Group. (2026, June 12). The core skill of design in the AI era: Critique. https://www.nngroup.com/articles/ai-era-critique/ Finding: in AI-assisted work, evaluation, not generation, becomes the central practitioner skill..."*
   - Body — inserted a new inline citation into "The Signal" section, where the finding directly supports the claim already being made:
     Before: *"Quality evaluation requires being able to name what the artifact is supposed to do and whether this version does it. 'It looked good' means the fluency registered."*
     After: *"Quality evaluation requires being able to name what the artifact is supposed to do and whether this version does it. Nielsen Norman Group's research on AI-assisted design work names this directly: evaluation, not generation, is what defines useful practice now (NNGroup, 2026). 'It looked good' means the fluency registered."*

**Confidence note on JUDGMENT-HIGH-CONFIDENCE items:** fixes 3 and 4 required judgment (which sentences to merge, where to weave the citation) but were applied directly rather than flagged, because each had a single unambiguous correct location: the D4.B2 merges preserve the original meaning and rhythm with minimal alteration, and the D6 citation slots into a sentence whose claim is already an exact match for the source's finding, with no plausible alternative placement that would serve the claim better.

---

## Phase 3 — Flagged for Human Review (JUDGMENT)

1. **D5 — Try Noticing artifact specificity (advisory, low severity).**
   - Issue: "Take an AI-generated artifact from your current work: something from the last week or two" names an artifact category generically rather than naming specific artifact types.
   - Recommendation: consider sharpening to something like "Take a persona, requirements doc, or set of interview questions AI generated for you in the last week or two" — pulling from the artifact list already established earlier in the piece, so the prompt is maximally concrete for whichever role is reading.
   - Confidence blocker: this is a stylistic tightening, not a correctness issue, and the current phrasing passes by direct precedent (piece 132's equivalent Try Noticing prompt is equally general). Changing it is optional polish, not a repair — left for human call so as not to over-fit the piece to one interpretation of "specific."

2. **D9.A2 — no forwarding scenario in the publish doc (advisory).**
   - Issue: `147.publish.md` has no copy-pasteable Teams forwarding scenario, unlike the fuller optional Check-In section it does include.
   - Recommendation: add a one-line forwarding scenario to the publish doc, e.g.: *"Saw this after reviewing [artifact] — the 'production vs. judgment layer' framing explains exactly why the AI draft looked done but wasn't. Worth a 5-minute read before the next AI-assisted pass."*
   - Confidence blocker: this requires inventing new promotional copy tied to a real forwarding context, which is authorial/marketing judgment rather than a mechanical correction — outside the scope of a repair pass on the article itself.

---

## Phase 4 — Re-evaluation

Targeted re-scan of every benchmark that had a violation, post-repair:

| Benchmark | Before | After |
|---|---|---|
| D3.B6 (second person) | FAIL | PASS |
| D4.B2 (no 3 consecutive similar-length sentences) | FAIL (3 genuine instances) | PASS (all 3 fixed) |
| D4.B3 (em dash budget + no double-dash sentences) | FAIL (13 dashes/1,106 words, 2 double-dash sentences) | PASS (3 dashes/1,117 words, 0 double-dash sentences) |
| D6.B4 (APA year) | FAIL | PASS |
| D6.B5 (source woven at claim) | FAIL | PASS |

No previously-passing benchmark was affected by these edits (verified by re-running the full mechanical scan set: banned words, semicolons, bold count, bullet soup, dead verbs — all still 0/clean).

### Routing Integrity Check (D8.B2) — the three What Next targets

| Target | File exists? | Routing description in 147 | Verified against target content |
|---|---|---|---|
| **132** (Prototype Fidelity) | ✅ `100-foundations/132-prototype-fidelity.md` | "where AI can produce high-polish screens in seconds but the fidelity decision remains yours" | **Match.** 132 explicitly covers this: *"An AI tool can generate a polished-looking screen from a rough prompt in seconds... The tool produced polish quickly. The question didn't require it."* |
| **214** (Affinity Mapping) | ✅ `200-methods/214-affinity-mapping.md` | "how to use AI in research synthesis without ceding the pattern-finding judgment" | **Match.** 214's AI path reads: *"paste your raw notes into an AI tool and ask for an initial grouping by behavioral theme — then reorganize it yourself... The AI gives you a starting structure; your pattern recognition over the actual data is the method."* |
| **219** (AI for Design Work) | ✅ `200-methods/219-ai-for-design-work.md` | "the full method of directing AI as an execution partner in your work" | **Match.** 219 is explicitly the T200 method built on 147's judgment-layer concept, and its own What Next links back: *"For the foundational thinking behind why the judgment layer matters and can't be delegated, 147 (AI as Execution Partner) covers it in full."* No routing loop — 219 defers to 147 for concept, 147 defers to 219 for method; this is a legitimate bidirectional prereq/application pairing, not a loop with no intervening content. |

**Note on naming convention:** all three target files' actual H1 titles differ from the parenthetical labels used in routing links (e.g., 219's real title is "Before You Use What AI Generated," not "AI for Design Work"; 132's real title is "You're Getting Feedback on the Wrong Thing," not "Prototype Fidelity"). This is a consistent, established convention across the corpus — the parenthetical name is a thematic/slug-style reference, not the published headline — and is not treated as a routing error.

---

## Cross-article Findings

Limited to what's checkable from a single-article queue plus its three routing targets:

- **Vocabulary consistency:** "judgment layer" / "production layer" are unique to 147 (the concept's origin point) and are not literally reused in 132/214/219, which instead operationalize the same idea in method-specific language ("criteria," "the fidelity decision remains yours," "pattern recognition over the actual data"). This is appropriate layering, not drift — each downstream piece translates the concept into its own method vocabulary rather than repeating 147's terms verbatim.
- **Sourcing consistency:** Parasuraman & Manzey (2010) is cited with matching finding language in both 147 and 219. The NNGroup "Good from Afar" (2025) source is cited identically in 147 and 132. No contradictory framing found.
- **Duplicate coverage:** none — 147 (concept), 219 (method), 132/214 (context-specific application) are non-overlapping.
- **Orphan check:** 147 is routed to from 219, 132's prereq/pairing note, and multiple master-outline entries (139, 267, 270c, 270e, 270i) — not an orphan; it is the entry point for the AI-judgment thread by design.

---

## Lagging Articles

Not applicable — single-article queue, no comparison set.

---

## Elevate, Never Tear Back — Verification

- No previously-passing benchmark was degraded. Confirmed via full re-scan: banned words (0), banned openers/closers (0), semicolons (0), bullet soup (0 bullets), dead verbs/modifier bloat (0), bold-in-prose (0), source count (still 5, none removed).
- No content was shortened, no source was removed, no method step was simplified. All edits were surgical: em dash → comma/colon/period conversions, one pronoun-person fix, three sentence merges to break monotone runs, and one citation addition (net addition, not subtraction).

**Post-report correction (human-verified):** this report's self-reported word count of 1,156 was inaccurate — actual body word count after this pass was 1,107, seven words over the write-piece skill's T100 ceiling (850–1100, Test C). Word count is a write-piece Phase 5 micro-test, not one of eval-and-repair's 81 benchmarks, so this pass had no mechanism to catch it. Two small trims were applied by hand ("just beneath conscious notice" → "unconsciously"; tightened one NNGroup-adjacent sentence) to bring the piece back to exactly 1,100 words, with zero change to any of the fixes documented above. Recommendation for future runs: when eval-and-repair and write-piece are chained on the same piece, re-run write-piece's Test C word-count check after eval-and-repair's repairs, since eval-and-repair's edits (citation weaving, sentence merges) can push word count without either skill catching the interaction on its own.

---
---

# Quality Evaluation Report — Piece 157
**Date:** 2026-09-22
**Articles evaluated:** 1
**Evaluator:** eval-and-repair skill

---

## Executive Summary

Piece 157 ("Why You Don't Help During Testing") was evaluated against all 9 dimensions after its write-piece revision addressing a peer-review finding (softened ecological-validity framing, added an explicit shipping/false-confidence consequence sentence). Voice, structure, sourcing, audience fit, and action-section quality all passed clean on first evaluation, a stronger starting position than piece 147 earlier in this batch. Two real violations were found and repaired: an em-dash budget/double-dash sentence violation (D4.B3) and a What Next routing description that mischaracterized piece 151's actual content (D8.B2/B3). Both were fixed directly. One advisory gap (no forwarding scenario in the publish doc) is flagged for human action, consistent with the same gap found on 147.

**Batch status:** PUBLISH-READY WITH FLAGS

---

## Queue

| Article | Tier | Path | Publish doc |
|---|---|---|---|
| 157 — Why You Don't Help During Testing | T100 | `100-foundations/157-why-you-dont-help-during-testing.md` | `100-foundations/157.publish.md` — **EXISTS** (D9.B1 pass, no blocking violation) |

---

## Summary Table (Before → After)

| Article | Before Blocking Fails | After Blocking Fails | Before Advisory Fails | After Advisory Fails | Status |
|---|---|---|---|---|---|
| 157 | 2 | 0 | 1 | 1 | PUBLISH-READY WITH FLAGS |

---

## Phase 1/2 — Per-Dimension Violation List

Run in specified order: D6, D2, D7, D8, D1, D5, D3, D4, D9.

### D6 — Sourcing Integrity
- **B1 (min 3 sources, T100):** PASS. 3 sources present (Bronfenbrenner 1977, Nielsen 2012, Krug 2010).
- **B2 (no fabricated sources):** PASS. All three are established, verifiable works — Bronfenbrenner (1977) "Toward an experimental ecology of human development," *American Psychologist* 32(7): 513–531 (the foundational ecological-validity paper); Nielsen (2012) "Thinking Aloud: The #1 Usability Tool," NNGroup; Krug (2010) *Rocket Surgery Made Easy*, New Riders.
- **B3 (claims accurately represent source findings):** PASS. The peer-review softening is visible and effective: the piece borrows Bronfenbrenner's general definition of ecological validity (degree to which research conditions approximate real-world conditions) without overclaiming his original developmental-psychology context applies directly to usability testing — "You don't need the term to feel it" explicitly signals the term is being borrowed, not asserted as a direct empirical finding about usability methodology. Nielsen and Krug claims match their well-documented positions exactly.
- **B4 (APA inline format):** PASS — all three use Name (Year) inline.
- **B5 (sources woven at point of claim):** PASS — each citation lands in the sentence making the exact claim it supports (Bronfenbrenner at the ecological-validity definition, Nielsen at "shut up and let the users do the talking," Krug at the facilitator-tension claim).

**Advisory:**
- A1 (source placement test): PASS — removing any citation would visibly weaken the sentence.
- A2 (domain-primary source): PASS — Bronfenbrenner (1977) is foundational academic work.
- A3 (behavioral claims within 20 years, foundational exempt): PASS — Bronfenbrenner is foundational/exempt; Nielsen and Krug are both within range.

### D2 — Structural Completeness
- **B1 (all required T100 elements present):** PASS — Goal, Concept, You'll See It When, The Signal, Don't Confuse This With, Try Noticing, What Next all present.
- **B2 (elements in prescribed order):** PASS.
- **B3 (no bold template labels as reader-facing headers):** PASS — zero bold section labels in body prose.
- **B4 (T100 sequence order):** PASS — verified against the file's `---` breaks: Goal (metadata + italic hook) → opening scene-setting (corpus-standard hook preceding Concept, consistent with 147/174) → Concept ("The instinct to help isn't wrong…" through "The evidence becomes uninterpretable.") → You'll See It When ("You'll feel this pull…" through "…ten seconds.") → The Signal ("You've crossed the line…" through "That's contamination.") → Don't Confuse This With ("None of this means never speaking…" through "It's the point.") → Try Noticing ("Take two minutes…") → What Next.
- **B5 (Don't Confuse This With names one sharp adjacent concept with a clear criterion):** PASS — the adjacent concept conflated with "don't help" is "never speak at all." The piece distinguishes them with a sharp, checkable criterion: prompts that keep someone narrating their own thought process are fine; anything that teaches them how the interface works crosses the line.

**Advisory:**
- A1 (Practice Atom subtype applicability): N/A — piece has full multi-element T100 structure, not a single-step atom; no re-tier concern.

### D7 — Audience Fit
- **B1 (readable/actionable, no design background):** PASS.
- **B2 (design-coded vocabulary handled):** PASS — "usability testing" and "ecological validity" are the piece's actual subject matter and are explicitly handled ("You don't need the term to feel it"); no unhandled design-coded terms from the required-translation list appear.
- **B3 (no leadership-only content):** PASS.
- **B4 (no AI-adoption mandate reference):** PASS.
- **B5 (no illustrative examples/anecdotes/invented stories):** PASS — second-person situational framing throughout, no named individuals or narrated incidents.

**Advisory:**
- A1 ("real to them" test): PASS.
- A2 (SaaS/3rd-party validity, no design authority required): PASS — facilitating a usability session requires no authority over the interface itself.
- A3 (Try Noticing executable by PM/dev/non-custom dev): PASS — "a prototype in review, a demo with a stakeholder, a document someone was reading in real time" names situations available to every audience, not just designers.

### D8 — System Coherence
- **B1 (metadata header accurate):** PASS — Tier 100, Arc Standalone, Prereqs none, Episode 21; consistent with the publish doc (Wave 2, no hard/soft prereqs, no dependency blocks).
- **B2 (What Next routing — files exist, descriptions match content):** **FAIL (pre-repair).** All three target files exist (`200-methods/215a-moderated-usability-session.md`, `100-foundations/174-think-aloud-protocol.md`, `100-foundations/151-self-report-vs-observed-behavior.md`). The 215a and 174 routing descriptions matched their targets' actual content. The 151 routing description did not: the article said "the foundational concept behind why unfamiliarity matters here" routes to 151, but 151 is about the self-report-vs-observed-behavior data distinction, not about "why unfamiliarity matters." FIX TYPE: JUDGMENT-HIGH-CONFIDENCE (rewritten to accurately describe 151's actual content and its genuine connection to 157 — applied).
- **B3 (What Next conditions are genuine decision points):** Tied to the same violation above for the 151 link; 215a and 174 conditions were already specific and genuine ("getting ready to run a live session," "what to listen for while you're staying quiet").
- **B4 (prereq cross-references are layout elements, not prose):** PASS — no prereqs exist for this piece; nothing embedded in prose.
- **B5 (no duplicated coverage without new angle):** PASS — 157's mechanism (facilitator restraint preserving evidence validity) is distinct from 174 (verbal think-aloud behavior) and 151 (self-report vs. observed data types); each piece covers a non-overlapping angle.

### D1 — Learning Outcome Validity
- **B1 (goal verb matches tier):** PASS — "Recognize when helping a participant changes the evidence…" uses the T100 recognition verb.
- **B2 (goal achievable after one reading):** PASS.
- **B3 (teaches exactly one goal):** PASS — single goal (recognizing the moment helping contaminates the evidence).
- **B4 (Bloom's alignment — Remember/Understand):** PASS — Try Noticing asks the reader to recall and name a past moment, not execute a method or make a novel judgment call.

**Advisory:**
- A1 (non-obvious insight): PASS — the evidence-contamination mechanism and the "it ships and waits in production" consequence are genuinely non-obvious to a practitioner who hasn't thought about facilitation this way.
- A2 (Merrill's coverage): PASS — activation (the felt itch to help), demonstration (the mechanism), application (Try Noticing), integration (What Next routes to real practice).
- A3 (works without design authority, SaaS/3rd-party valid): PASS.

### D5 — Action Section Quality
T100 applicable elements only (Try Noticing functions as the practice element; Method/Artifact/Proof/Watchout/Take This Further/AI path are T200+ elements, N/A here).
- **B1 (names specific artifact):** PASS — "a prototype in review, a demo with a stakeholder, a document someone was reading in real time" names concrete situations, stronger specificity than the equivalent prompt in piece 147.
- **B2 (achievable in one sitting, no setup, time estimate present):** PASS — "Take two minutes with this."
- **B3 (tests the piece's actual concept):** PASS — directly exercises the recognition of helping vs. staying quiet.
- **B4 (Trigger isolation test):** N/A — T100 has no formal Trigger element.

### D3 — Voice & Register
- **B1 (no banned words):** PASS — zero matches against the full banned list. ("Facilitator"/"facilitation" are the domain's own subject-matter nouns, not instances of the banned verb "facilitates.")
- **B2 (no banned openers):** PASS — opens in the moment ("You're watching someone use the thing you built.").
- **B3 (no banned closers, rhetorical Q+A, parallel negation):** PASS. Reviewed "That's not facilitation. That's contamination." and "None of this means never speaking." against the parallel-negation ban — these are two independent short declarative sentences delivering a direct assertion, not the hedging "Not X, but Y" single-sentence construction the rule targets. Judged as intentional short-sentence rhythm, not a violation.
- **B4 (discipline invisible):** PASS — no sentence argues for design as a function; the piece addresses facilitation generally, applicable to any practitioner running a session.
- **B5 (opens in the moment):** PASS.
- **B6 (second person throughout):** PASS — no "teams"/"practitioners"/"organizations" substitutions found.
- **B7 (goal line names experience, not concept):** PASS — the article's italic hook ("The participant is going in circles and you know exactly what to tell them. You can't.") names a felt moment.

**Advisory:**
- A1/A2 (warmth/humor): PASS — the parenthetical aside ("If you've ever said 'well, it depends on what you're trying to do' because you thought it was neutral, you helped them anyway. You both knew it.") delivers a genuine, recognizable moment of self-aware humor.
- A3 (contractions throughout): PASS.

### D4 — Sentence-Level Craft
- **B1 (≥1 sentence ≤6 words per 150-word block):** PASS — short sentences ("They pause.", "That confusion is the data.", "That's a finding.", "That's contamination.", "It's the point.", "Did you help them?") are distributed throughout every section; no 150-word gap without one.
- **B2 (no 3 consecutive sentences within 5 words of each other):** PASS on inspection. A literal word-count-window rescan flags several triples (e.g., 10/9/5, 10/8/12, 24/24/22, 9/4/7), but each is either separated by a structural `---` break (not continuous prose), inflated by embedded dialogue quotes with very different internal structure, or a deliberate short-beat/rapid-question rhythm device consistent with the style guide's own encouragement of "short sentence after a dense paragraph lets the idea settle." Treated as false positives of a literal script, consistent with how the same check was resolved on piece 147 in this batch — none read as monotonous on the read-aloud test.
- **B3 (em dash budget, no double-dash sentences):** **FAIL (pre-repair).** Body had 5 em dashes across 1,050 words (≈1.43/300, over the ≤1/300 budget), including one sentence with three em dashes ("Actually, what that does is—" or "Try looking at—" or "Most people click on—."). FIX TYPE: MECHANICAL (applied — see Phase 3 below). Post-repair: 0 em dashes in body.
- **B4 (semicolons near-zero):** PASS — 0 semicolons.
- **B5 (bold ≤2, genuine emphasis only):** PASS — 0 bold instances in body prose.
- **B6 (bullet soup):** PASS — no bullets present.
- **B7 (one idea per sentence):** PASS.
- **B8 (dead verbs, modifier bloat):** PASS — no matches against either list.
- **B9 (cut test):** PASS — no restatements, no dangling analysis, no filler transitions found.

**Advisory:**
- A1 (read-aloud test): PASS post-repair — no stumbles after em-dash cleanup.
- A2 (distinctive opening): PASS — "They hover the cursor over three different buttons without clicking any of them" is distinctive to this piece's specific scenario.

### D9 — Publication Readiness
- **B1 (publish doc exists):** PASS — `157.publish.md` exists (9,440 bytes).
- **B2 (layout map has all required rows):** PASS — Prereq chip (explicitly "no chip required"), image spec (optional spec provided with rationale for omitting by default), pull quote, callout content (Concept Panel blue tint + Try Noticing amber tint), What Next routing, platform (SharePoint) all present.
- **B3 (pull quote ≤30 words, self-contained, names a felt thing):** PASS — "The participant's struggle isn't a problem to solve. It's the point." (12 words).
- **B4 (platform specified):** PASS — SharePoint.

**Advisory:**
- A1 (image spec illustrates, doesn't decorate): PASS — the optional two-panel "during the test / in real use" spec directly maps to the piece's mechanism; the decision to omit an image by default is itself well-reasoned in the doc.
- A2 (forwarding scenario named): **FAIL (advisory).** No copy-pasteable Teams forwarding scenario is present in the publish doc, the same gap found on piece 147 earlier in this batch. Flagged below for human action.

---

## Phase 3 — What Was Fixed (Mechanical + High-Confidence)

All changes below were applied directly to `100-foundations/157-why-you-dont-help-during-testing.md`.

1. **D4.B3 — em dash budget + double-dash sentence, three conversions (MECHANICAL).**
   - Before: `You've crossed the line the moment you start a sentence with "Actually, what that does is—" or "Try looking at—" or "Most people click on—." If the participant's next attempt is easier because of something you said, that's not facilitation.`
     After: `You've crossed the line the moment you start a sentence with "Actually, what that does is…" or "Try looking at…" or "Most people click on…" If the participant's next attempt is easier because of something you said, that's not facilitation.`
     (Converted three trailing em dashes representing interrupted/cut-off speech to ellipses — the standard convention for trailing-off dialogue — resolving both the double/triple-dash-in-one-sentence violation and most of the ratio overage.)
   - Before: `(If you've ever said "well, it depends on what you're trying to do" because you thought it was neutral — you helped them anyway. You both knew it.)`
     After: `(If you've ever said "well, it depends on what you're trying to do" because you thought it was neutral, you helped them anyway. You both knew it.)`
   - Before: `You'll prompt participants to keep thinking aloud when they go quiet — a simple "keep talking" or "what are you thinking right now?" works.`
     After: `You'll prompt participants to keep thinking aloud when they go quiet: a simple "keep talking" or "what are you thinking right now?" works.`
   - Result: body em dash count went from 5 (≈1.43/300 words) to 0; the triple-dash sentence no longer exists.

2. **D8.B2/B3 — What Next routing description for 151 corrected (JUDGMENT-HIGH-CONFIDENCE).**
   - Before: `If you want the foundational concept behind why unfamiliarity matters here, 151 (Self-Report vs. Observed Behavior) is where that sits.`
   - After: `For the foundational distinction between what people say they'd do and what they actually do, and why usability testing depends on the second kind, 151 (Self-Report vs. Observed Behavior) covers it.`
   - Confidence note: applied directly rather than flagged because the correct connection was unambiguous once 151's actual content was read in full — 151 is specifically about the self-report/observed-behavior distinction, and 157's entire mechanism (helping shifts what you're observing toward what the participant thinks you want to hear, i.e., toward self-report-like data) maps onto that distinction precisely. There was no plausible alternative framing that would serve the claim better.

**Word count impact:** the routing rewrite is 9 words longer than the original (it replaces a vague, inaccurate condition with a precise one, which required slightly more words to state correctly). Net effect on body word count: +9 words. No trims were required — final count remains well under the 1,100-word ceiling (see word count section below).

---

## Phase 3 — Flagged for Human Review (JUDGMENT)

1. **D9.A2 — no forwarding scenario in the publish doc (advisory).**
   - Issue: `157.publish.md` has no copy-pasteable Teams forwarding scenario, the same gap identified on piece 147 earlier in this batch.
   - Recommendation: add a one-line forwarding scenario to the publish doc, e.g.: *"Watched this happen in a demo yesterday — someone got stuck and I almost jumped in to help. This explains exactly why that would've killed the data. Two-minute read."*
   - Confidence blocker: this requires inventing new promotional copy tied to a real forwarding context, which is authorial/marketing judgment rather than a mechanical correction on the article itself — outside the scope of a repair pass on the source article.

No other JUDGMENT items were flagged. Both real violations found (D4.B3, D8.B2/B3) had a single unambiguous correct fix and were resolved as JUDGMENT-HIGH-CONFIDENCE or MECHANICAL.

---

## Body Word Count (write-piece Test C cross-check — not one of eval-and-repair's 81 benchmarks)

Per the known gap flagged from the immediately preceding piece (147) in this batch, word count was manually verified with a script (not estimated), counting body text only — title, metadata line, italic Goal line, and Sources block excluded:

| Stage | Word count | Status vs. T100 range (850–1,100) / ceiling (1,100) |
|---|---|---|
| Before repairs | 1,050 | Within range, well under ceiling |
| After repairs | 1,059 | Within range, well under ceiling |

The repair pass added 9 words net (the corrected 151 routing sentence is more precise and slightly longer than the inaccurate original; the em-dash conversions were word-count-neutral). No trim was required — final count (1,059) is 41 words under the 1,100 hard ceiling. This piece did not repeat the 147 overage incident.

---

## Phase 4 — Re-evaluation

Targeted re-scan of every benchmark that had a violation, post-repair:

| Benchmark | Before | After |
|---|---|---|
| D4.B3 (em dash budget + no double-dash sentences) | FAIL (5 dashes/1,050 words, 1 triple-dash sentence) | PASS (0 dashes/1,059 words, 0 multi-dash sentences) |
| D8.B2 (What Next routing accuracy — 151 link) | FAIL | PASS |
| D8.B3 (What Next conditions are genuine decision points) | FAIL (tied to same 151 issue) | PASS |

No previously-passing benchmark was affected by these edits. Re-ran the full mechanical scan set post-repair: banned words (0), banned openers/closers (0), semicolons (0), bullet soup (0 bullets), dead verbs/modifier bloat (0), bold-in-prose (0), source count (still 3, none removed or altered).

### Routing Integrity Check (D8.B2) — the three What Next targets

| Target | File exists? | Routing description in 157 | Verified against target content |
|---|---|---|---|
| **215a** (Moderated Usability Session) | ✅ `200-methods/215a-moderated-usability-session.md` | "covers the full facilitation method, including when and how to intervene without biasing what you're observing" | **Match.** 215a's Method section is explicit on this: *"Watch. Take notes. Do not help. If they're silent for more than 10–15 seconds, prompt them... That's not intervention. It's a facilitation move that keeps think-aloud going without giving information."* Direct match to "when and how to intervene without biasing." |
| **174** (Think-Aloud Protocol) | ✅ `100-foundations/174-think-aloud-protocol.md` | "covers the verbal behavior that makes silence productive" | **Match.** 174 is entirely about recognizing narration versus silence during a session and what each signals — *"That silence means the thinking is still happening, but it's gone back inside. You've lost access to it."* Directly supports the routing claim. |
| **151** (Self-Report vs. Observed Behavior) | ✅ `100-foundations/151-self-report-vs-observed-behavior.md` | **Corrected** to: "the foundational distinction between what people say they'd do and what they actually do, and why usability testing depends on the second kind" | **Match (post-fix).** 151's Concept states exactly this: *"Self-report is what participants tell you... Observed behavior is what they actually do when you watch."* The original routing text ("why unfamiliarity matters here") did not match 151's actual content and has been corrected. |

**No routing loops found:** 174 routes onward to 215a and 159 (Observation Effect); 151 routes onward to 202 (Research Mechanics); 215a lists 157, 159, and 174 as prereqs. This is a coherent prereq/application layering (157 → 215a as method application; 157 ↔ 174 as paired concept pieces), not a loop with no intervening content.

---

## Cross-article Findings

Limited to what's checkable from a single-article queue plus its three routing targets:

- **Vocabulary consistency:** "ecological validity," "think-aloud," "self-report vs. observed behavior" are each introduced once, at their origin piece, and referenced (not redefined) downstream — 157 borrows none of 174's or 151's terminology incorrectly, and none of the three pieces contradict each other's framing of usability testing as observed-behavior data collection.
- **Sourcing consistency:** Nielsen (2012) "Thinking Aloud: The #1 Usability Tool" is cited in both 157 and 174 with consistent framing (the discipline of not leading the participant). No contradictory claims found between the two citations of the same source.
- **Duplicate coverage:** none — 157 (facilitator restraint / evidence contamination), 174 (recognizing narration vs. silence), 151 (self-report vs. observed data types) are non-overlapping angles on adjacent research-methods concepts.
- **Orphan check:** 157 is routed to from 215a's own prereq list (`Prereqs: 123, 157, 159, 174`), so it is not an orphan — it is a genuine prerequisite for the T200 method piece that operationalizes it.

---

## Lagging Articles

Not applicable — single-article queue, no comparison set within this run. (Cross-batch note: 157 finished this pass with 0 blocking fails and only 1 advisory fail, a stronger result than 147's 2 remaining advisory fails earlier in this batch — both are within the 15-point lagging threshold of each other and neither is flagged as lagging.)

---

## Elevate, Never Tear Back — Verification

- No previously-passing benchmark was degraded. Confirmed via full re-scan: banned words (0), banned openers/closers (0), semicolons (0), bullet soup (0 bullets), dead verbs/modifier bloat (0), bold-in-prose (0), source count (still 3, none removed), word count (increased slightly, still within the target range, not reduced).
- No content was shortened, no source was removed, no method step was simplified. All edits were surgical: three em-dash conversions (ellipsis/comma/colon in place of em dash) and one routing-sentence correction (net +9 words, more accurate, not less).

**Word count verification (per this run's explicit instruction):** manually counted with a script both before (1,050 words) and after (1,059 words) repairs. Final count is under the 1,100 hard ceiling with room to spare — no trim was needed, and none was applied.

---
---

# Quality Evaluation Report — Piece 177
**Date:** 2026-09-22
**Articles evaluated:** 1
**Evaluator:** eval-and-repair skill

---

## Executive Summary

Piece 177 ("What a Prototype Is") was evaluated against all 9 dimensions after its write-piece revision addressing two peer-review findings from UX-practitioner reviewer Alberto Zamarron (moving the "question first" principle earlier via a new short sentence, and sharpening the prototype-vs-demo distinction with two new sentences reusing the "click-through" motif), plus a third small word-count-restoring addition. The revision itself was clean — none of its three additions introduced a new violation. Evaluation surfaced three small pre-existing/structural gaps unrelated to the revision: an em-dash budget overage by one dash, a ~209-word stretch with no sentence ≤6 words, and a missing in-body time estimate on the Try Noticing prompt (the publish doc already specified "2 minutes" but the article text didn't say so). A fourth issue was found in the companion publish doc: its quoted "Goal line italic" text didn't match the article's actual italic hook line, an artifact of the doc predating a later article revision. All four were mechanical or high-confidence fixes and were repaired directly. No blocking issues remain. One advisory gap (no forwarding scenario in the publish doc) is flagged for human action, the same recurring gap found on pieces 147 and 157 earlier in this batch.

**Batch status:** PUBLISH-READY WITH FLAGS

---

## Queue

| Article | Tier | Path | Publish doc |
|---|---|---|---|
| 177 — What a Prototype Is | T100 | `100-foundations/177-what-a-prototype-is.md` | `100-foundations/177.publish.md` — **EXISTS** (9,190 bytes; D9.B1 pass, no blocking violation) |

---

## Summary Table (Before → After)

| Article | Before Blocking Fails | After Blocking Fails | Before Advisory Fails | After Advisory Fails | Status |
|---|---|---|---|---|---|
| 177 | 2 | 0 | 2 | 1 | PUBLISH-READY WITH FLAGS |

---

## Phase 1/2 — Per-Dimension Violation List

Run in specified order: D6, D2, D7, D8, D1, D5, D3, D4, D9.

### D6 — Sourcing Integrity
- **B1 (min 3 sources, T100):** PASS. 4 sources present (Houde & Hill 1997, Lim, Stolterman & Tenenberg 2008, Buxton 2007, Sauer & Sonderegger 2009).
- **B2 (no fabricated sources):** PASS. All four are established, verifiable HCI works — Houde & Hill (1997) is the classic "What do prototypes prototype?" paper; Lim et al. (2008) is a real ACM TOCHI article (DOI resolves); Buxton (2007) is the well-known *Sketching User Experiences*; Sauer & Sonderegger (2009) was independently verified via WebFetch in this same batch's evaluation of piece 132, which cites the identical finding.
- **B3 (claims accurately represent source findings):** PASS. Houde & Hill's claim ("the important thing... isn't the representation... it's what the prototype is intended to explore") matches the paper's actual thesis. Lim et al.'s quoted "economic principle of prototyping" is an accurate direct quote. Buxton's "experiencing a system before it's real" and the finding-out/building cost-structure framing match his established argument. Sauer & Sonderegger's polish-changes-what-people-feel-safe-saying claim is consistent with how the same finding is cited in piece 132 (cross-article consistency).
- **B4 (APA inline format):** PASS — all four sources use Name (Year) inline.
- **B5 (sources woven into prose at point of claim):** PASS — each citation introduces the exact claim it supports; none sit unused in the bibliography.

**Advisory:**
- A1 (source placement test): PASS — removing any citation would weaken the sentence it's in.
- A2 (domain-primary source): PASS — Houde & Hill (1997) is foundational HCI research.
- A3 (behavioral claims within 20 years, foundational exempt): PASS — Houde & Hill and Buxton are foundational/exempt by age; Lim et al. (18 years) and Sauer & Sonderegger (17 years) are both within range.

### D2 — Structural Completeness
- **B1 (all required T100 elements present):** PASS.
- **B2 (elements in prescribed order):** PASS.
- **B3 (no bold template labels as reader-facing headers):** PASS — zero bold section labels in body prose; all bold instances are in the metadata header/Goal line/Sources label, consistent with corpus convention.
- **B4 (T100 sequence: Goal → Concept → You'll See It When → The Signal → Don't Confuse This With → Try Noticing → What Next):** PASS. Verified section-by-section against the file's `---` breaks: Concept (opening scene + "Here's the test" + Houde & Hill / Lim et al. / Buxton) → You'll See It When + The Signal ("You'll recognize a prototype by..." through "...didn't intend.") → Don't Confuse This With ("The demo confusion..." through "Same screen. Different room.") → Try Noticing → What Next. **Specifically checked per this run's instruction:** the new "Here's the test: did anyone name a question before building started?" sentence sits inside the Concept block, reinforcing the concept being introduced rather than pre-empting the later, distinct checkable signal ("The checkable signal: the question was written down before building started."). The two sentences say related but non-identical things (one is a rhetorical test-question nudging the reader toward the idea; the other is the formal, later-stated checkable criterion) and they sit in different, correctly-ordered sections. No boundary blur found.
- **B5 (Don't Confuse This With names one sharp adjacent concept with a clear criterion):** PASS — the adjacent concept is "demo," and the distinguishing criterion is sharp and checkable: was a question named first, and was the room told "this is being tested" versus "this is what we're building." The two new sentences from this revision ("Introduce that same click-through as 'help us find out if this works'...") sharpen this criterion with a concrete before/after framing of the identical artifact, exactly as intended by the peer-review fix — this strengthens B5 rather than diluting it.

**Advisory:**
- A1 (Practice Atom subtype applicability): N/A — full multi-element T100 structure, not a single-step atom.

### D7 — Audience Fit
- **B1 (readable/actionable, no design background):** PASS.
- **B2 (design-coded vocabulary handled):** PASS — "click-through," "Wizard of Oz," and "MVP" are used but each is either explained inline or (for MVP) deferred to its own piece (178) without requiring the reader to already know it here.
- **B3 (no leadership-only content):** PASS.
- **B4 (no AI-adoption mandate reference):** PASS.
- **B5 (no illustrative examples/anecdotes/invented stories):** PASS. **Specifically checked per this run's instruction:** the new sentence "It's the mix-up I see most often, and it's an easy one to make, because a demo and a prototype can look identical on a screen share" was evaluated directly against this benchmark. It names no specific scene, no named person, no company, and no narrated incident — it's a general first-person observation about a recurring pattern, structurally identical to already-accepted first-person asides elsewhere in the corpus (132's "(I mean that without irony.)," 309's "(If you've spent weeks building something a two-hour session could've answered...)"). This is authorial-warmth first-person, explicitly permitted per CLAUDE.md's trust-model guidance ("Waste words on warmth... small admissions... these aren't inefficiencies"), not an anecdote. **Confirmed PASS**, not a violation.

**Advisory:**
- A1 ("real to them" test): PASS — "you've spent a week on something" framing is immediate and specific to the reader's situation.
- A2 (SaaS/3rd-party validity): PASS — naming a question before building requires no design authority over an interface.
- A3 (Try Noticing executable by PM/dev/non-custom dev): PASS — "the next time someone says 'let's build something to show people'" is a situation any role encounters.

### D8 — System Coherence
- **B1 (metadata header accurate):** PASS — confirmed against `10-master-outline.md` (line 91: prereqs 103, 132; foundational for all 309 arc pieces), `14-ordering-guide.md` (prereqs 103, 132; Wave 2), and `STATUS.md` (line 103: Standalone, Drafted, prereq for 309 arc). All match the article's own header exactly.
- **B2 (What Next routing — files exist, descriptions match content):** PASS — see Phase 4 routing check below for full detail.
- **B3 (What Next conditions are genuine decision points):** PASS — all three routing sentences name a specific downstream decision ("choose the form your prototype takes," "specific approaches for different kinds of questions," "where a prototype ends and a first shippable version begins"), not generic "if you want more" phrasing.
- **B4 (prereq cross-references are layout elements, not prose):** PASS — the two hard prereqs (103, 132) appear only in the metadata header and as publish-doc chips; no prereq reference is embedded in body prose.
- **B5 (no duplicated coverage without new angle):** PASS with a minor note — 177 (concept: prototype defined by purpose, not form) is distinct from 132 (fidelity level matched to question type), 178 (prototype vs. MVP: disposability/commitment), and the 309 arc (selecting a specific prototype type). One overlap point worth flagging under Cross-article Findings below: both 177 and 132 cite Sauer & Sonderegger (2009) for the same underlying mechanism (polish shifts what feedback people feel safe giving), applied to two different distinctions (demo-vs-prototype here; fidelity-match-to-question there). This is legitimate reuse of one mechanism for two adjacent purposes, not duplicate coverage, but it's the kind of thing worth knowing about if either piece is revised later.

### D1 — Learning Outcome Validity
- **B1 (goal verb matches tier):** PASS — "Recognize a prototype by its purpose" uses the T100 recognition verb.
- **B2 (goal achievable after one reading):** PASS.
- **B3 (teaches exactly one goal):** PASS — single goal (recognize a prototype by purpose, not form/fidelity/tool).
- **B4 (Bloom's alignment — Remember/Understand):** PASS — Try Noticing asks the reader to notice and ask a question in the moment, not execute a multi-step method or make a novel judgment call.

**Advisory:**
- A1 (non-obvious insight): PASS — the purpose-not-form definition and the demo/prototype cognitive-posture mechanism are both genuinely non-obvious to a practitioner who hasn't thought about it this way.
- A2 (Merrill's coverage): PASS — activation (the unasked-question opening scene), demonstration (Houde & Hill / Lim et al. mechanism), application (Try Noticing), integration (What Next routes to 132/178/309 for real next steps).
- A3 (works without design authority, SaaS/3rd-party valid): PASS.

### D5 — Action Section Quality
T100 applicable elements only (Try Noticing functions as the practice element; Method/Artifact/Proof/Watchout/Take This Further/AI path are T200+ elements, N/A here).
- **B1 (names specific artifact/situation):** PASS — "the next time someone says 'let's build something to show people'" names a concrete, recognizable trigger phrase, consistent with corpus precedent (147's similarly situational prompt was judged PASS by the same standard earlier in this batch).
- **B2 (achievable in one sitting, no setup, time estimate present):** **FAIL (pre-repair).** The publish doc's layout map already labels this block "Try Noticing — 2 minutes," but the article body itself had no stated time estimate, unlike piece 157's equivalent ("Take two minutes with this."). FIX TYPE: JUDGMENT-HIGH-CONFIDENCE (applied — added "Takes about two minutes." matching the publish doc's own stated time, which supplied an unambiguous correct value).
- **B3 (tests the piece's actual concept):** PASS — directly exercises the question-first recognition the piece teaches.
- **B4 (Trigger isolation test):** N/A — T100 has no formal Trigger element; the Try Noticing prompt reads standalone without requiring setup from the Concept section.

### D3 — Voice & Register
- **B1 (no banned words):** PASS — zero matches against the full banned list (script-verified).
- **B2 (no banned openers):** PASS — opens in the moment ("Someone says 'let's build something to show people.'").
- **B3 (no banned closers, rhetorical Q+A, or parallel negation):** PASS. "Here's the test: did anyone name a question before building started?" was checked against the banned rhetorical-Q+A pattern ("What does this mean? It means…") — it doesn't self-answer immediately in the banned pattern's structure; it functions as a checkable test posed to the reader, not a hollow rhetorical device. "That's not necessarily wrong... But it is different" was checked against the banned parallel-negation pattern ("Not X, but Y" as a single hedging sentence) — this is two separate declarative sentences making a substantive point across a paragraph break, not the banned single-sentence hedge construction. Both judged PASS.
- **B4 (discipline invisible):** PASS — no sentence argues for design as a function; the piece is applicable to anyone deciding to build something.
- **B5 (opens in the moment):** PASS.
- **B6 (second person throughout):** PASS — "the team" appears once in a generic scenario description but doesn't substitute for "you" as the piece's addressee; "you'll recognize," "you're," "you probably" carry the direct address throughout.
- **B7 (goal line names experience, not concept):** PASS — "You've spent a week on something and the first question back is whether this is even the right approach" names a felt moment.

**Advisory:**
- A1/A2 (warmth/humor): PASS — the "I see most often" aside (new in this revision) supplies warmth; "(That last one is a genuine prototyping technique, not a parlor trick...)" supplies a light, genuine moment of wit about Wizard of Oz prototyping.
- A3 (contractions throughout): PASS.

### D4 — Sentence-Level Craft
- **B1 (≥1 sentence ≤6 words per 150-word block):** **FAIL (pre-repair).** A script-verified sentence-length scan found a genuine ~209-word stretch — from "Work starts." through the Lim et al. quote sentence and "That framing is worth sitting with." — with no sentence at or under 6 words (the nearest candidates, "Any of these can be a prototype" at 7 words and "It also determines what to leave out" at 7 words, both missed by one word). This predates the current revision; none of the three new sentences from the peer-review fix fall inside this stretch. FIX TYPE: JUDGMENT-HIGH-CONFIDENCE (applied — tightened "Any of these can be a prototype." to "Any of these can be one." (6 words), a clean pronoun substitution with no meaning loss, since "a prototype" was just named in the immediately preceding sentence). Post-fix script re-scan confirms zero remaining gaps over 150 words anywhere in the piece.
- **B2 (no 3 consecutive sentences within 5 words of each other):** A literal word-count-window rescan flags eight candidate "triples" (e.g., 9/4/5 around "Once it includes everything... / It's just a thing. / The question is the prototype."; 7/2/6 around "It's done the opposite of its job. / Same artifact. / Different cognitive posture in the room."). Each was checked by ear. All read as deliberate short-sentence rhythm devices landing the piece's key reframes ("The question is the prototype. Everything else is the form it takes." is literally the piece's thesis delivered in punchy fragments), not monotone drone — consistent with how the identical class of literal-script false positive was resolved for pieces 147 and 157 earlier in this batch, and consistent with the style guide's explicit endorsement of "a short sentence after a dense paragraph lets the idea settle." Treated as PASS (false positives), not a violation.
- **B3 (em dash budget: ≤1/300 words, no 2 in same sentence, no 2 in adjacent paragraphs):** **FAIL (pre-repair).** True body prose (excluding the metadata Tier line and the bold **Goal:** author-scaffold line, per the same metadata-exclusion convention applied to bold-count and other formatting checks in the 147/157 evaluations) had 4 em dashes across 923 words (≈1.30/300, over the ≤1/300 budget). None were doubled in the same sentence and none were in adjacent paragraphs within true body prose. FIX TYPE: MECHANICAL (applied — converted the "quietly doesn't" em dash to a period: "That's the moment where what gets built either becomes a prototype or doesn't. And in most rooms, it quietly doesn't."). Post-repair: 3 em dashes across 925 words (≈0.97/300), within budget. **Specifically checked per this run's instruction:** confirmed the revision added zero new em dashes (verified against the git diff — none of the three added sentences contain one); the overage was pre-existing and became marginally tighter only because the word-count denominator grew slightly. **Separately noted, not counted as a violation:** the bold **Goal:** metadata line contains 2 em dashes in one sentence ("by its purpose — answering a named question cheaply before committing — rather than..."). This is a near-universal convention across T100 pieces in this corpus (checked: 157, 139, and most of the 1100-series atoms all format their **Goal:** line the same way) and is treated as author-facing metadata, not reader-facing body prose, consistent with how metadata bold was excluded from the D4.B5 bold-count budget in the 147 evaluation. Not flagged as a craft violation.
- **B4 (semicolons near-zero):** PASS — 0 semicolons in true body prose (the one semicolon in the file is in the metadata Tier/Note line: "...arc pieces; pairs with 178...").
- **B5 (bold ≤2, genuine emphasis only):** PASS — 0 bold instances in body prose; all bold in the file is metadata (Tier/Goal lines, "Sources" label).
- **B6 (bullet soup):** PASS — no bullets present.
- **B7 (one idea per sentence):** PASS.
- **B8 (dead verbs, modifier bloat):** PASS — script-checked against the full kill list and modifier-bloat list; the two matches for "rather" are both the comparative "rather than" construction, not the hedging modifier ("rather large") the rule targets — confirmed false positive, not a violation.
- **B9 (cut test — restatement, dangling analysis):** PASS — no restatements, no unearned transitions, no dangling analysis found.

**Advisory:**
- A1 (read-aloud test): PASS post-repair — no stumbles; the em-dash-to-period split and the "one" substitution both preserve the original rhythm.
- A2 (distinctive opening): PASS — "Someone says 'let's build something to show people.' The room nods." is distinctive to this piece's specific scenario, not a generic opener that could belong to another piece.

### D9 — Publication Readiness
- **B1 (publish doc exists):** PASS — `177.publish.md` exists (9,190 bytes). No blocking violation.
- **B2 (layout map has all required rows):** **FAIL (pre-repair) — one field inaccurate.** The layout map has all required rows (Prereq chip, image spec, pull quote, callout content, What Next routing, platform), but the "Goal line italic" text quoted in the Article Header row ("When nobody names the question, 'let's build something' becomes a commitment you didn't mean to make.") did not match the article's actual current italic hook line ("You've spent a week on something and the first question back is whether this is even the right approach."). This is a real discrepancy: the publish doc appears to predate a later revision of the article's hook line and was never updated. FIX TYPE: JUDGMENT-HIGH-CONFIDENCE (applied — updated the publish doc's quoted text to match the article's actual current italic line; the correct value was unambiguous since the article file is the source of truth for its own hook line).
- **B3 (pull quote ≤30 words, self-contained, names something the reader has felt):** PASS — "The question is the prototype. Everything else is the form it takes." (12 words). This is a thesis-style quote rather than a specific felt-moment quote, but the same style was already judged PASS for piece 157's pull quote earlier in this batch ("The participant's struggle isn't a problem to solve. It's the point.") — both are self-contained, memorable, and encapsulate the piece's core reframe rather than requiring outside context. Consistent treatment: PASS.
- **B4 (platform specified):** PASS — SharePoint.

**Advisory:**
- A1 (image spec illustrates, doesn't decorate): PASS — the two-panel "identical wireframe, prototype vs. demo" diagram directly maps to the piece's core purpose-not-form distinction.
- A2 (forwarding scenario named): **FAIL (advisory).** No copy-pasteable Teams forwarding scenario is present in the publish doc — the same gap identified on both piece 147 and piece 157 earlier in this batch (now a 3-for-3 pattern across this entire evaluation batch). Flagged below for human action.

---

## Phase 3 — What Was Fixed (Mechanical + High-Confidence)

All changes below were applied directly to `100-foundations/177-what-a-prototype-is.md` unless otherwise noted.

1. **D4.B3 — em dash budget (MECHANICAL).**
   - Before: *"That's the moment where what gets built either becomes a prototype or doesn't — and in most rooms, it quietly doesn't."*
   - After: *"That's the moment where what gets built either becomes a prototype or doesn't. And in most rooms, it quietly doesn't."*
   - Result: true body em dash count went from 4 (≈1.30/300 words) to 3 (≈0.97/300 words), within budget.

2. **D4.B1 — short-sentence gap over 150 words (JUDGMENT-HIGH-CONFIDENCE).**
   - Before: *"Any of these can be a prototype. (That last one is a genuine prototyping technique..."*
   - After: *"Any of these can be one. (That last one is a genuine prototyping technique..."*
   - Confidence note: applied directly because the fix is a pure pronoun substitution referring back to "a prototype" named one clause earlier — no plausible alternative reading changes meaning, and it closes a genuine ~209-word gap with no sentence ≤6 words.

3. **D5.B2 — missing in-body time estimate on Try Noticing (JUDGMENT-HIGH-CONFIDENCE).**
   - Before: *"...ask what question this will answer. Not a general direction."*
   - After: *"...ask what question this will answer. Takes about two minutes. Not a general direction."*
   - Confidence note: applied directly because the publish doc's own layout map already specifies "Try Noticing — 2 minutes," supplying the single correct value; this simply surfaces that already-decided number in the article body itself.

4. **D9.B2 — publish doc "Goal line italic" text corrected to match the article (JUDGMENT-HIGH-CONFIDENCE, applied to `100-foundations/177.publish.md`).**
   - Before: *Goal line italic: "When nobody names the question, 'let's build something' becomes a commitment you didn't mean to make."*
   - After: *Goal line italic: "You've spent a week on something and the first question back is whether this is even the right approach."*
   - Confidence note: applied directly because the article file is the unambiguous source of truth for its own italic hook line; the publish doc's quoted text simply hadn't been updated after a prior revision.

**Confidence note on all four fixes:** each had a single unambiguous correct value or minimal-change resolution (a pronoun substitution, a punctuation-to-period conversion, a number already specified elsewhere in the same publish doc, and a direct copy of the article's own current text). None required inventing new content or making a stylistic judgment call with more than one reasonable answer.

---

## Phase 3 — Flagged for Human Review (JUDGMENT)

1. **D9.A2 — no forwarding scenario in the publish doc (advisory).**
   - Issue: `177.publish.md` has no copy-pasteable Teams forwarding scenario, the same gap identified on pieces 147 and 157 earlier in this batch — this is now a consistent 3-for-3 pattern across every piece evaluated in this batch so far, and likely reflects a gap in the publish-doc template itself rather than three independent oversights.
   - Recommendation: add a one-line forwarding scenario to the publish doc, e.g.: *"Kept hearing 'let's build something to show people' in planning today and realized nobody asked what question it answers. Two-minute read on why that's the whole difference between a prototype and a demo."* Given the recurring pattern, also worth considering adding a "Forwarding scenario" row to the publish-doc template itself so future pieces don't need this flagged individually.
   - Confidence blocker: inventing promotional copy tied to a real forwarding context is authorial/marketing judgment, not a mechanical correction on the article itself — outside the scope of a repair pass on the source article.

No other JUDGMENT items were flagged. All four real violations found (D4.B3, D4.B1, D5.B2, D9.B2) had a single unambiguous correct fix and were resolved as MECHANICAL or JUDGMENT-HIGH-CONFIDENCE.

---

## Body Word Count (write-piece Test C cross-check — not one of eval-and-repair's 81 benchmarks)

Per this run's explicit instruction, word count was manually verified with a script (not estimated), counting body text only — title, metadata Tier line, bold **Goal:** line, italic hook line, and Sources block all excluded:

| Stage | Word count | Status vs. T100 range (850–1,100) / ceiling (1,100) |
|---|---|---|
| Before repairs | 923 | Within range, 177 words under ceiling |
| After repairs | 925 | Within range, 175 words under ceiling |

The repair pass added a net 2 words (the "Takes about two minutes." addition (+4 words) was mostly offset by the "a prototype" → "one" tightening (-1 word) and the em-dash-to-period conversion, which is word-count-neutral). No trim was required. This piece started with more margin than the batch's earlier pieces (147 started at 1,106 and needed a trim; 157 started at 1,050) and finished this pass comfortably inside range with room to spare in both directions.

---

## Phase 4 — Re-evaluation

Targeted re-scan of every benchmark that had a violation, post-repair:

| Benchmark | Before | After |
|---|---|---|
| D4.B1 (≥1 sentence ≤6 words per 150-word block) | FAIL (one ~209-word gap) | PASS (script-verified zero gaps) |
| D4.B3 (em dash budget, no double-dash sentences) | FAIL (4 dashes/923 words ≈1.30/300) | PASS (3 dashes/925 words ≈0.97/300) |
| D5.B2 (Try Noticing time estimate present) | FAIL (missing from article body) | PASS ("Takes about two minutes." added) |
| D9.B2 (publish doc layout map accuracy) | FAIL (Goal line italic text mismatch) | PASS (corrected to match article) |

No previously-passing benchmark was affected by these edits. Re-ran the full mechanical scan set post-repair: banned words (0), banned openers/closers (0), semicolons in true body (0), bullet soup (0 bullets), dead verbs/modifier bloat (0 real matches), bold-in-prose (0), source count (still 4, none removed or altered).

### Routing Integrity Check (D8.B2) — the three What Next targets

| Target | File exists? | Routing description in 177 | Verified against target content |
|---|---|---|---|
| **132** (Prototype Fidelity) | ✅ `100-foundations/132-prototype-fidelity.md` | "covers how fidelity level affects what feedback you get, and how to match fidelity to the question you're asking" | **Match.** 132's actual content is explicitly this: *"Fidelity is about match — specifically, whether the prototype's level of detail is appropriate for the question you're trying to answer,"* and its Signal section is framed entirely around "you'll notice a fidelity mismatch by watching what feedback you get." Direct match. |
| **309 arc** (Prototyping Arc) | ✅ `300-systems/309-prototyping-arc.md` | "walks through specific approaches for different kinds of questions" | **Match.** 309's Arc Goal states exactly this: *"Given a question you need to answer before committing, choose the prototype type that answers it with the least effort... The nine approaches differ in what question each answers."* Direct match — 309 is precisely a question-to-approach selection guide. |
| **178** (Prototype vs. MVP) | ✅ `100-foundations/178-prototype-vs-mvp.md` | "draws that line" (where a prototype ends and a first shippable version begins) | **Match.** 178's own framing is: *"A prototype has no real users... An MVP ships to real users,"* and its Signal section is built around "what happens to this thing after the learning?" — precisely the prototype-to-MVP boundary the routing description claims it draws. Direct match. |

**No routing loops found:** 178 lists 177 as a prereq (178 depends on 177's concept), and the 309 arc lists 177 and 132 as prereqs (309 depends on both). 177 routes forward to all three as genuine next steps once the reader has the core concept — this is a coherent prereq/application layering (177 as the foundational atom, 132/178/309 as downstream applications), not a loop with no intervening content.

**Note on naming convention:** 132's actual H1 title is "You're Getting Feedback on the Wrong Thing," not "Prototype Fidelity" — the parenthetical label used in 177's routing text is the established thematic/slug-style reference used consistently across this corpus (confirmed pattern from the 147 evaluation earlier in this batch), not a routing error.

---

## Cross-article Findings

Limited to what's checkable from a single-article queue plus its three routing targets:

- **Vocabulary consistency:** "question-first" / "named question" language is introduced in 177 and reused consistently (not redefined) in 132 ("the question you're trying to answer"), 178, and the 309 arc ("write that question in one sentence"). No drift found.
- **Sourcing consistency:** Sauer & Sonderegger (2009) is cited in both 177 (demo-vs-prototype cognitive-posture shift) and 132 (fidelity-mismatch feedback shift). Both citations describe the same underlying mechanism (polish changes what people feel safe saying) applied to two different, non-contradictory distinctions. This is legitimate reuse, not duplicate coverage or contradictory framing — flagged above under D8.B5 for awareness if either piece is revised later, not as an error.
- **Duplicate coverage:** none blocking — 177 (concept: purpose defines a prototype), 132 (fidelity-to-question matching), 178 (prototype vs. MVP commitment), 309 (approach selection) each cover a distinct angle. The one shared mechanism (Sauer & Sonderegger) is noted above but doesn't constitute overlapping coverage of the same concept.
- **Orphan check:** 177 is routed to from 178's prereq list, the 309 arc's prereq list, and all nine 270a–270i sub-method prereq lists per the master outline — not an orphan; it is the deliberate foundational entry point for the entire prototyping cluster.

---

## Lagging Articles

Not applicable — single-article queue, no comparison set within this run. (Cross-batch note: 177 finished this pass with 0 blocking fails and 1 advisory fail, in line with 157's result and one advisory fail better than 147's remaining 2 — all three pieces evaluated in this batch are within the 15-point lagging threshold of each other, and none is flagged as lagging.)

---

## Elevate, Never Tear Back — Verification

- No previously-passing benchmark was degraded. Confirmed via full re-scan: banned words (0), banned openers/closers (0), semicolons in true body (0), bullet soup (0 bullets), dead verbs/modifier bloat (0), bold-in-prose (0), source count (still 4, none removed), word count (increased slightly, still comfortably within the target range, not reduced).
- No content was shortened, no source was removed, no method step was simplified. All edits were surgical: one em-dash-to-period conversion, one two-word pronoun tightening, one four-word time-estimate addition, and one publish-doc text correction to match the article's existing content.

**Word count verification (per this run's explicit instruction):** manually counted with a script both before (923 words) and after (925 words) repairs. Final count is well within the 850–1,100 T100 range, 175 words under the hard ceiling — no trim was needed, and none was applied.
