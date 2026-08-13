# Service Blueprint / Dependency Map
**Tier:** 300 — Orchestrate | **Arc:** Standalone | **Prereqs:** 165 (Frontstage and Backstage), 175 (What a Journey Map Is), any of: 206c / 206a / 206b (Journey Mapping)

**Goal:** After this piece, you will be able to extend a journey map into a dependency map — naming what teams, systems, and processes each user-facing step relies on — before a change reveals a hidden dependency after it ships.

**Arc Trigger:** You're about to ship a change and haven't considered what else it touches beyond the immediate screen or flow.

---

**Part 1 — Know Your Input's Confidence Level**

**Concept:** A service blueprint's reliability inherits from the journey map that feeds it. An evidence-cited map (206a) produces a dependency map you can act on with confidence. A co-created map (206b) produces a collective mental model of dependencies — useful, but carrying the room's same potential blindspots. An assumption-first proto-map (206c) produces a hypothesis blueprint — it surfaces possible dependencies based on what your team believes, not what's been observed.

The confidence level doesn't change whether to build the blueprint. It changes how you label and use what you build.

**Method:**
- Identify which journey mapping approach your input came from: assumption-first (206c), discovery-driven (206a), or co-creative (206b).
- Label the blueprint to match: "hypothesis blueprint," "evidence-based blueprint," or "collective model blueprint."
- If your map is assumption-first, treat the dependency map as a list of dependencies to verify, not a list of known dependencies.

**What you end up with:** A blueprint labeled with the confidence level it inherits from its source map.

**Proof:** The label is on the blueprint before anyone acts on it. If a dependency is listed as "hypothesized," the team knows to verify it before treating it as a known constraint.

**Watchout:** A hypothesis map that feeds an unlabeled blueprint is the highest-risk outcome — the dependencies look confirmed because they're in a formal-looking document, and the uncertainty from the source map has vanished.

---

**Part 2 — Map the Dependencies**

**Concept:** Every step a user experiences in the front of the product is supported by systems, teams, and processes behind it. A service blueprint makes those supports visible — not as a complete architecture diagram, but as a dependency check: "what has to work correctly for this step to succeed?"

**Method:** Starting from your journey map (whatever approach produced it), work through each step and ask: what team, system, or process has to work correctly for this step to succeed? Write those below or behind each step.

**What you end up with:** A simple map showing what's connected behind the scenes, alongside the user-facing experience.

**Proof:** Starting from a journey map and asking "what else does this step touch?" either surfaces dependencies you hadn't considered or confirms you'd already considered them. Either result is useful — one prevents a surprise, the other gives you confidence. Not asking leaves you with neither.

**Watchout:** This can get complex fast. Stay at the level of "what am I likely to break or what will break this" — not a full system architecture audit. Depth of one level is enough to catch most shipping surprises.

---

**When You Don't Have a Journey Map**

**If no journey map exists and there's no time to build one:** Scope the blueprint to a single step rather than a full journey. Pick the step most likely to have hidden dependencies — typically the step that involves the most handoffs, the most systems, or the most recent changes. Ask for that step only: what team, system, or process has to work correctly for this step to succeed? You get a partial dependency check, not a full blueprint, but partial is better than none.

**What you still get:** Dependency visibility for the highest-risk step, which is usually the step most likely to cause a post-ship incident.

**What you give up:** The connective picture — how dependencies chain across steps, and where one step's hidden dependency affects an adjacent one.

**Don't do this:** Don't describe the whole system from memory and call the result a service blueprint. A mental model of the system is a starting point for the conversation, not a substitute for the structured question-per-step method.

---

**At Enterprise Scale**

When the product involves many interconnected systems, an attempt to blueprint everything produces an unusable wall of complexity. Scope the blueprint to the change, not the system. Ask: "which steps does this specific change touch, or which steps could this change break?" Blueprint only those steps. A focused dependency check for 3-5 steps is more actionable than a comprehensive system map of 30.

For multi-team enterprise systems, the "what has to work correctly for this step?" question often produces cross-team answers. When a dependency names a team rather than a system, follow up: who in that team owns this dependency? An unnamed-team dependency is a dependency without an owner, which is a dependency that will surprise you.

---

**Try This:** Pick one step from a journey map you already have (or sketch one step for something you're about to ship). Ask: what team, system, or process has to work correctly for this step to succeed? Write those down. That is the start of the dependency map. Label it with the confidence level of its source map.

**Take this further:** In the next week, extend the dependency map by one level — for each dependency you named, ask what those teams or systems in turn depend on. Write one sentence: where does the chain become uncertain, and what would you need to find out to resolve that uncertainty?

**Judgment Exercise:** You're building a blueprint for a change that touches a third-party vendor system at one step. The vendor's backend processes are opaque — you can see what the user-facing step looks like, but you can't verify what's behind it. The blueprint's core assumption is that you can identify the dependencies. What changes about the method when one step's dependencies are structurally unknowable, and what does the blueprint for that step become instead?

**After you've run this yourself:** Describe the user-facing step and what the product does at that moment to an AI tool and ask it to identify potential backend dependencies, third-party integrations, or team handoffs — then validate each against what you know is actually true in your system. Treat the AI output as a prompt list, not a confirmed dependency list.

**What Next:** If the dependency map reveals a handoff with unclear ownership, read 303 (One Feature, Three Handoffs) for the method to surface vocabulary and intent gaps before the change ships. If the blueprint surfaces a pain point that's systemic rather than screen-level, that's a 304 (Workshop) conversation — it needs the right people in the room.
