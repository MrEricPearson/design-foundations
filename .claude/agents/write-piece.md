---
name: write-piece
description: Full-process article drafter for the Design Foundations Library. Identifies audience, verifies concept understanding, researches and verifies real sources, generates title candidates, drafts to the exact tier template, runs post-draft micro-tests and the full Phase 1 checklist, then runs six multi-pass prose quality reviews toward world-class execution, then produces a companion publishing doc with layout annotations and Gemini image specs. Use when drafting or significantly revising any T100, T200, or T300 piece.
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

If any prereq is unpublished: flag it. The piece can still be drafted, but must be self-contained enough to stand alone. Handle unpublished prereqs one of two ways — (a) include the prereq concept in one bridging sentence within this piece's body, without naming the prereq by number or title, or (b) leave the piece silent on it and note the dependency in the publish doc as a chip that will activate once the prereq publishes.

**Critical rule — prereqs are layout elements, not prose.** Never write "if you haven't read X first, start there" or any variant of that sentence inside the article body. The piece reads as self-contained. The prereq chip lives below the article header in the publish doc layout — never embedded in the prose. Document it in the publish doc under "Prereq chip."

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

### Step 8 — Generate title candidates and goal line

Generate 3 candidate titles. For each, evaluate against the rule: does it name the recognizable situation (not the technique)?

**T100-specific note:** For foundational recognition pieces, the title sometimes IS the concept name stated plainly — "What a Prototype Is," "Mental Models," "The Cost of Novelty." Don't force these into situation-titles. The goal line and subtitle carry the recognition hook; the title carries the concept's identity. Apply the strong patterns below only when the concept benefits from being framed as a situation rather than named directly.

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

**Goal line (also required before drafting):** Draft the goal line — the subtitle that appears under the article header in the publish doc. This is distinct from the title. Rule: the goal line names the experience the reader has felt, not the concept the piece teaches. It's what makes someone decide to read.

Test: does it make the reader think "yes, that's me" — or "okay, so this article is about X"? The first version passes. The second describes the article; it belongs in the piece, not the subtitle.

- Passes: "When nobody names the question, 'let's build something' becomes a commitment you didn't mean to make." — the reader has felt this.
- Fails: "What a prototype is and why it matters." — describes the article; doesn't name an experience.

Commit to the goal line before writing. It will shape the opening.

---

### Step 9 — Tier boundary check + template selection

Confirm tier against the four-flag test:
1. Cognitive action: recognize/name (T100) vs. produce/run (T200)?
2. Artifact: observation (T100) vs. shared deliverable (T200)?
3. Method complexity: 0–1 steps (T100) vs. 3+ sequential steps (T200)?
4. Goal verb: recognition verb (notice/identify/name/spot) vs. application verb (run/produce/apply/map)?

Three or more T200 flags on a T100 draft → stop and flag for re-tiering before writing.

**Practice Atom subtype check (T100 only):** After confirming T100, check whether this piece is a Practice Atom. Criteria: is there a single lightweight step where performing the action IS the concept — not a method that produces an artifact, but one action where the doing is the understanding? (Examples: HMW reframing, squint test, assumption-labeling.) If yes, use the Practice Atom template:

**Practice Atom template:** Concept → [single-step Method] → Don't Confuse This With → Try Noticing → What Next

Three or more steps with a shareable artifact = re-tier to T200. The Practice Atom template is strictly for single-action, zero-artifact concepts.

**T300 note:** T300 arcs have a fundamentally different shape. Confirm with the user whether you're drafting (a) a full arc (arc-level header + 4 parts each with Concept → Method → What you end up with → Proof → Watchout + arc-level footer with Try This + Take This Further + Judgment Exercise + What Next) or (b) one standalone part of an existing arc. Clarify before drafting — a T300 piece written to the T100/T200 template will require a complete rewrite.

Load the exact template from CLAUDE.md for this tier. Use it exactly. Do not add, remove, or reorder sections.

---

## PHASE 4 — Draft

### Step 10 — Write the draft

**Apply all craft rules from CLAUDE.md.** The highest-failure-risk rules to actively hold while writing:

**Voice — the trust model:**
The reader's buy-in depends as much on liking the author as on understanding the content. Write like a smart friend sharing something they figured out — not a report, not a template, not a lesson. Practically, this means:
- Waste words on warmth. Asides, small admissions ("this took me a while to notice"), self-aware moments — these aren't inefficiencies. They make a reader feel like a person is talking to them.
- The author is present. First person ("I") is welcome when it adds warmth. "I want to tell you something" is a better opener than "here's a concept."
- Invoke excitement, not just understanding. A reader who's excited uses what they learned. Write toward wanting to try this, not just understanding it.
- Use "you're building something right now" not "teams often face." The reader should feel like this piece was written for their situation specifically.

**Structure — narrative, not labeled sections:**
Template elements (Concept, Signal, Don't Confuse, Try Noticing) are author checklists, not reader-facing headers. Do NOT write any template section label as a bold header or inline label anywhere in the piece. This ban is exhaustive and includes every named section from all tier templates: Concept, Goal, You'll see it when, The signal, Don't confuse this with, Try Noticing, What Next, Prior Knowledge Hook, Trigger, Method, Artifact, Watchout, Try This, Proof, Take This Further, AI Path, Judgment Exercise, and any Part headers. None of these appear as labels in the body. The structure is invisible — it lives in the prose and `---` breaks.

**Word count — write toward five minutes (~1000 words):**
Short is not a virtue. Under 700 words is a sign the piece was compressed, not crafted. Pieces need room to breathe — for asides, for the prose to slow down and sit with something, for the reader to feel invited rather than instructed. Compressing strips personality. Write toward 1000, not away from it.

**Plain language — familiarity over precision:**
If a phrase requires parsing, it failed. Use words people actually say at work. "Defending a decision" not "holding a direction." "You've put time into this" not "you've invested in it." If you wouldn't hear it in a normal conversation, rewrite it. Technically precise language that feels clinical loses readers. Familiar language wins them.

**Pattern description (required at Concept):**
- Describe the universal pattern so the reader supplies their own instance
- Present tense, second person, active motion: "You're a few weeks in. The ask shifts. Nobody announces it."
- Name the unspoken thing — what everyone experiences but nobody says out loud
- Let the recognition land before explaining it

**Reference writer techniques (apply to opening):**
- **Bear rule (Wes Kao):** Open at the highest-stakes moment. Not "here's the context" — open AT the thing.
- **Specific → universal (Morgan Housel):** Open with the specific observation, not the principle. The insight lands harder when the reader discovers it rather than being handed it.

**Anti-AI (actively enforce):**
- Zero banned words (full lists in Pass 3 — key ones to avoid while drafting: delve, leverage, seamless, robust, holistic, actually, certainly, essentially, ultimately, significant, facilitate, optimize)
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
- **Experiential bridge (required for every citation):** Never cite and move on. Before and/or after each citation, add a sentence that bridges the experiment's context to the reader's world. The research is proof, not the point. Pattern: [situation the reader recognizes] → [what the research found] → [what that means for the reader's situation]. A citation without a before-bridge has no anchor. One without an after-bridge has no consequence. The reader needs to feel why the research matters to them before they'll trust it.

**Humor (required unless topic is too serious):**
Every piece gets one genuine moment of levity unless the subject matter is too serious for it. Not a pun, not a setup-and-label ("this might sound funny but") — actual humor from something true and recognizable. Parentheticals work best: "(And if you've watched a team spend forty minutes on button color for a feature nobody's tested — you've seen this exact thing.)" The more the reader smiles, the more they trust the author. One moment per piece. Engineer it deliberately.

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
Count words (body text only — exclude sources block). At ~200 words per minute, the five-minute target ≈ 1,000 words.
- Under 700 words: FAIL — the piece was compressed, not crafted. Warmth, asides, and breathing room were sacrificed. Expand before proceeding.
- 700–850 words: WARNING — review for personality loss. Short pieces often cut warmth for efficiency. Verify every compression was deliberate.
- 850–1,100 words: PASS — on target
- Over 1,100 words: FAIL — the piece must be cut before proceeding. Look for sections doing more than one job, or a Try This that describes what was already said.

### Test D — Tonal consistency sweep
Read section by section and name the tone of each. Expected tone targets by tier:

**T100 pieces:**
- Opening: warmest — most personally recognizable; reader should feel seen before the first paragraph ends
- Concept: precise but still conversational — the mechanism named clearly, not academically
- Signal: concrete, checkable, second person — precision here earns trust
- Don't Confuse This With: direct but non-accusatory — name the confusion pattern, not the person making the mistake
- Try Noticing: energizing, present-tense "you" voice — reader should want to look for this
- What Next: matter-of-fact routing — not a recap, not a closing statement

**T200 pieces:**
- Prior Knowledge Hook: warmest in the piece — validate before teaching
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

### Test I — Opening sentence test
Read only the first sentence of the piece, isolated. Does it drop the reader into the highest-stakes moment? Does it name something recognizable without requiring setup? If the first sentence is scene-setting, contextualizing, or defining a term — rewrite it. The first sentence must earn the second sentence without explanation. A reader who would stop after one sentence is a reader this piece loses.

### Test J — Goal contamination check
After reading the complete draft, state the single thing this piece delivers in one sentence without using "and." If the sentence requires "and" — the piece has two goals. Name both explicitly. Cut or relocate everything serving the second goal; it belongs in its own piece.

### Test K — Self-consistency check
Read these five elements in sequence: (1) the goal line, (2) the opening sentence, (3) the concept's key claim, (4) the Try Noticing prompt, (5) the What Next routing. All five must point toward the same single thing. If any one points in a different direction — even partially — rewrite it to realign. Drift across these five elements is the most common cause of a piece that "feels off" without a diagnosable checklist failure.

### Test L — Audience-resonance spot check
Locate the opening scenario, the Try Noticing prompt, and the Try This artifact (or Try Noticing for T100). For each, ask: would a [target audience] immediately recognize this as their situation?
- PM: does it name a meeting, a requirement, or a stakeholder dynamic they'd recognize from last week?
- Custom Dev: does it involve code, a technical decision, or a dev workflow moment?
- Non-Custom Dev: does it reference a vendor, a configuration, or an adoption challenge?
- General: is it broad enough to land across all three without being so generic it's vague?
If any element reads as "sort of applicable" — make it more specific. Approximate recognition is no recognition.

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
- [ ] One genuine moment of humor or levity present (unless topic is too serious for it)

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
- [ ] Concept: opens with the situation, not a definition — pattern description used — mechanism named (why this works or why this happens, not just what it is)
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

## PHASE 7 — Multi-Pass Prose Quality Review

The Phase 1 checklist catches template-level failures. This phase catches the subtler failures that survive template compliance but undercut the reader experience. Run all passes in order. Fix every issue before moving to the next pass. Report what was found and what changed.

---

### Pass 0 — Source Accuracy Verification (mandatory — runs before all prose passes)

This pass has zero tolerance. If a source is wrong, no amount of prose quality fixes it. Run this before touching anything else.

For every source cited in the draft, do all of the following:

**Step 1 — WebFetch the source.** Use the URL from Phase 2 research, or re-locate the source now. If the source cannot be fetched (paywalled, 404, inaccessible): flag it immediately. Do not proceed with that citation. Either find a verifiable replacement or remove the claim it supported.

**Step 2 — Verify the attribution.** Confirm: author name(s) exactly as the draft states them. Year exactly as stated. Publication or journal name exactly as stated. These are not details to estimate — get them right from the source itself.

**Step 3 — Verify the finding.** Locate the specific passage, claim, or data point the draft attributes to this source. Confirm the draft's version:
- Has not reversed the direction of the finding (e.g., "X increases Y" stated as "X decreases Y")
- Has not inflated the effect size (e.g., "slightly more likely" stated as "far more likely")
- Has not stripped the original context in a way that changes what the finding means (e.g., a lab study on first-year students cited as evidence about enterprise software behavior)
- Has not attributed to Author A a finding that actually belongs to Author B

**Step 4 — Verify the context match.** Confirm that the situation in which the source made its claim is close enough to the situation in the piece to support the point being made. A lab study on word-processing software is not automatically evidence about enterprise UX. Name the gap if one exists; remove or qualify the citation if the gap is significant.

**Step 5 — Check for overstatement.** Confirm the draft's language matches the source's actual confidence level. A single controlled study "suggests" or "found evidence that" — it does not "prove" or "establish." A meta-analysis or decades of replication can claim more. If the draft states findings with more certainty than the source warrants, calibrate: "Barry Staw (1976) found evidence that…" not "Barry Staw (1976) proved that…." The claim can still be strong; the framing should be honest.

**After Pass 0, report for every source:**
- Verified: author / year / publication ✓
- Verified: the specific claim as written in the draft matches the source ✓
- Verified: context is appropriate ✓
- Verified: confidence level of the draft matches the source ✓

Any source that cannot be fully verified across all four steps is removed from the draft before the prose passes begin. The piece ships with fewer sources and accurate claims — not more sources and a hallucinated one.

---

### Pass 1 — Em dash full inventory

List every em dash in the body text with its paragraph location (e.g., "Para 2," "Try Noticing paragraph"). Then check:

- **Same sentence:** any sentence with two em dashes → replace the second with a period, comma, or colon
- **Adjacent paragraphs:** any two consecutive paragraphs each containing an em dash → replace one (visual proximity is the test — a `---` section break does not reset the adjacency clock if the paragraphs are visually close)
- **Total density:** the upper bound is roughly one em dash per 300 words. Over that, the piece leans on the device instead of the prose

After the inventory, make all fixes, then recount to confirm clean.

---

### Pass 2 — Identical-opener scan (prose bullet soup)

Scan for three or more consecutive sentences beginning with the same word or construction. Common failure patterns: "A [noun]." / "A [noun]." / "A [noun]." — "The [noun]..." three times — "You [verb]..." repeating. Any group of three or more → rewrite as flowing prose. One sentence with a comma-separated list beats three fragments with identical openers.

Also scan for parallel three-part structures framed as profound ("clarity, simplicity, and purpose"). These are the tricolon ban from the content craft rules. Rewrite as declarative prose.

---

### Pass 3 — Banned word and dead verb sweep

Run through the full lists from CLAUDE.md. Flag anything in the body text:

**Banned words (cut or replace):** delve, tapestry, testament, illuminate, paradigm, intricate, multifaceted, nuanced, juxtapose, endeavor, quintessential, burgeoning, ubiquitous, synergistic, pivotal, paramount, navigate (metaphorical), embark, realm, landscape, nestled, leverage, facilitate, optimize, catalyze, holistic, robust, seamless, foster, comprehensive

**Avoid list (strong pressure to cut):** crucial, notable, significant, innovative, transformative, impactful, actionable, scalable, actually, certainly, essentially, ultimately

**Dead verbs (replace with the thing they point at):** serves as, allows for, helps to, enables, supports, facilitates, functions as

**Structural bans:** semicolons (almost never — replace with a period); dangling analysis clauses (", highlighting the importance of…" → cut)

**Banned openers (scan the first sentence of every section):** "Let's dive in" / "Let's explore" / "It's important to note" / "It's worth mentioning" / "At its core" / "In essence" / "Fundamentally" / "Generally speaking" / "In many cases" / "Certainly!" / "Great question!"

**Banned closers (scan the final paragraph of the piece):** "In conclusion," / "To summarize," / "And that's why this matters"

**Banned patterns (scan throughout):** Rhetorical Q+A ("What does this mean? It means…" → state the answer directly without the question); parallel negation ("Not X, but Y" → state Y directly)

Fix every hit. If a banned word appears inside a direct quote, it stays — do not alter quoted material.

---

### Pass 4 — Rhythm audit

For each block of prose between `---` breaks, identify every sequence of three or more consecutive sentences. For each sequence, estimate the word count of each sentence. Apply the test: are any three consecutive sentences within five words of each other in length? If yes, break the pattern — shorten one, split another, combine two.

Then verify the short-sentence rule: at least one sentence of six words or fewer per 150 words of body text. Count the word blocks and locate the short sentences. If a 150-word window has none, engineer one. Short sentences do not occur naturally at the right frequency — they must be placed deliberately.

Check the rhythm shape within each block: does it build (longer → longer) then release (short)? A short sentence after a dense paragraph lets the idea settle. A short sentence at a key insight earns emphasis. A short sentence at the end of Try Noticing signals "your turn."

**Opening paragraph — dedicated rhythm check:** The opening paragraph earns separate attention because it's where the reader decides whether to continue. Run the rhythm checks above on it first and separately: does it have at least one sentence of six words or fewer in the first fifty words? Does it vary sentence lengths? Does the rhythm build to the paragraph's key moment, then release? A flat opening loses more readers than a flat middle section.

---

### Pass 5 — Logical and phrasing integrity

Read every sentence looking for:

**Circular phrasing:** subject and predicate share the same noun ("a prototype either becomes a prototype or doesn't" → "what gets built either becomes a prototype or doesn't"). When the sentence has to use its own subject to define itself, it's doing no work.

**Throat-clearing connectives:** "The insight underneath that is that…" / "What this means is that…" / "The reason for this is that…" / "It's worth noting that…" — these delay the point. Replace with a colon or rewrite to lead with the claim.

**Stacked hedges:** "often tends to sometimes suggest" — each hedge is a signal the writer isn't sure. One hedge per claim is the limit. Beyond that, the sentence needs to be cut or the claim needs to be more precise.

**"Actually":** specifically watch for this word. It appears on the Avoid list and often signals that the preceding sentence set up a false expectation that this sentence is correcting. Fix the preceding sentence instead.

**Passive voice:** Scan for any sentence where the actor is omitted or demoted ("assumptions are made," "the direction was changed," "it was decided that"). Passive constructions hide the human doing the thing — this piece needs the human visible. Rewrite with the actor as subject: "the team made an assumption," "they changed the direction," "someone decided." Every passive-to-active rewrite makes the sentence more concrete and makes the reader feel the situation more directly.

---

### Pass 6 — Read-aloud test

Read the full piece aloud, sentence by sentence, at normal speaking pace. This is the definitive fluidity test — stumbles the eye skips over become audible. When the narrator stumbles, something is wrong. Diagnose:

- **Stumble on a long sentence:** the sentence is carrying two ideas. Split it at the "and."
- **Stumble on a transition:** the connective is wrong or missing. Rewrite the opener of the following sentence.
- **Stumble on a quote or citation:** the attribution isn't smoothly introduced. Rewrite the lead-in.
- **Rhythm feels flat across a whole paragraph:** all sentences are the same weight. Break the pattern with a short sentence.
- **The piece doesn't build:** identify where the energy drops and why. Usually a section is too explanatory when it should be energizing (Try Noticing), or too personal when it should be precise (Method).

After Pass 6, the piece is ready for layout. If Pass 6 surfaces issues that require returning to an earlier pass — return. Do not skip the earlier pass re-check.

---

## PHASE 8 — Layout + Production

### Step 12 — Generate companion publish doc

Read `meta/layout-system.md` for pattern definitions and SharePoint web part mappings.

Map every section of the draft to the correct pattern. Then:

1. Identify where images add value — a diagram that reduces cognitive load vs. prose alone. Don't add images decoratively.
2. For each image identified, write a complete IMAGE-SPEC block (format in `meta/layout-system.md`).
3. Include the complete Gemini prompt for each image — precise enough to generate without additional instruction.

Write the companion file to `[piece-folder]/[piece-id].publish.md` using the template from `meta/layout-system.md`. The publish doc contains all of the following (all required):

1. **Metadata header:** tier, wave, word count, reading time
2. **Layout map table:** every prose section mapped to pattern name + SharePoint web part + notes
3. **Goal line and subtitle:** confirmed goal line for the article header (italic, below title in publish)
4. **Prereq chip specification:** label, link target, placeholder status — never embedded in article prose, layout element only
5. **Pull quote selection:** the quotable line from Test E, styled as P11
6. **IMAGE-SPEC block(s):** for each image identified — format from `meta/layout-system.md`, including complete Gemini prompt precise enough to generate without additional instruction
7. **Spacer schedule:** table of transitions and pixel heights between every section
8. **Publishing checklist:** all layout, typography, web part, and pre-publish approval items
9. **Source attribution section:** all sources in APA format, compact text styling

---

## PHASE 9 — Return

### Step 13 — Return

Return:
1. The complete draft written to the correct file path from `meta/10-master-outline.md`
2. The companion `[piece-id].publish.md` file at the same folder level
3. Phase 1 checklist with pass/fail per item — any failures that couldn't be resolved flagged with reason
4. Sourcing summary: what was found, strongest sources, any gaps remaining
5. The quotable line (named explicitly)
6. The forwarding scenario (one sentence)
7. Phase 7 prose review summary: what each pass (Pass 0 through Pass 6) found and what was changed — or "clean" for passes that found nothing
8. Final word count (body text only, excluding sources block) — confirmed against Test C range

**If any checklist item failed and couldn't be fixed:** state it clearly. Do not silently return a draft with known failures.

**For revisions:** continue this session — do not start a new one. State which checklist items the revision addresses before making changes.
