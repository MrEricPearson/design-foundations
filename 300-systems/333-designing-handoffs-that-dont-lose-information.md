# Designing Handoffs That Don't Lose Information
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Cross-audience | **Prereqs:** 100 (Assumption vs. Fact), 107 (Framing the Problem), 113 (Defining Success Before You Start), 130 (Scenario Writing), 209 (Design Decision Records)

**Goal:** Design handoff moments — between discovery and development, between development and QA, between PM and design, between platform and users — so that the knowledge built in one phase transfers accurately to the next phase, rather than being reconstructed from scratch or lost entirely.

**Trigger:** Development is building something different from what was designed because context didn't transfer from the design phase. Or: QA is testing against the wrong acceptance criteria because the intent wasn't documented. Or: a new team member is reconstructing context that was built by the previous team but never written down. Or: work that was done in one phase is having to be redone in the next because the handoff didn't carry the right information. Information loss at handoff points is producing rework that the work itself didn't require.

---

## Part 1 — What Gets Lost at Handoffs

**Concept:** Handoffs lose two categories of information: the decisions that were made (what to build) and the reasoning behind them (why to build it that way). Decisions are usually documented — in specs, in tickets, in design files. Reasoning is usually not. When the reasoning is lost, subsequent decisions made in the receiving phase are made without the context that shaped the original direction — producing conflicts between phases that look like errors but are actually information gaps.

The most consequential reasoning losses happen at the decision points: the moment a direction was chosen from among alternatives. When only the chosen direction is documented and the alternatives and rationale aren't, anyone who receives the handoff can only see what was decided. The context for why — which alternatives were considered, what information made the chosen direction right, what assumptions it rests on — is invisible. That context is precisely what the next phase needs to make decisions that are coherent with the first phase.

**Method:**
For any significant handoff, audit what information it currently contains:
1. **Decisions:** what was decided? (Usually present in documentation)
2. **Alternatives considered:** what other directions were evaluated before this one? (Rarely present)
3. **Rationale:** why was this direction chosen over the alternatives? What evidence or reasoning made it right? (Sometimes present, usually incomplete)
4. **Assumptions:** what would have to be true for this direction to remain correct? What conditions would cause the direction to change? (Almost never present)
5. **Open questions:** what wasn't resolved in this phase that the next phase will need to decide? (Present only in well-designed handoffs)

The handoff is complete only when all five categories are addressed.

**Proof:** Give the handoff documentation to someone who will receive it and ask them to describe what they'd build — without any verbal context from the person who created it. If they need clarification on any of the five categories, those categories are incomplete in the handoff.

**Watchout:** Completing all five categories is more work than current handoff practices for most teams. The investment pays off in reduced rework and clarification cycles. Start with the two categories most often missing: alternatives considered and assumptions.

---

## Part 2 — The Minimum Viable Handoff

**Concept:** Not every handoff requires the same level of documentation. A handoff between two people who worked on the same feature together can be lighter — they share context that doesn't need to be written. A handoff to a new team member, a different team, or a later phase has no shared context — everything must be written. The failure is applying the lighter standard to handoffs that require the heavier standard, which happens when the handoff creator doesn't fully realize how much context the receiver is missing.

The test is simple: how much context does the receiver have access to that was built in the originating phase? If the answer is "mostly through this document," the handoff needs to be more complete. If the answer is "they were part of most of the work," the handoff can be lighter.

**Method:**
For each handoff:
1. Estimate receiver context: how much of the decision-making process in the originating phase will the receiver have witnessed or been part of? (High = most, Low = little to none)
2. For High context receivers: the handoff can focus on decisions and open questions — they have the alternatives and reasoning in their own memory
3. For Low context receivers: the handoff must include all five categories from Part 1 — decisions, alternatives, rationale, assumptions, and open questions; anything less is a partial handoff
4. When in doubt: test the handoff on a Low context receiver before giving it to the actual receiver

**What you end up with:** A handoff calibrated to the receiver's context level — complete enough for Low context receivers, appropriately lightweight for High context receivers.

**Proof:** If the same handoff template is used for both a colleague who was in every review and a new team member who wasn't, it's calibrated for neither. The High context receiver is receiving more than they need; the Low context receiver is missing what they need.

**Watchout:** People systematically underestimate the context they carry that others don't. When estimating receiver context, default to "lower than I think" — the cost of a handoff that's slightly more complete than necessary is low; the cost of a handoff that's incomplete for the receiver is rework.

---

## Part 3 — Designing the Handoff Artifact

**Concept:** The handoff artifact is not the same as the work artifact. A design file, a spec, or a code review is a work artifact — it documents what was produced. A handoff artifact documents what a receiver needs to know to continue the work without losing fidelity to the original intent. These overlap but aren't the same: the handoff artifact may include summary context, decision rationale, and explicit open questions that aren't appropriate in the work artifact itself.

Well-designed handoff artifacts have a clear structure that prioritizes information in the order a receiver needs it: start from the goal (why this exists), move to the decisions (what was built and why), then the assumptions (what this depends on being true), then the open questions (what the next phase needs to decide).

**Method:**
For a significant handoff between phases:
1. Write a brief goal statement: one to two sentences on what this work is for and who it's for — the first thing the receiver needs to understand
2. Write the key decisions with rationale: for each major decision, one sentence on what was decided and one sentence on why (the evidence or reasoning that made it right)
3. Write the assumptions: the things that would need to be true for the decisions to remain correct — this is the most important category because it tells the receiver when to check back
4. Write the open questions: what specifically does the receiving phase need to decide? Name each question explicitly rather than leaving it to be discovered during implementation
5. Write the handoff verification: what should the receiver be able to do after reading this artifact, and what would they need to ask if the artifact is incomplete?

**What you end up with:** A handoff artifact designed around the receiver's needs rather than the creator's work product — structured to transfer intent, not just output.

**Proof:** A receiver who reads the handoff artifact should be able to make decisions in the receiving phase that are coherent with the originating phase, without asking for clarification on any of the five categories. Test this before finalizing the handoff.

**Watchout:** Handoff artifacts can become elaborate and time-consuming to produce. The minimum useful artifact is: goal statement, key decisions with rationale, and the most critical assumption. That's three elements. Everything else is valuable but not minimum. Start with the minimum; add what the receiver specifically needs.

---

## Part 4 — Handoff Verification and Closing the Loop

**Concept:** A handoff that was designed well but received poorly still loses information. The receiving phase may read the artifact and fill in gaps from their own assumptions rather than asking for clarification. Or the receiver may encounter ambiguities during their work — well after the handoff conversation happened — with no easy path to resolution. Handoff verification closes this gap: it checks that the intent transferred, while the person who originated it is still available to clarify.

Closing the loop is the symmetric action on the other side: after the receiving phase has completed their work, checking back to see whether the handoff carried the right information and what was lost or misunderstood. This isn't retrospective blame; it's learning that improves the next handoff.

**Method:**
For significant handoffs:
1. **Handoff verification (receiver-side):** after reading the handoff artifact, the receiver writes back: "I understand this as [their interpretation] — is that correct?" This takes five minutes and catches interpretation gaps before work begins
2. **Clarification window:** specify a time window during which the originating phase is available for questions from the receiving phase — "for the next week, any clarification questions should come to [person]; after that, the decision is yours to make from the documentation"
3. **Mid-phase check-in (optional for complex handoffs):** a brief check-in midway through the receiving phase to see whether questions have arisen that weren't anticipated in the handoff artifact
4. **Closing review:** after the receiving phase is complete, the originating phase reviews the output against the handoff intent: "did the work match the direction we intended? Where did it diverge, and why?" This review is learning input for the next handoff, not a quality gate.

**What you end up with:** A verified handoff that transferred intent, with a named path for clarification during the receiving phase and learning capture afterward.

**Proof:** If the closing review consistently finds that the receiving phase's work matches the originating intent, the handoff process is working. If it consistently finds divergence, something in the handoff is failing — the artifact, the verification, or the clarification window.

**Watchout:** Handoff verification requires the receiver to actually write back, which adds a step. In teams with high throughput, this step gets skipped. The cost of skipping it appears later as rework when interpretation gaps surface during implementation. The tradeoff is worth naming: a five-minute verification vs. a potentially days-long rework.

---

**Try This:** Take the last handoff you were involved in — either as originator or receiver. Audit it against the five categories from Part 1. Which categories were present? Which were absent? What clarification questions arose during the receiving phase that weren't answered in the handoff?

**Take This Further:** For the next handoff you originate, write the assumptions and open questions explicitly. After the handoff, ask the receiver: "what questions did you have that this document should have answered?" Write one sentence: what category of information are you consistently leaving out of your handoffs?

**Judgment Exercise:** You're the originator of a handoff that occurred two weeks ago. You've just learned that the receiving phase made a significant decision that diverges from your intent — not because they misread the handoff, but because the handoff didn't document the assumption that would have prevented the divergence. The divergent decision was reasonable given what they knew. What do you do now, and what do you change in the handoff process going forward?

**What Next:** 209 (Design Decision Records) for the specific artifact format that captures decisions and rationale within a phase. 318 (Writing Requirements That Survive the Build) for the PM-specific version of handoff design between discovery and development.
