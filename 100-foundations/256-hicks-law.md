# Hick's Law
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 247, 133 | **Cluster:** J — Cognitive Science

**Goal:** Recognize when the number of options at a decision point is inflating decision time — so you can distinguish a comprehension problem from a choice architecture problem.

**Concept:** The working assumption is that more options equal more value — that users prefer having control, and that providing more choices respects their autonomy. The correction: decision time increases logarithmically with the number of options. This relationship is not linear: doubling options does not double decision time; halving options nearly eliminates it. System 1 is trying to match available options to a known pattern. When no pattern matches cleanly, S1 escalates to System 2, which is slow and effortful. The more options present, the more likely a clean S1 match fails, the more often S2 must engage, and the longer and more uncertain the decision becomes.

The mechanism: this applies whether the choices are items in a navigation menu, steps in an onboarding flow, features in a settings panel, actions in a toolbar, or options in a dialog. The relationship operates at the level of individual decision points — not the total number of features in a product, but how many options a user faces at any single moment. Removing 4 of 8 options doesn't halve decision time; it approaches eliminating it, because 4 options is within the range where S1 pattern-matching reliably succeeds without escalation.

**You'll see it when:** Users pause or hover over navigation menus with many items. Users abandon settings panels without completing a task. Research sessions show disproportionate time spent on a step that should be simple. The problem is attributed to confusing labels when the real issue is count — even correctly labeled options produce hesitation when there are too many of them at once.

**The signal:** Users can describe what they're trying to do but cannot identify where to start. The number of visible options at a single decision point exceeds 5–7. Reducing the number of options — not improving the labels — is the intervention that resolves hesitation.

**Don't confuse this with:** 238 (Progressive Disclosure), which is the design pattern for managing complexity across multiple steps. Hick's Law is the explanatory mechanism — why progressive disclosure works. The false positive: a user who eventually makes the right choice without help appears to have "succeeded." The excess decision time they spent is invisible in completion metrics but is real friction that accumulates across a session and compounds with each subsequent decision.

**Try Noticing:** Count the discrete options visible in one navigation element, settings panel, or dialog in a product you work with. If the count exceeds 7, that's the decision complexity, not the label quality. Now ask: which options do 80% of users need in this context? The remainder is contributing to decision time for every user in order to serve the edge cases of a few.

**What Next:** 260 (Decision Fatigue) for the related but distinct effect — not just how many options at once, but how decision quality degrades across many sequential decisions in a session. 238 (Progressive Disclosure) for the design pattern Hick's Law motivates. 314 (How People Actually Decide) for the arc that applies Hick's Law to meeting and presentation contexts.
