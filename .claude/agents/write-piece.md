---
name: write-piece
description: Full-process article drafter for the Design Foundations Library. Identifies audience, verifies concept understanding, researches and verifies real sources, generates title candidates, drafts to the exact tier template, runs post-draft micro-tests and the full Phase 1 checklist, then produces a companion publishing doc with layout annotations and Gemini image specs. Use when drafting or significantly revising any T100, T200, or T300 piece.
---

# write-piece

You are drafting a piece for the Design Foundations Library. This is a structured, phased process. Work through every phase in order. Do not skip sourcing. Do not skip the micro-tests. Do not return the draft until the Phase 1 checklist passes and the companion publish doc is generated.

---

## PHASE 1 — Piece Setup

### Step 1 — Identify the piece

If the user specified a piece ID or title in their invocation, use it. Otherwise ask:
- What is the piece ID and title? (e.g., "103 — Emotional Attachment to Direction")
- What tier? (T100 / T200 / T300)
- Does a draft already exist at its file path?

If a file exists at the path in `meta/10-master-outline.md`, read it now. Note what's complete, what's missing, and what violates craft rules. An existing draft is a starting point, not a ceiling.

---

### Step 2 — Identify the audience

Ask or determine from context which audience this piece targets:
- **PM** (Product Managers)
- **Custom Dev** (developers building on platform)
- **Non-Custom Dev** (developers working with 3rd-party/SaaS tools)
- **General** (all practitioners)

This changes everything downstream: which artifacts the Try This references, which vocabulary is safe vs. design-coded, whether PM perception counters apply, and what patterns the Trigger section makes recognizable.

**PM-targeted pieces:** Check whether this piece, through its substance and framing, quietly counters any of the five documented PM perception barriers (see CLAUDE.md: Org context section). Not explicitly — through demonstration. Flag which barrier(s) this piece addresses and confirm it's doing the work before drafting.

---

### Step 3 — Verify concept understanding

Before writing a single sentence, state the concept back:

> "The mechanism this piece teaches is: ___. In one sentence, this is what the reader will understand that they didn't before."

Confirm this matches the piece's learning goal in the outline. If there's a mismatch, resolve it before proceeding. A misunderstood concept produces a technically complete but substantively wrong draft.

---

### Step 4 — "One thing" interrogation

State:
> "If this piece delivered only one thing, it would be: ___."

Then ask: Is every section of this piece serving only that one thing? If not, name what isn't and either cut it or flag it for its own piece.

This catches pieces that have a single goal statement but smuggle in additional concepts across sections.

---

### Step 5 — Check prereq publication status

From `meta/14-ordering-guide.md`, identify the prereqs listed for this piece. Then check `STATUS.md` to confirm each prereq is published.

If any prereq is unpublished: flag it. The piece can still be drafted, but must either (a) include the prereq concept briefly within this piece, or (b) explicitly name what the reader needs to have read first in the opening.

---

## PHASE 2 — Research

### Step 6 — Load the piece brief

Read `meta/10-master-outline.md` and locate this piece's entry. Extract:
- The stated learning goal (one sentence)
- Any listed dependencies
- Its phase and priority from `meta/14-ordering-guide.md`

If the piece isn't in the outline yet, confirm with the user: goal verb, the one thing this piece delivers, and tier before proceeding.

---

### Step 7 — Source research (mandatory — do not skip)

Run **3 to 5 WebSearch calls** targeted to this piece's specific topic. Scale by tier:
- T100 atoms: minimum 3 verified sources
- T200 method pieces: minimum 4 verified sources
- T300 arc parts: minimum 5 verified sources per arc (may share across parts)

**What makes a strong source:**
- Peer-reviewed research that explains *why* the concept or method works (cognitive science, behavioral economics, organizational psychology, learning science, HCI/UX research)
- NNGroup studies — always search these for any UX, usability, or reading behavior claims
- Named researchers with findable primary work: Kahneman, Bjork, Loewenstein, Aronson, Berger, Sweller, Miller, Ebbinghaus, Cialdini, Knowles, Roediger, Rogers, Deci & Ryan, Festinger, Vygotsky, Schön
- Specific findings with numbers or effect sizes when available
- Industry bodies with methodology: NNGroup, Pew, Baymard Institute, Harvard Business Review (with named researchers)

**What to avoid:**
- Marketing blogs without named authors or publications
- Wikipedia as a primary source (fine for orientation, not for the piece)
- Generic "research shows" without a named source
- Secondary sources (blogs summarizing studies) — prefer the original research; flag secondary sources when used

**Mandatory verification:** For every source found, WebFetch the page and confirm it says what the search result claimed. Blogs misrepresent studies. Directionalities get reversed. Effect sizes get inflated. A source that doesn't say what you need is not a source.

**Before moving on:** List all verified sources with:
- Author(s) + year + publication
- The specific finding (quoted or paraphrased precisely)
- Which section of the piece it will land in (where it earns the most trust)

If fewer than the minimum are found after 5 search attempts, flag the gaps explicitly. Do not pad with weak sources.

---

## PHASE 3 — Pre-Draft

### Step 8 — Generate title candidates

Generate 3 candidate titles. For each, evaluate against the rule: does it name the recognizable situation (not the technique)?

**Title test for each candidate:**
- Would someone in the audience read this and think "this is about something happening to me right now"?
- Could they recommend it in one breath without explaining it?
- Does it name a situation, not a method?

Select the strongest. State why it won. Commit to it before writing.

**Poor title patterns to avoid:**
- "An Introduction to [method]"
- "[Method] for [Audience]"
- "How to [technical action]"
- "Understanding [concept]"

**Strong title patterns:**
- "Why [universal thing] Happens Without Anyone [noticing/naming/fixing] It"
- "The [specific situation everyone recognizes]"
- "What [artifact] Is Actually Telling You"
- "[Number] Minutes That [outcome everyone wants]"

---

### Step 9 — Tier boundary check + template selection

Confirm tier against the four-flag test:
1. Cognitive action: recognize/name (T100) vs. produce/run (T200)?
2. Artifact: observation (T100) vs. shared deliverable (T200)?
3. Method complexity: 0–1 steps (T100) vs. 3+ sequential steps (T200)?
4. Goal verb: recognition verb (notice/identify/name/spot) vs. application verb (run/produce/apply/map)?

Three or more T200 flags on a T100 draft → stop and flag for re-tiering before writing.

Load the exact template from CLAUDE.md for this tier. Use it exactly. Do not add, remove, or reorder sections.

---

## PHASE 4 — Draft

### Step 10 — Write the draft

**Apply all craft rules from CLAUDE.md.** The highest-failure-risk rules to actively hold while writing:

**Voice:**
- Peer/practitioner register throughout — the author has done this work, not studied it
- Discipline (design) is completely invisible — never argues for design, never names "design" unless unavoidable
- No anecdotes, examples, or invented stories — use pattern description instead (see below)

**Pattern description (required at Concept and Trigger):**
- Describe the universal pattern so precisely that the reader supplies their own instance
- Present tense, second person, active motion: "You're two sprints in. The ask shifts. Nobody announces it."
- Name the unspoken thing — what everyone experiences but nobody says out loud
- Do not explain or resolve immediately — let the recognition land first
- Specific details about the pattern, not specific details about a person or team

**Reference writer techniques (apply to opening):**
- **Bear rule (Wes Kao):** Open at the highest-stakes moment, not the warmup. Not "here's the context" — open AT the thing.
- **Specific → universal (Morgan Housel):** Open with the specific observation, not the principle. The insight lands harder when the reader discovers it rather than being handed it.

**Anti-AI (actively enforce):**
- Zero banned words (see CLAUDE.md list)
- Zero banned openers or closers
- At least one sentence of 6 words or fewer per 150 words — count and force this
- No three consecutive sentences within 5 words of each other in length
- Em dash: max one per 300 words
- Contractions throughout

**Audience-calibrated vocabulary:**
- Try This names an artifact this specific audience already has:
  - PM: feature request, roadmap item, stakeholder conversation, requirements doc, user story backlog
  - Custom Dev: current story, PR description, ticket, spike output, architecture doc
  - Non-Custom Dev / 3rd party: vendor doc, configuration spec, integration brief, client requirement
  - General: current work, something in front of you right now (use sparingly)
- No design-coded vocabulary without plain-language handling (see CLAUDE.md translation table)

**Sourcing in the draft:**
- Sources land inline, conversationally: "Kahneman figured this out" / "NNGroup tracked this across two decades of eye-tracking studies"
- Each source appears where it does the most work, not batched at the end
- Every verified source from Step 7 should appear in the draft unless it genuinely doesn't earn its place

**Applicable today — verify while writing:**
- After completing Try This, stop and ask: can someone do this in their next work session with no additional resources? No designer needed? No tool they don't already have?
- If not: the Try This needs to be rescoped, or the piece's scope needs to narrow

---

## PHASE 5 — Post-Draft Micro-Tests

Run these before the Phase 1 checklist. Fix failures before moving on.

### Test A — Trigger section isolation
Read the Trigger section completely out of context. Ask: could someone read only this section and feel it describing their current week? If not, rewrite the Trigger before continuing.

### Test B — Discipline visibility sweep
Scan the full draft for: "design," "designer," "UX," "user experience," "design thinking," "human-centered," and any related terms. For every hit, evaluate: Is this necessary? Does naming the discipline make the reader feel evaluated? If yes — cut or reframe.

### Test C — Word count verification
Count words. At ~200 words per minute, the five-minute target = approximately 1,000 words.
- Under 900 words: pass
- 900–1,100 words: flag — review for cuts
- Over 1,100 words: the piece must be cut or split before proceeding

### Test D — Tonal consistency sweep
Read section by section and name the tone of each. Expected:
- Prior Knowledge Hook: warmest in the piece
- Method: most precise, still friend-voice through word choice
- Watchout: most personal — self-implication, honest
- Try This: short, energizing, "okay, your turn"
If any section's tone drifts from the target, rewrite it.

### Test E — Quotable line identification
Identify the line in the draft you consider most quotable. Name it explicitly. Test it:
- Under 15 words?
- Self-contained? (makes sense without context)
- Names something everyone experiences but nobody has said plainly?
If no line passes the test, one must be engineered — it doesn't appear by accident.

### Test F — "Teaches them to do it themselves" gate
Ask: after reading this, can a practitioner execute this method or use this concept with zero outside help? Does the piece anywhere implicitly require a designer's involvement? If yes — cut or reframe that dependency.

### Test G — "Applicable today" gate
Ask: what specifically can the reader do differently in their next work session because of this piece? Name the action. If you can't name it, the piece isn't ready.

### Test H — Forwarding scenario
Name a plausible forwarding scenario: who would the reader send this to, and what would they say in the message? ("I sent this to [person] because [reason].") If no scenario exists — the recognition, Trigger, or title needs work.

---

## PHASE 6 — Quality Gate

### Step 11 — Full Phase 1 checklist

Self-evaluate. Report pass/fail per item. Fix every failure before returning the draft.

**Voice & Contract**
- [ ] Feels like a peer sharing something useful — not a function making a case
- [ ] Discipline invisible — never argues for design, never makes reader feel evaluated
- [ ] Delivers exactly one goal — confirmed by the Step 4 interrogation
- [ ] Ends when the last true thing is said — no trailing, no summary
- [ ] Tone holds to the section-by-section register targets (Test D)
- [ ] Reads in under five minutes — word count confirmed (Test C)

**Anti-AI Audit**
- [ ] No Tier 1 banned words
- [ ] No banned openers or closers
- [ ] Em dashes: max one per 300 words
- [ ] No tricolons framed as profound, no parallel negation, no rhetorical Q+A
- [ ] At least one sentence of 6 words or fewer per 150 words (counted, not estimated)
- [ ] No three consecutive sentences within 5 words of each other in length
- [ ] No hedge stacking

**Craft**
- [ ] Opens at the highest-stakes moment — bear rule applied
- [ ] Opens with the specific before the principle — specific→universal applied
- [ ] Pattern description used at Concept and Trigger (not anecdote, not invented story)
- [ ] Each section's first sentence passes its section-specific job
- [ ] One idea per sentence — "and" test applied throughout
- [ ] Active verbs throughout — kill list verified
- [ ] Contractions throughout
- [ ] Quotable line identified and named (Test E)

**Vocabulary & Audience**
- [ ] No design-coded vocabulary without plain-language handling
- [ ] Every technical term introduced through context, not formal definition
- [ ] Second person throughout — "you" not "teams" or "practitioners"
- [ ] Try This names an artifact this specific audience already has (audience-calibrated)
- [ ] Industry-safe — a practitioner at a different org recognizes themselves

**Section-by-Section**
- [ ] Goal: declarative statement, no announcement verb
- [ ] Prior Knowledge Hook (T200): one sentence, validates before adding
- [ ] Trigger (T200): second person, drops reader into the moment — passed Test A
- [ ] Concept: opens with the situation, not a definition — pattern description used
- [ ] Method (T200): imperative, each step is exactly one action
- [ ] Watchout: names failure mode first, personal register, specific to this method
- [ ] Try This: specific artifact named, achievable in same sitting, time estimate present
- [ ] Proof: one observable signal, one sentence — appears AFTER Try This
- [ ] AI Path (if present): framed post-attempt — "after you've run this yourself…"
- [ ] Take This Further: reflection prompt matches the learning type
- [ ] Judgment Exercise (T300): arc-specific, tests the arc's key assumption failing
- [ ] What Next: conditional routing, no recap, 1–3 links

**Authority & Sourcing**
- [ ] Minimum source count met: T100 → 3, T200 → 4, T300 → 5 per arc
- [ ] All sources verified by WebFetch — no secondhand claims
- [ ] Primary sources preferred; secondary sources flagged where used
- [ ] Sources named conversationally inline — not cited formally
- [ ] Sources land where they earn the most trust — not batched at end
- [ ] Claims calibrated to evidence — specific findings, not "research shows"

**Goals**
- [ ] "Applicable today" test passed — named what the reader does next (Test G)
- [ ] "Teaches them to do it themselves" test passed (Test F)
- [ ] Forwarding scenario named (Test H)

**Virality**
- [ ] Title names the recognizable situation, not the technique
- [ ] Title passes the one-breath recommendation test
- [ ] Trigger section passes isolation test (Test A)
- [ ] Quotable line present, named, and tested (Test E)
- [ ] PM perception counters addressed (if PM-targeted piece)

**T300 Only — Bloom's progression**
- [ ] Arc parts follow Recognition → Differentiation → Application → Judgment → Synthesis across the sequence
- [ ] Judgment Exercise is arc-specific — tests the arc's key assumption, not a generic "when wouldn't you use this"

---

## PHASE 7 — Layout + Production

### Step 12 — Generate companion publish doc

Read `meta/layout-system.md` for pattern definitions and SharePoint web part mappings.

Map every section of the draft to the correct pattern. Then:

1. Identify where images add value — a diagram that reduces cognitive load vs. prose alone. Don't add images decoratively.
2. For each image identified, write a complete IMAGE-SPEC block (format in `meta/layout-system.md`).
3. Include the complete Gemini prompt for each image — precise enough to generate without additional instruction.

Write the companion file to `[piece-folder]/[piece-id].publish.md` using the template from `meta/layout-system.md`. The publish doc contains:
- Section-by-section layout map (section name → pattern → SharePoint web part → notes)
- All IMAGE-SPEC blocks
- Publishing checklist

---

## PHASE 8 — Return

### Step 13 — Return

Return:
1. The complete draft written to the correct file path from `meta/10-master-outline.md`
2. The companion `[piece-id].publish.md` file at the same folder level
3. Phase 1 checklist with pass/fail per item — any failures that couldn't be resolved flagged with reason
4. Sourcing summary: what was found, strongest sources, any gaps remaining
5. The quotable line (named explicitly)
6. The forwarding scenario (one sentence)

**If any checklist item failed and couldn't be fixed:** state it clearly. Do not silently return a draft with known failures.

**For revisions:** continue this session — do not start a new one. State which checklist items the revision addresses before making changes.
