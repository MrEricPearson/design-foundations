# Designing What You're Building
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Custom Dev primary | **Prereqs:** 103 (Attachment), 111 (Self-Critique), 123 (Usability Testing), 126 (Mental Models), 132 (Prototype Fidelity), 157 (Why You Don't Help During Testing), 158 (Task Statement Design), 241 (Empty States), 242 (Error States and Error Messages), 253 (Sunk Cost Fallacy), 254 (Mode Errors), 259 (Cognitive Dissonance)

**Goal:** Apply evaluative distance to work you built yourself — identifying the specific mechanisms that make builders poor evaluators of their own work, and the specific practices that partially restore that distance.

**Trigger:** You're building and evaluating your own work with no dedicated designer in the loop. You want to find real problems before users do — not after the cost of fixing them has compounded.

---

## Part 1 — The Expertise Trap

**Concept:** Expertise in a system makes its own logic invisible. What feels obviously correct to the person who built something is opaque to someone encountering it for the first time — because the builder's understanding of *why* something works is layered directly on top of their perception of *whether* it works. They can't see the feature without simultaneously seeing the reasoning behind it. This is not a failure of effort or attention — it's a structural feature of how expertise is encoded.

The additional factor: builders have often made multiple versions of the same feature. Each version felt right to them when they built it, and each one was revised. By the time a version ships, it has the builder's accumulated reasoning behind it. What they evaluate is not "will a stranger understand this?" but "does this reflect what I was trying to do?" — which is almost always yes.

**Method:**
Before self-reviewing any user-facing feature:
1. Write down what a first-time user would not know when they encounter this — not what they'd need to know to use it correctly, but what they'd *assume* coming in that might be wrong
2. List at least 3 things the feature takes for granted: a convention, a prior step, a piece of vocabulary, a relationship between elements
3. For each item: ask "is this visible to someone who hasn't made these assumptions?" If no, that's a potential failure point
4. Review the feature as if these assumptions were absent — not as the person who built it, but as the person who wrote the list

**What you end up with:** A set of candidate failure points identified before any user encounters them, surfaced through the mechanism that makes them invisible in normal review.

**Proof:** If the list is empty — if you can't identify anything a first-time user would assume incorrectly — you haven't regained evaluative distance. The list itself is the first signal of whether the review was possible. A completed, specific list means the review is viable; a blank list means the expertise trap is still active.

**Watchout:** Writing the list is not the same as testing the assumptions. The list identifies where to look, not whether there's a problem. Completing the list and calling it a review produces the confidence of testing without the signal.

---

## Part 2 — Your User's Mental Model of Your System

**Concept:** Users approach custom software with mental models built from whatever software they use most — not from yours (126, 255). System behaviors that seem logical based on implementation often conflict with the model users bring from their prior tools. Where they diverge, the user experiences the discrepancy as a product failure — not as a gap in their own knowledge.

This is particularly acute in custom software, where the builder often designed the architecture and the interface simultaneously. The system's behavior feels natural because the architecture feels natural — but the user has no access to the architecture. They see the interface, which inherits decisions made at the model level, with no explanation of why.

**Method:**
For the feature being built:
1. Identify: what other software do target users use for the analogous task today?
2. For each: how does that software handle the core interaction? What does the user expect to happen at each key step?
3. Compare: where does your implementation match that expectation? Where does it deviate?
4. For each deviation: is there a user-facing benefit that makes the deviation worth the mental model cost? Is the deviation explicitly surfaced — labeled, explained, or scaffolded — or does it just produce unexpected behavior?
5. Deviations without either a clear user benefit or explicit communication are model gaps waiting to produce confusion

**What you end up with:** A mapping of where your implementation aligns with or departs from user expectations — with the departures either justified, communicated, or identified as risks.

**Proof:** A deviation that's justified and communicated will be described by users as "different from what I expected, but it makes sense because X." A deviation that's neither will be described as "this doesn't work right" or "this is confusing" — even when the behavior is technically correct.

**Watchout:** "Our software is different by design" is a valid response only when the difference provides concrete user value and the user can discover and make sense of the difference without being told. Unexplained deviation that provides no user value is a mental model gap dressed up as a product decision.

---

## Part 3 — Testing Without Coaching It

**Concept:** A builder watching someone use their software has the strongest possible pull toward coaching. The implementation decisions were made for reasons, and watching someone not understand those reasons is cognitively uncomfortable — it creates cognitive dissonance between "I know this makes sense" and "this person clearly doesn't understand it." The natural response is to help, explain, or guide. That response removes the signal you need most.

The moment someone asks for help or visibly struggles is the moment you have a finding. Coaching converts that finding into a success: the person completes the task, the session ends without a recorded failure, and the problem remains in the product. The coaching feels like helping. It is actually silence about a problem.

**Method:**
Run exactly one unmoderated task before shipping any user-facing feature:
1. Pick the flow you're most uncertain about — not the one you're most confident in
2. Write one task statement in user terms using 158 (Task Statement Design): "You're trying to do X. See if you can figure out how." No hints, no context about where things are
3. Give the task to someone who hasn't seen the software — the least-informed person you have access to
4. Say nothing. Record what happens: where they click first, where they pause, where they ask questions or go back, where they stop
5. Note the moment they needed help or stopped — that moment is a finding, regardless of whether they eventually completed the task

**What you end up with:** At least one specific finding — a moment where the product failed a real person — before it fails real users at scale.

**Proof:** If the person completes the task without help or visible hesitation, the task is passing. If they stop, ask, or require guidance, you have a problem and a location. The session produces one of two useful things: confirmation that the specific flow works for this person in this context, or a specific failure mode to address.

**Watchout:** Picking someone who knows your product domain — a colleague, a teammate, anyone who's worked with similar software — produces expert review, not naive user testing. Experts bring the right mental model and succeed at tasks that will fail for real users. The test is only as good as the mismatch between the tester's model and a first-time user's model.

---

## Part 4 — Edge States and Error Design as the Trust Moment

**Concept:** For engineers, error states and edge cases are handled by exception handling — they're implementation details. For users, the way a system fails is when it reveals whether it can be trusted. The happy path is expected; everything is supposed to work. The edge case or error is unexpected — it's the moment of highest user attention, and what they see there determines whether they'll trust the product enough to continue using it.

Mode errors (254) are a specific form of this: the system is in a state the user didn't register, and the behavior is unexpected as a result. Most edge states go undesigned not because developers are careless, but because the happy path is what's built to spec and edge states don't appear in requirements. Whatever the framework's default behavior is becomes the designed behavior, by default.

**Method:**
Before shipping any feature, for the feature as a unit:
1. List every state the feature can be in beyond the happy path: loading, empty, partial data, error, offline, permission denied, time-out, conflicting state
2. For each state: write exactly what the user sees and exactly what they can do next
3. For error states specifically: does the message tell the user what went wrong (specific, not "something went wrong") and what they should do? Can they recover without leaving the feature or calling for help?
4. For mode-dependent interactions: is the current mode visible when the user is focused on the task — not in a small indicator they'd need to look away from their work to find?
5. Any state without a defined user-visible response is an undesigned state

**What you end up with:** A feature where every non-happy-path state has a defined response — not a feature where most states have a defined response.

**Proof:** A feature with designed edge states produces a different kind of bug report than one without. "The error message told me what happened and I was able to fix it" vs. "it just stopped working and I didn't know why." The former is a feature working. The latter is an undesigned state.

**Watchout:** Writing the states is not the same as testing them. For any feature before shipping: trigger at least the most likely error state manually. If you can't trigger it in testing, neither can you verify what users will see when they encounter it in production.

---

**Try This:** Take the feature you're currently building. Before writing any more code, complete Part 1 (list what a first-time user would not know) and Part 4 (list every state beyond the happy path, with what the user sees and can do in each). If either list stops you — if you can't complete it — that's the finding.

**Take This Further:** In the next sprint, before shipping anything user-facing: run one unmoderated task (Part 3) with one person. Write one sentence afterward: what did you find that you wouldn't have found in code review or self-testing?

**Judgment Exercise:** You're 3 days from launch. A single-person usability test reveals that users can't complete the primary flow without stopping to ask for help at step 3. The fix requires a 2-day rewrite. You can't delay the launch. What specifically do you ship, what do you patch with a workaround, and what do you document as a known gap with a plan to address it? What would change about your answer if you had no plan and date to address the gap?

**What Next:** 215 (Running a Usability Session) for more rigorous testing with multiple participants and a structured protocol. 300 (Cost You Don't See — Flagging Design Debt) for when you've shipped with known gaps and need to track them without losing them.
