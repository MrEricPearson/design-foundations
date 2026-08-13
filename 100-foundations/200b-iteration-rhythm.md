# Iteration Rhythm
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 103, 105 | **Note:** Caps the testing/prototyping cluster; pairs with 200a; numbered 200b

**Goal:** After this piece, you will be able to recognize the difference between iteration that generates learning and iteration that generates motion — so you know when to continue iterating and when to ship or pivot.

**Concept:** Iteration has an implicit promise: doing it more times produces a better result. This is true when each iteration generates new information that changes the next version. It is false — and expensive — when each iteration makes modifications within a fixed set of assumptions without questioning those assumptions. The first is learning. The second is churn.

Here is the mechanism that distinguishes them: genuine iteration requires that each cycle ends with an explicit statement of what was learned and how it changes the next cycle. "We tested version 3. Users completed the primary task successfully. We learned that the secondary path caused confusion for users who hadn't completed setup first. Version 4 will gate the secondary path behind setup completion." That is iteration. "We tested version 3. The stakeholder wanted the header redesigned. Version 4 changes the header." That is modification — valuable if the stakeholder's reaction reflects real evidence, an infinite loop if it doesn't.

The three states iteration can produce:

**Iterate**: new information changes the next version, and the question it answers is still open. Testing continues.

**Ship**: the question is answered. Evidence supports the current direction. The cost of additional testing exceeds the expected benefit of further learning.

**Pivot**: the question was answered, but the answer was "this direction doesn't work." The concept, flow, or approach needs to change — not the implementation. Continuing to iterate on the wrong direction is the most expensive form of churn.

The signal that distinguishes iterate from pivot: if each iteration reveals a new problem in the same underlying area — a different expression of the same user confusion, a different failing of the same structural assumption — the problem is structural. Iteration can't fix a structural problem. The pivot is to address the structure.

**You'll see it when:** A team has been in an "iteration" loop for multiple cycles and the design feels like it's not converging — each cycle resolves something and introduces something else. If the "something else" is a new class of problem (not a refinement of a previously identified problem), the design may be addressing symptoms of a structural issue rather than the issue itself.

**The signal:** An iteration review where the retrospective note is "we fixed the header but now the footer is the problem" — and on reflection, header and footer are expressions of the same underlying issue. The problems are moving, not resolving.

**Don't confuse iteration with refinement** — refinement is the execution-quality improvement cycle that happens after a validated direction is confirmed: polish the visual design, tighten the copy, fix edge cases. Iteration is the validation cycle that runs before the direction is confirmed. These happen at different phases. Treating refinement as iteration (running user tests on visual polish questions) generates the wrong kind of feedback. Treating iteration as refinement (making visual improvements to an unvalidated concept) delays the learning that iteration is designed to produce.

**Try Noticing:** Look at your current or most recent design work. How many iteration cycles has the current design been through? For each cycle: what was learned, and how did the learning change the next version? If you can't answer "what was learned" for a given cycle, it may have been a modification cycle rather than an iteration cycle. That's a flag — not necessarily a problem, but a signal that the iteration discipline wasn't running.

**What Next:** Knowing when to ship comes down to knowing what the design was trying to prove and whether you've proved it. Read 113 (Defining Success Before You Start) if that baseline wasn't established at the beginning. If iteration has surfaced a structural problem — something that can't be resolved by further implementation improvement — read 198 (Pattern vs. Model Problem) for how to recognize it and 310 (Strategic Design Judgment) for what to do.
