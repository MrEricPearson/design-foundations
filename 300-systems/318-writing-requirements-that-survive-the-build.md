# Writing Requirements That Survive the Build
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** PM-primary | **Prereqs:** 130 (Scenario Writing), 107 (Framing the Problem), 113 (Defining Success Before You Start), 100 (Assumption vs. Fact), 317 (From a Vague Ask to a Solvable Problem)

**Goal:** Write requirements that produce the intended feature without a mid-build clarification round — by identifying what a requirement actually needs to say, surfacing the UX decisions embedded in a spec, writing acceptance criteria that are testable, and reviewing a spec before it goes to development.

**Trigger:** A feature shipped and it wasn't what you intended. Or: development is asking clarifying questions that should have been answered in the spec. Or: a design review keeps reopening settled decisions because the spec was ambiguous. The spec was complete in the sense that it covered the happy path — but it didn't survive contact with implementation.

---

## Part 1 — What Requirements Actually Need to Say

**Concept:** Most requirements describe what should be built. What they routinely omit: why it should be built (the underlying job the feature addresses), who specifically will use it in what situation, what "working" means in terms the developer can verify, and what happens when things don't go as expected. A requirement that describes only the happy path leaves every edge case, every error state, and every exception to be decided by whoever is building — which is usually the person least positioned to make an experience-quality decision at that moment.

The working assumption is that completeness means covering the feature. The correction: completeness means covering the feature AND the decision space around it — the choices a developer or designer will have to make during implementation that the spec didn't answer.

**Method:**
For each requirement or user story, verify it contains four elements:
1. **The situation:** who is doing this, in what context, prompted by what trigger? A story written without a situation produces ambiguous edge cases because the reader has to imagine a user rather than reason from a specific one
2. **The goal:** what is the user trying to accomplish — not what button they're pressing, but what outcome they need to reach
3. **The done signal:** what observable change in the system or the user's state means the goal was achieved? This is different from "the feature is implemented" — it describes the state the user reaches when the feature works
4. **The fallback:** what happens when the happy path doesn't complete? What does the user see and what can they do?

**What you end up with:** A requirement that answers the four questions a developer will ask before making implementation decisions: who, what, done-when, and what-if.

**Proof:** A requirement without a fallback will have its fallback decided during development. If you find your team's error states are inconsistent across features, the specs are missing the fallback element.

**Watchout:** The situation isn't a full persona document — it's one sentence that gives the developer enough context to make reasonable implementation choices. "A user who just imported data for the first time" is sufficient. A three-paragraph persona profile is not a requirement.

---

## Part 2 — Identifying Hidden UX Decisions

**Concept:** Every spec contains decisions that weren't made. They're implicit — embedded in the description of a feature as if they'd been resolved, when they haven't been. A developer encountering an unresolved decision during implementation will make one, because they have to in order to continue. The decision they make will be a technical one, optimized for implementation rather than for user experience. This is not a failure of care — it's a predictable outcome of a spec that left the decision to the person who can't evaluate it from the user's perspective.

Hidden decisions cluster in four places: naming (what is this thing called?), defaults (what state does it start in?), sequencing (when in the flow does this appear?), and edge conditions (what happens when expected data is absent, malformed, or extreme?).

**Method:**
For any spec before handing it to development:
1. **Naming scan:** identify every noun in the spec that will become visible to users — buttons, labels, headers, categories, status indicators. For each: is the name decided, or is the developer expected to label it? Write the decision if it hasn't been made.
2. **Default scan:** identify every configurable state — toggles, filters, selections, pre-populated fields. For each: what is the default? If "empty" is the default, is that the right user experience for a first-time encounter vs. a return visit?
3. **Sequence scan:** identify every decision point in the user flow. For each: what are the options, and which one should be presented first or emphasized? If the sequence isn't specified, it will be decided by implementation order.
4. **Edge condition scan:** for each input or data dependency: what happens when the data is absent, the maximum is exceeded, or the input is invalid? This is the "fallback" from Part 1 applied systematically to every touchpoint.

**What you end up with:** A list of decisions that the spec assumed were made but weren't — surfaced before implementation begins, when they're cheapest to resolve.

**Proof:** If the edge condition scan produces no items, the scan wasn't done carefully. Every feature that accepts user input or depends on external data has at least one edge condition that matters to the user experience.

**Watchout:** Don't resolve every hidden decision in the spec itself — some should be surfaced to design before they're answered. The goal is to make the implicit explicit, not to unilaterally fill the gaps.

---

## Part 3 — Acceptance Criteria That Are Testable

**Concept:** Acceptance criteria exist to define the boundary between "done" and "not done." Most acceptance criteria fail this function because they describe behavior rather than outcomes: "the user can filter by date" is a behavior. It says nothing about whether the filter works correctly when there are no results, whether it persists between sessions, or whether it performs acceptably under the data load the feature will realistically encounter. A tester who can check the box on "user can filter by date" while leaving all of those questions unresolved has met the criterion as written. The criterion didn't do its job.

Well-formed acceptance criteria are written as verification statements: if you run this specific action in this specific context, you observe this specific result. They're falsifiable — you can be wrong about them. If you can't be wrong about an acceptance criterion, it's not a criterion.

**Method:**
For each acceptance criterion:
1. Write it as a condition: "Given [starting state], when [action], then [observable result]" — the "given/when/then" format forces specificity about context, trigger, and outcome
2. Test it for falsifiability: is there a realistic scenario where the criterion would fail? If not, the criterion is too vague to test
3. Verify the observable result is visible to a tester: does the result appear in the interface, in a system state the tester can check, or in a behavior the tester can observe? If the result requires code inspection to verify, it's an implementation criterion, not a user experience criterion
4. For each criterion: add the edge condition that would invalidate it — the scenario where the criterion passes but the feature still fails the user

**What you end up with:** Acceptance criteria that a QA pass can confirm or deny — and that catch the failure modes that technically-passing implementations still produce.

**Proof:** Hand the acceptance criteria to a developer unfamiliar with the feature and ask them to describe what they'd build. If their description matches your intent, the criteria are specific enough. If it doesn't, the criteria left room for interpretation.

**Watchout:** Acceptance criteria are not a substitute for a definition of done that covers non-functional requirements — performance, accessibility, cross-device behavior. These should exist alongside acceptance criteria, not be buried in them.

---

## Part 4 — The Spec Review

**Concept:** A spec review is different from a requirements review. A requirements review evaluates whether the right thing is being built. A spec review evaluates whether the spec, as written, will produce the right thing when a developer implements it without being able to ask the PM questions. The test: can someone who wasn't in the discovery conversation build this feature from the spec and produce what was intended?

Most specs aren't reviewed this way. They're reviewed by people who already know the context — who fill the gaps automatically from shared background. The spec review deliberately removes that context to surface what the spec itself fails to communicate.

**Method:**
Before finalizing any spec:
1. Find someone who hasn't been involved in the feature — a developer or designer from a different team, or a colleague who can give 20 minutes
2. Give them the spec with no verbal context: "read this and tell me what you'd build"
3. Listen for the clarifying questions they ask — each question is a gap the spec left open
4. Listen for the implementation choices they make explicitly — each choice they name is a decision the spec required them to make independently
5. For each gap and each independent decision: update the spec or confirm that the resolution is acceptable

**What you end up with:** A spec that was tested against the question "will this produce the intended feature?" before development began.

**Proof:** If the spec review produces no questions and no independent decisions, either the spec is unusually complete or the reviewer had enough background context to fill the gaps without noticing. Repeat with someone who has less context.

**Watchout:** A spec that produces many questions isn't necessarily a bad spec — it might be a complex feature. The issue is questions that should have been answered before the reviewer needed to ask them. Distinguish between questions about business context (acceptable to surface during development) and questions about what the user should see or be able to do (not acceptable to leave open).

---

**Try This:** Take a spec you wrote recently that produced clarifying questions during development. Apply the hidden-decision scan from Part 2 to the original spec. Write a list of decisions the spec left open. How many of the developer's questions appear on your list?

**Take This Further:** For the next spec you write, conduct the spec review from Part 4 before handing it to development. Write one sentence afterward: what did the reviewer surface that you thought was obvious? That answer tells you what you consistently under-specify.

**Judgment Exercise:** You've written a spec that your team lead has approved and development is scheduled to start next week. During a pre-review, you identify three hidden UX decisions the spec left open — decisions that, if made incorrectly, would require a significant rework. Resolving them properly requires input from a stakeholder who is unavailable for four days. Development can't slip. What do you do?

**What Next:** 318 connects to 317 (From a Vague Ask to a Solvable Problem) — the brief from 317 is the input to the spec in 318. 209 (Design Decision Records) for documenting the decisions that were surfaced and how they were resolved.
