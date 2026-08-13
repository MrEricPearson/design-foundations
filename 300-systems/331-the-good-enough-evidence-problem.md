# The Good-Enough Evidence Problem
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Cross-audience | **Prereqs:** 100 (Assumption vs. Fact), 101 (Not All Assumptions Are Equal), 103 (Attachment), 149 (Research vs. Anecdote), 247 (Dual Process Theory), 253 (Sunk Cost Fallacy), 330 (From Findings to Decisions)

**Goal:** Make decisions confidently from partial evidence — by recognizing when more evidence wouldn't change a decision, identifying when it would, distinguishing productive uncertainty from avoidance, and acting decisively on the evidence that exists while naming what remains open.

**Trigger:** Research was collected, findings are available, and the decision still isn't being made. Or: someone is calling for more research before acting, and it's not clear whether the call is a legitimate gap or a way to defer a decision that's difficult to make. Or: a decision was made with insufficient evidence and the consequences were predictable. The organization is either action-without-evidence or evidence-without-action — both are failures, and they require the same underlying skill to navigate.

---

## Part 1 — When More Evidence Would Change the Decision

**Concept:** The right question before commissioning additional research is not "do we have enough evidence?" but "what would the evidence need to show to change what we decide?" If there's no answer to the second question — if no possible finding would alter the direction — then additional research isn't informing the decision, it's deferring it. This is a critical diagnostic because research-as-deferral is functionally indistinguishable from research-as-evidence-gathering until you ask the question explicitly.

Research is appropriate when there's a specific question that the research could answer, the answer could plausibly change the direction, and the cost of getting the answer is less than the cost of being wrong. When none of these three conditions hold, research is a delay.

**Method:**
Before commissioning additional evidence:
1. Write the specific question the research would answer — not "we need more evidence about users" but "we need to know whether [specific user type] would complete [specific action] without [specific intervention]"
2. Write two possible answers to the question and the decision each answer would support: if the research shows X, we'll do A; if it shows Y, we'll do B
3. If you can't write the "if Y, we'll do B" answer — if every possible research outcome leads to the same decision — the research is not informing the decision. Name this explicitly and make the decision
4. If you can write the two-branch outcome: the research is appropriate. Specify the minimum evidence needed to answer the question and proceed

**What you end up with:** A clear test for whether additional research serves the decision or defers it — before the research investment is made.

**Proof:** If the two-branch outcome exercise produces "I guess we'd do A either way," the research isn't needed. If it produces genuinely different directions based on different outcomes, the research is load-bearing.

**Watchout:** The two-branch test can be gamed: it's possible to write a second branch that sounds like it changes the direction but would never actually be acted on. The test is whether you would genuinely do B if the research showed Y — not whether you can write a sentence describing B.

---

## Part 2 — Recognizing Evidence-Avoidance

**Concept:** Evidence-avoidance is the mirror image of evidence-deferral. Where evidence-deferral avoids decisions by calling for more research, evidence-avoidance avoids evidence by making decisions before evidence can question them. Both are driven by the same underlying mechanism: deciding feels more comfortable than uncertainty, and the method of avoidance depends on whether the person prefers action or process.

Evidence-avoidance presents as: making decisions before research is complete, dismissing findings that conflict with the preferred direction, selectively citing evidence that supports a predetermined conclusion, or moving forward so quickly that evidence would only arrive after the commitment is made. It's indistinguishable from genuine decisive action in the moment, which makes it harder to identify than evidence-deferral.

**Method:**
The diagnostic is not about motivation — it's about the process. Ask these questions after a significant decision is made:
1. Was evidence actively sought, or only considered when it arrived organically?
2. Were findings that conflicted with the direction explicitly considered, or were they noted and set aside without evaluation?
3. Could the decision have been made before any evidence was gathered? If yes — and no new evidence changed the direction — was there a genuine learning process or was evidence validation after the fact?
4. Were the residual unknowns (from 330 Part 4) named and monitored, or invisible?

Evidence-avoidance produces one specific diagnostic pattern: a decision with supporting evidence and no residual unknowns. Real decisions made under uncertainty always have residual unknowns. A decision where everything is confirmed and nothing is open is either unusually well-evidenced or evidence-avoided.

**Proof:** If a team can't name what evidence would have changed the decision they made, the evidence was gathered for validation, not for learning. That's evidence-avoidance, regardless of how much research preceded the decision.

**Watchout:** Some evidence-avoidance is appropriate — for low-stakes, reversible decisions, moving quickly and learning from outcomes is often better than slowing for research. The problem is evidence-avoidance on high-stakes, hard-to-reverse decisions where the cost of being wrong is significant.

---

## Part 3 — Acting Decisively on Partial Evidence

**Concept:** The goal is not to eliminate uncertainty before acting. That's impossible for most product and platform decisions — the world changes faster than research cycles, and complete certainty about complex human behavior is not achievable. The goal is to act decisively on the evidence that exists, with explicit naming of what remains uncertain, and with a monitoring plan for the residual unknowns.

Acting decisively from partial evidence is different from acting without evidence. The difference: acting without evidence is a bet on intuition; acting from partial evidence is a reasoned judgment that names its basis, its confidence level, and the conditions that would cause revision. The first is opaque; the second is transparent and correctable.

**Method:**
For any decision made from partial evidence:
1. State the decision clearly — what is being done, by when, and by whom
2. State the evidence basis — what findings support this direction, at what confidence level (from 330 Part 3)
3. State the key assumption — what would have to be true for this direction to be right? This is the residual unknown you're most dependent on
4. State the monitoring signal — what observable outcome would tell you whether the key assumption is holding, and how long you'll wait before checking?
5. Communicate all four elements to anyone who needs to understand or execute the decision

**What you end up with:** A decision that's explicit about its basis, its confidence, and its monitoring plan — so it can be executed confidently by the team and revised when evidence demands it.

**Proof:** A decision communicated with all four elements can be challenged productively: "I think the key assumption isn't right because..." or "the monitoring signal you've named won't actually tell us what we need to know because..." Those are good challenges. A decision communicated without them can only be challenged on whether the decision was right — a much less useful conversation.

**Watchout:** Naming uncertainty in public decisions requires a team culture that treats acknowledged uncertainty as competence rather than weakness. In environments where admitting uncertainty signals failure, practitioners avoid naming residual unknowns to appear more confident — which produces exactly the evidence-avoidance pattern from Part 2. This is a team culture problem; the practice is still right, but it may need to be introduced gradually.

---

## Part 4 — Calibrating Evidence Investment to Decision Type

**Concept:** Evidence investment should be calibrated to decision type, not uniformly applied. The calibration has two dimensions: reversibility (how expensive is it to change course after committing to this decision?) and scale (how many people are affected if this decision is wrong?). High-reversibility, low-scale decisions deserve minimal evidence investment. Low-reversibility, high-scale decisions deserve significant evidence investment. Most decisions fall between the extremes and require judgment about where on the spectrum they sit.

The failure mode on both ends: teams that apply their maximum evidence standard to every decision (slow, expensive, not competitive) and teams that apply their minimum evidence standard to every decision (fast, cheap, frequently wrong in costly ways). Calibration is the skill that matches evidence investment to decision consequences.

**Method:**
For any decision before determining evidence investment:
1. Estimate reversibility: if this decision is wrong, how long and how expensive is correction? (hours/days = High; weeks/months = Medium; quarters/permanent = Low)
2. Estimate scale: if this decision is wrong, how many users or stakeholders are materially affected? (< 20 = Low; 20-200 = Medium; > 200 = High)
3. Match evidence investment to position:
   - High reversibility, Low scale: move and monitor; formal evidence optional
   - High reversibility, High scale OR Low reversibility, Low scale: lightweight evidence (1-3 user sessions, one analytics review); document assumptions
   - Low reversibility, High scale: substantial evidence (multiple research methods, statistically meaningful sample); formal research investment appropriate

**What you end up with:** A calibration framework that matches evidence investment to decision consequences — preventing both over-investment and under-investment.

**Proof:** A team using this calibration will invest more in platform-level decisions that affect all users and are expensive to change, and less in feature-level decisions that affect a segment and can be reversed in a sprint. If both types of decisions receive the same evidence investment, the calibration isn't being applied.

**Watchout:** Reversibility is often overestimated. "We can just change it if it's wrong" is frequently true in theory and expensive in practice — because of stakeholder commitments made based on the decision, technical implementation that assumed it, and organizational momentum that built around it. When estimating reversibility, account for the social and organizational costs of reversal, not just the technical ones.

---

**Try This:** Take a decision that was made in the last month in your context that you now have some information about. Apply Part 1 retroactively: would different evidence have produced a different decision? If yes, was the evidence sought before the decision was made? If not, why not?

**Take This Further:** For the next three decisions you're part of, apply the calibration matrix from Part 4 to set the evidence investment level before research begins. Write one sentence after each: did the investment level match the decision's stakes? What would you calibrate differently?

**Judgment Exercise:** You're on a team that's calling for more research before acting on findings that have consistently pointed in the same direction across multiple sources. The research has been running for six weeks. The direction is clear. But someone influential is calling for one more study before committing. You believe this is evidence-deferral, not evidence-gathering. How do you engage with this situation, and what would it take for you to be wrong about your diagnosis?

**What Next:** 330 (From Findings to Decisions) for the structured process of converting findings into actionable recommendations. 319 (Lightweight Validation) for rapidly gathering the minimum evidence a decision needs.
