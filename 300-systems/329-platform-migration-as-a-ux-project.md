# Platform Migration as a UX Project
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Non-Custom Dev / Platform / Configuration primary | **Prereqs:** 126 (Mental Models), 250 (Status Quo Bias), 249 (Loss Aversion), 253 (Sunk Cost Fallacy), 130 (Scenario Writing), 206 (Journey Mapping)

**Goal:** Run a platform migration in a way that protects user productivity, manages cognitive load during transition, and builds trust in the new platform — by treating migration as a user experience project rather than a technical cutover.

**Trigger:** A platform migration is being planned as a technical event with a communication plan attached. Or: a previous migration produced a significant adoption struggle that wasn't anticipated. Or: the migration is technically complete but users haven't meaningfully adopted the new platform weeks after cutover. The technical migration may succeed; the user experience migration may not, unless it's designed as deliberately as the technical transition.

---

## Part 1 — Mapping What Users Are Actually Losing

**Concept:** Platform migrations are often framed as improvements: the new platform is better, has more features, is more secure, is more cost-effective. From a user's perspective, the migration is primarily a loss: their learned workflows don't work the same way, the mental model they've built over months or years doesn't transfer, and the implicit knowledge they've accumulated — the workarounds, the shortcuts, the quirks they've learned to navigate — disappears. This loss is real even when the new platform is objectively superior.

Loss Aversion means this loss registers more strongly than the anticipated gain from the new platform's advantages. Status Quo Bias means the current platform's costs are invisible (they're the baseline) while the new platform's costs are salient. Understanding what users are actually losing is a prerequisite for designing a migration that doesn't underestimate the transition effort.

**Method:**
Before migration planning begins, map the user's perspective on what changes:
1. **Mental model inventory:** what has each user type learned about the current platform that won't transfer? Navigation patterns, terminology, workflow sequences, data organization — list the elements of learned knowledge that will need to be rebuilt in the new context
2. **Workaround inventory:** what are users doing in the current platform to accomplish things the platform doesn't officially support? These workarounds represent real user needs — if the new platform doesn't address them, users will notice their absence
3. **Trust inventory:** what do users trust the current platform to do reliably? The things that just work without thinking — these are invisible until they change, at which point they produce the most friction
4. **Loss statement:** for each user type, write one honest sentence: "In this migration, [user type] loses [specific things], and gains [specific things]." The statement should be accurate — if the gains are real, name them; if the loss is larger than the gain in the short term, say so. Planning is grounded in honest assessment, not aspirational framing.

**What you end up with:** An honest inventory of what migration actually costs users — so the transition support plan is calibrated to the real loss, not an idealized version of it.

**Proof:** If the loss inventory is mostly empty ("they're not really losing anything"), the inventory wasn't done from the user's perspective. Even migrations that produce net improvement have real transition costs.

**Watchout:** The loss inventory isn't an argument against migration. It's a planning input that determines how much support is needed and where. A migration team that knows exactly what users are losing can design specifically for those losses; a team that hasn't thought about it discovers them during the post-migration support surge.

---

## Part 2 — Designing the Transition Period

**Concept:** The transition period — the weeks between announcement and full adoption — is where migration succeeds or fails. Technical migrations can be fast (switch on date X, switch off date Y). User experience migrations take longer: users need to rebuild their mental models, re-establish their productive workflows, and reach the point where the new platform is fluent rather than effortful. The gap between technical completion and user productivity completion is the transition period, and it needs to be designed, not just endured.

The most common failure in this period: treating users who are struggling as failures to communicate rather than users who are doing the expected and necessary work of rebuilding mental models. The appropriate response to transition-period friction is support and scaffolding, not better communication of why the new platform is better.

**Method:**
For the transition period:
1. **Set a realistic productivity recovery timeline:** how long will it take for each user type to reach their pre-migration productivity level? This isn't a communication promise; it's a planning assumption. For most migrations, 2-6 weeks is realistic for power users; for occasional users, the recovery period may be longer
2. **Design the learning path for primary tasks:** for each user type's most common tasks, write a step-by-step path in the new platform. Don't reference the old platform; write the path from the new platform's perspective, with the new terminology and navigation. This is distinct from documentation — it's a task-specific "here's how to do the thing you do most" guide
3. **Create explicit bridges for major mental model shifts:** where the new platform's model is fundamentally different from the old one (different vocabulary, different hierarchy, different workflow sequence), name the shift explicitly: "In [old platform], you [did X]. In [new platform], you [do Y]." These bridges convert a confusing difference into a learnable one
4. **Design the support escalation path:** what should users do when they're stuck? Name it specifically and make it visible from within the new platform during the transition period

**What you end up with:** A designed transition experience — not just a migration date and a training session, but a structured path from current-platform fluency to new-platform fluency.

**Proof:** A user who completes the transition period should be able to complete their most common tasks without consulting documentation or asking for help. If users are still regularly seeking help for core tasks 6 weeks post-migration, the transition support was insufficient.

**Watchout:** The transition period design should be proportional to the migration's disruption. A minor platform update with minimal workflow changes needs minimal transition support. A major platform replacement that changes vocabulary, navigation, and workflow sequences needs significant transition investment. The inventory from Part 1 calibrates the level.

---

## Part 3 — Communication That Builds Trust, Not Anxiety

**Concept:** Migration communication typically focuses on information: here's what's changing, here's the date, here are the resources. Information is necessary but not sufficient for trust-building. Users who understand what's changing but are uncertain whether they'll be able to do their jobs effectively after the change experience informed anxiety, not informed confidence. Trust-building communication addresses the uncertainty beneath the information: will I be okay? Will I be supported? What if I can't figure it out?

The distinction is subtle but significant. "Here's what's changing on [date]" is information. "Here's what's changing, here's exactly how to do the three things you do most, here's how to get help, and here's how long we expect the transition to take" is trust-building. The difference is whether the communication acknowledges the user's experience of the change, not just the change itself.

**Method:**
For each significant communication milestone in a migration:
1. **Announcement communication:** what's changing, when, and why — in user impact terms, not business rationale terms; include what's specifically being done to support users during the transition; name the timeline for productivity recovery honestly
2. **Pre-migration communication (1-2 weeks before):** concrete preparation guide — what users should do before the cutover to minimize disruption (data they should locate, workflows they should document, questions they should answer)
3. **Launch communication:** "it's live" with an immediate action path — the first three things to try on the new platform, and the most important things to know that are different from before
4. **Ongoing support communication:** regular updates during the transition period acknowledging that learning takes time, surfacing the most common help questions and their answers, and marking milestones ("two weeks in, here's what most users have figured out")

**What you end up with:** A communication plan that builds user confidence in the migration rather than just informing them of it.

**Proof:** A communication plan that's only announcements and resources hasn't addressed the anxiety component. The "launch communication" and "ongoing support communication" steps are the trust-building ones — if those are missing, the communication plan is information-only.

**Watchout:** Over-communicating during migration produces fatigue. Users stop reading migration communications if they arrive too frequently with too little new information. Calibrate cadence to significant moments: announcement, pre-migration preparation, launch, and then only when there's genuinely new information or common questions to address.

---

## Part 4 — Post-Migration: Closing the Loop and Capturing Learning

**Concept:** The migration is "done" when the old platform is decommissioned. The user experience migration is "done" when users are as productive on the new platform as they were on the old one. These two dones rarely coincide. Post-migration measurement tracks the gap between them and provides signal for the remaining support investment.

Every migration also produces learning that's valuable for the next migration: what the transition support underestimated, what communication landed and what didn't, what mental model shifts were harder than predicted. This learning exists only if it's captured — without capture, the next migration inherits the same blind spots.

**Method:**
In the 4-6 weeks post-migration:
1. **Track productivity recovery:** are users completing their core tasks? How much support is being consumed relative to pre-migration baseline? Is the consumption trend declining (expected) or flat (intervention needed)?
2. **Identify persistent friction:** what are users still struggling with 4 weeks post-migration? These indicate where transition support was insufficient, where mental model bridges are missing, or where the new platform has genuine usability issues that weren't identified in pre-migration evaluation
3. **Measure trust:** a simple one-question survey 4 weeks post-migration: "How confident are you that [new platform] will support you as well as [old platform] did?" — tracks whether trust has been rebuilt, not just whether technical issues have been resolved
4. **Write the migration retrospective:** what the pre-migration inventory got right, what it underestimated, what transition support was most and least used, what would be done differently. This document is the input to the next migration plan.

**What you end up with:** A post-migration measurement and learning capture that closes the loop on the migration as a user experience project, not just a technical event.

**Proof:** A migration that ends with the decommission date and no follow-up measurement treated the migration as complete at technical cutover. The user experience migration status is only knowable from post-migration signal.

**Watchout:** Post-migration measurement has diminishing returns after the productivity recovery period. Measuring 6 weeks post-migration is useful; measuring 6 months post-migration is less useful because by then, other factors (platform evolution, team turnover, new use cases) have mixed with the migration signal. Set a measurement window and close it at the appropriate time.

---

**Try This:** For an upcoming or recent migration, complete the loss inventory from Part 1. Write the loss statement for your primary user type. Does your current transition support plan specifically address each item in the loss inventory?

**Take This Further:** For the next migration in your context, apply Part 2's transition period design before finalizing the migration date. Write the learning path for primary tasks before launch. After launch: which tasks generated the most support requests? Were those tasks in your learning path?

**Judgment Exercise:** You're two weeks into a migration that's technically complete. User productivity has dropped significantly from pre-migration baseline and hasn't recovered. Support requests are high and not declining. Users are expressing frustration. The business is asking why adoption is struggling and when it will recover. What do you do right now, what do you tell the business, and what would you do differently in the next migration?

**What Next:** 328 (Running the Platform Like a Product) for the ongoing platform management practices that prevent the productivity gaps that make migrations harder. 315 (Psychology of Resistance) for the cognitive science behind adoption struggles.
