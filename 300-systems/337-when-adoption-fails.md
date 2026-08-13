# When Adoption Fails
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Non-Custom Dev / Platform primary | **Prereqs:** 107 (Framing the Problem), 113 (Defining Success Before You Start), 138 (Delight as Behavioral Trust), 249 (Loss Aversion), 250 (Status Quo Bias), 251 (Social Proof), 253 (Sunk Cost Fallacy), 313 (UX in a Product You Didn't Build), 315 (Psychology of Resistance)

**Goal:** Diagnose the root cause of low platform adoption and apply the response matched to that specific failure mode — not the one that's easiest to run.

**Trigger:** A platform or tool has been deployed and adoption is lower than expected, stalled, or actively declining. The team is being asked "why aren't people using this?" before any corrective action is taken.

---

## Part 1 — What Your Data Can and Can't Tell You

**Concept:** Usage data tells you that people aren't using the platform. It rarely tells you why. Low adoption has four distinct root causes — awareness failure, friction failure, trust failure, and credibility failure — that look identical in headline numbers but require completely different responses. Treating the wrong root cause wastes time and signals that the team doesn't understand the problem, which itself erodes trust further.

**Method:**
Before drawing any conclusions, answer three diagnostic questions from whatever data you have access to:
1. Was it ever used? Look at first-use data, not just recent activity. If no one ever activated, the root cause differs from a platform that was used and abandoned
2. Was it used once and stopped? Look for single-session or early-abandon patterns — especially users who accessed the platform in the first two weeks and haven't returned
3. Is it used by some but not others? Segmented adoption often has a credibility explanation: certain user groups don't believe the platform applies to their situation

If you don't have granular enough data to answer these questions, Part 2's conversation protocol is your primary diagnostic tool.

**What you end up with:** A preliminary hypothesis about which failure mode you're in, before you talk to anyone. The conversation protocol in Part 2 tests it.

**Proof:** If you can't distinguish "never tried" from "tried and stopped" in your data, you're not ready to diagnose yet — the two map to different failure modes and different responses. Segment the data before forming a hypothesis.

**Watchout:** Aggregate numbers hide the diagnosis. "15% adoption" could mean 15% of users use the platform regularly — or 60% tried it once and 40% never activated. Both read identically in the headline metric. Segment before interpreting.

---

## Part 2 — The Four Failure Modes: Diagnosing Which One You're In

**Concept:** Each failure mode has a distinct signature in both data and conversation — and each requires a different response. Misdiagnosing costs more than the delay of running the diagnosis first.

- **Awareness failure:** users don't know the platform exists, don't know what it does, or don't know it's intended for them. They haven't tried it. They have no opinion because they have no experience
- **Friction failure:** users tried the platform and encountered a specific obstacle — a confusing step, a workflow that didn't match their mental model, a feature they couldn't locate. They stopped at a specific point and didn't return
- **Trust failure:** users tried the platform, it did something unexpected or failed at a critical moment, and they stopped trusting it. They may have a workaround. They can name what went wrong
- **Credibility failure:** users haven't tried it because they believe — based on reputation, prior experience with similar tools, or what they've heard from colleagues — that it won't work for their specific situation. They may be actively skeptical before any direct experience

**Method:**
Interview four non-adopters using four questions in sequence:
1. "Did you know [platform] existed and was intended for your team?"
2. "Have you used it at all, even once?"
3. "What happened when you used it?" — or if they haven't — "What made you decide not to try it?"
4. "What would need to be true for you to use it regularly?"

Map each answer to a failure mode. The distribution across four interviews gives you enough signal to prioritize your response.

**What you end up with:** A failure mode diagnosis — or a distribution across modes — that shapes which response you apply.

**Proof:** If every interviewee gives you a different answer, you may have multiple failure modes active in different user segments — that's a valid finding. Name the primary mode and address it first. If all four converge on the same mode, you have a clear diagnosis and a clear starting point.

**Watchout:** Don't sample only the loudest critics. Users with friction failure are often silent — they found a workaround and moved on. Locate them by looking at who activated and stopped, not by asking who's complaining.

---

## Part 3 — The Response Matched to the Failure Mode

**Concept:** Applying the wrong response to a failure mode doesn't just fail to help — it often makes things worse. An awareness campaign when users have a trust failure signals that you're not listening. Better documentation when users have a credibility failure tells them nothing they didn't already not know. Each failure mode has a specific response that addresses its actual cause, and only that response.

**Method:**
Match the response to the diagnosis:

**Awareness failure → communication and discovery**
1. Put the platform where people already are: their workflow, their existing tools, their team communication channels
2. Use language that describes what the platform helps people accomplish, not what it is or how it works — "gives you a complete view of your vendor's support history before a renewal call" lands differently than "vendor management platform"
3. Don't ask people to find the platform; bring the platform to them

**Friction failure → specific friction point removal**
1. Identify the step where users abandon — your data or interviews should name it specifically
2. Fix that specific thing before any communication or promotion
3. Do not ask users to retry until the friction point is removed — they will experience the same failure and update their mental model downward. A fixed platform that people don't know is fixed is not yet fixed enough

**Trust failure → see Part 4**

**Credibility failure → peer evidence and scenario demonstration**
1. Find a user from the skeptical segment who adopted successfully and ask if they'll share their experience with colleagues — peer testimony travels further than team communication
2. Show the specific scenario the skeptics say "won't work for them" — not a general demo, but a direct answer to their stated objection
3. Don't tell people the platform will work for their situation; show them, with someone they recognize as a peer as the witness

**What you end up with:** A response plan tied to the specific failure mode — not a general "adoption campaign."

**Proof:** If your response plan could apply to any adoption problem regardless of root cause, it's not diagnostic enough. A well-matched response names the failure mode in its rationale.

**Watchout:** Running all four responses simultaneously is tempting — it covers all bases — but it signals lack of diagnosis and diffuses the effort. Address the primary failure mode first. Secondary modes often resolve or become clearer once the primary is addressed.

---

## Part 4 — Trust Recovery When Things Already Went Wrong

**Concept:** Trust failure is the hardest to recover from because the recovery itself requires trust. Users who stopped using the platform because it failed them — or behaved unexpectedly in a way that cost them something — need evidence that the failure was understood and specifically addressed. A feature release doesn't restore trust. An acknowledgment followed by a specific fix, followed by a low-stakes re-entry point, does.

**Method:**
Three-step trust recovery, in order:
1. **Acknowledge in user terms:** name what failed in the user's language, not the system's — "the import failed without telling you what to fix" is a user-terms acknowledgment; "there was a bug in the error handling" is not, because it locates the problem inside the system rather than inside the user's experience
2. **Fix and signal specifically:** fix the thing that failed, then communicate the fix with specificity — "the import error messages now tell you exactly which column is misformatted and how to fix it before retrying" is specific; "we've made improvements to the import experience" is not, because it asks users to trust the claim without evidence they can verify
3. **Low-stakes re-entry:** give users a way to verify the fix is real without depending on the platform for anything important — a sandbox, a non-critical workflow, a walkthrough of the previously-failing scenario; restoring trust requires the user to accumulate their own evidence, which you cannot transfer to them

**What you end up with:** A specific, credible recovery path for users who left because the platform failed them — not a communication that asks them to trust you without a way to verify.

**Proof:** If a former user who had the original failure experience says "oh, that's the thing that broke for me — they actually fixed it and explained what changed," the recovery worked. If they say "they say it's better now," the communication was too generic to be credible and the user still hasn't verified the fix for themselves.

**Watchout:** Trust recovery takes longer than trust building. A platform that failed users conspicuously may need months of reliable operation before those users resume regular use. Don't interpret slow recovery as evidence that the fix was insufficient — stay consistent and let the track record accumulate.

---

**Try This:** Identify one tool or platform in your current work with lower adoption than expected. Answer the three diagnostic questions from Part 1 with whatever data you have access to. Then identify one non-adopter you could interview using the four questions from Part 2. Even one interview moves you from hypothesis to evidence.

**Take This Further:** In the next two weeks, interview two non-adopters using Part 2's protocol. After both, write one sentence: what failure mode is primary, and what does that mean you should do first? If you share this in a platform team channel, compare your diagnosis with how the team has been describing the adoption problem.

**Judgment Exercise:** Your arc's key assumption is that adoption failure has a diagnosable root cause that a targeted response can address. Name the situation where that assumption doesn't hold: the platform is genuinely unsuited to the job it was deployed for. Users haven't adopted it not because of awareness, friction, trust, or credibility — but because the platform doesn't actually solve their problem. You've run the four-question interviews and this is what you're hearing. What do you do with that finding, and what changes about your response? What makes this finding harder to act on than any of the four diagnosable failure modes — and why?

**What Next:** 326 (Evaluating Vendor Products Before You're Locked In) to prevent adoption failure at the evaluation stage. 328 (Running the Platform Like a Product) for ongoing platform health before failure occurs. 329 (Platform Migration as a UX Project) when the adoption failure involves users resisting a platform change. 315 (Psychology of Resistance) for the behavioral mechanics underlying all four failure modes.
