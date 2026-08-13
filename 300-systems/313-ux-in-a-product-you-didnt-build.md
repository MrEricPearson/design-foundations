# UX in a Product You Didn't Build
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Non-Custom Dev / 3rd-Party / Configuration | **Prereqs:** 126 (Mental Models), 255 (Jakob's Law), 249 (Loss Aversion), 250 (Status Quo Bias), 124 (Nielsen's Heuristics), 110 (Constraints as Design Input), 130 (Scenario Writing)

**Goal:** Apply design judgment to the decisions you control in a vendor or SaaS implementation — configuration, onboarding design, adoption strategy, and documentation — in the absence of access to the source code.

**Trigger:** You're configuring, implementing, or extending a vendor product and need to make decisions that will affect whether real users can actually do their jobs — without access to the code, without a dedicated designer, and without a process that was built to produce UX quality.

---

## Part 1 — What Users Bring to Your Implementation

**Concept:** Users of a vendor platform you're implementing arrive with mental models built from the software they use most — not from yours (255, 126). When your configuration choices produce navigation in unexpected places, terminology that doesn't match their vocabulary, or interaction patterns that conflict with what they know, confusion is automatic. It is not addressable with training, because the mental model that produces the confusion was built over years and fires faster than training recall.

The configuration lever you have here is not absolute. You can't change where the vendor put the navigation or rename core system objects. But you can choose between configuration options based on which one aligns more closely with users' existing models — and where no option aligns, you can design the scaffolding (labels, navigation aids, contextual help) that bridges the gap.

**Method:**
Before any significant configuration decision:
1. List the 2–3 tools your target users use most for the analogous work today
2. For the core feature you're configuring: how does each of those tools handle the equivalent function? What does the user expect to see and where?
3. For each: compare to the vendor product's default and your available configuration options. Which option is closest to what users already know?
4. Where no option aligns: identify the specific divergence and decide whether to (a) add navigation scaffolding (a label, a redirect, a visible shortcut), (b) train on the specific divergence, or (c) accept it as a known adoption cost
5. Document your decisions and the user context behind them — this record becomes the rationale when the configuration is questioned later (→ 209)

**What you end up with:** Configuration choices grounded in what users already know rather than in what the vendor defaults to or what the admin found easiest to configure.

**Proof:** Users encountering familiar patterns succeed faster and require less support. A simple signal: at 30 days post-launch, which aspects of the product generate repeat "where is X?" questions? The repeat questions are the gaps where the configuration didn't meet the mental model.

**Watchout:** This method assumes all mental models should be accommodated — they shouldn't. Sometimes the vendor's pattern is genuinely better and users should adapt to it. The goal is deliberate choice: consciously deciding to match the model, bridge the gap, or accept the cost — not defaulting to whatever the vendor set.

---

## Part 2 — Evaluating What the Vendor Built

**Concept:** Heuristic evaluation (124) is not only for products you built. It's an evaluation lens for anything a user will interact with — including a vendor product before you commit implementation time to it. A pre-implementation heuristic review identifies which usability problems are configurable, which aren't, and which are significant enough to require explicit adoption strategy before go-live.

Most vendor product evaluations focus on features, integration, and pricing. Usability is evaluated informally — team members try the product, form impressions, and report back. Informal evaluation reliably misses the usability problems that only surface when users who aren't motivated to succeed try to complete real tasks under real constraints.

**Method:**
Before committing to full configuration, run a 30-minute heuristic review of the primary user flow:
1. Walk through the most common user task from start to finish
2. For each of Nielsen's 10 heuristics (124), note any violations you observe
3. Classify each violation as:
   - (a) Configurable away — can be addressed through your implementation choices
   - (b) Not configurable, minor — will exist in production but low severity
   - (c) Not configurable, significant — will exist in production and will affect adoption
4. For any category (c) items: document them now as known adoption risks before go-live

**What you end up with:** A documented list of usability problems categorized by your ability to address them — and a pre-mortem for your adoption strategy before you've committed configuration effort.

**Proof:** Category (c) violations that you identified before launch, documented, and developed explicit adoption strategy for, produce fewer surprises post-launch. When support requests appear around those violations, you have a record of why, which is different from discovering them reactively.

**Watchout:** Heuristic review is expert evaluation, not user testing. It predicts where users will likely struggle based on principles; it won't catch everything, and it may flag violations that users in your context find acceptable. It's faster than usability testing and sufficient for vendor evaluation decisions — but it's not a substitute for watching real users attempt real tasks.

---

## Part 3 — Configuration as Design

**Concept:** Every configuration choice is a user experience decision. "What should this setting be?" is always a question about what a user in a specific situation needs — which means answering it without a user scenario is making a UX decision without UX input. The vendor's default is also a decision: it reflects the vendor's assumption about what most customers need most of the time. It may or may not be correct for your users and your context.

Configuration decisions made without documented rationale create a category of tribal knowledge (the specific type described in the plan) that causes problems later: settings get changed without understanding why they were set, "why is it this way?" questions recur without resolution, and migrating to a new version of the product requires re-learning all the original decisions from scratch.

**Method:**
For each significant configuration decision:
1. Write a scenario (130 format) for the primary user affected: who they are, what triggered this session, what they're trying to accomplish, what constraint complicates it, what success looks like for them
2. Answer the configuration question from the scenario perspective — not from "what's easiest to configure" or "what's the vendor default"
3. If one scenario produces a different answer than another user type's scenario, determine whether a single configuration serves both users or whether you need role-based configuration
4. Document: the decision, the scenario that drove it, and the alternative you didn't choose and why

**What you end up with:** A configuration set with documented rationale — a record that answers "why is it this way?" without requiring the person who configured it to still be available.

**Proof:** A configuration choice with a documented scenario is explicable when questioned. A choice made without one requires reverse-engineering the rationale from the setting itself — which often produces an incorrect story about why it was made.

**Watchout:** Writing one scenario doesn't mean you've covered all users. If the system will be used by meaningfully different user types — people with different tasks, different access levels, or different contexts — check whether a single configuration accommodates all of them or creates a good experience for one while producing friction for others.

---

## Part 4 — Adoption as a Design Problem

**Concept:** User resistance to a new tool is not fixed by training. It's driven by cognitive mechanisms that training doesn't address. Status Quo Bias (250) makes the current state feel "free" — the existing workflow requires no evaluation cost, no transition cost, and no uncertainty. Loss Aversion (249) makes the switch feel costly regardless of objective improvement — the new thing has to overcome not just evaluation, but the emotional weight of leaving what is familiar and known.

Users who had no input into the tool selection have no ownership stake in its success. Training-first adoption strategies address the cognitive layer (users learn how to use the tool) while leaving the motivational layer unaddressed (users don't feel invested in it working). The result: users who know how to use the tool and choose not to.

**Method:**
Before launch:
1. Identify the 3 tasks users perform most frequently today in whatever the new tool replaces — not features they'll use eventually, but the things they need to do in their first session
2. Map exactly how to perform those 3 tasks in the new tool — not a general walkthrough, a step-by-step path for each specific task
3. Make those task paths the visible center of onboarding: "here's how to do the 3 things you already need to do" — not a tour of features
4. Name explicitly what's preserved from the current workflow: "the approval process works the same way — it's now in X instead of Y"
5. Post-launch: track which help requests repeat in the first 30 days. Repeat questions on the same interaction are adoption failures, not training failures — they indicate a gap between what was explained and what the user can execute under real conditions

**What you end up with:** An onboarding structure that addresses the Status Quo Bias barrier directly — users can complete their most important tasks in the first session, which means they've paid the switching cost and have evidence it works.

**Proof:** A user who completes their 3 most common tasks in the first session without assistance has cleared the Status Quo Bias barrier. A user who completes an onboarding tour without doing any of their actual tasks hasn't — they know the product exists, but they haven't paid the switching cost, so the Status Quo pull remains.

**Watchout:** "Users resist change" is not an explanation for sustained adoption failure 3+ months post-launch. Status Quo Bias and Loss Aversion explain early resistance — they attenuate as users build familiarity. Sustained resistance after familiarity has been established is a product problem: the tool doesn't actually serve the users' needs as well as what it replaced. That's a different problem and requires a different response.

---

**Try This:** Take a vendor tool you're currently implementing or have recently implemented. Complete Part 2 (a 30-minute heuristic review of the primary flow) and list any category (c) violations — significant, non-configurable usability problems. For each, write one sentence about your adoption strategy.

**Take This Further:** In the 30 days after go-live, track which help requests repeat. Write one sentence: did the recurring questions match the category (c) violations you identified before launch? If not, what did you miss and why?

**Judgment Exercise:** Your heuristic review reveals a significant mental model mismatch in the vendor product's navigation — users will look for the most frequently used function in the wrong place. The vendor won't address it. You can't rename or reposition it in the configuration. Training doesn't fix it (users don't consult training when they're trying to complete a task in flow). What can you actually do, and what do you document as a permanent adoption cost — meaning: what is the ongoing support burden this gap will create, and who needs to know?

**What Next:** 209 (Design Decision Records) for documenting the configuration rationale so it survives the people who made the decisions. 305 (Did It Work Follow-Up Habit) for tracking adoption signals post-launch with a structured check.
