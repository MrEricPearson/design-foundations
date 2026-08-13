# Sample Size and What It Means
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 244, 245 | **Episode:** 11

**Goal:** Recognize what "enough" participants means for qualitative versus quantitative research — so you can stop using qualitative sample size to make quantitative claims, and stop running larger qualitative studies than the method requires.

**Concept:** The working assumption is that bigger samples are always more reliable. The correction: reliability is measured relative to the question being answered. For qualitative research, the relevant threshold is saturation. For quantitative research, the relevant threshold is statistical power. These are not the same standard and cannot be applied interchangeably.

**Qualitative sample size — saturation:**
Qualitative research identifies mechanisms: the patterns of confusion, the sources of motivation, the moments of trust or doubt. Mechanisms saturate — after a sufficient number of participants who fit the research context, new participants stop surfacing new mechanisms. They produce familiar patterns in new contexts.

The classic finding in usability research (Nielsen, 1993) is that five participants identify approximately 85% of usability problems in a product that has a consistent interaction paradigm. This is not a universal rule — it is a property of mechanism saturation in usability contexts. More participants catch more problems, with diminishing returns after the first few. The appropriate sample for a qualitative study is enough participants to reach saturation — typically 5–12 in most UX contexts, with variation based on participant diversity and topic breadth.

Running a qualitative study with 50 participants does not produce quantitative data. It produces a large qualitative sample — richer, more diverse, more confident in mechanisms — but not statistically representative of the full user population.

**Quantitative sample size — statistical power:**
Quantitative research identifies magnitude and frequency. Statistical power determines the minimum sample needed to detect a real effect of a given size with a given confidence level. Power calculations are specific to the research design: a simple A/B test of a major change needs fewer participants than a test designed to detect a 2% conversion difference. Running fewer participants than the power calculation requires produces an underpowered study that may fail to detect real effects or produce false positive findings.

The standard threshold for statistical significance (p < 0.05) means findings at this level would appear by chance in 1 in 20 studies with null results — not that they are certainly true. Statistical significance is a threshold for reporting, not a guarantee of reality. Effect size and confidence interval matter alongside the p-value.

**You'll see it when:** A team conducts twelve interviews and reports that "40% of users experience X" — twelve is not a sufficient sample for a frequency claim. Or when a team runs an A/B test with 200 sessions and declares a winner — 200 may be severely underpowered depending on the baseline conversion rate and the expected effect size.

**The signal:** A frequency or percentage claim derives from a qualitative study. Or a quantitative study declares significance without reporting effect size and confidence intervals.

**Don't confuse this with:** Large qualitative samples being useless. A qualitative study with 20 participants provides richer, more confident mechanism findings than one with 5 — it just doesn't become statistically representative by virtue of its size. The claim that can be made changes with size; the type of claim that is appropriate doesn't.

**Try Noticing:** Look at the last frequency claim made from research in your current project ("X% of users..."). What was the sample size? What was the research method? If the method was qualitative (interviews, usability sessions), the percentage claim is not supported by that sample — identify what quantitative data would be needed to support it, and whether that data was actually collected.

**What Next:** This completes the quant/qual cluster. Return to 215a and 215b (Moderated and Unmoderated Usability) to re-read them with the sample size framing: what claims can the outputs of these methods support, and what claims require additional quantitative confirmation?
