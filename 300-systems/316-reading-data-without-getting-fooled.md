# Reading Data Without Getting Fooled
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Cross-audience (PM primary; applicable to all practitioners encountering analytics or research data) | **Prereqs:** 100 (Assumption vs. Fact), 135 (Leading vs. Lagging Indicators), 149 (Research vs. Anecdote), 261 (Correlation vs. Causation), 262 (Statistical vs. Practical Significance), 263 (Selection Bias), 264 (Survivorship Bias)

**Goal:** Evaluate a data finding at the level of a skeptical practitioner — not a statistician — so that you can identify what a number actually proves, what it doesn't, and what question to ask before it drives a decision.

**Trigger:** You're being asked to make product decisions based on analytics data, test results, or research findings — or to evaluate someone else's conclusions from that data — and you're not sure how much confidence the data actually supports. The analysis looks complete. The conclusion feels uncertain.

---

## Part 1 — What Your Dashboard Doesn't Know

**Concept:** Dashboards show co-movement between metrics. They do not show which metric caused which, or whether either was caused by what you think. System 1 produces causal stories automatically when it observes co-occurrence (261): feature X launched, retention went up, therefore feature X caused the retention increase. The dashboard confirms the timing. It cannot confirm the mechanism. And without a mechanism, the causal claim is an assumption that looks like a finding.

The additional complication: the most recent action is almost always available as a causal story, because it's the most salient event in S1's pattern-completion. A seasonal traffic increase, an unrelated behavior change in a different team's product, a change in the user population entering the funnel — any of these could produce the same metric movement and is invisible in a dashboard that only shows your product's metrics.

**Method:**
When a metric moves, before attributing it to your most recent action:
1. Name the most recent action and the observed metric movement — this is the hypothesis
2. Write three plausible alternative explanations that are NOT your most recent action: a seasonal pattern, a population shift, a third-party change, a confounding variable, a delayed effect from a prior action
3. For each alternative: what evidence would you need to confirm or rule it out?
4. Before attributing causation to your action, require that at least two of the three alternatives are specifically ruled out — not assumed away

**What you end up with:** A causal claim with named evidence, rather than a causal claim with confirmed timing.

**Proof:** If you can't produce three plausible alternatives, your knowledge of the system is insufficient to claim the causal story you're telling. If you can produce them but can't rule any of them out, you have a hypothesis, not a finding. The alternatives don't have to be likely — they have to be plausible. If one becomes more plausible than the original story, you have a better hypothesis.

**Watchout:** This method is not "never trust your data." It's "know what your data actually shows." A correlation that's been confirmed across multiple time periods, across different user populations, and with competing explanations ruled out, is a strong basis for action. The goal is not paralysis — it's a one-time shift in how you read dashboards, so you know which findings have causal support and which are well-confirmed correlations.

---

## Part 2 — Who's Missing From Your Data

**Concept:** Users who appear in your analytics are the users who stayed. Users who left before the analytics window are invisible. Power users who interact daily are overrepresented; first-time users who tried the product once and never returned are either absent or present as a single session. The data is real — it accurately describes the users it contains. The question is whether the users it contains are the users you want to know about (263, 264).

Survivorship bias is particularly persistent in product analytics because the filter operates silently: analytics tools don't label the users who aren't there. A 90-day active user retention report describes users who were active for 90 days. It tells you nothing about the users who left at day 15 — which may be exactly the population whose behavior you most need to understand to improve your product.

**Method:**
For any analytics finding, ask three questions before drawing conclusions:
1. "Who generated this data?" — what is the actual definition of the users or sessions in this dataset?
2. "How did they get here?" — what did they have to do, survive, or be selected for to appear in this data?
3. "Who is missing?" — which users, sessions, or behaviors would NOT appear here, and are they different on the dimension you're studying?

If the missing population would behave differently on the dimension being studied, name them explicitly and note that the finding applies to the present group but may not generalize.

**What you end up with:** A finding with a clear scope: "this is true for X type of user, based on Y dataset" — rather than "this is what users do."

**Proof:** If a finding is stated as "users do X" without qualification, the population hasn't been named yet. A scoped finding survives the question "which users?" with a specific answer. The working signal: if a non-technical colleague reads the finding and immediately asks "which users are you describing?" — the scoping wasn't in the finding. If they understand which users are described and why, the scoping is complete.

**Watchout:** Sometimes the survivors are exactly who you want to study. If you're improving the experience for retained users, studying retained users is correct — survivorship bias only matters when you're drawing conclusions about a broader population. The check is whether the conclusion is applied to the same population the data describes.

---

## Part 3 — What Test Results Actually Prove

**Concept:** "Statistically significant" is the most commonly misread phrase in product analytics (262). It means the observed difference is unlikely to be explained by random chance at the sample size tested. It says nothing about whether the difference is large enough to matter, nothing about whether the measurement instrument captured the right behavior, and nothing about causation. A large-enough sample will detect any nonzero difference as statistically significant — including effects so small they are irrelevant to user behavior or business outcomes.

Practical significance is the separate question: if this effect is real, does it matter? Does a 0.3% improvement in conversion change anything the product team should care about? Does a 2-second reduction in task completion time affect any user outcome you actually value? These are judgment calls, not statistical computations — and they require knowing what effect size would be meaningful in your context before you run the test.

**Method:**
For any test result:
1. Record the effect size, not just the significance level — what was the actual size of the observed difference, in absolute terms?
2. Apply the "would I notice this in daily life?" test: if the same proportional change appeared in something you measure regularly, would it be perceptible? Would it change behavior?
3. Check whether the metric tested is the one that matters — task completion time may be statistically improved while the task's actual outcome (a decision made, an object created, a process completed) is unchanged
4. Ask the pre-registration question: what effect size would we need to see to change our decision? If the bar was set before the test, apply it now; if it wasn't, set it now and note that it was set after seeing the data

**What you end up with:** A test result evaluated for both statistical validity and practical relevance — so the decision follows from what the result actually proves, not from the presence or absence of a p-value.

**Proof:** If the conversation after a test result focuses on whether to ship based on the significance level alone, practical significance was skipped. If the conversation includes "the effect is real, and the effect size is X, which means Y in user experience terms" — and Y is evaluated against a pre-stated threshold — the result is being applied correctly.

**Watchout:** Requiring large effect sizes before taking action is not the same as requiring statistically significant results. An underpowered test (too small a sample) may show a large, practically significant effect that doesn't reach significance because the uncertainty band is too wide. The right response is: run a larger sample, not "the effect doesn't exist." Statistical insignificance means the test couldn't detect the effect at this sample size. It doesn't mean the effect is zero.

---

## Part 4 — Better Questions for Your Analytics Tool

**Concept:** Most analytics tools answer the question you didn't ask. The gap is usually instrumentation: what's tracked wasn't designed to answer your actual question. Analytics tools record events and calculate metrics; they return answers to the questions their data model can support. If your question requires data that was never instrumented, the tool will return the nearest answerable question rather than telling you it can't answer yours — and the nearest answerable question may be far from the right one (135).

Funnel analysis tells you where users drop off, not why. DAU/MAU tracks who comes back, not what they came back to do. Session length measures time in product, not value derived. In each case, the metric is visible and real; the question it answers is a proxy for the question you actually need, and the gap between the proxy and the actual question is where bad decisions live.

**Method:**
Before opening an analytics tool to answer a question:
1. Write the specific question you need to answer, in user terms: "do users understand how to do X without prompting?"
2. Write what metric would directly answer it — ideally behavior, not a proxy
3. Check whether that metric exists and was instrumented for your purpose: is the behavior captured, is the population sampled correctly, is the event defined the way you need it?
4. If the metric doesn't exist or wasn't instrumented correctly: name the best available proxy and explicitly write the gap between the proxy and the real question
5. If the gap is large enough to change the decision: the data can't answer your question yet; name what you'd need to instrument to answer it, and make a decision on the proxy with acknowledged uncertainty

**What you end up with:** A clear record of what question was asked, what data was used to address it, and how large the gap is between the two — so the confidence of the decision matches the quality of the evidence.

**Proof:** A decision documented as "we made this choice based on X metric, which is our best proxy for Y behavior; the gap between X and Y is Z; we would reverse this decision if we saw evidence of Z" is more durable than a decision made from an unstated proxy. When the decision is revisited, the original reasoning is recoverable and can be evaluated rather than reconstructed.

**Watchout:** Waiting for perfect instrumentation before making decisions is equivalent to not making decisions. Every metric is a proxy for something harder to measure. The goal is knowing how good your proxy is — not eliminating the gap between proxy and reality, but knowing how much the gap should affect your confidence.

---

**Try This:** Take the last analytics finding that influenced a product decision in your context. Apply Part 1: write three alternative explanations for the metric movement that are not the action that was attributed to it. Then apply Part 2: who is missing from this data? Were either of these questions asked before the decision was made?

**Take This Further:** In your next three data-informed decisions, apply the Part 4 method before opening an analytics tool: write the question first, then identify the metric that would answer it, then check whether that metric exists. After the third: how often was the metric you needed already instrumented? What would you instrument if you could start over?

**Judgment Exercise:** Your dashboard shows a 23% increase in daily active users in the two weeks following a feature launch. Leadership wants to attribute the increase to the feature and scale investment in a similar direction. Before endorsing the attribution: what specifically would you need to know? Name at least two alternative explanations that cannot be ruled out from the dashboard alone. If the information needed to rule them out isn't available, what do you recommend as the next step — and what do you say to leadership in the meantime?

**What Next:** 217 (Usability Metrics) for designing measurement that answers design questions rather than usage questions. 135 (Leading vs. Lagging Indicators) for the foundational concept behind which metrics anticipate outcomes versus confirm them after the fact.
