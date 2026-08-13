# One Feature, Three Handoffs
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Prereqs:** 115 (giving and receiving feedback), 162 (The Interpretation Gap), 209 (decision records); Part 1 (Vocabulary Checks) also listed as Tier 100 atom in the master outline — this file is the single source
**Note:** Part 4 connects to 132 (Prototype Fidelity) for the concept behind the fidelity-as-signal principle.

**Goal:** After this arc, you will be able to surface vocabulary mismatches, surface unresolved intent, and match fidelity to decision stage before a feature crosses a handoff — so what arrives is what was intended.

**Trigger:** a feature is about to cross a handoff — PM to dev, dev to QA, or dev to a third party — and the terms and intent of the handoff haven't been made explicit yet.

---

## Part 1: The Vocabulary Gap

The same word can mean different things depending on who's saying it. "MVP," "done," "ready" — everyone nods along, but often means something different by it.

**Method:**
1. Pick a term that's central to your current work.
2. Ask two or three people involved to define it in their own words, separately.
3. Compare the answers before assuming everyone's aligned.

**What you end up with:** either confirmation that everyone's actually on the same page, or a specific gap to close before it costs you later.

**Proof:** If three people define the same term the same way, you have real alignment. If they don't, you've found a gap that was already present — the check didn't create it. Finding it before the handoff means it can be closed while it's still cheap to close.

**Watchout:** nodding isn't alignment. Check definitions explicitly rather than assuming agreement from silence.

---

## Part 2: The Missing Brief Sentence

A brief that describes what to build often skips the one sentence that matters most: what decision this unblocks.

**Method:** add one line to your next brief — "This unblocks: ___." If you can't fill it in clearly, that's worth pausing on before the brief goes out.

**What you end up with:** a brief that connects the work to a purpose, not just a list of requirements.

**Proof:** If "This unblocks: ___" can't be filled in, you've found a brief that describes what to build but not why — and now you know that specifically, rather than having a vague sense the brief feels incomplete.

**Watchout:** one sentence doesn't replace a real conversation when the stakes are high — use it as a check, not a substitute for talking.

---

## Part 3: The Handoff Moment

Handoff is often treated as done the moment work is passed along. It isn't done until what was built actually matches what was intended.

**Method:**
1. After something ships, compare it directly against the original spec or design.
2. Note any differences — even small ones.
3. Decide together whether the difference is fine or needs fixing, rather than letting it pass silently.

**What you end up with:** a quick, honest check that catches drift before it becomes the new normal.

**Proof:** Differences noted immediately after ship are addressable. The same differences noticed three sprints later have already been normalized — someone has worked around them, or built on top of them, or silently accepted them as the new spec. The timing is what gives the check its value.

**Watchout:** matching the spec doesn't catch what the spec itself got wrong — this check isn't a substitute for questioning the spec too.

---

## Part 4: What a Mockup Promises

A polished, high-fidelity mockup can accidentally signal more certainty than actually exists — making people think a decision is final when it's still being explored.

**Method:** match the fidelity of what you show to the actual stage of the decision. Early and uncertain → keep it rough. Locked and ready → polish it. Don't let visual polish outrun your actual confidence.

**What you end up with:** a mockup that honestly communicates how settled (or not) the direction really is.

**Proof:** Fidelity is a signal your audience reads whether you intend it to be one or not. A polished mockup communicates finality even without a label saying so. A rough one communicates openness. Matching the fidelity to the actual stage means the signal you're sending matches the reality — rather than accidentally committing to something you're still exploring.

**Watchout:** too-low fidelity can mislead too — if something's actually decided, a sketch might make it look less final than it is. Match fidelity to the decision, in both directions.

---

**Try This:** before your next handoff, run the vocabulary check from Part 1: name three key terms in the feature and ask one person on the receiving team what each one means to them. If the definitions don't match, you've found the gap before it ships.

**Take this further:** in the next week, run the vocabulary check on one more term in the same feature. Write one sentence: was the gap wider or narrower than the first one you checked, and what does that say about where the real alignment work needs to happen?

**Judgment exercise:** You're the only person responsible for this feature — there's no PM-to-dev handoff, no QA team, no third party. The arc is built around surfacing gaps between roles. What do you get from it when you're all the roles yourself? Which parts fall away, and which still create value?

**What Next:** if the vocabulary check surfaces a fundamentally unclear problem statement, step back to 107 (Framing the Problem). If the fidelity question is blocking — you're not sure how polished is "too polished" for this stage — read 132 (Prototype Fidelity) for the decision framework.
