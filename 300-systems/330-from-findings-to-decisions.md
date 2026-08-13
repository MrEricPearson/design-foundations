# From Findings to Decisions
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Cross-audience | **Prereqs:** 100 (Assumption vs. Fact), 101 (Not All Assumptions Are Equal), 149 (Research vs. Anecdote), 244 (Qualitative vs. Quantitative Research), 316 (Reading Data Without Getting Fooled)

**Goal:** Convert research findings, user feedback, and data into actionable decisions — by distinguishing observation from interpretation, evaluating evidence strength against decision stakes, building a recommendation stakeholders can act on, and documenting what you decided and what you still don't know.

**Trigger:** You have findings — from a user session, an analytics review, a discovery conversation, a usability test — and you need to make a decision. Or: research was conducted but the findings are sitting in a document without a decision attached. Or: a recommendation was made but stakeholders asked "what's the evidence?" and the connection wasn't clear. The research happened; the decision-making didn't complete.

---

## Part 1 — Separating Observation From Interpretation

**Concept:** Every research finding has two layers: what happened (observation) and what it means (interpretation). These collapse in practice — people describe interpretations as if they were observations, and observations get reported with interpretations baked in. "Users were confused by the navigation" is an interpretation. "Seven of ten users clicked the back button within 5 seconds of arriving at the navigation page" is an observation. The distinction matters because observations are facts that multiple people can agree on; interpretations are hypotheses that can be correct or incorrect.

When interpretations are reported as observations, they resist challenge. "Users were confused" doesn't invite the question "how do you know?" in the same way "seven of ten clicked back" does. And interpretations-as-findings prevent the most important move in findings-to-decisions: evaluating whether the interpretation is the right one.

**Method:**
For any set of findings, before drawing conclusions:
1. Separate each finding into its observation component (what was seen or measured) and its interpretation component (what you believe it means)
2. For each interpretation: write the competing interpretation — what else could this observation mean?
3. Evaluate which interpretation is better supported: does the observation more strongly support your interpretation or the competing one? What additional observation would distinguish them?
4. Label findings explicitly: "Observation: [X]. Interpretation: [Y]. Alternative: [Z]. Confidence in interpretation: High / Medium / Low."

**What you end up with:** A findings set that's transparent about what was seen vs. what it's believed to mean — so recommendations built on it can be challenged at the interpretation level, not just the observation level.

**Proof:** If every finding in your research set is stated as a direct observation with no interpretation layer visible, either the research produced unusually clear findings or the interpretation has been silently collapsed into the observation. Research almost always requires interpretation; making it explicit is doing the work that the findings-to-decisions step requires.

**Watchout:** This step produces more uncertainty than collapsing observation and interpretation — that's the point. "Users were confused" is less honest about uncertainty than "we believe this behavior indicates confusion, but it might also indicate unfamiliarity." The additional uncertainty doesn't prevent decision-making; it produces better decisions by naming what's known and what's inferred.

---

## Part 2 — Evaluating Evidence Against Decision Stakes

**Concept:** Not every decision requires the same quality of evidence. A decision that affects 5 internal users and can be easily reversed requires less evidence than a decision that will be embedded in a platform affecting 5,000 users and will be expensive to change. Applying the same evidence standard to all decisions produces waste (over-evidencing low-stakes, reversible decisions) and risk (under-evidencing high-stakes, irreversible ones).

The calibration question: what's the minimum evidence quality needed to make this decision confidently given its consequences? This is different from "what evidence do we have?" — it's a standard applied before evaluating the evidence, not after.

**Method:**
Before evaluating evidence for a decision:
1. Name the decision stakes: what's the consequence if the decision is wrong? What does reversal cost? Who's affected?
2. Set the evidence threshold: for this decision's stakes, what minimum evidence level is needed? (One user session? Five usability sessions? A statistically significant A/B test? A multi-method research study?)
3. Evaluate the evidence you have against the threshold: does what you have meet the threshold? If yes, you can make the decision. If no, name what additional evidence is needed or make the decision explicitly under the threshold with that limitation stated.
4. For decisions made below the evidence threshold: document the assumption being acted on and the signal that would cause you to revisit

**What you end up with:** An evidence evaluation that's calibrated to the decision's consequences — preventing both under-investment in high-stakes decisions and over-investment in low-stakes ones.

**Proof:** If every decision gets the same evidence treatment regardless of stakes, the calibration isn't happening. The appropriate output is different evidence levels for different decision types — and explicit documentation of decisions made below the required evidence threshold.

**Watchout:** "We don't have enough evidence" can become a way to avoid making decisions. Evidence calibration is about setting the right threshold, not the highest possible threshold. Most product decisions can be made on less evidence than feels comfortable, provided the reversal path is clear.

---

## Part 3 — Building a Recommendation Stakeholders Can Act On

**Concept:** Findings don't automatically produce decisions, and decisions don't automatically produce action. A recommendation that stakeholders can act on makes three things explicit: what the findings show, what direction they support, and what specifically should happen next. Without all three, stakeholders either can't act (they agree with the findings but don't know what they're being asked to do) or won't act (they don't understand the connection between the findings and the recommended action).

The most common failure in translating findings to decisions is stopping at the findings summary: "users struggled with X" without "therefore we should Y" and "specifically, the next step is Z." The full chain — findings → direction → next step — is what makes research actionable.

**Method:**
For each key finding set:
1. **Findings summary:** what did you observe and interpret? (One sentence per key finding, using the separation from Part 1)
2. **Direction:** what does this finding support? Not a specific solution, but a direction — "this finding supports prioritizing improvements to the navigation before adding new features" or "this finding suggests the current approach to onboarding isn't landing for new users"
3. **Recommendation:** given the direction, what specifically should happen next? One specific next action that someone can own and execute
4. **Confidence:** how confident are you in this recommendation given the evidence quality from Part 2? High (evidence meets threshold), Medium (evidence is below threshold but direction is consistent), Low (evidence is weak; recommendation is a hypothesis to test, not a finding to act on)

**What you end up with:** A recommendation that connects findings to direction to next action — with a confidence level that tells stakeholders how much to weight it.

**Proof:** A stakeholder who reads the recommendation should be able to describe the specific action they're being asked to take and why. If the recommendation requires explanation to produce that understanding, it's a findings summary, not an actionable recommendation.

**Watchout:** Confidence labeling makes recommendations feel weaker. It doesn't — it makes them more credible by being honest about their basis. A High confidence recommendation from partial evidence is worse than a Medium confidence recommendation from explicitly limited evidence, because the High confidence claim will be discovered as overstated when someone questions the methodology.

---

## Part 4 — Documenting the Decision and What Remains Unknown

**Concept:** A decision made from research has two components: the decision itself and the residual unknowns it was made despite. Documenting only the decision produces a record that looks more confident than it was. Documenting both — the decision and the assumptions it carries — creates a record that's usable later: when the decision is questioned, when conditions change, or when the residual unknowns surface as real problems.

Residual unknowns are not failures. Every decision made before complete evidence is known will have residual unknowns. The question is whether they're named and monitored or invisible and discovered.

**Method:**
After a decision is made from research findings:
1. Write the decision: what was decided, when, and by whom?
2. Write the findings that supported it: which observations and interpretations were most influential?
3. Write the residual unknowns: what questions remain unanswered that would have changed the decision if we'd had the answers?
4. Write the trigger conditions: at what point would a residual unknown become significant enough to revisit the decision? What signal would tell you the assumption underlying the decision is wrong?
5. Assign ownership of monitoring the triggers: who is responsible for watching the signal that would cause a revisit?

**What you end up with:** A decision record that captures both the decision and its assumptions — creating a living document that can be revisited as conditions change, rather than a static record that ages without update.

**Proof:** A decision record is working when it can answer "why did we decide this?" and "what would cause us to change it?" If the second question can't be answered from the record, the residual unknowns weren't captured.

**Watchout:** Decision records grow stale. A decision record should be dated and include a review trigger, not just a monitoring trigger — if six months pass without any signal, someone should still check whether the decision remains appropriate.

---

**Try This:** Take the most recent piece of user research or data analysis that didn't clearly produce a decision. Apply Part 1 (separate observation from interpretation) and Part 3 (write findings → direction → recommendation). What decision does the research support, and why wasn't that conclusion drawn at the time?

**Take This Further:** Over the next three decisions made from research, write the residual unknowns from Part 4. After two months, check: which unknowns surfaced as real issues? Which didn't? What does that tell you about where to invest more evidence-gathering upfront?

**Judgment Exercise:** Your research produced clear findings from a small sample (three users) that strongly suggest a significant usability problem in your primary flow. The confidence in the interpretation is High (the behavior was unambiguous) but the confidence in the generalizability is Low (three users is not a representative sample). You have two weeks until launch. You can act on the finding and delay the launch, or you can launch and monitor. What do you do, and what do you document about the basis for your decision?

**What Next:** 316 (Reading Data Without Getting Fooled) for the data-literacy foundation that informs evidence evaluation. 319 (Lightweight Validation) for gathering additional evidence when the threshold isn't met.
