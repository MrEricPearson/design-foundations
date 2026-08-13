# Statistical vs. Practical Significance
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 100 (Assumption vs. Fact), 261 (Correlation vs. Causation) | **Cluster:** K — Data Literacy

**Goal:** Recognize when a test result is statistically significant but practically meaningless — and when the opposite is true — so you can ask the right question about data before it drives a decision.

**Concept:** The working assumption is that "statistically significant" means the result is real and meaningful — that it proves the effect is worth caring about. The correction: statistical significance means one specific thing: the result is unlikely to be explained by random chance alone, given the sample size and the observed difference. It says nothing about whether the size of the effect matters. A test with a very large sample will detect an effect so small it would never change a user's behavior. A test with a very small sample will miss a large effect entirely.

The mechanism: statistical significance is a function of three variables — the size of the effect, the sample size, and the variability in the data. Large samples shrink the uncertainty band around any observed difference, which means even tiny differences reach significance with enough participants. A 0.1% improvement in conversion can be "statistically significant" at p < 0.01 with a million-user sample. The test is valid. The math is correct. The finding may still be irrelevant to the decision you're trying to make.

Practical significance is a judgment call: would this effect size, if real, actually change anything a user does or anything the business cares about? A 0.1% conversion improvement may be real but insufficient to justify the maintenance cost of the change that produced it. A 20% improvement in task completion time may be practically significant even if it doesn't reach statistical significance because the sample was small.

**You'll see it when:** A test result is reported as significant with a percentage change that, on its own, wouldn't be noticeable to a user or meaningful to a business metric. The p-value is reported prominently without the effect size. A large-scale test is cited as "proving" something that a small-scale test would need to be much more dramatic to demonstrate.

**The signal:** The report leads with "statistically significant" or "p < 0.05" without naming the actual size of the effect and whether that size matters. The question "how much of a difference does this make in practice?" wasn't asked or answered. The decision to ship or not ship is based entirely on significance without any check on effect size.

**Don't confuse this with:** Statistical insignificance meaning no effect exists. An insignificant result in an underpowered test (too small a sample) means the test couldn't detect the effect, not that the effect doesn't exist. The false positive: a test that reached significance is treated as definitive proof, when it may have been large enough to detect small noise as significant. Both directions require the same check: what was the sample size, what was the effect size, and would the effect size matter if real?

**Try Noticing:** The next time a test result is presented, notice whether the effect size is named alongside the significance level. How large was the observed difference? If the same proportional difference appeared in something you measure in daily life — a 2% change in something you normally experience — would you notice it or care? If not, ask whether the practical significance matches the statistical conclusion being drawn.

**What Next:** 261 (Correlation vs. Causation) for the related concept — a statistically significant correlation is still not a causal claim. 316 (Reading Data Without Getting Fooled) Part 3 for the arc-level method on evaluating test results for both statistical and practical significance before they drive decisions.
