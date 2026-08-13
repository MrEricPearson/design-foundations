# The Ship / Patch / Hold Decision
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Custom Dev primary | **Prereqs:** 100 (Assumption vs. Fact), 101 (Not All Assumptions Are Equal), 109 (Weighing Tradeoffs), 110 (Constraints as Design Input), 113 (Defining Success Before You Start), 137 (The Quality Ladder), 249 (Loss Aversion)

**Goal:** Make confident ship / patch / hold decisions by defining the right criteria before a feature is ready to test, evaluating launch risks against those criteria, and choosing a launch path that protects users without defaulting to either "always ship" or "never ship with known issues."

**Trigger:** A feature is "done" from an implementation standpoint but something isn't quite right — a known issue, a rough edge, a test result that wasn't clean. The team is under pressure to ship and under equal pressure not to ship something broken. The decision being made is: is this good enough? The problem is that "good enough" hasn't been defined.

---

## Part 1 — Defining "Good Enough" Before You Can Evaluate It

**Concept:** "Good enough to ship" is not a quality level — it's a relationship between quality and the consequences of shipping. Something that's good enough for a feature affecting 10 internal users isn't good enough for a feature affecting 10,000 external ones. Something that's good enough for a beta with explicit feedback channels isn't good enough for a general release with no rollback plan. The error in most ship/patch/hold conversations is evaluating quality in the abstract rather than against a specific consequence model.

The result: every issue looks either catastrophic or trivial depending on who's making the evaluation, because no one has said what the threshold is. The threshold needs to be set before the feature is ready to evaluate — not in the moment of pressure.

**Method:**
Before a feature enters final testing, write the evaluation criteria:
1. **Impact scope:** who will be affected if this feature fails after launch? Number of users, type of users (internal/external, role, dependency on this feature), and how discoverable failures will be
2. **Failure cost:** what's the worst-case user experience if this feature fails? Lost data, lost work, security exposure, workflow interruption, visible error state?
3. **Recovery path:** if a failure is discovered post-launch, what's the fastest path to resolution? Rollback (how long?), hotfix (how long?), workaround users can take?
4. **Good-enough threshold:** given 1-3, write the specific quality level this feature needs to reach before launch — the exact criteria, not "no critical bugs" but "no failures in the primary flow for the user types in scope"

**What you end up with:** A specific quality threshold set before the feature is evaluated — so the ship/patch/hold decision is made against a pre-defined standard, not under launch pressure.

**Proof:** If the criteria can't be written before testing, they'll be invented during the ship/patch/hold conversation, at which point they'll be influenced by the results of testing and the pressure of the moment. Pre-defined criteria produce a decision that can be defended. Criteria invented in the moment produce a decision that can only be rationalized.

**Watchout:** Setting the threshold too high ("no known issues") is as much a failure as setting it too low ("ship it and see"). The threshold should reflect the actual consequence model for this specific feature — not a general standard applied uniformly.

---

## Part 2 — Evaluating Known Issues Against the Threshold

**Concept:** The ship/patch/hold decision almost always happens with known issues on the table. The question isn't whether to ship something perfect — it's how to evaluate which issues are blockers and which are acceptable. Two issues that produce the same error rate may have very different consequences: one affects a rarely-used edge case, the other affects the primary workflow for most users. Error rate is not the evaluation criterion — user impact is.

The common failure mode: evaluating known issues by their technical severity (complexity to fix, code surface area affected) rather than their user severity (consequences for the user who encounters it). A technically trivial bug that breaks a critical user flow is a launch blocker. A technically complex bug that only surfaces in an unusual configuration with no data loss may not be.

**Method:**
For each known issue before a launch decision:
1. Write the user scenario in which the issue is encountered — who, doing what, in what context
2. Write the user consequence — what does the user experience when the issue occurs?
3. Classify against the criteria from Part 1:
   - **Blocker:** issue falls within the impact scope defined in Part 1 AND the user consequence exceeds the failure cost threshold
   - **Patch (ship with a plan):** issue is outside primary impact scope or consequence is below failure cost threshold; ship and address in next cycle with a documented timeline
   - **Accept (log and monitor):** issue is edge-case, low-consequence, and below the defined threshold; document it, add monitoring, and move on

**What you end up with:** A classification of every known issue against pre-defined criteria — so the ship/patch/hold decision is a calculation, not a debate.

**Proof:** A decision made against these criteria can be explained to a non-technical stakeholder: "We evaluated three issues; one exceeded our failure cost threshold for users in the primary flow, so we're holding. The other two are below the threshold and will be patched in the next cycle." That's a defensible decision. "We thought it was probably fine" is not.

**Watchout:** The classification should be challenged when the person classifying has a conflict of interest in shipping. A developer who's been working on a feature for a month has Loss Aversion-driven incentive to classify issues as below the threshold. Have someone not emotionally invested in the launch review the classification.

---

## Part 3 — The Three Launch Paths

**Concept:** Ship, patch, and hold aren't discrete endpoints — they're launch strategies with different risk/speed tradeoffs. Most teams operate as if "ship" means unrestricted release and "hold" means nothing ships. The space between them — phased release, beta access, feature flagging, staged rollout — is where the most useful decisions live, because they let you ship with risk controls rather than choosing between shipping fully and not shipping at all.

The mechanism: risk is a function of exposure, not just issue severity. The same issue that's a blocker for a full release may be acceptable in a 10% rollout with monitoring and a fast rollback. Choosing the right launch path means choosing the exposure level that's appropriate for the current risk level.

**Method:**
For any feature with remaining issues above the "accept" threshold but below a clear "hold" level:
1. **Assess exposure control options:** can the release be staged (10% → 50% → 100%)? Can it be gated behind a feature flag? Can it be limited to a specific user group (internal users, opt-in beta)?
2. **Define the monitoring signal:** what would tell you in real time whether the known issue is affecting users? What's the threshold at which you'd pause the rollout?
3. **Define the rollback plan:** if the monitoring signal is triggered, how quickly can you reduce exposure or rollback entirely? Who needs to be available for that decision?
4. Choose the launch path that matches the risk level:
   - **Full release:** issues are below threshold; launch unrestricted
   - **Staged release:** issues are near threshold; launch at reduced exposure with monitoring
   - **Gated release:** issues are above threshold for general users; release only to specific users who can absorb the risk
   - **Hold:** issues exceed threshold for all reasonable exposure scenarios

**What you end up with:** A launch decision that includes not just what ships but how — with explicit risk controls appropriate to the known issue level.

**Proof:** A staged release with a defined monitoring signal and a clear rollback plan is lower risk than a full release without those controls, even if the underlying issue is identical. The plan is part of the quality decision.

**Watchout:** Staged releases and feature flags create complexity. "We'll monitor it" is only a risk control if someone is actually monitoring and has authority to act on what they see. A staged release without operational readiness to respond to the monitoring signal is a full release with extra steps.

---

## Part 4 — Documenting the Decision and Its Conditions

**Concept:** Every ship/patch/hold decision creates assumptions about what's acceptable and what isn't. Those assumptions need to be documented — not for bureaucratic reasons, but because ship/patch/hold decisions get revisited, challenged, and second-guessed. Without documentation, the decision becomes tribal knowledge held by whoever was in the room, and it's relitigated every time a stakeholder who wasn't in the room encounters the issue.

The documentation also creates accountability for the conditions that justified the decision. "We shipped with this issue because X, and we said we'd revisit when Y" is a different record than "we shipped with this issue." The former creates a clear trigger for the next conversation. The latter leaves the issue floating indefinitely without a defined resolution path.

**Method:**
After any ship/patch/hold decision:
1. Write what was decided and why: the criteria applied, the issues evaluated, and how each was classified
2. Write the conditions that justified the decision: "we shipped with Issue X because it's outside the primary user flow and the reversal cost is low"
3. Write the monitoring signal and the trigger for revisiting: "if we see [metric or user report], we revisit the classification of Issue X"
4. Write the patch timeline for any issues classified as "patch (ship with a plan)": a specific sprint or date, not "soon"

**What you end up with:** A decision record that transfers the reasoning, names the conditions, and creates a defined path for revisiting.

**Proof:** A stakeholder who wasn't in the decision conversation can read the record and understand what was decided, why, and when they should expect the patched version. If the record requires explanation to make sense, the documentation isn't complete.

**Watchout:** Decision records for ship/patch/hold don't need to be formal or lengthy. A paragraph in a ticket is sufficient. The goal is that the reasoning exists somewhere it can be found — not that it fills a template.

---

**Try This:** Take a feature currently in final testing or about to enter it. Write the evaluation criteria from Part 1 before looking at the testing results. Then apply Part 2 to any issues found. How does the pre-defined threshold change the ship/patch/hold conversation?

**Take This Further:** After your next launch, review the decision record from Part 4 against what actually happened. Write one sentence: which issues you classified as acceptable turned out to matter? Which issues you flagged turned out not to matter? What does this tell you about your threshold calibration?

**Judgment Exercise:** Testing has surfaced an issue that affects 8% of users in a specific edge case. The edge case is uncommon but the consequence is significant: users lose work if they encounter it. Fixing it would delay launch by a week. A staged release (10% of users, monitored) is technically feasible. The business is under pressure to launch this week. Your threshold criteria, written before testing, didn't clearly account for this scenario. What do you decide, and how do you justify it to both the team and to stakeholders?

**What Next:** 325 (When Things Break in Production) for the operational response when a post-launch issue exceeds what was acceptable at launch. 300 (Design Debt) for tracking issues that were accepted at launch and need to return to the backlog.
