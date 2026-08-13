# Designing for AI Trust — Agentic Experience (AX)
**Tier:** 300 — Orchestrate | **Arc:** Full arc (5 parts) | **Prereqs:** 302 arc (spotting AI surprises and agent handoff), 116 (error states), 103 (attachment is the real risk), 167 (Automation Bias and Calibrated Trust), 168 (Explainability vs. Transparency in AI), 169 (Affordance)

**Trigger:** you've identified where an AI surprises users in your product (302 arc), and now you need to design the interface around those findings — not just find the problems, but decide what to build.

---

## Part 1: Make the AI's Behavior Visible

**Goal:** After this part, you will be able to name what a user needs to see when AI is acting on their behalf.

**Trigger:** an AI is doing something in your product and users can't tell what it's doing, when it's doing it, or why.

**Method:**
1. List every action the AI takes in your product — including background actions users don't initiate explicitly.
2. For each action: define what the user needs to see. Three components: (a) **the action** — what the AI is doing right now, (b) **the trigger** — what caused it to act, (c) **the outcome** — what it produced or changed.
3. Design a visible surface for each: a status message, a notification, a summary line, a log entry. The format depends on stakes — high-stakes actions need explicit confirmation surfaces; low-stakes actions need ambient visibility.
4. Test with one person: "what is the AI doing right now?" should be answerable from the interface without explanation.

**Artifact:** a visibility map: every AI action in your product with its current visibility state (none / ambient / explicit) and a target state.

**Proof:** If a user can accurately describe what the AI just did, without being told, the visibility is working. If they have to ask, or guess, or assume it did nothing — the action is invisible, and trust will erode when it eventually surprises them.

**Watchout:** don't surface every AI action at maximum verbosity — that's as disorienting as surfacing nothing. Match visibility level to action stakes. An AI that summarized your email doesn't need a modal; an AI that sent it does.

**Try This:** pick one AI action in something you're currently building. Write the three components (action, trigger, outcome) as a one-sentence status message a user would read. If it sounds alarming without context, the action needs more visibility design.

**After you've run this yourself:** describe your AI feature to an AI tool and ask it to write status messages for each action state (in progress, complete, failed) — then check whether each message passes the "what just happened?" test.

---

## Part 2: Let Users Stay in Control

**Goal:** After this part, you will be able to identify every point where a user might want to stop or redirect the AI — and design an exit for each.

**Trigger:** an AI can take action on a user's behalf, and users don't know how to stop it, undo it, or redirect it once it starts.

**Method:**
1. Map every decision point in your AI's workflow — moments where the AI makes a choice that affects the user's work or data.
2. At each decision point: define an override. The override doesn't need to be complex — "undo," "edit before applying," "cancel and start over," "don't do this automatically" are all valid forms.
3. For high-stakes decision points (ones that change data, send communications, commit resources): require explicit confirmation before the AI acts, not just after.
4. For low-stakes decisions: provide a visible override even if you don't require pre-confirmation. The user should be able to see and correct the result without feeling like the system already decided for them.
5. Document which decisions are reversible and which aren't. Irreversible AI actions need pre-confirmation regardless of stakes perception.

**Artifact:** a decision map with override design for each: the decision the AI makes, the override mechanism, and whether it's pre- or post-action.

**Proof:** Ask one person to use the AI feature and then intentionally make a mistake by letting the AI do something they didn't want. Can they recover without your help? If yes, control is designed. If no, there's a decision point without an override.

**Watchout:** override mechanisms that are buried (in settings, in logs, in places users don't naturally look during a task) function as if they don't exist. The override needs to be visible at the moment the user would want to use it — not discoverable after the fact.

**Try This:** write down every AI action in your current feature and mark each as "reversible" or "irreversible." Every irreversible one currently shipping without explicit user confirmation is a trust risk.

---

## Part 3: Explain the Reasoning

**Goal:** After this part, you will be able to surface one sentence of AI reasoning at every high-stakes output — in plain language, without a log dump.

**Trigger:** users don't trust or understand why the AI chose a particular action, recommendation, or result.

**Method:**
1. Identify every AI-generated output in your product where users might reasonably ask "why did it suggest this?"
2. For each output: write a one-sentence explanation of the reasoning in plain language. Not a confidence score, not "based on your data," not a probability — a human-readable cause. "This was flagged because it's the third similar request this week." "This recommendation matches your last confirmed preference."
3. Attach the explanation to the output at the point of first encounter. Not in a tooltip, not in a sidebar — adjacent to the output itself.
4. Test: ask a user to read the explanation. Can they say in their own words why the AI did this? If not, rewrite.

**Artifact:** a one-sentence plain-language explanation for every high-stakes AI output in your product — surfaced at point of encounter.

**Proof:** If a user, after reading the explanation, either accepts the output more confidently or knows specifically why they want to override it, the explanation is working. The goal is informed decision-making, not compliance. Both acceptance and rejection are correct outcomes when the user has the reasoning.

**Watchout:** "our AI analyzed your data" is not an explanation. Neither is a percentage. Users cannot act on those. An explanation that doesn't tell users what they can do differently to get a different result is noise — it performs transparency without providing it.

**Try This:** pick one AI-generated output in your product. Write the one-sentence explanation that would appear next to it. Then ask: if a user read this, would they know what caused the AI to act, and what they could do to change the result?

**After you've run this yourself:** describe your AI's logic to an AI tool and ask it to write plain-language explanations for the top five output states — then check each one against the "would a user know what caused this?" test.

---

## Part 4: Design Graceful AI Failures

**Goal:** After this part, you will be able to apply error state design specifically to AI outputs — distinguishing AI uncertainty from system error.

**Trigger:** the AI gets it wrong, produces a low-confidence result, or can't complete a task — and users have no clear path forward.

**Method:** Apply the error state principles (116) specifically to AI outputs. AI failures are different from system errors in one critical way: the AI often produces something instead of nothing, which is more dangerous — it's a confident-sounding wrong answer rather than an obvious error.

For each AI failure mode, design explicitly:

1. **AI produced something, but it's uncertain:** show the output with a confidence signal and an explicit "review before using" prompt. Don't suppress the output; label its confidence level in plain language.
2. **AI couldn't complete the task:** tell users specifically what it couldn't do ("couldn't find data from before [date]"), offer what it could do instead, and give a path forward. Never say "an error occurred" alone.
3. **AI produced something wrong that users might not catch:** design a recovery path that doesn't require users to start over. Preserve their context, pre-fill what it got right.

Three rules for all AI failure states: name what the AI couldn't do (not "something went wrong"); give a path forward that doesn't start from zero; never imply user fault for an AI limitation.

**Artifact:** a failure state design for each AI failure mode in your product: what the user sees, what it says, and what action they can take next.

**Proof:** If users who encounter an AI failure can explain what happened and what to do next, the failure state is working. If they close the tab, restart, or file a bug report without knowing whether the issue was theirs or the system's — the failure state is invisible.

**Watchout:** designing graceful AI failures is more important than making the AI more accurate. Users forgive failures they understand. They don't forgive failures that leave them stranded, embarrassed, or unsure whether their work is lost.

**Try This:** write down the top two ways your AI feature currently fails or produces uncertain results. For each: draft the user-facing message that names the limitation and offers a next step. Check whether the message passes the "whose fault is this?" test — it should never feel like the user's.

---

## Part 5: Test Trust Calibration

**Goal:** After this part, you will be able to run a simple session that tells you whether users are trusting your AI at the right level — not too much, not too little.

**Trigger:** you've shipped AI features and don't know whether users are accepting AI outputs when they should be questioning them, or questioning them when the AI is reliably right.

**Method:**
1. Run a usability session (215) with one task that requires the user to interact with the AI — either accepting its recommendation, overriding it, or deciding whether to trust it.
2. Choose two scenarios: one where the AI is right, one where it's wrong or uncertain. Don't tell the user which is which.
3. Observe: do they accept the AI's output without evaluating it? Do they override it without looking? Do they know how to tell the difference?
4. After each scenario, ask: "what made you decide to [accept/override/ignore] that?" The reasoning is the data.
5. Trust calibration failure modes to look for: (a) automation bias — accepting AI outputs without review because it feels authoritative; (b) automation distrust — overriding consistently because they don't know what the AI is doing; (c) uncertainty blindness — can't tell when the AI is confident vs. uncertain.

**Artifact:** a trust calibration assessment: which failure mode appeared, what caused it (visibility, explanation, or control design gaps), and which Part 1-4 fix addresses it.

**Proof:** If users accept the AI when it's right and override it when it's wrong — using the reasoning it provided — trust calibration is working. If outcomes are random relative to AI accuracy, or users consistently accept or consistently override regardless of AI quality, calibration is off and the design needs to change.

**Watchout:** the goal isn't maximum trust — it's appropriate trust. A user who blindly accepts every AI output is a trust calibration failure even if the AI is usually right. The design should help users evaluate, not skip evaluation.

**Try This:** observe one person using an AI feature in your product for 20 minutes. Without telling them you're watching trust specifically, count how many AI outputs they accepted vs. questioned. Then check whether their acceptance rate matched the AI's actual accuracy on those outputs. The gap is your trust calibration delta.

---

*This arc assumes you've already run 302 (Spotting AI Surprises → Mocking and Testing an Agent Handoff) and know where in your product AI creates friction. Parts 1-4 design the fixes; Part 5 validates them.*

---

**Try This:** run the trust calibration observation from Part 5 for 20 minutes with one real user. Before you start, write down which failure mode you expect to see most (automation bias, distrust, or uncertainty blindness). Afterward, write one sentence: did the result match your prediction?

**Take this further:** in the next two weeks, revisit the trust calibration delta you measured. Which failure mode appeared — automation bias, distrust, or uncertainty blindness — and which Part 1-4 element most directly addresses it? Write one sentence: what would you change in the design first?

**Judgment exercise:** You're evaluating trust design in a vendor AI tool you've deployed — you have no ability to change the interface. Parts 1-4 assume you can redesign. What can you still learn from running Part 5? What can you recommend, and to whom, and in what form — and what do you give up when the interface is outside your control?

**What Next:** if trust calibration reveals automation bias (users accepting outputs without review), return to Part 1 (visibility design) and Part 3 (explanation) — both reduce over-trust. If it reveals automation distrust (users overriding without looking), Part 2 (control design) may be too prominent — recalibrate the override affordances. If the AI features are being designed from scratch, pair this arc with 147 (AI as Execution Partner) for the foundational framing your team needs before building.
