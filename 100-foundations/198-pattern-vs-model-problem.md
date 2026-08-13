# Pattern vs. Model Problem
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 197, 194 | **Note:** High-leverage diagnostic atom; prereq for 199; used in strategic design judgment arc (310)

**Goal:** After this piece, you will be able to recognize when a design problem needs a better solution — and when it needs a different question.

**Concept:** There are two fundamentally different types of design problem. In the first type, the underlying model is sound — the system knows the right things about the right things — and the problem is finding the best component, layout, interaction pattern, or flow to express it. Solving this type of problem produces a better implementation of the right structure.

In the second type, the underlying model is wrong — the system is organized around the wrong concepts, the wrong relationships, or the wrong level of abstraction — and the problem cannot be solved by any implementation, however skillful. Solving a model problem at the pattern level produces a well-designed interface to a fundamentally wrong structure. Users will still fail, and the design will be blamed for something the model caused.

The mistake: applying pattern-level solutions to model-level problems. This is the most expensive misdiagnosis in design work, because pattern solutions are concrete and feel like progress, while model problems are abstract and require a different kind of work. It is easier to design a better version of a broken screen than to question whether that screen should exist at all.

Four signals that distinguish a model problem from a pattern problem:

**Fragmentation**: Multiple screens are solving "similar but different" versions of the same thing. The similarity suggests they're the same concept. The differences are used to justify keeping them separate. When multiple screens require "similar but different" treatment, the question is: are these genuinely different things, or is this the model failing to recognize what they have in common?

**Manual bridge**: People are communicating manually — email, Slack, spreadsheets, meetings — to fill a gap the design doesn't fill. Manual bridging is almost always the sign of a concept the system should contain but doesn't. The manual work is doing what the model couldn't.

**Vocabulary divergence**: Different teams name the same thing differently. Vocabulary divergence marks concept fragmentation. If two teams have different words for the same underlying thing, the model is treating that thing as two things — with all the duplication and inconsistency that produces.

**Workaround tools**: Users have built shadow systems (spreadsheets, personal trackers, Slack channels used as databases) to do what the designed system doesn't do. These workarounds are the user's model of what they need. The gap between the workaround and the designed system is the gap between the user's model and the system's model.

**You'll see it when:** A product review surfaces the same problem repeatedly and the response is always a pattern-level fix — a better layout, a clearer label, a reorganized flow — and the problem persists in the next cycle. If the same underlying problem keeps returning despite pattern-level improvements, the problem is likely structural.

**The signal:** A design conversation that keeps circling back to the same user confusion, the same missing feature, the same workflow gap — despite multiple iterations of UI improvement. The recurrence is the signal that the fix is at the wrong level.

**Don't confuse a model problem with an implementation problem** — an implementation problem means the right model is present but badly expressed in the interface. An implementation problem gets better with design work. A model problem means the model is wrong. Design work makes a model problem worse, not better — it polishes something that shouldn't exist in its current form.

**Try Noticing:** Think of a design or system that has had multiple iterations without resolving the core user complaint. List the iterations: what did each change? If the changes were all at the pattern level — layout, flow, component choice — but the complaint persisted, consider: is the complaint actually about how the system presents information, or about what the system knows about? If the latter, you're looking at a model problem.

**What Next:** Recognizing a model problem is the diagnostic step. Acting on it — finding the concept that unifies the fragments, the name that unlocks the architecture, the structural change that resolves what pattern-level work can't — is the strategic judgment work covered in 199 (Transformation Within Constraints) and the Strategic Judgment arc (310).
