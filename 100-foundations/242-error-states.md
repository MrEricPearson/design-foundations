# Error States and Error Messages
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 238, 240 | **Episode:** 9

**Goal:** Recognize when an error state is treating the error as an endpoint rather than a recovery moment, so you can evaluate error design as a continuation of the user's flow rather than an interruption to it.

**Concept:** The working assumption is that error messages communicate what went wrong. The correction: communicating what went wrong is the minimum viable error state. The error state's actual job is to return the user to a path toward their goal — which requires explaining what went wrong, why, and specifically what to do next.

The mechanism: errors occur at moments of elevated cognitive load — the user was attempting something, it failed, and they are now holding the incomplete action in working memory while trying to interpret the error message and determine what to do. Error messages that are vague, technical, or blame-attributing add to this load rather than reducing it. They require the user to translate the message into an actionable response without guidance, while already carrying the context of the failed action.

The design job of an error message is to remove decision work from the user at the moment when their capacity to do that work is lowest. That requires: (1) stating what failed in terms the user recognizes, not in terms of system internals; (2) explaining why, if the reason is actionable (if it's not actionable, it doesn't need to be in the error message); (3) stating exactly what the user should do to recover.

Three failure patterns that appear in error design:

**Vague diagnosis:** "Something went wrong" — tells the user nothing actionable. Produces either retry attempts or abandonment. Retry is correct only if the problem was transient; in all other cases, retry is busywork.

**System-centric framing:** "Error 404 — resource not found" accurately describes the system state and means nothing to the user attempting to accomplish a goal. Errors written for developers debugging a system are not the same as errors written for users recovering from a failure.

**No path forward:** A complete error message diagnoses the problem but ends there. The most common omission: a specific next action. "Invalid email format — please enter a valid email address" is better than "invalid format" but still requires the user to figure out what "valid format" means. "Email addresses must follow the format name@example.com" removes that ambiguity.

Tone: error messages should be specific, neutral, and actionable. Apologetic framing ("we're sorry, something went wrong") spends words on emotional management rather than recovery assistance. Blaming framing ("you entered an invalid value") creates defensiveness that disrupts recovery. Specific framing ("phone number must be 10 digits, without dashes") produces immediate correction.

**You'll see it when:** Users contact support to resolve errors they encountered in an interface — the error message did not give them enough to self-recover. Or when error metrics show high retry rates on the same error — the message described the failure but not the fix.

**The signal:** The error message says what went wrong but not what to do. The user's next step after reading it requires inference rather than instruction.

**Don't confuse this with:** Validation being the solution to error states. Real-time validation (showing errors as the user types, before submission) reduces the incidence of errors by catching them earlier in the flow. It does not eliminate them. Error states and real-time validation are complementary: validation reduces how often users reach error states; good error design determines what happens when they do.

**Try Noticing:** Trigger three error states in your current product intentionally — an invalid input, a network error, and a permission error if available. For each: (a) does the message say what went wrong in user terms? (b) does it say why, if the why is actionable? (c) does it say specifically what to do next? Count the fields in each answer. A complete error state answers yes to all three.

**What Next:** Read 243 (Onboarding Design Patterns) — onboarding flows are where new users are most likely to encounter their first errors, and those first errors are disproportionately influential on whether they continue. Read 223 (Form Design Method) for how error design is incorporated into the form design process rather than added at the end.
