# Phase 0 Content Audit Table
**Status:** Complete — all 28 rows populated + 309 prototyping arc added 2026-08-07.
**Date:** 2026-08-07
**Scope:** All 19 Tier 200 methods (200-218) + all 9 Tier 300 arcs (300-308) + new arc 309 (Prototyping).
**Governs:** Execution sequencing for Phase 1 restructuring and Phase 2 atom discovery.

---

## How to read this table

**Q1 Approach count:** How many distinct approaches exist that warrant separate pieces.
**Q1 Decision:** Single (one piece affirmed), Two files (two separate Tier 200 pieces with trigger-embedded selection), Arc (3+ approaches with arc-header selection guidance).
**Q2 Constraint-degraded path:** Exists (piece addresses constraints), Missing (gap identified), Hard limit only (piece should name the limit and redirect).
**Q3 Scale sensitivity:** Agnostic / Section needed (add "At Enterprise Scale" section) / Companion needed (structural difference too large for one piece).
**Q4 Missing atom prereqs:** Atoms required before this method publishes. Priority A = blocking; Priority B = soft prereq.
**Q5 Tool classification:** Agnostic / AI-assisted / Tool-dependent.
**Q5 AI path verdict:** Preserved (judgment stays with practitioner) / Shortcut (AI makes evaluative decisions) / N/A (no AI path).
**Q6 Restructuring decision:** Specific action. None = piece is content-complete.
**Priority:** A = blocks Track B or other Priority A work; B = significant gap; C = minor gap or no action.

---

## Tier 200 Methods

### 200 — Story Mapping in Cursor

| Column | Value |
|---|---|
| Q1: Approach count | 1 (Cursor-specific) |
| Q1: Decision | Single — but tool-agnostic equivalent missing from library entirely |
| Q2: Assumptions | Requires Cursor access |
| Q2: Constraint-degraded path | Missing — no path for non-Cursor practitioners |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (147 exists) |
| Q5: Tool classification | Tool-dependent (Cursor) |
| Q5: AI path verdict | N/A (IS the AI path) |
| Q6: Restructuring decision | Add "If you're not using Cursor:" adaptation note within method. Assess separately whether a tool-agnostic story mapping piece should precede this one (story mapping exists as a method independently of Cursor). |
| Priority | B |

---

### 201 — Grooming with AI

| Column | Value |
|---|---|
| Q1: Approach count | 1 (3-part arc: size → criteria → session) |
| Q1: Decision | Single — arc structure is correct for scope |
| Q2: Assumptions | Requires AI tool |
| Q2: Constraint-degraded path | Hard limit: org AI mandate covers this; non-AI grooming is out of scope for this piece |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (109, 111, 147 exist) |
| Q5: Tool classification | AI-assisted |
| Q5: AI path verdict | Preserved — each part explicitly names the judgment call that remains with the practitioner. Watchouts strong. |
| Q6: Restructuring decision | No action. Arc structure and judgment preservation are solid. |
| Priority | C |

---

### 202 — Lightweight Research Mechanics

| Column | Value |
|---|---|
| Q1: Approach count | 3 distinct approaches |
| Q1: Decision | Arc — approaches differ in required skill, access, and artifact type |
| Q2: Assumptions | Synchronous participant access; participant willingness to do 1:1 conversation |
| Q2: Constraint-degraded path | Missing — no guidance for: (1) no direct participant access at all (client firewalls, internal tools), (2) participants who can't do synchronous sessions, (3) situations requiring behavioral observation rather than self-report |
| Q3: Scale sensitivity | Enterprise gap: no path when participant access is completely blocked |
| Q4: Missing atom prereqs | 151 (Self-Report vs. Observed Behavior) — Priority A; 152 (Behavior vs. Attitude) — Priority A |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved — "check questions for bias" keeps practitioner in control of question design |
| Q6: Restructuring decision | Arc structure with 3 approach pieces: 202a (Conversational Interview — revise current), 202b (Remote/Async Research — new), 202c (Observational Research — new). Arc header addresses approach selection and no-access-at-all constraint. |
| Priority | A — foundational research method; blocks 301 persona arc and is core to practitioner capability |

---

### 203 — Structured Ideation / Crazy 8s

| Column | Value |
|---|---|
| Q1: Approach count | 1 (8 ideas / 8 minutes) |
| Q1: Decision | Single — the method is genuinely one approach |
| Q2: Assumptions | Room is in generative mode; participants haven't already converged on a solution |
| Q2: Constraint-degraded path | Missing — no guidance for pre-converged room (most common enterprise failure) |
| Q3: Scale sensitivity | Section needed — large groups (10+) need breakout structure; current method assumes one group sketching simultaneously |
| Q4: Missing atom prereqs | None (107, 128 exist) |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved — AI generates descriptions, practitioner sketches each; practitioner does the ideation work |
| Q6: Restructuring decision | (1) Add "When the Room Is Already Anchored" constraint section with de-anchoring steps before running the method. (2) Add large-group note in "At Enterprise Scale." |
| Priority | B |

---

### 204 — Information Architecture

| Column | Value |
|---|---|
| Q1: Approach count | 3+ (task-based, content-based, workflow-based, hybrid) |
| Q1: Decision | Two files minimum — task-based IA (most common, revise current) and content-based IA (new). Workflow-based and hybrid can be addressed within the task-based piece as variants. |
| Q2: Assumptions | Existing IA is a blank slate or starting from scratch; labels can be changed; team has authority to restructure |
| Q2: Constraint-degraded path | Missing — no guidance for: (1) inheriting legacy IA that can't be restructured, (2) vendor systems where labels are fixed, (3) systems with 3+ levels that don't simplify |
| Q3: Scale sensitivity | Section needed — multi-role systems where different user types need different entry points; deeply nested enterprise hierarchies where "keep choices small" is structurally impossible |
| Q4: Missing atom prereqs | 172 (Browse vs. Search) — Priority B soft prereq |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved — AI suggests groupings based on mental models, practitioner cross-references with actual user knowledge |
| Q6: Restructuring decision | (1) Revise 204 into 204a (Task-Based IA) with approach selection trigger. (2) Draft 204b (Content-Based IA). (3) Add "At Enterprise Scale" section for nested hierarchy and multi-role contexts. (4) Add constraint note for legacy/vendor IA. |
| Priority | A — structural gap affects navigability of most enterprise products |

---

### 205 — Content Design / UX Writing

| Column | Value |
|---|---|
| Q1: Approach count | 1 (out-loud test) |
| Q1: Decision | Single — the approach is correct and well-scoped |
| Q2: Assumptions | Practitioner can rewrite the copy (not vendor-locked) |
| Q2: Constraint-degraded path | Exists (implicitly) — the method works on any copy you control; scope is stated |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 171 (Interface Copy vs. Marketing Copy) — Priority B soft prereq |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved — AI rewrites, practitioner checks precision against original meaning |
| Q6: Restructuring decision | No structural change. Add cross-reference to atom 171 when drafted. |
| Priority | C |

---

### 206 — Journey Mapping

| Column | Value |
|---|---|
| Q1: Approach count | 3 distinct approaches |
| Q1: Decision | Arc — approaches differ fundamentally in skill, access, and artifact |
| Q2: Assumptions | Current version assumes observations already exist |
| Q2: Constraint-degraded path | Missing — Approach C (assumption-first) is the missing minimum-viable version |
| Q3: Scale sensitivity | Section needed — swimlanes for multi-persona enterprise maps |
| Q4: Missing atom prereqs | "What a Journey Map Is" — not drafted; "Swimlanes as a Comparison Tool" — not drafted. Both Priority A. |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved for Approach C and A. Limited for Approach B (facilitation context). |
| Q6: Restructuring decision | Full audit complete in governing plan. Create: 2 new atoms, 3 method pieces (206c/206a/206b), arc header. Revise 306. |
| Priority | A — executing in Phase 1 |

---

### 207 — Premortem

| Column | Value |
|---|---|
| Q1: Approach count | 1 (imagine failure, list causes) |
| Q1: Decision | Single — the method is correct; solo and group variants are execution modes, not distinct approaches |
| Q2: Assumptions | Participants can honestly name failure modes (psychological safety present) |
| Q2: Constraint-degraded path | Missing for the low-safety case — but this is a minor gap; the solo version implicitly addresses the no-safety constraint |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (108 exists) |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved — AI roleplays skeptic, practitioner "reacts to and extends" |
| Q6: Restructuring decision | No structural change. Optional: add one sentence noting that the solo version is valid when group honest failure-naming is organizationally unsafe. |
| Priority | C |

---

### 208 — Five Second Test

| Column | Value |
|---|---|
| Q1: Approach count | 1 (5-second exposure, recall test) |
| Q1: Decision | Single — genuinely one method |
| Q2: Assumptions | One person available to test with |
| Q2: Constraint-degraded path | Exists (implicitly) — the method already describes the minimal version (one person) |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | No action needed. |
| Priority | C |

---

### 209 — Design Decision Records

| Column | Value |
|---|---|
| Q1: Approach count | 1 (write at time of decision) |
| Q1: Decision | Single — correct for scope |
| Q2: Assumptions | Decision is being made in present; practitioner is at the table when the decision is made |
| Q2: Constraint-degraded path | Missing for retrospective records — what if the decision was made before the habit started? |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (113 exists) |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | Add one sentence about writing retroactive records (reconstruction from memory, labeled as reconstructed). Minor. |
| Priority | C |

---

### 210 — Retrospective Design Decisions

| Column | Value |
|---|---|
| Q1: Approach count | 1 (retrospective check) |
| Q1: Decision | Single — this IS the retrospective method |
| Q2: Assumptions | Decision context is findable (DDR was written, or memory is sufficient) |
| Q2: Constraint-degraded path | Exists (implicitly) — piece addresses "can't tell" as a valid outcome; that IS the degraded case |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (209 exists) |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved |
| Q6: Restructuring decision | No action needed. |
| Priority | C |

---

### 211 — Quick Comparative Scan

| Column | Value |
|---|---|
| Q1: Approach count | 1 (compare against relevant examples) |
| Q1: Decision | Single — correct for scope |
| Q2: Assumptions | Relevant comparisons exist and are findable |
| Q2: Constraint-degraded path | Missing for niche domains (no comparables exist) — minor gap |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (136 Critique vs. Feedback covers vocabulary) |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved |
| Q6: Restructuring decision | No structural change. Optional: note what to do when no relevant comparables exist in your domain. |
| Priority | C |

---

### 212 — Data Visualization

| Column | Value |
|---|---|
| Q1: Approach count | 1 (one chart → one question → one decision) |
| Q1: Decision | Single — correct and well-scoped |
| Q2: Assumptions | Data exists and practitioner has access to it |
| Q2: Constraint-degraded path | Exists (implicitly) — the method works at any data availability level |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 170 (Exploratory vs. Explanatory Visualization) — Priority B soft prereq |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved |
| Q6: Restructuring decision | No structural change. Add cross-reference to atom 170 when drafted. |
| Priority | C |

---

### 213 — Accessibility Forms Checklist

| Column | Value |
|---|---|
| Q1: Approach count | 1 (checklist walkthrough) |
| Q1: Decision | Single — correct for scope |
| Q2: Assumptions | Practitioner has access to modify the form |
| Q2: Constraint-degraded path | Missing for vendor/locked forms — but overlap with "Working in Vendor Software" piece covers this |
| Q3: Scale sensitivity | Agnostic at method level. Enterprise note: automated accessibility scanning tools change the mechanics at scale. |
| Q4: Missing atom prereqs | None |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | No structural change. Optional: add one sentence noting automated tooling for enterprise-scale accessibility auditing. |
| Priority | C |

---

### 214 — Affinity Mapping

| Column | Value |
|---|---|
| Q1: Approach count | 1 (sticky clustering) |
| Q1: Decision | Single — the method is correct; the scale version uses the same judgment, different mechanics |
| Q2: Assumptions | Data volume is manageable (under ~100 observations); synchronous session for physical clustering |
| Q2: Constraint-degraded path | Missing for high-volume data (400-600 observations from enterprise research rounds) |
| Q3: Scale sensitivity | Section needed — high-volume data requires stratified sampling and AI-assisted first-pass clustering |
| Q4: Missing atom prereqs | 155 (Synthesis vs. Analysis) — Priority A blocking; 156 (Name What People Do, Not What They Think) — Priority A blocking |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved — "paste notes, ask for grouping, reorganize yourself treating AI output as a draft to argue with" |
| Q6: Restructuring decision | (1) Add "At Enterprise Scale" section with high-volume mechanics. (2) Atoms 155 and 156 are blocking prereqs — method does not publish until they are drafted. |
| Priority | A — core synthesis method; atoms 155/156 are also needed by 202 and 301 |

---

### 215 — Usability Session

| Column | Value |
|---|---|
| Q1: Approach count | 3 distinct approaches |
| Q1: Decision | Two files minimum — moderated (revise current as 215a) and unmoderated (new 215b). Guerrilla is a variant within 215a or a third piece. |
| Q2: Assumptions | Synchronous participant access; permission to screen-record; recruitable participants; moderator availability |
| Q2: Constraint-degraded path | Missing for: regulated environments (no recording, legal constraints on participation), remote-only contexts, situations with zero participant access |
| Q3: Scale sensitivity | Agnostic at method level |
| Q4: Missing atom prereqs | 157 (Why You Don't Help During Testing) — Priority A blocking; 174 (Think-Aloud Protocol) — Priority A blocking; 123 (What Usability Testing Is) — should exist, verify |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A (no AI path in current version — this is correct; AI doesn't participate in usability sessions) |
| Q6: Restructuring decision | (1) Revise 215 → 215a (Moderated Usability Session) with approach selection trigger. (2) Draft 215b (Unmoderated Usability Testing). (3) Add regulated-environment constraint section to 215a. (4) Atoms 157 and 174 are blocking prereqs. |
| Priority | A — critical validation method; most practitioners lack guidance for their actual access conditions |

---

### 216 — Heuristic Evaluation

| Column | Value |
|---|---|
| Q1: Approach count | 1 (expert walk-through by heuristic) |
| Q1: Decision | Single — multi-evaluator is a scaling enhancement, not a different approach |
| Q2: Assumptions | Evaluator has internalized the 10 heuristics; evaluator has access to the interface |
| Q2: Constraint-degraded path | Exists (implicitly) — one evaluator is the minimum; the method works at that level |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 124 (Nielsen's Heuristics) — exists |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Needs review — current path has AI generating a heuristic assessment. If AI is producing the severity ratings, practitioner is accepting AI evaluation rather than conducting their own. This is a Condition 6 concern. |
| Q6: Restructuring decision | Review AI path. Revise to: AI assists identifying potential violations, practitioner severity-rates all of them. AI does not rate. |
| Priority | C (but AI path must be verified before piece is marked complete) |

---

### 217 — UX Metrics

| Column | Value |
|---|---|
| Q1: Approach count | 1 (HEART framework) |
| Q1: Decision | Single — correct for scope |
| Q2: Assumptions | Baseline measurement is possible; team has instrumentation to measure the chosen metric |
| Q2: Constraint-degraded path | Missing — no guidance for "we want to measure but have no existing baseline or instrumentation" |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 160 (Metrics vs. KPIs) — Priority B soft prereq; 161 (Why Baselines Matter) — Priority B soft prereq |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved |
| Q6: Restructuring decision | Add constraint-degraded section: what to do when no baseline exists yet (define the baseline before the project starts, measure it first, THEN set the target). Atoms 160, 161 are soft prereqs. |
| Priority | C |

---

### 218 — Card Sorting

| Column | Value |
|---|---|
| Q1: Approach count | 1 (open sort) |
| Q1: Decision | Single — open sort is the correct starting method. Closed sort and tree testing are validation follow-ons, not separate approaches; add as "What Next" routing. |
| Q2: Assumptions | Participants available (same constraint as 215) |
| Q2: Constraint-degraded path | Missing for no-participant constraint — but can be addressed with one sentence redirecting to IA heuristic approach |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 172 (Browse vs. Search) — Priority B soft prereq |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved (verify current version — add if missing) |
| Q6: Restructuring decision | Add "What Next" routing to closed sort / tree testing as follow-on validation. Add no-participant constraint note. |
| Priority | C |

---

## Tier 300 Arcs

### 300 — Cost You Don't See / Flagging Design Debt

| Column | Value |
|---|---|
| Q1: Approach count | 1 (identify → flag → track) |
| Q1: Decision | Single — correct for custom dev context. Fails for non-custom dev (vendor software). |
| Q2: Assumptions | Practitioner has ability to flag debt to someone who can act on it; product is one the team controls |
| Q2: Constraint-degraded path | Missing — no path for non-custom dev (vendor software): can identify debt, cannot flag it for action, cannot fix it |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 134 (Design Debt concept) — exists |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | Add "When You Don't Control the System" section: what to route to the vendor (documented with evidence), what to work around at configuration/workflow layer, what to document for future procurement decisions, when to escalate. |
| Priority | B — critical for non-custom dev audience (one of three Track B chapters) |

---

### 301 — From Vague Ask to Real Persona

| Column | Value |
|---|---|
| Q1: Approach count | 1 (discovery-driven through Parts 1-5) |
| Q1: Decision | Companion piece needed — 301c (Assumption-First Proto-Persona) mirrors the 206c pattern |
| Q2: Assumptions | Research access exists; team can run at least lightweight interviews |
| Q2: Constraint-degraded path | Missing — no path for when research access is blocked entirely |
| Q3: Scale sensitivity | Minor — multi-persona scope selection not addressed; but swimlanes atom from journey mapping covers the comparison concept |
| Q4: Missing atom prereqs | 151 (Self-Report vs. Observed) — Priority A; 152 (Behavior vs. Attitude) — Priority A; 173 (Empathy as Cognitive Simulation) — Priority A |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved generally — verify each part |
| Q6: Restructuring decision | Draft 301c (Assumption-First Proto-Persona) as a companion Tier 200 piece that can be run before research access exists. Update arc header to include approach selection: "If you have research access → use this arc. If you don't yet have research access → start with 301c." Atoms 151, 152, 173 are blocking prereqs for the existing arc. |
| Priority | A — core to PM chapter talk; companion piece enables no-research-access practitioners |

---

### 302 — Spotting AI Surprises / Agent Handoff

| Column | Value |
|---|---|
| Q1: Approach count | 1 (observe existing AI feature for surprises) |
| Q1: Decision | Single — but pre-deployment constraint path is missing |
| Q2: Assumptions | AI feature already deployed; user behavior data or logs available to observe |
| Q2: Constraint-degraded path | Missing — Judgment Exercise names the constraint but doesn't answer it. Piece body needs a pre-deployment path: design visibility/control/explanation structures in advance based on documented intended AI behaviors, test with simulated outputs. |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 167 (Automation Bias) — Priority A; 168 (Explainability vs. Transparency) — Priority A; 169 (Affordance) — Priority A |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved generally |
| Q6: Restructuring decision | Move pre-deployment constraint path from Judgment Exercise into the piece body as a "Before Deployment" constraint-degraded section. Atoms 167, 168, 169 are blocking prereqs. |
| Priority | B |

---

### 303 — One Feature, Three Handoffs

| Column | Value |
|---|---|
| Q1: Approach count | 1 — correct |
| Q1: Decision | Single |
| Q2: Assumptions | At least two distinct roles involved in the handoff; practitioner can facilitate the vocabulary check |
| Q2: Constraint-degraded path | Minor gap — single-owner context (same person plays all roles). Minor note only. |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 162 (Interpretation Gap) — Priority A |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | Atom 162 is a blocking prereq. Add single-owner context note. Otherwise no structural change. |
| Priority | C (atom 162 controls publish timing) |

---

### 304 — Running One Workshop

| Column | Value |
|---|---|
| Q1: Approach count | 1 (live synchronous session) |
| Q1: Decision | Single — but remote-first constraint path is missing, and async workshop may be a companion piece |
| Q2: Assumptions | All relevant participants available synchronously; decision-maker present or represented; moderately sized group (under 12) |
| Q2: Constraint-degraded path | Missing for: remote-first (camera-off, distributed, time zones), decision-maker absent, large group (15+) |
| Q3: Scale sensitivity | Section needed — large-group facilitation requires breakout structure, different convergence mechanics, different commit-capture |
| Q4: Missing atom prereqs | 163 (Alignment vs. Consensus) — Priority A; 164 (Generative vs. Convergent Thinking) — Priority A |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | (1) Add remote-first constraint-degraded section with specific mechanics (breakout timing, async-segment design, camera-optional facilitation moves). (2) Add large-group scale section. (3) Evaluate async workshop as potential companion piece (Tier 200). Atoms 163, 164 are blocking prereqs. |
| Priority | A — workshop is foundational to alignment work; remote-first is the dominant enterprise reality |

---

### 305 — Generalized Did-It-Work

| Column | Value |
|---|---|
| Q1: Approach count | 1 — correct |
| Q1: Decision | Single |
| Q2: Assumptions | A success condition was defined before the work started |
| Q2: Constraint-degraded path | Judgment Exercise addresses the no-success-condition constraint — verify this path also exists in the piece BODY (not just the Judgment Exercise). If absent from body, add it. |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | None (113, 209, 210 exist) |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | Verify the no-success-condition constraint path is in the piece body. If it lives only in the Judgment Exercise, move it to a constraint-degraded section in the body. |
| Priority | C |

---

### 306 — Service Blueprint

| Column | Value |
|---|---|
| Q1: Approach count | 1 (start from journey map, map dependencies) |
| Q1: Decision | Single — correct for scope. Input type (which of 3 journey map approaches) now changes the artifact's confidence level. |
| Q2: Assumptions | A journey map exists as input; team has access to information about backend systems/teams |
| Q2: Constraint-degraded path | Partially exists (Judgment Exercise: no journey map, no time to build one). Add this path to piece body. |
| Q3: Scale sensitivity | Section needed — multi-system enterprise blueprints become overwhelming without scope guidance |
| Q4: Missing atom prereqs | 165 (Frontstage and Backstage) — Priority A blocking |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Preserved |
| Q6: Restructuring decision | (1) Update dependency language: "starting from your journey map (any of the three types)" with a note that the map's confidence level sets the blueprint's confidence level. (2) Add "At Enterprise Scale" note about scoping: blueprint the change, not the whole system. (3) Atom 165 is a blocking prereq. (4) Move no-journey-map constraint path from Judgment Exercise to piece body. |
| Priority | B (depends on journey mapping cluster completion) |

---

### 307 — Dark Pattern Awareness

| Column | Value |
|---|---|
| Q1: Approach count | 1 (gut-check test) |
| Q1: Decision | Single — correct and well-scoped |
| Q2: Assumptions | Practitioner has some influence over the design decision or can name it to someone who does |
| Q2: Constraint-degraded path | Judgment Exercise addresses the not-the-decision-maker constraint. Verify this path also exists in the piece BODY. |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 166 (Default as a Design Decision) — Priority B soft prereq |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | N/A |
| Q6: Restructuring decision | Verify body addresses the practitioner-authority constraint (not just the Judgment Exercise). If absent, add. |
| Priority | C |

---

### 308 — Designing for AI Trust (AX Arc)

| Column | Value |
|---|---|
| Q1: Approach count | 1 (5-part arc: visibility → control → explanation → failures → trust calibration) |
| Q1: Decision | Single — arc structure is correct |
| Q2: Assumptions | AI feature is deployed; practitioner can influence the interface design |
| Q2: Constraint-degraded path | Judgment Exercise addresses vendor AI constraint (can't change interface). Pre-deployment path is absent from piece body — only Judgment Exercise references it. |
| Q3: Scale sensitivity | Agnostic |
| Q4: Missing atom prereqs | 167 (Automation Bias) — Priority A; 168 (Explainability vs. Transparency) — Priority A; 169 (Affordance) — Priority A |
| Q5: Tool classification | Agnostic |
| Q5: AI path verdict | Review per-part AI paths — most appear preserved based on reading. Verify each part. |
| Q6: Restructuring decision | (1) Add pre-deployment path to piece body (design the structures in advance based on intended AI behaviors, test with simulated outputs). (2) Verify all five per-part AI paths for judgment preservation. (3) Atoms 167, 168, 169 are blocking prereqs. |
| Priority | B |

---

---

### 309 — Prototyping Arc

| Column | Value |
|---|---|
| Q1: Approach count | 3 distinct approaches |
| Q1: Decision | Arc — approaches differ in required tools, question type, and fidelity level |
| Q2: Assumptions | Full: practitioner has the right tool for the chosen approach; concept is ready to prototype |
| Q2: Constraint-degraded path | Exists — 309a is the minimum-viable approach (no tools); 309c includes degraded path (fall back to 309b if AI generation fails); 309 arc header includes vendor software constraint path |
| Q3: Scale sensitivity | Section added in each approach piece — multi-stakeholder review context, regulated environments (309c), video walk-through distribution (309b) |
| Q4: Missing atom prereqs | 177 (What a Prototype Is) — drafted; 178 (Prototype vs. MVP) — drafted. Both are now in library. |
| Q5: Tool classification | 309a: Agnostic; 309b: Agnostic (any connected-page tool); 309c: AI-assisted (tool-agnostic prompt approach) |
| Q5: AI path verdict | 309a: Preserved — AI annotates after sketch; practitioner creates and evaluates. 309b: Preserved — AI simulates first-time user; practitioner builds and interprets. 309c: Preserved — AI generates production artifact; practitioner defines question/scope (before generating) and evaluates output (after generating). The judgment layer is explicit in both step 1 (question definition) and step 4 (output evaluation). |
| Q6: Restructuring decision | Arc structure with three approach pieces and arc-level Try This + Take This Further + Judgment Exercise. All files drafted. |
| Priority | A — foundational to prototype-as-learning-tool behavior; Judgment Exercise addresses the approval-culture failure mode (approval-culture prototyping is the dominant enterprise failure for this method) |

---

## Audit Summary

### Priority A (blocks Track B or other Priority A work — execute first)

| Piece | Primary failure | Restructuring action |
|---|---|---|
| 202 — Research Mechanics | Q1: Single approach (3 exist) | Arc: 202a/202b/202c |
| 204 — IA | Q1: No approach selection | Two files: 204a/204b + enterprise section |
| 206 — Journey Mapping | Q1: Single approach (3 exist) | Arc: 206c/206a/206b + 2 atoms — **executing now** |
| 214 — Affinity Mapping | Q3: Scale failure; atoms 155/156 blocking | Scale section; atoms before publish |
| 215 — Usability Session | Q1: Single approach (3 exist) | Two files: 215a/215b; atoms 157/174 blocking |
| 301 — Persona arc | Q1: Discovery-only; atoms blocking | Draft 301c (Assumption-First Proto-Persona) |
| 304 — Workshop arc | Q2: Remote-first missing | Remote-first constraint section + scale section |

### Priority B (significant gap — execute after A)

| Piece | Primary failure | Restructuring action |
|---|---|---|
| 200 — Story Mapping | Q5: Tool-dependent, no manual equivalent | Tool adaptation note; assess agnostic primary piece |
| 203 — Crazy 8s | Q2: Pre-converged room constraint | Constraint section + large-group scale note |
| 300 — Design Debt | Q2: Vendor context missing | "When You Don't Control the System" section |
| 302 — AI Surprises | Q2: Pre-deployment path in wrong place | Move from Judgment Exercise to piece body |
| 306 — Service Blueprint | Q4: Atom 165 blocking; input confidence | Dependency language update; scale note |
| 308 — AI Trust | Q2: Pre-deployment path missing from body | Add to body; verify AI paths |

### Priority C (minor gap or no action — after A and B)

201, 205, 207, 208, 209, 210, 211, 212, 213, 216 (AI path verify), 217, 218, 303, 305, 307

---

## Blocking Atom Dependencies

The following Priority A atoms must be drafted before their dependent method or arc can publish:

| Atom | Priority | Blocks |
|---|---|---|
| 151 — Self-Report vs. Observed Behavior | A | 202, 301 |
| 152 — Behavior vs. Attitude | A | 202, 214, 301 |
| 155 — Synthesis vs. Analysis | A | 214 |
| 156 — Name What People Do, Not What They Think | A | 214 |
| 157 — Why You Don't Help During Testing | A | 215 |
| 162 — The Interpretation Gap | A | 303 |
| 163 — Alignment vs. Consensus | A | 304 |
| 164 — Generative vs. Convergent Thinking | A | 304, 203 |
| 165 — Frontstage and Backstage | A | 306 |
| 167 — Automation Bias and Calibrated Trust | A | 302, 308 |
| 168 — Explainability vs. Transparency in AI | A | 302, 308 |
| 169 — Affordance | A | 302, 308 |
| 173 — Empathy as Cognitive Simulation | A | 301 |
| 174 — Think-Aloud Protocol | A | 215 |
| New — What a Journey Map Is | A | 206c, 206a, 206b |
| New — Swimlanes as a Comparison Tool | A | 206 enterprise section |
