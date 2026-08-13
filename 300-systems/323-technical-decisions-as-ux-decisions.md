# Technical Decisions as UX Decisions
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Custom Dev primary | **Prereqs:** 126 (Mental Models), 100 (Assumption vs. Fact), 107 (Framing the Problem), 110 (Constraints as Design Input), 242 (Error States and Error Messages), 254 (Mode Errors), 255 (Jakob's Law)

**Goal:** Recognize when an architectural or implementation decision has user experience consequences — data model choices that become vocabulary, async patterns that become wait states, error handling that becomes trust signals — and make those decisions with the user in front of mind, not only the implementation.

**Trigger:** Users are confused by terminology that maps to your data model rather than their mental model. Or: what looks like a simple async call is producing wait states that feel broken. Or: a feature that works correctly is described by users as "not working" because the system's behavior doesn't match what they expected. The implementation is correct — but a technical decision produced a user experience that nobody designed.

---

## Part 1 — Data Models Become Vocabulary

**Concept:** The names in a data model tend to become the names in the interface. This happens through proximity: the developer building the interface has the data model in mind, the terms are available, and using them is efficient. The problem is that data model vocabulary reflects implementation logic — how the data is structured, how entities relate, how operations are classified. Users operate in domain vocabulary — how they think about their work, what they call things, what categories make sense from their perspective.

When implementation vocabulary surfaces in the interface, users encounter a conceptual translation burden at every interaction point: label X in the product maps to concept Y in my work — and I have to do that translation every time I use it. Repeated translation burden is not just friction; it breaks the mental model that would let users operate fluently.

**Method:**
For any feature where the data model includes named entities (tables, fields, types, categories, states):
1. List every data model term that will appear in the interface — labels, status names, error messages, menu items, headers
2. For each term: what does a user who hasn't read the technical documentation call this concept in their own work?
3. Where the terms differ: which is correct from a user's perspective? The answer should be the user's term, with translation happening in the application layer rather than the user's head
4. Write the mapping: "data model term → interface term" — this becomes the vocabulary layer, and it should be a living document that updates when user research reveals better terms

**What you end up with:** A vocabulary decision for every user-visible term in the data model — based on how users think about their work, not how the database is structured.

**Proof:** Show a non-technical colleague the interface without context. For each label, ask: "what do you think this means?" If their interpretation matches the data model but not their actual work, the vocabulary is wrong. If their interpretation matches both, the translation is working.

**Watchout:** User vocabulary isn't always precise or correct in a technical sense. Sometimes the implementation term is genuinely better because it's more precise. The goal isn't to defer to whatever users call things — it's to make a conscious decision about which vocabulary to surface and to choose the user's term unless there's a specific reason the technical term serves them better.

---

## Part 2 — Async Patterns Become Wait States

**Concept:** An async operation that takes 200ms feels instantaneous. An async operation that takes 2 seconds without feedback feels broken. An async operation that takes 2 seconds with a spinner feels slow but working. The gap between "works correctly" and "feels like it's working" is almost entirely a UX concern, not a technical concern. The underlying operation is identical; what changes is what the user sees while it runs.

Async patterns that emerge from implementation choices — background processing, eventual consistency, fire-and-forget writes, polling-based updates — produce a class of user experience problems that aren't visible in technical testing. The system is working correctly; the user experience is that nothing happened, or something is happening but I can't tell when it's done, or I submitted but I don't know if it succeeded. These are all UX failures produced by async patterns that weren't designed for.

**Method:**
For any async operation in a feature:
1. Identify the start, processing, and completion states — when does the operation begin, what happens during processing, when is it definitively complete?
2. For each state: what does the user see and what feedback tells them which state they're in?
3. Identify the failure states: what does the user see if the operation fails during processing? After completion? After a timeout?
4. Write the user-visible response for each state and failure:
   - Initiated: immediate acknowledgment that something started ("Saving...")
   - Processing: indication that it's ongoing and expected to complete ("Still working...")
   - Completed: confirmation that it's done and what the result is ("Saved" / "3 items processed")
   - Failed: what went wrong and what the user can do ("Couldn't save. Check your connection and try again.")

**What you end up with:** A designed response for every async state — so the experience of "this worked" is as deliberate as the implementation of "this works."

**Proof:** Have someone run through the feature. Watch for any moment where they hesitate and say "wait, is it doing something?" — that's an async state without designed feedback. The feature passes when every async transition is legible to a user who doesn't know the implementation.

**Watchout:** Over-communicating async state is also a failure mode. If every minor operation produces a loading indicator and a success toast, the feedback becomes noise. Calibrate: immediate operations (< 100ms) don't need feedback; fast operations (100ms - 1s) need instant-start indication; slow operations (> 1s) need progressive feedback and completion confirmation.

---

## Part 3 — Error Handling Is Experience Design

**Concept:** Error handling in code is about catching exceptions and maintaining system integrity. Error handling in experience design is about maintaining user trust and enabling recovery. These are not the same goal, and satisfying the first does not satisfy the second. A technically complete try-catch block that renders `Error: 500` to the user has handled the error correctly from an implementation perspective and failed completely from a user experience perspective.

The trust implication runs deeper than the specific error message. When a system fails clearly and helpfully, users attribute the failure to the situation (server unavailable, input invalid) and continue trusting the system. When a system fails opaquely — generic error message, no recovery path, no explanation — users attribute the failure to the system and begin doubting its reliability overall. A single opaque failure can undermine confidence in features that have never failed.

**Method:**
For any feature before shipping, identify every error state it can produce:
1. **Validation errors** (user-side): the user did something that can't be processed — wrong format, missing field, value out of range. Response: explain what's wrong in the user's terms, identify where, tell them what to do to fix it
2. **System errors** (server-side, recoverable): something went wrong that might work if tried again — network timeout, temporary service unavailability. Response: tell them it didn't work, reassure them their data is safe, give them a clear retry path
3. **System errors** (permanent): something went wrong that won't be fixed by retrying — invalid state, permanent resource unavailability. Response: explain what happened, what they can't do, and what alternatives exist
4. **Silent failures** (the worst case): the operation appeared to succeed but didn't — write failed but no error was shown, submission confirmed but data wasn't saved. Response: the goal is to never produce this state; audit for any async path where failure could be swallowed without user feedback

For each error state: write the actual message the user will see. Not a description of the message — the message itself.

**What you end up with:** A designed response for every system failure — written in user terms, with a clear explanation and a recovery path.

**Proof:** Show the error messages to someone outside the team. For each: do they understand what went wrong and what they should do? If the answer requires technical context to interpret, the message is written for the developer who wrote it, not the user who will see it.

**Watchout:** Good error messages require knowing what went wrong. For errors that are hard to diagnose precisely ("something went wrong"), the message should at least tell the user their action didn't complete and give them a recovery path — even if the technical cause is unknown. A clear "it didn't work, try again" is better than a precise but opaque technical error.

---

## Part 4 — Architecture Decisions That Lock In UX

**Concept:** Some technical decisions made early in a feature's life create UX constraints that are expensive to change later. The decision to use a specific data structure constrains what queries are efficient. The decision to implement a feature as batch processing constrains whether real-time feedback is possible. The decision to store state server-side vs. client-side constrains the offline experience. None of these were UX decisions at the time they were made — they were implementation decisions with implicit UX consequences.

The cost of these decisions often surfaces late: when a user need requires something the architecture doesn't support efficiently, or when a design direction requires changing something that's deeply embedded in the data model. At that point, the technical debt isn't just code — it's UX debt, and it has a user-facing cost.

**Method:**
For any significant architectural decision in a new feature, run a two-question UX impact check before committing to the implementation:
1. "What user experiences does this architecture make easy?" — what interactions are fast, what feedback is natural, what patterns are supported well?
2. "What user experiences does this architecture make hard?" — what interactions will require workarounds, what feedback will be delayed, what patterns will be resisted by the implementation?

For any hard constraint identified in question 2:
- Is that constraint acceptable given the features currently planned?
- If a reasonable extension of this feature needed to do the hard thing, what would the cost be?
- Is the architecture decision reversible, or does reversing it require significant rework?

**What you end up with:** An explicit UX impact assessment for architectural decisions — before they become locked-in constraints.

**Proof:** When a user need requires something the architecture resists, check whether that need was in scope during the architectural decision. If it was in scope and the architecture was designed to resist it, something was missed. If it wasn't in scope, the architecture decision may have been appropriate — but now it's a named constraint with a known cost.

**Watchout:** Running a UX impact check on every technical decision is too expensive and produces analysis paralysis. Reserve this check for decisions that involve data model choices, async patterns, or caching strategies — the categories where implementation patterns most directly constrain user experience patterns.

---

**Try This:** Take a feature currently in implementation. List every user-visible label that comes from the data model (Part 1), every async operation (Part 2), and every error state (Part 3). For each category, identify one item where the current implementation choice hasn't been evaluated from a user experience perspective. What's the cost of addressing it now vs. after shipping?

**Take This Further:** In the next sprint, add one UX impact check to your architecture decision process: before finalizing a data model, write what the user-visible vocabulary will be. Before implementing async operations, write the feedback states. After the sprint: what decisions were changed by the check, and what did that prevent?

**Judgment Exercise:** You're implementing a feature where the most efficient data structure produces user-visible terminology that doesn't match how users think about their work. The terminology mismatch is significant enough that some users would be confused. A translation layer that maintains the efficient structure and surfaces correct vocabulary is feasible but adds complexity and implementation time. You have two days left in the sprint. What do you do?

**What Next:** 322 (What's Missing From Your Spec) for finding other pre-implementation gaps. 312 (Designing What You're Building) for the broader arc on self-evaluating features without a designer in the loop.
