# From a Vague Ask to a Solvable Problem
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** PM-primary | **Prereqs:** 107 (Framing the Problem), 122 (Starting Questions), 125 (Jobs-to-Be-Done), 100 (Assumption vs. Fact), 101 (Not All Assumptions Are Equal)

**Goal:** Convert a vague incoming ask into a problem statement precise enough to act on — by distinguishing what was requested from what's actually needed, identifying the constraint that makes it hard, and producing a brief that development and design can execute against without re-asking the same questions mid-build.

**Trigger:** You've received a request — a feature ask, a stakeholder directive, a business complaint, a "can we just add X?" — and you can tell it describes a solution but not the problem. Or you've started discovery and the direction keeps shifting because no one has named what problem a good result would solve. The ask exists; the problem doesn't yet.

---

## Part 1 — Interrogating the Ask

**Concept:** Almost every incoming ask is a solution dressed as a request. "We need a dashboard" is a solution. "Users can't find the status page" is a problem. "Add a filter" is a solution. "Users are missing relevant records" might be the problem — or it might not be. The distinction matters because solutions baked into requirements prevent alternatives from being considered and lock in cost before the problem is understood. The working assumption is that the person making the request knows what they need. The correction: they know what they want, which is a proposed solution to a problem they may or may not have named accurately.

The mechanism: when someone experiences a frustration, their brain generates a candidate solution faster than they can articulate the underlying need. By the time it becomes a request, it has already been packaged as a specific intervention. The ask feels like the problem because it arrived as a proposed answer. Interrogating the ask means working backward from the solution to the situation it was meant to address.

**Method:**
For any incoming ask, before accepting it as a problem statement:
1. Write the ask as received: "we need X" or "can we add Y"
2. Ask: what would be different for the user or business if X existed? What can't they do now that they need to do?
3. Ask: what triggers this need? What situation is the person in when they need X?
4. Ask: is X the only way to solve that? If there were no cost or constraint, what would the ideal outcome look like — independent of X?
5. Write what you now believe the actual need is, separate from the proposed solution

**What you end up with:** A separation between the ask and the underlying need — which is the starting material for a problem statement.

**Proof:** If the underlying need you wrote in step 5 is the same as the ask in step 1, either the ask was already a problem statement or you haven't interrogated it yet. The interrogation worked when step 5 is different from step 1 in a meaningful way — broader, narrower, or differently framed.

**Watchout:** Interrogating the ask isn't arguing with it. If the underlying need turns out to support the original solution, the ask was probably right. The goal is to confirm or revise, not to reject.

---

## Part 2 — Testing the Problem Statement

**Concept:** A well-formed problem statement is testable: you can evaluate a proposed solution against it and determine whether the solution addresses the stated problem. A vague problem statement prevents evaluation — when you can't tell whether a solution is on-target, every solution looks equally valid and stakeholder preference fills the gap. Most problem statements fail one of three ways: they describe a symptom (low satisfaction scores) rather than a cause; they contain an implicit solution (users need a better way to find X); or they're so broad that almost anything would technically address them.

**Method:**
Once you have a candidate problem statement:
1. Apply the symptom test: does this describe an observable outcome (low usage, error rate, support tickets) or the reason for it? A symptom needs one more "why" — follow it until you reach something causal.
2. Apply the implicit-solution test: remove any reference to how the problem should be solved. Does the statement still make sense? If the framing collapses without a solution embedded in it, the problem isn't fully formed.
3. Apply the boundary test: would you know when this problem is solved? Write what "solved" looks like in observable terms. If you can't write it, the statement isn't specific enough to evaluate solutions against.
4. Revise until the statement passes all three.

**What you end up with:** A problem statement that is causal (not just symptomatic), solution-agnostic, and bounded enough to evaluate solutions against.

**Proof:** Hand the problem statement to someone not involved in the request and ask them to describe two possible solutions. If they can describe two genuinely different approaches, the statement is specific enough to constrain direction. If every solution they describe looks the same, the problem still has an implicit solution embedded.

**Watchout:** The problem statement isn't the same as a requirements document. It's one sentence to two sentences. Longer is usually a sign that multiple problems are being combined into one statement — which prevents focus.

---

## Part 3 — Finding the Constraint

**Concept:** Every problem has a reason it hasn't been solved yet. The constraint is the specific thing that makes the problem persist — the barrier between the current state and the desired state. Without naming the constraint, you're solving for the destination but not for the obstacle. A solution that doesn't address the actual constraint will produce a temporary fix that resurfaces, a workaround that migrates the problem, or a feature that goes unused because users still can't get past the thing that was in their way.

The constraint is almost never "we haven't built the solution yet." That's the absence of a solution. The constraint is something structural: users don't know the option exists, the process requires a step that breaks flow, the vocabulary in the product doesn't match the vocabulary users think in, the user doesn't know the outcome before they commit to an action.

**Method:**
For the problem you've now defined:
1. Describe the current state in user terms: what does a user in this situation actually do right now?
2. Describe the desired state: what would they do if the problem were solved?
3. Identify the gap: what's between those two states? What's the specific thing that prevents the move from current to desired?
4. Test whether the gap is addressed by the proposed solution: if the solution doesn't address the gap you named in step 3, the solution is solving a different problem than the one you defined.

**What you end up with:** A named constraint — the specific, testable thing a good solution must address.

**Proof:** When the constraint is well-named, you can evaluate a solution by asking "does this address the constraint?" without also needing to ask "is this the right problem?" Both questions should already be answerable.

**Watchout:** Some problems have multiple constraints. When this happens, pick the primary one — the one that, if removed, would make the others solvable or irrelevant. Trying to address all constraints at once in a single feature is a scope problem, not a problem-definition problem.

---

## Part 4 — The Brief

**Concept:** A problem brief is a single-page artifact that captures: the problem statement, the constraint, the measure of success, and the assumptions that are being made. Its purpose is to create a shared starting point for everyone who will work on the problem — including people who weren't in the conversation when the problem was defined. A brief that can be read in three minutes and produces shared understanding of what the work is for is the output that makes everything downstream more efficient and less likely to require restart.

Most products don't have briefs. They have tickets, which describe solutions; roadmaps, which describe sequences; and PRDs, which describe specifications. None of these replace a brief, because none of them answer the question: "What problem are we solving and how will we know when we've solved it?"

**Method:**
The brief contains four elements — write each as a single, direct statement:
1. **The problem:** one sentence, solution-agnostic, causal, bounded (output from Parts 1-2)
2. **The constraint:** what specifically is in the way — the barrier identified in Part 3
3. **The measure of success:** what observable outcome confirms the problem is solved — not a feature shipped, but a user behavior or business metric that would only change if the problem were actually addressed
4. **The key assumptions:** what has to be true for the problem to be real and the constraint to be correct? List the 2-3 assumptions that, if wrong, would invalidate the direction entirely

**What you end up with:** A one-page brief that can be handed to anyone who will work on this problem and produce the same shared understanding of what the work is for.

**Proof:** A brief is working when the team can evaluate candidate solutions against it without a PM in the room. If every solution review requires the PM to re-explain the problem, the brief isn't doing its job.

**Watchout:** The brief is a starting point, not a contract. As work begins, assumptions get tested and the problem statement may need revision. The brief should be revisited when significant learning occurs — not treated as immutable once written.

---

**Try This:** Take the most recent ask you received that felt vague or off-target. Apply Part 1 (interrogate the ask) and Part 2 (test the problem statement). Write a problem statement that passes the three tests. Then check: does the original solution request still address the problem you defined?

**Take This Further:** Over the next three briefs you write, bring the brief to the first design or development review. Write one sentence afterward: did the team need to re-ask questions the brief should have answered? If yes, which part of the brief failed — and what would you add?

**Judgment Exercise:** You've interrogated an ask and determined the actual problem is significantly different from what was requested. The stakeholder who made the request is senior and has already committed to the original solution publicly. Addressing the real problem would mean building something different from what was announced. How do you handle the gap between the defined problem and the committed solution — and what do you do if the stakeholder insists the original ask was correct?

**What Next:** 301 (From a Vague Ask to a Real Persona) for building the user model once the problem is defined. 311 (Psychology of Stakeholder Decisions) for the dynamics of the conversation when the defined problem contradicts what was requested.
