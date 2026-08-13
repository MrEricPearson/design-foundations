# Evaluating Vendor Products Before You're Locked In
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Non-Custom Dev / 3rd-Party / Configuration primary | **Prereqs:** 124 (Nielsen's Heuristics), 216 (Heuristic Evaluation), 126 (Mental Models), 110 (Constraints as Design Input), 100 (Assumption vs. Fact), 101 (Not All Assumptions Are Equal), 255 (Jakob's Law), 250 (Status Quo Bias)

**Goal:** Evaluate a vendor or SaaS product for adoption before significant configuration investment — by applying a structured heuristic review, auditing the fit between the vendor's model and your users' mental models, identifying non-configurable UX risks, and documenting the evaluation so the decision is defensible and the risks are pre-visible.

**Trigger:** You're being asked to evaluate, recommend, or implement a vendor product, and the decision will be difficult to reverse once configuration investment begins. Or: a vendor product was adopted without a UX evaluation and adoption is now struggling in ways that were predictable — and you want to prevent that pattern on the next one. The platform or tool selection is happening, and UX quality is either not being factored in or not being factored in rigorously.

---

## Part 1 — What You Can and Can't Evaluate

**Concept:** A vendor product evaluation has a specific scope: you're evaluating whether this product, as configured for your context, will work for your users. You're not evaluating whether it's well-designed in general. A product that's excellent for its intended market may be poorly suited to your users' mental models, their existing workflows, or the specific use cases you need to support. And a product that has real usability issues in general may be configurable into something that works well for your specific context.

This distinction matters for the evaluation method. Heuristic evaluation tells you about the product's general quality. Configuration capability assessment tells you about how much you can close the gap between the product's defaults and your users' needs. The combination of both tells you whether adoption is likely to succeed.

**Method:**
Before a vendor evaluation begins, define the scope:
1. **Your user profiles:** write 2-3 brief user descriptions — who will use this product, what are they trying to do, what software do they use most today? These become the evaluation lens.
2. **Your primary use cases:** list the 3-5 most common tasks the users above will perform in the vendor product — not features you hope to use, but the core daily tasks
3. **Your configuration constraints:** what can you control? Terminology, navigation, workflows, onboarding, integrations — and what is the vendor's configuration ceiling (what can't be changed)?
4. **Your evaluation criteria:** what would make this product acceptable for your users? Write the threshold before you see a demo — "users can complete primary tasks without escalating to support within 2 weeks" is a criterion; "seems intuitive" is not

**What you end up with:** An evaluation frame that keeps the assessment grounded in your users' reality rather than the vendor's demo narrative.

**Proof:** If the evaluation criteria can't be written before the demo, you don't yet have a frame — you're evaluating based on how the demo made you feel, which is exactly what the vendor's demo is designed to optimize for.

**Watchout:** The vendor demo is designed by experts who know the product well and have built a path that avoids rough edges. Your users will not have the benefit of that path. Build your evaluation around your users' most likely path, not the demo path.

---

## Part 2 — Heuristic Review of the Primary Flow

**Concept:** Nielsen's ten heuristics (124) are a fast, expert-level evaluation lens that surfaces usability issues without requiring user testing. Applied to a vendor product's primary flow, they identify violations that predict where users will struggle. The goal isn't to find every issue — it's to find the issues that will most affect your users in your primary use cases, and to determine whether those issues are in the configurable or non-configurable layer.

The configurable/non-configurable distinction is the critical output of a heuristic review in a vendor context. An issue in the configurable layer is your problem to fix. An issue in the non-configurable layer is a permanent adoption risk.

**Method:**
For the vendor product's primary flow for each of your core use cases:
1. Walk through each use case yourself, taking notes on friction points and confusion — don't fix or explain anything, just note what happens
2. Apply three heuristics that predict the highest-risk issues for most SaaS products:
   - **Visibility of system status:** does the product communicate what it's doing? Where are there states the user can't interpret?
   - **Match between system and real world:** does the vocabulary and model match how your users think about their work? Where are the vocabulary gaps?
   - **User control and freedom:** can users undo, backtrack, or escape? Where are they trapped in a flow?
3. For each friction point or heuristic violation: classify as (a) configurable — you can fix this with configuration, (b) trainable — users can learn this with appropriate onboarding, or (c) permanent — this requires the vendor to change it and they haven't or won't
4. List your category (c) items explicitly — these are the permanent adoption risks

**What you end up with:** A list of permanent UX risks for this vendor product in your specific context, surfaced before configuration investment begins.

**Proof:** If the review produces no category (c) items, either the product is unusually well-designed for your users, or the review wasn't deep enough. Run the review on the flow a typical user would encounter in their first week — not the flow you'd show in a demo.

**Watchout:** Heuristic review is an expert evaluation — it predicts problems based on design principles, not evidence from actual users. It's faster than user testing and appropriate for evaluation decisions; it's not appropriate as a substitute for user testing once the product is implemented.

---

## Part 3 — Mental Model Fit Assessment

**Concept:** A product can pass a heuristic review and still fail for your users if the underlying conceptual model conflicts with how your users understand their work. Mental model fit is distinct from usability — a perfectly usable interface built around the wrong model requires users to translate between what the product calls things and what they call things, every time they use it. That translation burden compounds across sessions and predicts both adoption resistance and long-term user frustration.

The assessment asks: does this product's conceptual model match your users' domain model? If your users think about their work in terms of "projects" and "tasks," a product built around "workspaces" and "items" requires translation. If the translation is small and the vocabulary is adjustable through configuration, it's manageable. If the translation is large and the vocabulary is fixed, it's a sustained adoption cost.

**Method:**
For the core concepts in the vendor product (entities, categories, status labels, workflow stages):
1. Write the vendor's model: list the primary entities the product uses and how they relate (a Project contains Tasks; a Task has Statuses)
2. Write your users' model: how do your users think about equivalent concepts in their current work? What do they call things? How do they group and relate them?
3. Map the two models: where do they align? Where do they conflict?
4. For each conflict: is the vendor's terminology configurable? If yes, can you close the gap with configuration? If no, assess the translation burden: is this conflict in a peripheral area of the product or in the primary daily workflow?

**What you end up with:** A mental model fit assessment that identifies where your users will need to "think in two languages" — and whether that gap can be closed with configuration.

**Proof:** If the mental model fit assessment produces no conflicts, either the vendor built for exactly your users — uncommon — or the reviewer is too familiar with the product to see the translation gaps their users will encounter. The working signal: you can name at least one concept that your users call one thing and the vendor product calls another, and you've classified whether that gap is closable through configuration or permanent.

**Watchout:** Some mental model differences are fine — users adapt to new vocabulary over time, especially for concepts that are genuinely novel. The issue is large conflicts in high-frequency concepts. A user who has to translate "workspace" to "project" ten times a day has more friction than a user who had to learn a new term once during onboarding and never encountered it again.

---

## Part 4 — Documenting the Evaluation and Its Assumptions

**Concept:** A vendor evaluation that's not documented has a short lifespan. The person who conducted the evaluation carries the findings in their head; when they're not in a decision conversation, the findings aren't present either. The decision gets made based on the demo, the price, and whoever argued most recently — not on the evaluation that actually happened. Documented evaluations persist through personnel changes, get referenced when adoption issues arise, and create accountability for the assumptions that justified the decision.

The evaluation document also creates the pre-visible risk record: the issues identified during evaluation that were accepted as manageable become visible when post-launch adoption is struggling. Without the document, those issues get discovered after significant investment. With the document, they're known and planned for — and if they turn out to be worse than predicted, the record shows what was expected.

**Method:**
After a vendor evaluation:
1. Write a brief evaluation summary (1-2 pages maximum) covering:
   - The evaluation frame (user profiles, primary use cases, evaluation criteria from Part 1)
   - The heuristic review findings, including all category (c) permanent risks (Part 2)
   - The mental model fit assessment, including major conflicts and whether they're configurable (Part 3)
   - A recommendation: adopt / adopt with mitigation plan / do not adopt — with specific reasoning against the pre-defined criteria
2. If recommending adoption with known risks: write the mitigation plan for each permanent risk and the metric you'd use to determine whether the mitigation is working
3. If recommending against adoption: be specific about which criteria the product fails to meet — a "not recommended" that can't be explained against criteria is an opinion, not an evaluation

**What you end up with:** An evaluation record that is referenced at adoption, consulted during implementation, and revisited when adoption struggles to see whether the pre-identified risks are the actual source of friction.

**Proof:** Six months after launch, someone encountering an adoption problem should be able to check the evaluation record to see whether this issue was identified in advance. If the issue is in the record, the response is different than if it's a new discovery.

**Watchout:** Evaluation records are point-in-time assessments. Vendor products update; configuration options expand; your users' needs evolve. Add a scheduled review date to the evaluation record — "this evaluation should be revisited if [product version changes significantly / primary user profiles change / adoption metrics fall below X]."

---

**Try This:** Take a vendor product you've adopted or are currently evaluating. Apply Part 2 (heuristic review of the primary flow) for one of your primary use cases. List every friction point. Classify each as (a) configurable, (b) trainable, or (c) permanent. What's in the permanent column?

**Take This Further:** Before the next vendor evaluation decision in your context, write the evaluation criteria from Part 1 before anyone sees a demo. After the demo, apply those criteria. Write one sentence: how did the pre-defined criteria change the post-demo conversation?

**Judgment Exercise:** Your heuristic review has identified a significant mental model conflict in the vendor product's core workflow. The conflict is in the non-configurable layer — the vendor won't change it. Your options are: (a) recommend against adoption, (b) recommend adoption with a training investment to bridge the gap, or (c) recommend adoption and accept the ongoing translation burden as a permanent cost. The product's other capabilities significantly outperform available alternatives. What do you recommend, and what would you need to include in the evaluation record to make that recommendation defensible?

**What Next:** 313 (UX in a Product You Didn't Build) for the full arc on navigating UX decisions in a vendor context once adoption is decided. 209 (Design Decision Records) for documenting the configuration decisions that follow adoption.
