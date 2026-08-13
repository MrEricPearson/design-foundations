# Documentation as Experience Design
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Non-Custom Dev / 3rd-Party / Configuration primary | **Prereqs:** 126 (Mental Models), 130 (Scenario Writing), 107 (Framing the Problem), 113 (Defining Success Before You Start), 255 (Jakob's Law)

**Goal:** Write documentation that people actually use — by designing it for the situation where it's needed (not the moment it's written), structuring it around user goals rather than product features, testing whether it closes the task loop, and maintaining it so it doesn't become a trap.

**Trigger:** Users are asking support questions that the documentation should answer. Or: documentation exists but users don't consult it before asking for help. Or: someone new to the platform needs to complete a task and the documentation produces more confusion than resolution. Documentation was written — but it's not serving the people it was written for.

---

## Part 1 — When Documentation Is Needed and What It Should Do

**Concept:** Documentation is written at the moment something is understood — by someone who knows the product. It's read at the moment something isn't working — by someone who doesn't. These two moments have opposite knowledge states and opposite needs. The writer has full context and writes from that context; the reader has no context and needs enough to act. Most documentation fails at the reader's moment because it was optimized for the writer's moment.

The failure is structural: documentation written from "here is how this feature works" answers the question "what does this do?" Documentation written from "here is what someone needs to do" answers the question "how do I accomplish my goal?" Users in the moment of needing documentation are asking the second question. Most documentation answers the first.

**Method:**
Before writing any documentation:
1. Name the situation: what is happening for the person who will need this documentation? Not "they want to learn about Feature X" but "they're trying to do Task Y and they've hit a specific problem or gap"
2. Name the user's goal in the situation: what outcome do they need to reach? "Successfully completed [specific task]" is a goal; "understands how Feature X works" is not
3. Name what they already know: what context can you assume? What can't you assume?
4. Write one sentence: "This documentation helps someone who [situation] accomplish [goal]." If you can't write that sentence, the documentation isn't ready to be written.

**What you end up with:** A documentation brief — who, when, what situation, what goal — that keeps the writing grounded in the reader's context rather than the writer's.

**Proof:** If the documentation brief produces a sentence that could apply to multiple different documents without changing, it's too vague. "This documentation helps someone who is configuring the platform for the first time set up user permissions" is specific. "This documentation helps someone learn how permissions work" is too broad to guide useful writing.

**Watchout:** Documentation briefs take 5 minutes to write and prevent hours of documentation that misses its audience. The temptation to skip the brief and start writing is strong when the knowledge feels obvious — which is exactly when the writer is most likely to write from their own context rather than the reader's.

---

## Part 2 — Structuring for the Task, Not the Feature

**Concept:** Product documentation is typically organized by feature: here is everything about Feature X, here is everything about Feature Y. Feature organization makes documentation easy to maintain (features have clear owners) and easy to write (the writer thinks feature by feature). It makes documentation hard to use, because users don't organize their needs by feature — they organize them by task and goal. A user who wants to "add team members and set their access levels" doesn't know whether that's a Feature X or Feature Y topic; they know what they're trying to do.

Task-organized documentation meets users where they are. It's harder to write and maintain because tasks often span multiple features, and ownership is less clear. The investment pays off in reduced support load and improved adoption.

**Method:**
For any significant documentation piece:
1. List the top 5-7 tasks users will try to complete using this documentation — in the user's language ("add a team member", "change my notification settings", "export my data") not the feature's language ("User Management", "Notification Configuration", "Data Export API")
2. For each task, write the documentation from the task's perspective: start from the user's situation, walk through what they need to do, end with what they should see when it works
3. Where a task touches multiple features, document the whole task flow — don't split it into feature articles and require users to assemble the path themselves
4. Add a cross-reference layer: from each feature article, link to the tasks that use that feature. Users who arrive via search or navigation can find their task; users who arrive via task can find the feature reference if they need depth.

**What you end up with:** Documentation that is organized by what users need to do, with a cross-reference to feature-level depth for users who need it.

**Proof:** Ask someone completing a task to find the documentation they'd use to accomplish it. If they can find the relevant documentation and complete the task from it without asking for help, the task-based structure is working. If they find it but can't complete the task, the documentation content needs revision. If they can't find it, the organization needs revision.

**Watchout:** Task-organized documentation has a higher maintenance cost than feature-organized documentation, because when a feature changes, every task that uses it needs updating. Build a task-to-feature mapping when writing, and update it when features change — otherwise task documentation becomes stale faster than feature documentation does.

---

## Part 3 — Testing Whether Documentation Closes the Loop

**Concept:** Documentation that was written and reviewed by people who know the product doesn't test whether it works for people who don't. "This looks accurate" and "this is usable" are different judgments. Accuracy is evaluated by someone with product knowledge. Usability is evaluated by someone trying to use the documentation to accomplish a task they couldn't accomplish without it. Most documentation is only evaluated for accuracy.

A documentation test is not a formal usability test. It's a simple check: can someone who doesn't know the product use this documentation to complete the task it's designed for? The answer to this question is not obvious until you try it — documentation that seems clear to the writer routinely produces confusion in the reader, for the same reason that code that works in the developer's environment doesn't always work in the user's.

**Method:**
For any significant documentation before publishing:
1. Find one person who will encounter this documentation in the way the target user would — someone who isn't deeply familiar with the product or feature, but represents the actual user profile
2. Give them the documentation with no context or verbal supplement: "read this and try to complete [specific task]"
3. Watch (or ask them to think aloud): where do they stop? Where do they re-read? Where do they ask a question that the documentation should have answered?
4. Note every point of confusion — not "they just didn't read carefully enough" but "what change to the documentation would have prevented this confusion?"
5. Revise based on what you observed, not what you inferred they needed

**What you end up with:** Documentation that was tested against the task it's designed to close — before it's published and before users encounter it in a moment of need.

**Proof:** A documentation test that produces no confusion points either found unusually good documentation or unusually forgiving test conditions. Most first-draft documentation produces 3-5 confusion points when tested with an appropriate user. That's normal and expected — the test exists to find and fix them.

**Watchout:** Testing documentation with a single user is sufficient for finding obvious issues. It doesn't guarantee the documentation works for all users or all situations. Treat the test as a minimum bar ("at least one person can complete this") not a sufficient bar ("anyone can complete this").

---

## Part 4 — Maintaining Documentation That Doesn't Become a Trap

**Concept:** Documentation has a half-life. Products change; documentation doesn't always change with them. When a user follows outdated documentation, the failure is worse than if no documentation existed: the user trusted the documentation, followed it, and reached a state they didn't expect. That experience damages trust in the documentation and in the product.

Outdated documentation is especially dangerous in configuration-heavy environments where the documentation describes steps that produce visible, specific results — if the steps change, the user's experience diverges from the documentation at the exact point they need it most.

**Method:**
Build maintenance into the documentation workflow:
1. **Version-tag any documentation that describes steps tied to a product version:** "this reflects [product] as of [date/version]" — users can see whether the documentation is current for their version
2. **Link documentation to the feature or configuration it describes:** when a feature changes, the change generates a notification that documentation may need to update
3. **Set a review cadence for high-traffic documentation:** any page with significant usage should be reviewed after each major product release — not to rewrite from scratch, but to verify the steps still produce the described results
4. **Add a feedback mechanism:** a simple "was this helpful?" with a path to "what needs updating?" gives you signal from users who encountered a gap

**What you end up with:** A documentation maintenance workflow that treats accuracy as an ongoing commitment, not a one-time effort at publication.

**Proof:** The test: pick a top-traffic documentation page and follow its steps. Do they still produce the described result? If not, the maintenance workflow isn't working. If yes, run the test quarterly.

**Watchout:** Documentation maintenance has a cost, and the cost scales with the breadth of documentation. More documentation isn't always better — documentation that's accurate and well-maintained for the 5 most common tasks is more valuable than documentation that covers 50 tasks and is accurate for 40 of them. Scope the documentation to what you can maintain.

---

**Try This:** Take a piece of existing documentation that receives regular support questions about the topic it covers (or documentation you've written recently). Apply Part 3: find one person who hasn't used this documentation and ask them to complete the task it describes. Note every point of confusion. What would you change?

**Take This Further:** For your next documentation piece, write the brief from Part 1 before writing a word of the documentation. Share the brief with one person who knows the platform and one who doesn't. Write one sentence: did the two perspectives agree on what the documentation needed to accomplish?

**Judgment Exercise:** You have 10 documentation pages that need updating after a platform change. You have time to properly update 6. The other 4 will be outdated. The 4 you'd deprioritize all have some usage — they're not dead pages. What do you update and what do you do about the pages you can't update? Do you leave them as-is, take them down, or add a disclaimer?

**What Next:** 313 (UX in a Product You Didn't Build) for the broader arc on making UX quality decisions in a vendor context. 326 (Evaluating Vendor Products) for the pre-adoption evaluation that shapes what documentation will need to cover.
