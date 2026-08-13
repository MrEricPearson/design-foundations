# Jobs-to-Be-Done
**Tier:** 100 — Recognize (Practice Atom) | **Arc:** Standalone | **Prereqs:** 107 | **Episode:** 3

**Goal:** Recognize when a requirement describes what to build instead of why someone needs it — and reframe it as a job statement that names the situation, goal, and context that makes the feature worth building.

**Concept:** The working assumption is that user needs are feature requests: "users need a search function," "users want to export to CSV." The correction: features are responses to jobs, and a feature designed without reference to the job it's responding to can satisfy the requirement while missing the actual need. The mechanism: every feature serves a situation — a context in which someone finds themselves and needs an outcome they can't currently produce. A feature specified as a function (what it does) can be substituted by any feature that does the same function. A feature specified as a job (the situation, goal, and outcome) can't be substituted as easily, because it has to fit the specific context of the person's situation, not just match a capability.

The job has three layers, each adding constraint that the functional layer alone can't provide:
- **Functional**: *When I [situation], I want to [action], so I can [outcome].* The visible need.
- **Social**: *How does this person want to be seen as a result of this?* What successful use signals — about competence, efficiency, care.
- **Emotional**: *How do they want to feel?* Relief, confidence, control, not being embarrassed. The internal state the successful outcome enables.

A feature that addresses only the functional layer is easy to substitute. One that addresses all three is much harder to replace.

**The move:** Take one requirement in your current work. Write the three-layer job statement for it: functional → social → emotional. Where the social and emotional layers are unclear, that's the part of the context you don't yet have.

**Don't confuse the job with the solution.** "I need a faster dashboard" is a feature preference. "When I'm presenting progress to a client, I want to pull live data without waiting, so I can demonstrate responsiveness without preparation" is a job — it names the situation and what successful use enables. A false positive: a well-written user story ("As a user, I want to export data, so I can share it with my team") fills the functional layer and still misses the job. The situation (what triggers the need?) and the social context (what does sharing with the team enable?) aren't in the story.

**Try Noticing:** Look at one requirement or ticket in your current work. Can you write the three-layer job for it — functional, social, emotional? Notice which layer is hardest to write: that layer represents the context you know least well about the person you're designing for.

**What Next:** To connect the job to a specific user, read 301 (From a Vague Ask to a Real Persona) — JTBD tells you why, personas tell you who. To use the job statement as the basis for a problem framing, read 107 (Framing the Problem).
