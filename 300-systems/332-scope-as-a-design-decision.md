# Scope as a Design Decision
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Cross-audience | **Prereqs:** 100 (Assumption vs. Fact), 107 (Framing the Problem), 109 (Weighing Tradeoffs), 110 (Constraints as Design Input), 113 (Defining Success Before You Start), 249 (Loss Aversion), 253 (Sunk Cost Fallacy)

**Goal:** Make scope decisions with the same rigor as design decisions — by recognizing scope as the primary lever for shipping something that works for users, evaluating cuts against user impact rather than feature completeness, negotiating scope changes with explicit evidence, and documenting scope boundaries so they can be revisited when conditions change.

**Trigger:** A feature is in development and scope has expanded incrementally until the whole feature is at risk of being late. Or: scope cuts are being made under deadline pressure without evaluating their user experience consequences. Or: the question "what can we cut?" produces a list of things nobody wants to be responsible for cutting. Scope is being managed as a schedule problem rather than a user experience decision.

---

## Part 1 — What Scope Actually Controls

**Concept:** Scope controls two things simultaneously: what gets built and what users experience. These are usually treated as equivalent, but they're not. Building 80% of a feature that produces a complete and coherent user experience for the primary use case is different from building 80% of a feature that produces a broken or incomplete user experience for the primary use case. The first 80% is a scope cut that protects the user. The second 80% is a scope cut that doesn't.

The distinction requires knowing which 80% to build. That requires a clear model of the user's primary use case, a definition of what "complete" means for that use case, and an evaluation of scope options against that definition. Scope cuts made without this model produce features that are technically complete but experientially incomplete.

**Method:**
Before any scope discussion:
1. Write the primary use case: the specific user, the specific situation, the specific outcome they need to reach
2. Write the minimum coherent experience for that use case: what's the smallest set of capability that produces a complete, useful experience for this user in this situation? Not everything in the spec — just enough for the primary use case to work end-to-end
3. Evaluate the current scope against the minimum: what in the current spec is required for the primary use case? What is enhancement beyond it? What is a different use case entirely?
4. Name the scope explicitly: "the minimum scope is X; current scope is Y; the difference is Z"

**What you end up with:** A scope map that distinguishes between what's required for the primary use case and what extends beyond it — which is the foundation for scope cut decisions that protect user experience.

**Proof:** If a scope cut would break the primary use case, it's not a scope cut — it's a different feature. Naming this distinction before cutting prevents the mistake of shipping something that technically "exists" but doesn't serve its intended purpose.

**Watchout:** The minimum coherent experience is not the minimum viable product in the sense of "whatever we can get out the door." It's the minimum that serves the user's goal without leaving them in a worse state than before the feature existed. A feature that partially exists and partially fails is sometimes worse than no feature, because it creates user expectations that aren't met.

---

## Part 2 — Evaluating Scope Cuts by User Impact

**Concept:** Scope cuts under deadline pressure tend to happen by convenience: what's easiest to cut, what hasn't been started, what doesn't have a vocal stakeholder defending it. The result is scope decisions made by availability and organizational dynamics rather than by user impact. A capability that happens to be technically difficult to cut may survive, even if users rarely need it. A capability that's easy to cut may be removed, even if it's critical for a significant user segment.

User-impact evaluation reverses the order: identify which scope items have high user impact first, then evaluate the technical and organizational cost of keeping them. Items with high user impact and low cut cost stay. Items with low user impact and high keep cost are candidates for cutting. The sequence — user impact first, then cost — is what makes scope decisions defensible.

**Method:**
For each item in a scope cut conversation:
1. Write the user impact of removing it: which user(s) would be affected, in what scenario, what would they lose access to, is there an alternative path?
2. Classify user impact: High (required for primary use case or significant secondary use case, no alternative path), Medium (improves the experience for a meaningful user segment, workaround exists but is worse), Low (edge case, nice-to-have, or has a functional alternative)
3. Classify cut cost: Low (can be removed cleanly, no dependencies), Medium (requires rework but manageable), High (significant rework or creates technical debt)
4. Apply the matrix: High user impact = keep regardless of cut cost; Medium user impact = keep if cut cost is Low, evaluate carefully if Medium, cut if High; Low user impact = cut if any cut cost exists

**What you end up with:** A scope cut decision for each item that's based on user impact before cut cost — so the resulting scope prioritizes the experience users need rather than what happens to be easiest to keep or cut.

**Proof:** A scope cut conversation that produces mostly Low user impact cuts and preserves High user impact items is working. A scope cut conversation that produces cuts across user impact levels — removing some High user impact items because they were inconvenient to defend — isn't.

**Watchout:** User impact classification requires knowing who the users are and what they need. If the primary use case wasn't written before the scope cut conversation (Part 1), user impact classification defaults to whoever in the room has the most intuition about users — which may or may not be accurate.

---

## Part 3 — Negotiating Scope With Evidence

**Concept:** Scope negotiation without evidence is a social negotiation — whoever argues most persistently or has the most authority tends to win, regardless of user impact. Scope negotiation with evidence is a different conversation: the question is not "what do you want to keep" but "which scope decisions are supported by what we know about users?" Evidence changes the nature of the negotiation from preference to reasoning.

The evidence in scope negotiation is not always research data. It can be: user stories that make the scope item concrete, an observation from a user session, a pattern in support tickets, a scenario that makes the user impact real. The goal is to make the user's perspective present in the conversation rather than abstract.

**Method:**
For scope items with contested classification (High vs. Medium user impact, or different stakeholders with different views):
1. Make the user scenario concrete: write a brief scenario (two sentences) that makes the user's situation vivid — who they are, what they're trying to do, what happens to them if this scope item is cut
2. Ask: "If we remove this, what does a user in this scenario do?" — name the alternative path or the absence of one
3. If there's disagreement about whether the scenario is representative: ask "what would we need to know to settle this question?" — this converts the scope disagreement into a research question, which is a different conversation than a preference disagreement
4. For items where the scenario can't be written: the scope item doesn't have a clear user need attached to it — which is itself a signal about whether it belongs in scope

**What you end up with:** A scope negotiation that's grounded in user scenarios rather than stakeholder preferences — where evidence settles disputes that would otherwise be resolved by authority or volume.

**Proof:** A scope negotiation that produces decisions connected to user scenarios is using evidence. A scope negotiation that produces decisions connected to stakeholder preferences or delivery constraints isn't — even if it arrives at the right answer.

**Watchout:** Scenarios can be manufactured to defend scope items rather than illuminate user need. The test is whether the scenario represents a real user doing a real thing, or a hypothetical constructed to justify keeping a preferred feature. The difference is usually visible in whether the scenario is specific ("someone who just transferred from another division and is setting up their access for the first time") vs. generic ("a user who needs this").

---

## Part 4 — Documenting Scope Boundaries and Their Rationale

**Concept:** Scope decisions made without documentation become invisible. Three months after a feature ships, nobody remembers which scope items were cut and why — which means the cuts get rediscovered by users, reopened by stakeholders, or re-debated in the next planning cycle without the benefit of the original reasoning. Documented scope boundaries create continuity: the cuts that were made, the user impact that was evaluated, and the conditions under which the cuts should be revisited.

Documentation also creates accountability for the "out of scope" designation. An item that's marked "out of scope for v1, revisit if [condition]" is different from one that's simply omitted. The former has a named condition for return; the latter disappears indefinitely.

**Method:**
After any significant scope decision:
1. Write what's in scope: the primary use case the feature serves and the minimum coherent experience it provides
2. Write what was cut and why: each scope item that was removed, the user impact classification that justified the cut, and the alternative path users have (if any)
3. Write the conditions for revisiting cuts: for each High-impact cut, name the trigger that would cause it to be re-evaluated — a launch milestone, a user feedback threshold, a specific future capability
4. Write what the scope decision assumes: the user population for which this scope is sufficient, the future state where deferred items will be addressed, the alternative paths that make the cut acceptable

**What you end up with:** A scope decision record that can be referenced when a cut item resurfaces, when users report the absence, or when the next planning cycle asks what to prioritize.

**Proof:** Six months after launch, someone can check the scope decision record to see why [specific capability] wasn't included and what would need to be true for it to be added. If that answer isn't in the record, the scope decision wasn't documented.

**Watchout:** Scope decision records are planning artifacts, not contracts. If conditions change — if a cut item turns out to be more impactful than assessed, or if the conditions for revisiting arrive earlier than expected — the record should be revisited and updated, not treated as permanent.

---

**Try This:** Take a feature currently in development that has more scope than the timeline can support. Apply Part 1 (write the primary use case and minimum coherent experience). Then apply Part 2 (classify each scope item by user impact and cut cost). What does the matrix suggest about which items to protect?

**Take This Further:** In the next planning cycle, try applying Part 3 to one scope disagreement: write the user scenario for the contested item before the negotiation. Write one sentence afterward: did making the user scenario concrete change the conversation?

**Judgment Exercise:** Your scope cut analysis has identified three items as High user impact — things users genuinely need to accomplish the primary use case. Keeping all three will put the launch at risk by two weeks. Cutting one would protect the timeline but create a meaningful gap for a specific user segment. The pressure to launch on time is significant. What do you decide, how do you document it, and how do you communicate the gap to affected users?

**What Next:** 317 (From a Vague Ask to a Solvable Problem) for defining the problem clearly enough that scope decisions are grounded. 330 (From Findings to Decisions) for making the user impact assessments that scope decisions depend on.
