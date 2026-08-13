# What's Missing From Your Spec
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Custom Dev primary | **Prereqs:** 100 (Assumption vs. Fact), 107 (Framing the Problem), 110 (Constraints as Design Input), 113 (Defining Success Before You Start), 126 (Mental Models), 130 (Scenario Writing), 318 (Writing Requirements That Survive the Build)

**Goal:** Read an incoming spec with the lens that finds what it doesn't say — silent assumptions, undefined edge states, missing user context, and decisions handed off to implementation — so you can surface gaps before they become rework.

**Trigger:** Development is mid-sprint and requirements are being clarified in real time. Or: a feature shipped correctly from the spec's point of view but wrongly from the user's point of view. Or: the spec looks complete but three reviewers are making different assumptions about the same feature. The spec was written — but it left the hard questions open.

---

## Part 1 — What Specs Routinely Leave Out

**Concept:** A spec describes the happy path. It describes what happens when the right user does the right thing in the right sequence with valid data. Everything outside that path — failed inputs, missing data, unusual sequences, users who don't match the assumed model — is either left to implementation discretion or left to be discovered in QA. This isn't negligence; it's a structural feature of how requirements get written. The spec author has the happy path clearly in mind and writes from that mental model. The ambiguities are invisible to them because they've already resolved them in the mental model they're not writing down.

For a developer, the spec is a set of constraints on one path through a much larger space of possible system states. Every state the spec doesn't describe is a decision that will be made during implementation, usually by whoever is building at that moment, under time pressure, without user context.

**Method:**
For any spec before or during implementation, scan for four categories of omission:
1. **Missing user context:** who specifically will encounter this feature, in what situation, prompted by what? If the spec doesn't name a user type and situation, the developer will invent one — and it may not match the intended user
2. **Undefined entry states:** what state is the user in when they arrive at this feature? First-time or returning? With data already loaded or starting empty? On a mobile device or desktop? Each entry state may require different behavior; an unspecified entry state defaults to whatever the developer implements first
3. **Absent failure modes:** for each user action, what happens when it fails — invalid input, server error, timeout, missing dependency? If failure modes aren't specified, they'll be handled by exception handling or framework defaults, which rarely produce good user experiences
4. **Implicit decisions:** where does the spec describe an outcome without specifying the path? ("The user sees a confirmation" — what triggers it? what does it say? can they dismiss it?) Count these as open decisions, not spec completions

**What you end up with:** A list of what the spec assumed was handled without saying so — the questions that, if not answered before implementation, will be answered during it.

**Proof:** For every item on the list, ask: will a developer encountering this point in the build have enough information to make a user-quality decision? If no, the gap is real and needs resolution. If yes, the gap may be acceptable delegation.

**Watchout:** Not every gap needs to be filled before implementation starts. Some gaps are fine to resolve during implementation if they're low-stakes and reversible. The goal is conscious delegation ("I know this is open and here's how to handle it") rather than accidental delegation ("this wasn't specified, so I made a call").

---

## Part 2 — Reading for Unstated Assumptions

**Concept:** Every spec rests on assumptions about the user, the environment, the data, and the product state. These assumptions aren't wrong — they're necessary simplifications that make a spec writable. The risk is that they're invisible: the spec was written as if the assumptions were true without marking them as assumptions. When an assumption turns out to be wrong — a user type that wasn't considered, a data state that wasn't anticipated — the feature built against it needs rework.

Finding unstated assumptions in a spec is a different skill from finding omissions. Omissions are what's absent. Assumptions are what's stated as if it were settled when it hasn't been confirmed. The tell is language that implies a user state or behavior without specifying how it was verified: "users will know to," "the user expects," "the natural action is."

**Method:**
For any spec, read for assumption language:
1. Mark every phrase that describes user behavior without evidence: "users will," "users expect," "naturally," "obviously" — each is an unstated assumption about the user model
2. Mark every phrase that assumes a specific data state: "when the data is available," "after onboarding is complete," "assuming the user has already" — each assumes a prior condition that may not hold
3. Mark every phrase that assumes a context the spec doesn't specify: "on desktop," "in a browser environment," "in the current implementation" — each constrains the feature without naming the constraint
4. For each marked phrase: write the assumption explicitly and classify it as: (a) confirmed by evidence, (b) reasonable but unconfirmed, or (c) unknown

**What you end up with:** A visible assumption map — every place the spec is implicitly relying on something being true, with a confidence classification.

**Proof:** If the assumption scan produces no (b) or (c) items, either the spec is unusually well-grounded in evidence or the scan wasn't thorough. Most specs written before significant user research will have several (b) items and at least one (c).

**Watchout:** Assumption mapping isn't spec critique — it's risk identification. The goal is to know which assumptions are load-bearing before building against them, not to require every assumption to be confirmed before a line of code is written.

---

## Part 3 — Translating Spec Language to User Reality

**Concept:** Specs are written in product language — features, states, actions. Users operate in goal language — tasks, outcomes, situations. The translation between them is usually implicit and usually incomplete. A spec that says "the user can filter by date" has made a product language statement. The user reality might be "I need to find the records from last Tuesday" — which may or may not be addressed by a date filter, depending on how the filter is built and whether the user can use it without help.

This translation gap is where features that technically meet the spec still fail users. The spec was correctly implemented; the product language statement was correctly executed. The failure was in translating product language to user reality — a step the spec author skipped because they were thinking in product terms.

**Method:**
For the core features in any spec:
1. Write the spec statement in product language as given
2. Write the user goal the feature is presumably serving — what is the user trying to accomplish that this feature addresses?
3. Write the user scenario in which they'd use this feature — who, what triggered the need, what did they try before, what are they hoping to get?
4. Check: does the feature as described actually serve the user goal in the scenario you wrote? Specifically:
   - Can the user find and understand the feature without instruction?
   - Does using the feature produce the outcome the user goal requires?
   - What happens if their situation doesn't match the assumed scenario?

**What you end up with:** A translation check that surfaces where the spec's product language doesn't map cleanly to user reality — before those mismatches become shipped features.

**Proof:** When a developer can describe a feature in user goal terms — not just product terms — the translation has been done. "This feature lets users filter by date" describes product language. "This feature helps someone find records from a specific week without having to scroll through all their history" describes user reality. Both can be true simultaneously; only the second tells you whether the feature will actually work for users.

**Watchout:** Writing the user scenario requires some knowledge of the user. If you don't have that knowledge, name the gap: "I'm assuming the primary user is X in Y situation — is this right?" That question is faster to answer than the rework.

---

## Part 4 — Surfacing Gaps Without Blocking Progress

**Concept:** A developer who finds gaps in a spec has two failure modes: surfacing every gap as a blocker (which creates process overhead and is seen as obstruction) or not surfacing gaps at all (which produces the exact implementation failures the spec gaps enable). The skill is discrimination — identifying which gaps are decision-quality and need resolution before implementation proceeds, and which gaps are implementation-quality and can be delegated safely.

Decision-quality gaps change what the feature does or whether it serves the user's goal. They need resolution before implementation starts. Implementation-quality gaps affect how the feature does what it does — the specific wording of an error message, the exact timing of an animation — and can be delegated to whoever is implementing, with a constraint: document the decision when it's made.

**Method:**
For gaps found in Parts 1-3, classify each:
1. **Decision-quality (resolve before implementation):** gaps where different answers would produce meaningfully different features or user experiences; the decision can't be recovered cheaply after the fact
2. **Implementation-quality (delegate with documentation):** gaps where any reasonable implementation decision would produce an equivalent user experience; the specific choice matters less than documenting what was chosen and why

For decision-quality gaps:
- Identify the minimum information needed to make the decision — not a full research study, but the specific question that needs an answer
- Name who can answer it — PM, designer, or a specific user context
- Set a time constraint: "I need this by [date] to keep the implementation on track"

For implementation-quality gaps:
- Make the decision during implementation
- Write it in a comment, a ticket update, or a brief decision record — something that can be referenced if the decision is later questioned
- Note what would cause you to revisit it: "if we discover users consistently struggle with this, the decision should be reconsidered"

**What you end up with:** A triage process that surfaces real blockers efficiently and delegates safe decisions with appropriate documentation.

**Proof:** If every gap becomes a blocker, the triage isn't discriminating. If no gaps are surfaced, the spec reader isn't doing the scan. The working state is: 2-4 items surfaced as decision-quality per spec, remainder handled during implementation with documentation.

**Watchout:** Decision-quality classification requires judgment about user impact. A developer who hasn't thought about the user scenario (Part 3) will misclassify implementation-quality items as decision-quality (because any unknown feels like a blocker) and miss decision-quality items that seem obvious from a technical perspective.

---

**Try This:** Take a spec you've recently received or are currently implementing. Apply the omission scan from Part 1. List every gap you find. Then classify each as decision-quality or implementation-quality using Part 4. How many items need resolution before implementation? Are those items currently unresolved?

**Take This Further:** For the next sprint, before implementation begins, apply Part 2 (assumption scan) to each major story or requirement. Write one sentence after the sprint: which assumptions turned out to be wrong, and how did discovering them during implementation differ from discovering them during spec review?

**Judgment Exercise:** You've found a decision-quality gap in a spec mid-implementation: the feature handles the happy path correctly, but there's a common edge state the spec didn't address — one that a significant percentage of users will encounter. Getting the answer requires a stakeholder who's currently unavailable. Waiting will push the sprint. Guessing will produce a decision that may need to be reversed. What do you do?

**What Next:** 318 (Writing Requirements That Survive the Build) for the PM-side skill that produces specs with fewer gaps. 209 (Design Decision Records) for documenting implementation-quality decisions so they can be found and questioned later.
