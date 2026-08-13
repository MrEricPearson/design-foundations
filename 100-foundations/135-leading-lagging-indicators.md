# Leading vs. Lagging Indicators
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 113 | **Episode:** 12

**Goal:** Recognize when a success metric only tells you what happened after the fact — so you can identify an earlier signal that lets you catch a problem before it ships.

**Concept:** The working assumption is that measurement happens after release — you ship, you measure, you learn. The correction: most post-release metrics are lagging indicators, and lagging indicators arrive too late to prevent the failure they're measuring. The mechanism: a lagging indicator is an outcome measured after the outcome has occurred — task completion rate, error rate, NPS, retention. These are valid and necessary, but they report on what already happened. By the time a lagging indicator reveals a problem, the problem is already in production. A leading indicator is a signal that appears earlier in the development cycle and predicts the later outcome. It doesn't guarantee the outcome, but it creates a decision point before the cost of being wrong is highest.

The practical value: a leading indicator turns "we found out it was broken after we shipped" into "we found the signal during development and changed the design." That shift is what makes the indicator worth identifying before the work is done.

Leading indicators live in places like: hesitation during a usability session, "what does this mean?" questions during demos, difficulty completing a task that should be easy, or consistent confusion at the same screen across multiple participants. Each is a signal that something may not survive contact with real users at scale.

**You'll see it when:** A team defines success only in post-release terms ("we'll know it worked if the metric improves"). When a usability session surfaces problems that make the team say "we already knew about that" — the session found what everyone suspected but no one flagged as a decision point.

**The signal:** The only way the team will know if a design decision worked is to wait until after it ships. No earlier signal has been identified.

**Don't confuse a leading indicator with a prediction.** A prediction claims to know the outcome. A leading indicator identifies a signal that, if it fires, creates an obligation to investigate before shipping. A false positive: a usability session that produces no hesitation or confusion feels like a validated design. But if the session used participants who were familiar with the product, or tasks that were simpler than real use cases, the absence of a signal doesn't confirm the design is ready — it confirms the session wasn't designed to surface problems.

**Try Noticing:** Name the primary success metric for something you're currently working on. Ask: if this is going to fail, what would you see first — during development, before shipping? That signal, identified with a threshold, is your leading indicator.

**What Next:** Once you have both leading and lagging indicators, read 217 (UX Metrics) to formalize the lagging one using a recognized framework. To track decisions made against these indicators over time, read 209 (Design Decision Records).
