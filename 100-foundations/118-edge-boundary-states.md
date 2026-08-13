# Edge and Boundary States
**Tier:** 100 — Recognize (Practice Atom) | **Arc:** Standalone | **Prereqs:** 107 | **Episode:** 9

**Goal:** Recognize when edge cases are being decided by default code behavior rather than by deliberate design — and make those decisions explicitly before they get made by accident.

**Concept:** The working assumption is that edge cases are handled by the engineer — they'll write code for what to do when things break. The correction: default code behavior is a decision made by whoever wrote the underlying framework, not by anyone who thought about the specific user context. The mechanism: every interface behavior in an edge case was decided by someone or defaulted to something. The difference between a deliberate decision and a default is not the behavior — it's who made the choice and whether they considered the user. An app that shows a blank screen when results are empty decided to show a blank screen (by not deciding otherwise). A team that explicitly says "when results are empty, show [X] and offer [action Y]" made the same decision deliberately. Both produce behavior. Only one produced it for the user.

**The move:** Name the 2-3 most likely edge cases for a flow you're building (empty input, maximum input, an unexpected combination, a failure state). For each, write: "If this happens, the user sees [X] and can [do Y]." That's the decision made explicitly.

**Don't confuse this with QA testing.** QA finds bugs in defined behavior. Edge state design defines the behavior before QA tests it — they need the definition to know whether a behavior is a bug or a feature. A false positive: writing bug reports for unexpected edge case behavior feels like catching the problem. But if the edge case behavior was never defined, there's no standard against which to call it a bug. QA found an undefined state, not a bug.

**Try Noticing:** Walk through a flow you're currently working on. At each step, ask: what happens if the user provides nothing, provides the maximum possible input, or does something unexpected? Is each of those behaviors defined somewhere, or is it whatever the code defaults to?

**What Next:** If an edge case produces an error state, read 242 (Error States) for how to design the recovery message. If you want to test whether real users encounter these edge cases naturally, add them as secondary tasks in a 215a (Moderated Usability Session).
