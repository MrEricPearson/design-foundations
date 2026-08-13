# Designing a Reward Loop
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** 234, 235, 236 | **Episode:** 4

**Goal:** Design a reward structure that creates genuine engagement in service of users' actual goals — rather than compulsive usage that serves platform metrics at users' expense.

**Prior Knowledge Hook:** The standard approach to gamification is to identify an engagement metric and add points/badges/streaks until it improves. This produces engagement that is real in the short term and fragile in the long — users working for rewards, not for the underlying value. When the reward structure changes, behavior collapses. The method below starts from the opposite direction: from the user's genuine goal, backward to the reward structure that makes achieving it feel motivating.

**Trigger:** Use when designing a system meant to build a repeated behavior, establish a habit, drive course completion, or sustain engagement in a multi-session activity. Not appropriate for one-time conversion flows where extrinsic incentive is the honest design target.

**Why This Works:** Intrinsic motivation (doing something because it's genuinely valuable) produces more stable, self-sustaining behavior than extrinsic reward (doing something for the reward). The design problem is that intrinsic motivation often has a slow start — the early phases of learning or building a habit don't feel rewarding yet. Extrinsic rewards can bridge that gap without displacing intrinsic motivation, if they're structured to decrease as intrinsic motivation grows, and if they reinforce progress toward genuine user goals rather than platform activity.

**Method:**

1. **Name the genuine user goal.** What does the user actually want to achieve? State it in terms of the user's outcome, not the product's metric. "Complete the certification" not "finish the course." "Build a writing practice" not "log in daily." If you can't name the genuine user goal, you're designing incentives for a goal you've assumed.

2. **Map the motivation curve.** When in the experience is intrinsic motivation likely to be low (early stages, before competence is felt; after plateau, when progress is less visible)? When is it likely to be high (after a breakthrough moment; after visible progress)? Extrinsic reward is most valuable at the motivation troughs — adding it at the peaks displaces intrinsic motivation without adding anything.

3. **Design the reward for the right behavior.** The reward should reinforce the specific behavior that produces progress toward the genuine user goal — not the proxy behavior that's easy to measure. "Completed a lesson" is a proxy. "Applied what you learned and produced [artifact]" is the goal behavior. Design rewards that are contingent on goal-relevant behaviors, not just activity counts.

4. **Set the schedule.** Variable-ratio schedules (reward after unpredictable number of actions) produce the strongest behavioral persistence but also the highest compulsion risk. Fixed-interval schedules (reward after a defined time or completion threshold) produce more stable behavior without the compulsion profile. Choose the schedule that matches the ethical test: would users continue the behavior if the reward were removed, once the genuine value was established?

5. **Apply the three-test check.** Before finalizing: (a) informed consent — would users choose this reward structure if they understood its mechanism? (b) goal alignment — does the behavior being rewarded produce the user's genuine goal? (c) unhurried choice — would a user who is not under urgency or cognitive load engage with this the same way?

**Artifact:** A reward structure document specifying: the genuine user goal, the motivation curve with identified troughs, the specific rewarded behaviors, the reward schedule and schedule rationale, and the results of the three-test check.

**Watchout:** Designers with good intentions design reward structures that feel genuinely engaging in the early phase — users get hooked — and only discover months later that the engagement was compulsive rather than valuable. Smart, well-intentioned practitioners make this mistake because the early signal (high engagement) looks identical in both cases. The diagnostic is the follow-up question: when a user hasn't engaged for a week, do they feel they missed out on progress toward their goal, or do they feel guilty about their streak? Goal-oriented absence feels like missed opportunity. Compulsion-oriented absence feels like guilt or failure independent of progress. Design for the former.

**Try This:** Take a behavior your product currently incentivizes with a streak, badge, or points. Apply the motivation curve analysis: at what stage in the user's experience with this behavior is intrinsic motivation highest? Is the reward applied at that stage? If so, you may be displacing the intrinsic motivation that would sustain the behavior after the reward is removed.

**Proof:** The reward loop is working when users continue the core behavior during a period when the reward structure is interrupted (a streak breaks, the badge has been earned, the points aren't available). If behavior stops when the reward does, the design has produced extrinsic dependence, not genuine engagement.

False positive: high engagement metrics during the reward period feel like success. They are not — they are necessary but not sufficient. The test is behavior when the reward is interrupted, not behavior when it's active.

**Take This Further:** Over the next two weeks, track at least one user who has been engaged with the incentivized behavior through a moment where the reward structure is interrupted (missed a day, completed the badge tier, etc.). What happens to their behavior? If it recovers without the reward, intrinsic motivation is present. If it doesn't, the reward was load-bearing.

Afterward, write one sentence: What does the behavior look like when it's running on intrinsic motivation versus on reward dependency?

**After you've run this yourself:** Share the reward structure document with the three-test check completed with a team member who wasn't involved in its design. Ask them to apply the tests independently. Divergences in how you scored the tests reveal where the ethical risk is ambiguous.

**What Next:** Read 234 (Persuasion vs. Manipulation) if you haven't yet — the three tests are defined there and form the backbone of this method's ethical check. Read 235 (Gamification Principles) for how different reward schedules interact with compulsion risk.
