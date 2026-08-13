# Running the Platform Like a Product
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Non-Custom Dev / Platform / Configuration primary | **Prereqs:** 100 (Assumption vs. Fact), 113 (Defining Success Before You Start), 135 (Leading vs. Lagging Indicators), 149 (Research vs. Anecdote), 125 (Jobs-to-Be-Done), 250 (Status Quo Bias), 313 (UX in a Product You Didn't Build)

**Goal:** Apply product thinking to platform management — by treating users of the platform as customers with real needs, defining success metrics that track outcomes not activity, gathering signal systematically rather than reactively, and making configuration and change decisions with the same rigor as product decisions.

**Trigger:** Platform changes are made based on support tickets and squeaky wheels rather than systematic signal about what users actually need. Or: success is measured by uptime and ticket count rather than by whether users are accomplishing their goals on the platform. Or: the platform team is reactive — always solving the last problem reported — rather than proactive about where friction is building. The platform exists; the users are on it; but it's being managed as infrastructure rather than as a product.

---

## Part 1 — Defining Success for a Platform

**Concept:** Infrastructure success metrics (uptime, response time, ticket volume) measure whether the platform is running. Product success metrics measure whether the platform is working for its users. These are not the same, and optimizing for the first does not guarantee the second. A platform with excellent uptime and low ticket volume may still be failing its users — if users have stopped trying to do things that the platform doesn't support well, ticket volume drops not because the platform improved but because users stopped escalating.

Platform success from a product perspective looks different: are users able to accomplish their goals efficiently? Are adoption rates for key capabilities growing? Are users who are new to the platform able to onboard to productivity within a reasonable window? Are there repeated patterns in support requests that indicate systematic gaps rather than individual edge cases?

**Method:**
For the platform you manage, define success at three levels:
1. **Operational success:** the platform is available and performing — uptime, error rates, response times; necessary but not sufficient
2. **Adoption success:** users are actively using the platform's core capabilities — adoption rate, feature usage, active user trends; signals whether the platform is being used as intended
3. **Outcome success:** users are accomplishing their goals on the platform — task completion rate, time-to-productivity for new users, reduction in support escalations for core workflows; signals whether the platform is working as intended

Write at least one metric for each level. If you can only measure level 1, name it explicitly — you're optimizing for operational health without visibility into whether the platform is working for users.

**What you end up with:** A success definition that goes beyond infrastructure health and includes signals about whether users are achieving their goals.

**Proof:** If your platform was at 100% uptime last quarter and you can't answer "what percentage of users successfully completed their most common task without a support request," you're measuring level 1 only.

**Watchout:** Outcome metrics are harder to measure than operational metrics. That's not a reason to ignore them; it's a reason to find proxies. Support ticket patterns, user survey responses, and a quarterly "can a new user complete Task X without help?" test can all approximate outcome success without requiring sophisticated instrumentation.

---

## Part 2 — Gathering Signal Systematically

**Concept:** Reactive platform management responds to what users report. Proactive platform management actively seeks signal about where friction is building — including friction that users aren't reporting because they've worked around it, accepted it as normal, or given up trying. Silent friction is the category that reactive management misses: problems that exist but don't generate tickets because users have adapted to them.

Systematic signal gathering fills the gap. It's not about collecting more data; it's about collecting data that reveals what reactive management can't see: where users are working around the platform instead of with it, what they're not using that they should be, and where new users struggle before they've learned the workarounds.

**Method:**
Establish a systematic signal cadence:
1. **Monthly review of support ticket patterns:** don't just count tickets — categorize them by task or workflow. Tickets that repeat across multiple users on the same task indicate a systematic platform gap, not individual user error
2. **Quarterly new-user observation:** once per quarter, watch a new user attempt to complete the 3 most common platform tasks without assistance. Note every point of confusion or help request. This surfaces friction that experienced users have adapted to and no longer notice or report.
3. **Semi-annual user survey:** two questions: "Is there something you need to do on this platform that you currently do some other way?" and "What's the most friction you encounter in a typical week?" The first question reveals workarounds; the second reveals friction users have normalized
4. **Ad hoc signal from change requests:** when users request new features or configuration changes, log the underlying need (the goal they're trying to accomplish), not just the specific request (the proposed solution). Pattern-matching on underlying needs reveals systematic gaps faster than feature request tallies

**What you end up with:** A systematic signal picture that includes the friction users are reporting and the friction they've stopped reporting.

**Proof:** If your signal sources are limited to support tickets and change requests, you're seeing only what users chose to escalate. The quarterly new-user observation and the workaround survey question are the two practices most likely to reveal what reactive management misses.

**Watchout:** Systematic signal gathering has a minimum useful frequency. A new-user observation done once and never repeated shows a snapshot, not a trend. Quarterly is frequent enough to catch regression in new-user experience as the platform evolves.

---

## Part 3 — Making Configuration Decisions Like Product Decisions

**Concept:** Platform configuration decisions have user experience consequences that are structurally identical to product feature decisions: they determine what users can do, what they see, and how they accomplish their goals. But configuration decisions are often made casually — a setting is changed because someone asked for it, or because it seemed like a reasonable default, or because the previous configuration was causing a specific issue. The absence of a structured decision process means that configuration decisions accumulate without a coherent user experience rationale.

Applying product decision discipline to configuration means treating configuration changes the same way product teams treat feature decisions: write the user need driving the change, identify who's affected, evaluate tradeoffs, and document the decision.

**Method:**
For any non-trivial configuration change:
1. Write the user need: what does this configuration change accomplish for users? Who specifically? In what situation?
2. Identify affected users: will this change affect all users, or a subset? Will it help some users and create friction for others?
3. Evaluate tradeoffs: what does this configuration make possible that wasn't possible before? What does it constrain or change? Are there users for whom the change is neutral or negative?
4. Document the decision: what was changed, why, who it affects, and what signal you'll use to evaluate whether it accomplished the goal — this is the "Design Decision Record" (209) applied to configuration

**What you end up with:** A configuration decision record that provides rationale for every non-trivial change — so "why is it configured this way?" has a specific, findable answer.

**Proof:** If you can answer "why is [specific configuration] set the way it is" with a specific user need and a documented rationale, the process is working. If the answer is "it was always that way" or "someone asked for it once," the configuration decision record isn't being maintained.

**Watchout:** Not every configuration change requires this level of rigor. The threshold for a structured decision: changes that affect a significant portion of users, changes that constrain something users could previously do, and changes that are hard to reverse. Small, easily-reversed changes to low-traffic configuration can be made informally with a brief log.

---

## Part 4 — Proactive Platform Improvement

**Concept:** A platform managed reactively gets better at solving past problems. A platform managed proactively gets better at solving problems before they become widespread. The distinction is in where attention is directed: reactive management directs attention at what has already failed; proactive management directs attention at where failure is becoming more likely as the platform evolves.

Proactive improvement requires a different kind of attention: regular review of signal trends rather than point-in-time issue response, evaluation of upcoming platform changes for their user experience consequences before they ship, and deliberate investment in the friction areas that systematic signal reveals.

**Method:**
Build a proactive platform improvement rhythm:
1. **Quarterly platform review:** review the systematic signal from Part 2 across the last quarter; identify the top 3 friction areas based on signal; write one improvement target for each with a success metric
2. **Pre-change review:** before any significant platform change (major version upgrade, new feature rollout, configuration change affecting many users): apply the mental model fit check from 313 (UX in a Product You Didn't Build) to predict user impact before the change ships
3. **Improvement backlog:** maintain a list of known platform friction areas with user impact assessment; prioritize this backlog the same way you'd prioritize a product backlog — by impact and effort, not by recency of complaint
4. **Communicate platform changes:** when making improvements, tell affected users what changed and why — not just a release note, but a brief communication that acknowledges what was hard before and what's better now; this converts platform improvements into trust-building moments

**What you end up with:** A proactive improvement process that addresses friction before it becomes widespread and builds user trust in the platform as something that gets better over time.

**Proof:** A platform managed proactively has a known improvement backlog — items that are being addressed in priority order with an expected timeline. If the response to "what are the top 3 platform friction areas?" is reactive discovery rather than reference to a maintained backlog, the proactive management practice isn't in place.

**Watchout:** Proactive management requires time investment that reactive management doesn't formally require. The quarterly review, the new-user observations, the pre-change reviews — these take time that could be spent on immediate ticket resolution. The investment pays off in reduced future reactive load, but that payoff is invisible to any individual quarter's productivity measurement. This is a structural tension in platform work; naming it is more useful than pretending it doesn't exist.

---

**Try This:** For the platform you manage, complete Part 1: write one metric for each of the three success levels (operational, adoption, outcome). Which level can you currently measure? Which can't you currently measure, and what proxy would give you approximate signal?

**Take This Further:** Conduct one new-user observation using Part 2's quarterly cadence. Ask someone new to the platform to complete your three most common user tasks without assistance. Write one sentence: what did you learn that wasn't in your support ticket log?

**Judgment Exercise:** Your systematic signal review reveals a significant adoption gap: 40% of users are not using a core platform capability that they would benefit from and that they're currently accomplishing through a less-efficient workaround. The adoption gap has existed for at least 6 months based on the signal. Addressing it would require both a documentation investment and a change to the default configuration. You have limited time this quarter. What do you prioritize: fixing the documentation, changing the default, or gathering more signal about why the gap exists?

**What Next:** 327 (Documentation as Experience Design) for addressing adoption gaps with documentation improvements. 313 (UX in a Product You Didn't Build) for the broader arc on UX decision-making in vendor/configuration contexts.
