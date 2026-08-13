# Code Review as UX Review
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Custom Dev primary | **Prereqs:** 100 (Assumption vs. Fact), 107 (Framing the Problem), 113 (Defining Success Before You Start), 116 (Error States), 117 (Empty States), 118 (Edge/Boundary States), 120 (Performance / Perceived Speed), 137 (The Quality Ladder), 138 (Delight as Behavioral Trust), 323 (Technical Decisions as UX Decisions)

**Goal:** Review implementation decisions for experience implications before they ship, at the moment they're cheapest to change.

**Trigger:** Any pull request where implementation choices affect what users see, wait for, or experience when something goes wrong — data models, async operations, error handling, or state management that reaches the user interface.

---

## Part 1 — What Code Review Typically Misses

**Concept:** Code review is optimized for implementation correctness: does this work, is it secure, does it follow conventions? These are the right questions for code quality. They are the wrong questions for user experience. A technically correct implementation can still produce an experience that breaks users' mental models, leaves them waiting with no feedback, or presents error messages that describe the system's problem rather than their path to a solution. Most UX failures in custom software are traceable to implementation decisions that nobody challenged in review — because reviewers didn't have a lens for it, and because code review culture doesn't typically invite this type of feedback.

**Method:**
Before reading the code, identify which of three experience-relevant zones this PR touches:
1. **Data models:** what vocabulary can the interface use? What relationships can it express? What can it not store or retrieve? The data model defines the ceiling on user-facing language and structure
2. **Async patterns:** what do users see while operations run? Where are the wait states, and what feedback is shown during them?
3. **Error handling:** what do users see when things go wrong? Is the message oriented toward the system's state or toward the user's next action?

Read the PR with only the relevant zones in mind before evaluating implementation details. A PR that doesn't touch any of these zones doesn't require experience review.

**What you end up with:** A pre-reading orientation that makes experience implications visible before you reach the implementation details — so the lens is active before confirmation bias sets in.

**Proof:** If you finish reading the PR and can't describe what a user sees during an error or a slow operation, you haven't read it with this lens yet. Apply the lens again before submitting your review.

**Watchout:** Experience review is not feature review. You're not asking whether the feature was designed correctly — that decision has been made. You're asking whether this specific implementation of the feature creates experience consequences the design didn't anticipate.

---

## Part 2 — Four Questions for Any PR

**Concept:** Most experience failures in custom software trace to one of four implementation patterns: vocabulary mismatch (the system names things differently than users do), invisible wait states (users can't tell what the system is doing), opaque errors (messages describe what the system experienced, not what the user should do), and terminal states (users reach a dead end with no recovery path). Each is preventable at review time, at a fraction of the cost of addressing it post-ship.

**Method:**
For any PR that touches user-facing behavior, ask these four questions in sequence:
1. **Vocabulary:** does the data model constrain the interface to use terms, categories, or relationships users don't recognize? A field named `entity_type` that surfaces as "Type" in the UI is fine. A data structure that forces user-visible labels no one uses is a vocabulary failure.
2. **Wait states:** what does a user see while this operation runs? Is there feedback? Is it proportional to the wait? Is there a timeout condition, and what happens when it fires?
3. **Error states:** when this fails, what does the user see? Does the message name what went wrong in system terms ("Error 500"), or in user terms with a recovery path ("The file couldn't be imported — check that it's in CSV format and try again")?
4. **Dead ends:** after an error or edge condition, where is the user? Can they retry? Is there a path back to a working state, or does failure leave them without a next step?

**What you end up with:** Four specific answers for any user-affecting PR. If any answer surfaces an unresolved problem, you have a specific, scoped concern — and a specific question to raise.

**Proof:** If you can answer all four questions from reading the PR, you've read it for experience implications. If you can't answer one or more, the PR may not handle those conditions explicitly — which is itself the concern.

**Watchout:** "Error handling will be done in a follow-up ticket" is not an answer to question 3. Experience failures that ship alongside working features are harder to fix than ones addressed before ship. Error handling is part of the feature, not a polish enhancement.

---

## Part 3 — Naming Experience Concerns Without Redesigning

**Concept:** Experience feedback in code review fails in two ways: it's dismissed because it "isn't what code review is for," or it blocks a review for concerns that don't warrant blocking. The goal is to surface the concern in a form that's actionable and maintains the team's velocity. Code review culture — rightfully — resists feedback that sounds like redesigning the feature. The distinction to maintain: you're flagging an implementation choice that creates a consequence the design didn't intend, not proposing a different feature.

**Method:**
1. For each experience concern from Part 2, write it as a consequence statement: "this implementation means users will see [X] when [Y] happens — is that the intended behavior?" — not "the error message is bad"
2. Name the specific state you're concerned about: "if the operation times out, the user reaches a dead end with no recovery path" — not "we should redesign how errors are displayed"
3. Separate naming the concern from evaluating its severity — name it first, then decide whether it warrants a block (Part 4)
4. Submit consequence-framed concerns as review comments, not as prescriptions for change

**What you end up with:** Consequence-framed concerns that the author can respond to without feeling their implementation is being redesigned from the outside.

**Proof:** If the author's response is "good catch, I'll add a retry path" or "that was intentional because X — here's why," the framing worked. If it's "that's a design decision, not a code problem," the framing suggested you were crossing into design scope — revise and restate.

**Watchout:** Not every experience concern warrants blocking. Conflating all experience concerns with blocking concerns trains reviewers to tune out valid ones. Name every concern; block only the ones that cross the threshold defined in Part 4.

---

## Part 4 — When to Flag vs. When to Ship

**Concept:** The block-or-flag decision for experience concerns is calibrated to the quality threshold the feature is being shipped to — the same logic as 324 (Ship / Patch / Hold). A functional-threshold feature with a confusing error message should be flagged and addressed in the next cycle; it shouldn't block ship if the core task completes. A feature positioned as trusted — one where users encounter that error regularly and calibrate their reliance on the system based on what they see — warrants a block.

**Method:**
Before deciding whether to block, identify which quality threshold this feature is being shipped to:
1. **Functional threshold** (can a prepared user complete the task?): block on errors that prevent task completion; flag but don't block on experience quality concerns that don't stop task completion
2. **Usable threshold** (can a user complete the task without sustained active attention?): block on comprehension failures and terminal states; flag but don't block on polish
3. **Trusted threshold** (will users build their workflow around this?): any experience failure in the primary path warrants a block — users who depend on a tool calibrate their trust based on every interaction, and edge states are not edge cases

**What you end up with:** A threshold-calibrated block or flag decision for each concern found in the review — one you can articulate if the block is challenged.

**Proof:** If you blocked a review for an experience concern and could explain specifically why it crosses the quality threshold this feature is being shipped to — not just "it's bad UX" — your decision is defensible. If you weren't sure which threshold applies, that's the place to start.

**Watchout:** "Ship it and we'll fix it later" has a well-documented track record of not being fixed later. A follow-up ticket can substitute for a block only if the follow-up is on the immediate next sprint's backlog — not the someday backlog.

---

**Try This:** Take the last three PRs you reviewed. For each one, answer the four questions from Part 2. How many had explicit error handling? How many specified what users see during async operations? Write one consequence-framed concern you would raise if reviewing one of them now — not what to fix, but what consequence to name.

**Take This Further:** In the next sprint, raise one experience concern in a code review using the consequence-framing from Part 3. After the PR ships, write one sentence: was the concern addressed? If not, why not — and was that the right call given the quality threshold?

**Judgment Exercise:** You're reviewing a PR implementing a data import workflow for a finance team that will depend on it daily. The success path is correctly implemented. For failures, the PR returns a raw system error code with no explanation and no recovery path — the original ticket explicitly scoped error handling as "phase 2." The team is under deadline pressure. What quality threshold applies to a trust-critical workflow? What do you do, and how do you make the case without prescribing the fix?

**What Next:** 324 (Ship / Patch / Hold Decision) for the launch decision after the build is complete. 323 (Technical Decisions as UX Decisions) for making the implementation decision before the PR is written. 312 (Designing What You're Building) for building self-review discipline into your build process.
