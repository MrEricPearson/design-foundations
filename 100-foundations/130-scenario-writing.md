# Scenario Writing
**Tier:** 100 — Recognize (Practice Atom) | **Arc:** Standalone | **Prereqs:** 125 | **Episode:** 3

**Goal:** Recognize when design or testing decisions are floating free of a specific user context — and write the one paragraph that grounds every subsequent decision in a real situation.

**Concept:** The working assumption is that knowing the user type (the persona) is sufficient context for making design decisions and writing test tasks. The correction: a persona describes who the user is in general; a scenario describes what they're doing right now, today, under a specific constraint. Without the scenario, design decisions are made against a generic user in a generic situation — which produces interfaces that work in the abstract and fail in the specific. The mechanism: a constraint (time pressure, incomplete information, a prior experience that set an expectation) is what makes a situation testable. Without a constraint, any reasonable design choice is defensible. A well-written constraint makes some choices clearly better than others, which is what design decisions actually require.

A scenario is one paragraph, present tense, third person. Five elements in sequence: who (brief, relevant context), what triggered this (what happened today that brought them here), what they're trying to do (their goal in their terms), what constraint complicates it (the thing that makes this harder than ideal), what success looks like for them (not product success — their success).

**The move:** Write the one paragraph answering all five elements for the primary user situation your current work addresses. If question 4 (the constraint) stops you, that's the part of the context you don't yet know — and that gap is the finding.

**Don't confuse a scenario with a persona.** A persona is a general description of a user type. A scenario is a specific situation. A false positive: a persona with detailed biographical information (job, goals, frustrations) feels specific enough to design from. But "senior operations manager who values efficiency" doesn't tell you whether she's trying to do this on her phone during a meeting break or on a laptop with four hours to focus — and that difference changes the design.

**Try Noticing:** Take a recent design or test decision. Is there a scenario behind it — a specific situation with a specific constraint? If not, what is the decision actually optimizing for?

**What Next:** If the scenario is for testing, take it to 215a (Moderated Usability Session) where it becomes the task context. If it's for design, use it to pressure-test a storyboard (127) or early wireframe. If the "who" in your scenario is still vague, read 301 (From a Vague Ask to a Real Persona).
