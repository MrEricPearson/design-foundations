# Mixed Methods
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 244 | **Episode:** 11

**Goal:** Recognize when a research question requires both qualitative and quantitative methods — and in which order — so you can design research that produces both the mechanism and the magnitude needed for confident decisions.

**Concept:** The working assumption is that mixed methods means running qualitative and quantitative research together and combining the findings. The correction: qualitative and quantitative research answer different questions and are most powerful in a specific sequence, not in parallel. The sequence is: qualitative first to identify what matters and why, quantitative second to confirm how much it matters and at what scale.

The mechanism: running quantitative research before qualitative means measuring things you've assumed matter rather than things you've verified do. A survey about the checkout experience measured against a scale you designed will produce numbers — but if the scale is built around assumptions about what drives satisfaction, the numbers will be precise measurements of the wrong variables. Qualitative research first identifies the actual variables: what users notice, what they trust, what confuses them, what makes them hesitate. Quantitative research then measures those specific variables at scale.

Running qualitative research after quantitative is also valuable — but answers different questions. Quantitative data produces patterns without explanations: abandonment spikes at a specific screen, satisfaction scores drop after a specific release, a feature is used by 30% of users rather than the expected 70%. Qualitative research run after quantitative diagnosis produces the mechanism: why that screen, why after that release, why 30% and not 70%.

The full mixed-methods pattern:
- **Qual → Quant:** Understand the mechanism first, then measure its frequency and magnitude. Used for designing new experiences, identifying what to build, and confirming that identified problems are large enough to prioritize.
- **Quant → Qual:** Identify the pattern first, then understand its mechanism. Used for diagnosing production problems, explaining unexpected metrics, and prioritizing where to investigate.

The research question determines which direction applies: "what should we build?" runs qual first; "why is this metric declining?" runs quant first.

**You'll see it when:** A team runs qualitative research to discover a problem and then needs to prioritize it against other problems — they need quantitative data to establish the problem's scale before committing resources. Or when production metrics surface an unexpected pattern and qualitative research is needed to explain it.

**The signal:** The research output produces findings that are rich in mechanism but thin on scale (qualitative-only), or rich in scale but thin on mechanism (quantitative-only), and decisions require both.

**Don't confuse this with:** Triangulation — using multiple methods to validate the same finding from different angles. Mixed methods in the sense used here is about sequencing complementary methods to answer complementary questions, not about confirming the same finding through redundant methods. A false positive: a research plan that includes both interviews and a survey looks like mixed methods. If the survey measures the themes the interviews identified, it is mixed methods done correctly. If the survey was designed independently of the interview findings, it's two parallel research efforts that don't benefit from each other's strengths.

**Try Noticing:** Look at your current research plan or the research being referenced in decisions on your current project. Is there a point where a qualitative finding needs quantitative confirmation before it can be prioritized? Or a quantitative pattern that needs qualitative investigation before the team knows what to do about it? That gap is where mixed methods applies.

**What Next:** Read 246 (Sample Size and What It Means) for how to calibrate the quantitative component of a mixed-methods plan — what "enough" looks like depends on what question the quantitative phase is answering.
