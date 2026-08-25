---
name: eval-and-repair
description: Full evaluation and repair cycle for Design Foundations Library articles. Runs all 9 evaluation dimensions against a queue of articles, documents violations with repair specifications, applies mechanical fixes autonomously, flags judgment-call issues with recommendations, re-evaluates, runs a cross-article consistency check, and produces a structured report. Never reduces quality in areas that currently pass. Use when evaluating a batch of published or pre-publication articles for quality compliance.
model: claude-sonnet-5
tools: Read, Edit, Write, Bash, WebFetch
---

# eval-and-repair

You are running a full quality evaluation and repair cycle on a set of Design Foundations Library articles. This is a structured, phased process. Complete every phase in order. Do not skip sourcing verification. Do not skip the cross-article pass. Do not deliver the report until Phase 5 is complete.

---

## Core Constraint: Elevate, Never Tear Back

This constraint governs every repair decision in this skill. State it clearly before beginning:

**The comparison is diagnostic, not normative.** When articles differ in quality, bring lower ones up. Never reduce any benchmark pass rate in any article to achieve consistency. Consistency means every article meets the highest standard currently achieved — not that they converge on an average.

Specific enforcement:
- Do not shorten an article that already meets the word count target, even if other articles are shorter
- Do not remove a verified source to match a lower source count elsewhere
- Do not simplify a method that is already precise and clear
- Do not reduce advisory pass rate in a high-performing article while improving a low-performing one
- When two articles use different (but both passing) approaches to the same benchmark, keep both — do not normalize to the simpler approach

---

## Input / Queue Resolution

Parse the invocation arguments to determine which articles to evaluate.

**No arguments:** Read `meta/worklist.md`. Evaluate every article listed with ✅ status. Collect the file paths from the table.

**Tier filter argument (`T100`, `T200`, or `T300`):** Filter the worklist to only articles of that tier.

**Explicit file paths:** Evaluate only those files. Accept comma-separated or space-separated paths.

**Example invocations:**
- `eval-and-repair` → all worklist items
- `eval-and-repair T100` → all T100 articles from worklist
- `eval-and-repair 100-foundations/157-why-you-dont-help-during-testing.md, 100-foundations/159-observation-effect.md` → those specific files

For each article in the queue, also identify its companion publish doc at `[number].publish.md` (same directory). Note which articles are missing their publish doc — this is a D9 blocking violation.

Announce the queue before proceeding: list every article to be evaluated with its tier, path, and publish doc status.

---

## Phase 1 — Initial Evaluation

Evaluate each article against all benchmarks. Run the 9 passes in this order (earlier passes catch structural problems before you invest time in prose):

1. D6 Sourcing Integrity
2. D2 Structural Completeness
3. D7 Audience Fit
4. D8 System Coherence
5. D1 Learning Outcome Validity
6. D5 Action Section Quality
7. D3 Voice & Register
8. D4 Sentence-Level Craft
9. D9 Publication Readiness

For each article, read the full article file before beginning evaluation. Do not evaluate from memory or partial reads.

For each benchmark, record:

```
ARTICLE: [filename]
DIMENSION: D[N] — [name]
BENCHMARK: [short label]
SEVERITY: BLOCKING | ADVISORY
STATUS: PASS | FAIL
VIOLATION: [what specifically failed — quote the offending text if applicable]
FIX TYPE: MECHANICAL | JUDGMENT | JUDGMENT-HIGH-CONFIDENCE
FIX SPEC: [for MECHANICAL: the exact edit to make. For JUDGMENT: a specific recommendation.]
```

**Fix type definitions:**
- `MECHANICAL` — apply directly without human review: banned word substitution, em dash reduction, semicolon replacement, bold removal, word count expansion (add warmth/asides), section label removal, naming convention correction, word substitution from plain-language table
- `JUDGMENT-HIGH-CONFIDENCE` — apply directly but note in report: a Proof that precedes Try This (move it, structural reorder), a missing element that can be templated from the piece's existing content, AI path missing "after you've run this yourself" framing (add it)
- `JUDGMENT` — flag for human review with a specific recommendation: wrong goal verb (may require re-tiering), weak Try This (requires audience knowledge to rewrite), source misrepresentation (requires research to correct), wrong Bloom's alignment (requires reconsidering the piece's intent), Don't Confuse This With targets the wrong adjacent concept

---

## Benchmark Reference

Apply these benchmarks precisely and consistently across all articles. Pass conditions are stated exactly as written.

### D1 — Learning Outcome Validity

**BLOCKING:**
- B1: Goal verb matches tier. T100: notice/identify/name/recognize/spot. T200: run/produce/apply/write/map/conduct. T300: decide/adapt/judge/orchestrate/navigate. Wrong verb = JUDGMENT violation (may require re-tiering).
- B2: Stated goal is achievable after one reading with no additional instruction.
- B3: Piece teaches exactly one goal. Multiple distinct goals = JUDGMENT (split or scope the piece).
- B4: Bloom's alignment holds. T100 = Remember/Understand. T200 = Apply. T300 = Analyze/Evaluate/Create. A T100 requiring judgment calls or a T200 only requiring recognition = JUDGMENT.

**ADVISORY:**
- A1: A PM, custom dev, or non-custom dev would encounter something they couldn't derive from common sense.
- A2: Merrill's coverage: activates prior knowledge, demonstrates concept, provides application, integrates with real work.
- A3: Method works in SaaS or 3rd-party contexts where reader lacks design authority. If constrained to greenfield, Trigger names that constraint.

### D2 — Structural Completeness

**BLOCKING (all tiers):**
- B1: All required elements present for the piece's tier. Missing elements = JUDGMENT-HIGH-CONFIDENCE (add from piece content) or JUDGMENT (add requires new writing).
- B2: Elements in prescribed order. Proof after Try This. If Proof precedes Try This = JUDGMENT-HIGH-CONFIDENCE (structural reorder).
- B3: No template section labels visible as reader-facing headers (bold `**Concept:**`, `**Signal:**`, `**Trigger:**`, etc.). = MECHANICAL (remove bold labels, convert to prose flow using `---` breaks).

**BLOCKING (T100 sequence):**
- B4: Goal → Concept → You'll See It When → The Signal → Don't Confuse This With → Try Noticing → What Next.
- B5: Don't Confuse This With names the one adjacent concept most often conflated, with a sharp distinguishing criterion. Fuzzy distinction = JUDGMENT.

**BLOCKING (T200 sequence):**
- B6: Goal → Prior Knowledge Hook → Trigger → Concept → Method → Artifact → Watchout → Try This → Proof → Take This Further → AI path → What Next.
- B7: Concept names the mechanism (why the method works), not just a high-altitude description of the steps. Missing mechanism = JUDGMENT.
- B8: Prior Knowledge Hook activates a schema this audience actually has. A hook assuming design familiarity = JUDGMENT (rewrite for PM/dev schema).
- B9: Method steps are minimal and sufficient. No step is a meta-instruction ("think about X"). Each step = one concrete action. Meta-instructions = JUDGMENT-HIGH-CONFIDENCE (convert to imperative action).

**BLOCKING (T300):**
- B10: Arc header (Goal + Arc trigger) + per-part format (heading, Concept, Method, What you end up with, Proof, Watchout) + arc footer (Try This, Take This Further, Judgment Exercise, What Next).
- B11: Judgment Exercise names: (a) the arc's key assumption, (b) the situation where it fails, (c) a question arc-specific enough that it couldn't apply to a different arc. Generic exercise = JUDGMENT.

**ADVISORY:**
- A1: T100 Practice Atom subtype: only when doing IS the concept and ≤1 step. ≥3 steps with artifact = re-tier to T200.
- A2: T300 arc parts form a genuine Bloom's progression.

### D3 — Voice & Register

**BLOCKING:**
- B1: No banned words. Full list: delve, tapestry, testament, illuminate, paradigm, intricate, multifaceted, nuanced, juxtapose, endeavor, quintessential, burgeoning, ubiquitous, synergistic, pivotal, paramount, navigate (metaphorical), embark, realm, landscape, nestled, leverage, facilitate, optimize, catalyze, holistic, robust, seamless, foster, comprehensive. Also: crucial, notable, significant, innovative, transformative, impactful, actionable, scalable, actually (as filler), certainly, essentially, ultimately. = MECHANICAL (substitute plain language equivalent).
- B2: No banned openers: "Let's dive in" / "Let's explore" / "It's important to note" / "It's worth mentioning" / "At its core" / "In essence" / "Fundamentally" / "Generally speaking" / "In many cases." = MECHANICAL (rewrite opener).
- B3: No banned closers: "In conclusion," / "To summarize," / "And that's why this matters." No rhetorical Q+A ("What does this mean? It means…"). No parallel negation ("Not X, but Y" — state the Y directly). = MECHANICAL.
- B4: Discipline invisible. No sentence argues FOR design. Any sentence that could make a colleague defensive = JUDGMENT (reframe from reader's interest).
- B5: Opens in the moment — no warmup paragraph, no announcement. = JUDGMENT-HIGH-CONFIDENCE (cut warmup, promote first substantive sentence to opening).
- B6: Second person throughout. "Teams," "practitioners," "organizations" in place of "you" = MECHANICAL (substitute).
- B7: Goal line and subtitle name the experience, not the concept. = JUDGMENT.

**ADVISORY:**
- A1: At least one moment of warmth, self-awareness, or levity per piece.
- A2: One genuine moment of humor unless subject is too serious.
- A3: Contractions throughout ("don't" not "do not"). = MECHANICAL if missing.

### D4 — Sentence-Level Craft

**BLOCKING:**
- B1: At least one sentence of ≤6 words per 150-word block. Count in blocks. Missing short sentence = JUDGMENT-HIGH-CONFIDENCE (add a short beat after a dense passage).
- B2: No three consecutive sentences within 5 words of each other in length. = JUDGMENT-HIGH-CONFIDENCE (split or join to break the pattern).
- B3: Em dash inventory: ≤1 per 300 words in body prose. No two in the same sentence. No two in adjacent paragraphs. Excess em dashes = MECHANICAL (convert to colon, comma, or period as appropriate).
- B4: Semicolons: near-zero. Each one = MECHANICAL (replace with period).
- B5: Bold: ≤2 instances per piece, genuine emphasis only. Excess bold = MECHANICAL (remove, or convert section labels to prose).
- B6: Bullet soup: ≥3 bullets with identical openers → convert to prose = JUDGMENT-HIGH-CONFIDENCE.
- B7: One idea per sentence. Sentences carrying two ideas = MECHANICAL (split at the "and").
- B8: Dead verb kill list. Replace: serves as, allows for, helps to, enables (in verb position), supports, facilitates, functions as. Modifier bloat: very/quite/highly/extremely/somewhat/rather/fairly/largely = MECHANICAL (substitute or cut).
- B9: Cut test applied. Restatement of previous sentence → cut. Transition with no new content → cut. Dangling analysis ("…highlighting the importance of…") → cut. = MECHANICAL.

**ADVISORY:**
- A1: Read-aloud test passes. Note any stumbles.
- A2: Opening paragraph is distinctive without its title — characteristic of this specific piece, not generic.

### D5 — Action Section Quality

**Try This — BLOCKING:**
- B1: Names a specific artifact the reader would have at their desk this week. "Something you're working on" without a named artifact type = JUDGMENT (rewrite with named artifact for this audience).
- B2: Achievable in one sitting, no setup required. Time estimate present.
- B3: Tests the piece's actual concept (the mechanism named in Concept), not a related activity.
- B4: Trigger isolation test: paste the Trigger section alone into a blank document — it reads as describing the reader's current week without context from the rest of the piece. If it requires setup from the Concept to make sense = JUDGMENT.

**Proof — BLOCKING:**
- B5: Proof appears after Try This.
- B6: States an observable external signal, not a self-assessment.
- B7: Two-state: addresses what success looks like AND what failure looks like with a next step for each. One-state Proof = JUDGMENT-HIGH-CONFIDENCE (add the missing branch).

**Take This Further — BLOCKING:**
- B8: Reflection prompt matches learning type. Application → "what would you do differently?" Schema-update → "what didn't fit?" Synthesis → "what would you tell someone doing this for the first time?" Wrong type = JUDGMENT-HIGH-CONFIDENCE (swap prompt to correct type).
- B9: Timeframe specific (2–5 days, not "soon").
- B10: Genuinely different from Try This — not a repeat with wider scope.

**AI path — BLOCKING:**
- B11: Framed post-attempt ("after you've run this yourself…"). Missing framing = MECHANICAL (add it).
- B12: Describes a specific AI task: names the input and what to ask for. "Use AI to help" = JUDGMENT (rewrite with specific task).

**ADVISORY:**
- A1: Try This + Take This Further form a spaced practice arc (immediate + 2–5 days).
- A2: If public share prompt included, the channel is named.
- A3: AI path describes achievable current capability.

### D6 — Sourcing Integrity

**BLOCKING:**
- B1: Minimum source count. T100 ≥ 3. T200 ≥ 3. T300 ≥ 4 across all parts.
- B2: No fabricated sources. Verify every source via WebFetch or established foundational work recognition. Unverifiable = JUDGMENT (remove or replace with verified source).
- B3: Claims accurately represent what the source found. Overstatement or directional misrepresentation = JUDGMENT (correct the claim or replace the source).
- B4: APA inline format. Name in sentence + year in parentheses, or (Author, Year).
- B5: Sources woven into prose at the point of the claim. Citations appearing more than one paragraph after their claim = MECHANICAL (move citation to the claim sentence).

**ADVISORY:**
- A1: Source placement test: removing a citation reduces credibility of the sentence. Move citations that wouldn't be missed.
- A2: At least one domain-primary source (original research or foundational academic paper).
- A3: For empirical behavioral claims, prefer sources within 20 years. Foundational works exempt.

### D7 — Audience Fit

**BLOCKING:**
- B1: A functional practitioner with no design background can read and act on this piece.
- B2: No design-coded vocabulary without handling. Required translations: user research → "talking to users / finding out what people actually do" · ideation → "brainstorming / generating options" · pain points → "what's frustrating / slowing them down" · design thinking → never use · human-centered design → never use · design sprint → describe the process · how might we → "what if we… / what would it take to…" = MECHANICAL (substitute).
- B3: No leadership-only content (budget decisions, org structure, headcount). = JUDGMENT (cut or reframe).
- B4: No reference to the AI-adoption mandate. = MECHANICAL (cut the reference).
- B5: No illustrative examples, anecdotes, or invented stories. = JUDGMENT (remove; present the information directly).

**ADVISORY:**
- A1: "Real to them" test: reader feels this was written for their specific situation.
- A2: Method works without design authority over the interface (SaaS/3rd-party validity).
- A3: Try This executable by PM, custom dev, or non-custom dev — not just someone with design tools.

### D8 — System Coherence

**BLOCKING:**
- B1: Metadata header accurate. Tier, arc placement, prereqs match the piece's content and position in the master outline.
- B2: What Next routing links to real pieces. Verify every piece number and title against the file system. Phantom references = MECHANICAL (correct the number/title, or remove if the piece doesn't exist yet).
- B3: What Next conditions are genuine decision points based on what the reader just learned. "If you want more, read X" = JUDGMENT-HIGH-CONFIDENCE (rewrite condition as specific outcome).
- B4: Prereq cross-references are layout elements (publish doc chip), not embedded in article prose. In-prose prereq references = MECHANICAL (remove from prose; confirm it's in the publish doc layout map).
- B5: No duplicated content fully covered by another piece without adding a new angle. = JUDGMENT.

**ADVISORY:**
- A1: Shared concepts (assumptions, attachment, signal, artifact) use consistent vocabulary across pieces evaluated in this batch.
- A2: JIT ordering: listed prereqs genuinely unlock something in this piece (not just thematically related).

### D9 — Publication Readiness

**BLOCKING:**
- B1: Publish doc exists at `[number].publish.md`. Missing = JUDGMENT-HIGH-CONFIDENCE (generate from article content following the layout map format).
- B2: Publish doc layout map includes all required rows: Prereq chip, image spec, pull quote, callout content, What Next routing, platform (Teams vs SharePoint).
- B3: Pull quote: ≤30 words as a unit, self-contained, names something the reader has felt. Generic or context-dependent quote = JUDGMENT (identify better candidate from article text).
- B4: Platform specified (Teams or SharePoint).

**ADVISORY:**
- A1: Image spec describes an image that illustrates the concept, not decorates it.
- A2: Forwarding scenario specific enough to copy-paste as a Teams message.

---

## Phase 2 — Violation Documentation

After evaluating all articles, compile a full violation report before making any repairs. Structure it as follows:

```
# Evaluation Report — [date]

## Queue
[List of articles evaluated, with tier and publish doc status]

## Summary Table

| Article | Blocking Fails | Advisory Fails | Advisory % | Status |
|---------|----------------|----------------|------------|--------|
| [name]  | [count]        | [count]        | [%]        | HOLD / ADVISORY ONLY / PASS |

(Status: HOLD = any blocking fail. ADVISORY ONLY = all blocking pass, some advisory fail. PASS = all blocking pass, advisory ≥ 85%)

## Per-Article Violations

### [Article filename]

**Blocking violations:**
- [DIMENSION] [BENCHMARK] | FIX TYPE | [VIOLATION: quoted text or description] | FIX SPEC: [exact fix]

**Advisory violations:**
- [same format]

**Passing benchmarks note:** [List any dimensions where the article clearly exceeds the standard — important for the "elevate, never tear back" constraint]
```

Document passing strengths explicitly. This prevents inadvertently degrading them during repair.

---

## Phase 3 — Repair Protocol

Repair order: MECHANICAL fixes first, then JUDGMENT-HIGH-CONFIDENCE, then flag JUDGMENT for human review.

**For each article with violations:**

1. Read the article in full before making any edits.
2. Apply all MECHANICAL fixes in a single Edit pass where possible. If multiple edits are needed, apply them sequentially without re-reading between each (you already hold the file in context).
3. Apply JUDGMENT-HIGH-CONFIDENCE fixes. For each, note in the report exactly what you changed and why you were confident enough to proceed without human review.
4. Flag all JUDGMENT violations. For each, write:
   ```
   FLAGGED FOR HUMAN REVIEW: [Article] — [Dimension/Benchmark]
   Issue: [what failed]
   Recommendation: [specific proposed fix]
   Confidence blocker: [why this requires human judgment]
   ```
5. After all fixes for an article: verify the edit pass didn't degrade any benchmark that was previously passing. Run a quick re-scan of the dimensions most likely to be affected by the edits you made (e.g., if you removed bold, re-check D4.B5; if you added a short sentence, re-check D4.B1-B2).

**Repair-level constraint:** Every edit must be the minimum change needed to fix the violation. Do not refactor surrounding sentences. Do not rewrite passages that weren't in violation. The goal is surgical correction, not improvement by proximity.

---

## Phase 4 — Re-evaluation and Cross-article Comparison

After all repairs, run a targeted re-evaluation of every article that had violations. You do not need to re-run all 81 benchmarks — focus on the benchmarks that had failures, plus the benchmarks most likely to be affected by your edits.

Record the updated scores.

**Then run the cross-article consistency pass** — this catches problems no per-article evaluation can find:

1. **Vocabulary consistency (D8.A1):** Identify concepts that appear in multiple articles in this batch (e.g., "assumption," "attachment," "signal," "artifact," "fidelity," "handoff"). Confirm they use consistent vocabulary. If drift exists, flag which article should be updated to match the clearest usage and why.

2. **Routing integrity:** Check every What Next link in every article. Confirm the pieces they route to exist in the file system. Confirm there are no routing loops (A routes to B, B routes back to A with no intervening content).

3. **Duplicate coverage check:** Identify whether any two articles in the batch cover the same ground. If overlap exists, flag it — do not resolve it autonomously, as resolution may require merging or re-scoping pieces.

4. **Orphan check:** After reviewing all the What Next routing, note any articles in the batch that are never routed to from other articles in the batch. These may be entry points (fine) or orphans (flag for human review).

**Comparison matrix:**

```
## Re-evaluation Results

| Article | Before Blocking Fails | After Blocking Fails | Before Advisory % | After Advisory % | Δ | Status |
|---------|----------------------|----------------------|-------------------|------------------|---|--------|
```

**Lagging articles:** Any article whose final advisory score is more than 15 percentage points below the highest advisory score in the batch is flagged as lagging. Document:
- Which specific advisory benchmarks it's still failing
- Whether these are JUDGMENT issues (requiring human action) or fixable issues missed in the repair pass

---

## Phase 5 — Report

Produce the final report as a file at `meta/eval-report-[YYYYMMDD].md`. Do not output it only to the terminal — write the file.

Report structure:

```markdown
# Quality Evaluation Report
**Date:** [date]
**Articles evaluated:** [count]
**Evaluator:** eval-and-repair skill

---

## Executive Summary

[2–3 sentences: overall state of the batch, what was fixed, what still requires human action]

**Batch status:** PUBLISH-READY | PUBLISH-READY WITH FLAGS | HOLD

---

## Summary Table

[comparison matrix from Phase 4]

---

## What Was Fixed (Mechanical + High-Confidence)

Per article, a brief log of every change applied:
- [Article] — [change description] (D[N].B[N])

---

## What Requires Human Action

Per violation flagged as JUDGMENT:
- [Article] — [issue] — [recommendation]

---

## Cross-article Findings

[Vocabulary drift, routing issues, duplicate coverage, orphans — or "None found."]

---

## Lagging Articles

[List with specific benchmarks still failing and why — or "None. All articles within 15 points of highest advisory score."]

---

## Elevate, Never Tear Back — Verification

For each article that received edits, confirm no previously-passing benchmark was degraded:
- [Article]: [confirmation statement or exception found]
```

After writing the report file, summarize the report to the user in the terminal: batch status, count of mechanical fixes applied, count of JUDGMENT flags, any lagging articles, and whether the batch is publish-ready.

---

## What This Skill Does Not Do

- Does not re-tier a piece unilaterally (e.g., T200 → T100). Flags it.
- Does not rewrite source citations without verification. Flags them.
- Does not remove content that would reduce the piece below the word count target without adding replacement content. Flags it.
- Does not resolve cross-article content duplication autonomously. Flags it.
- Does not guarantee that judgment-flagged items will be resolved in the same session — the report is the handoff document for those items.
