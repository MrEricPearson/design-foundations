# 206c — Assumption-First Proto-Map
**Tier:** 200 — Practice | **Arc:** Journey Mapping (see 206-journey-mapping-arc.md for approach selection) | **Prereqs:** 175 (What a Journey Map Is), 153 (Experience vs. Process), 154 (What a Pain Point Is) | **Note:** Minimum-viable approach — works without research access. Prereq for 306 (Service Blueprint).

**Goal:** After this piece, you will be able to build a proto-map from what your team currently knows — explicitly labeled as a hypothesis — so you can make decisions with stated uncertainty rather than unstated assumptions.

**Prior knowledge hook:** Think of a direction your team has committed to — a feature, a flow, a sequence of steps — where no one has actually watched a user attempt what that direction assumes they do. The mental model exists. What's missing is a record of it as a hypothesis instead of a fact.

**Trigger:** You need to understand a user's experience to make a decision, but you don't have access to users yet — or the right first step is to build a testable hypothesis before investing in observation or research.

**Why this works:** Making team assumptions explicit changes how they're used. An unwritten mental model gets treated as fact. A written, labeled hypothesis gets treated as something to verify. The proto-map does the same work as any journey map — it makes the current experience visible and marks pain points — but it adds one thing: it makes visible where you're guessing.

**Method:**
1. **Scope.** Name one persona and one goal at the top of the map: "This is [persona] trying to [goal]." One persona, one goal. If you're tempted to write two personas in the same lane, stop — that's where the map will mislead you. Two personas get separate lanes (see 176: Swimlanes as a Comparison Tool) or separate maps.
2. **Lay out the steps.** List what you believe this persona does, left to right, in the order you believe it happens. Use whatever your team already knows: prior conversations, support tickets, existing documentation, your own experience. Leave visible gaps for steps you don't know — write "?" or "unknown" — and don't fill them with guesses you're not labeling as guesses.
3. **Mark confidence.** For each step, mark how you know what you know: "Seen" (observed directly), "Heard" (told by someone who experienced it), or "Assuming" (team inference with no external data). Use any consistent marking — color, symbol, label — as long as it's visible at a glance.
4. **Mark the pain points.** Identify the worst two frustrations, confusions, or drop-offs you believe exist. Write what you believe happens and label it: "Hypothesized pain point."

**Artifact:** A hypothesis map — a sequence with confidence markers and labeled pain points — that makes explicit what you know, what you've heard, and what you're inferring.

**Watchout:** A proto-map built without confidence markers is not a minimum-viable journey map. It is an assumption wearing the format of a finding. The confidence markers are what separate this method from building false certainty into your direction — skip them and you've produced the worst-case outcome: a map that looks validated and isn't.

**Try This:** For something you're currently working on, write the persona name and their goal. List the steps left to right using only what your team already knows. For each step, mark whether it's "Seen," "Heard," or "Assuming." Mark your two worst hypothesized pain points with the word "Hypothesized." Stop when the map covers the full sequence or when you hit a gap you can't fill honestly.

**Proof:** Count the "Assuming" steps. If the map has zero, either you have unusually complete knowledge of this experience or you haven't been honest about where you're guessing. Real confidence distribution for most enterprise teams skews toward "Assuming" — often a third or more of the map. The count tells you where to focus future observation; a map that hides the count hides that information too.

**Take this further:** In the next 2-3 days, share the proto-map with one other person who knows this user or process from a different angle — someone from support, a team member who's seen a related part of the flow, or someone who's talked to users recently. Ask: "What did we get wrong or miss?" Note which steps' confidence labels change based on what they tell you. Write one sentence: what did you assume was "Seen" that turned out to be "Assuming"?

**After you've run this yourself:** Describe your persona's goal and process context to an AI tool and ask it to draft a step sequence. Compare what it produces against what you wrote. Where they diverge is either a gap in your map or a gap in the AI's — either way, the divergence generates specific questions you now know to investigate.

**What Next:** If you want to validate this map with actual user observation or research, read 206a (Discovery-Driven Journey Map). If you need the team to build it together and alignment is part of the goal, read 206b (Co-Creative Journey Map). If pain points cluster around a handoff between teams, read 303 (One Feature, Three Handoffs). When you're ready to add the teams and systems that support each step, read 306 (Service Blueprint).
