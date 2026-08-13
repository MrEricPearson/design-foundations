# Conversational Prototype
**Tier:** 200 — Practice | **Arc:** 309 (Prototyping) | **Prereqs:** 177, 132, 147 | **Wave:** 4

**Goal:** Run a conversational prototype session that tests the logic, language, and flow of a voice or chat interaction — before building the dialogue system.

**Prior Knowledge Hook:** Most practitioners approach conversational AI or chatbot design the same way they approach screen design: they design what it should say, then build it, then test it. This sequence has a specific failure mode: conversational design has to work across hundreds of possible user inputs, and no amount of design-time review reveals the gaps in the dialogue logic that become obvious the moment a real user says something unexpected. Testing conversation logic requires live conversation — and live conversation doesn't require a built system to test.

**Trigger:** Use this when designing voice assistants, chatbot flows, AI conversational features, or any system where the interaction is primarily language-based rather than point-and-click. Also useful for testing conversational onboarding, guided workflows, or support flows that walk users through a process via dialogue.

**Why this works:** Conversation is a protocol. Both sides operate with expectations about turn-taking, topic maintenance, appropriate responses to ambiguity, and what happens when the expected input doesn't come. Conversational design breaks when the protocol assumptions diverge from user behavior — when the system expects a confirmation and the user asks a follow-up question, or when the system handles "yes" but the user says "sure" or "I guess so" or "maybe?" A conversational prototype surfaces these divergences by running the protocol with a real user before encoding it in a system. Every unexpected user turn is a gap in the design.

The mechanism: a human plays the "system" role in real time, responding to user inputs according to a designed script. The user doesn't know they're talking to a person. The facilitator captures every moment where the human-playing-system had to improvise — every user input that the script didn't account for — as a design gap.

**Method:**

**Step 1: Map the intended dialogue.** Write out the expected conversation — the "happy path" — as a structured flow: system turn, user turn, system response. Include the 3-5 most likely variations at each branch. This is the script your human operator will work from.

**Step 2: Identify the gap risk areas.** Before the session, review your dialogue map and mark the 3-5 points where user input is most likely to diverge from expectation. These are the moments to watch most closely in sessions.

**Step 3: Set up the session format.** The user interacts with the interface as if it were real — a voice interface, a chat window, an app. The human operator types or speaks responses in real time from the script, improvising when the user goes off-script. The facilitator observes and notes every improvisation.

**Step 4: Run a debrief focused on off-script moments.** After the session, review every moment where the operator had to improvise. Each one is a dialogue gap: a user input the script didn't handle. Categorize each gap: is it a common input the system should handle (add to the design), or an edge case the system should gracefully decline?

**Step 5: Revise the dialogue map.** Add the gaps discovered. Re-run with another participant until the dialogue map handles most inputs without operator improvisation.

**Artifact:** A revised dialogue map with annotated gaps from sessions — each gap marked with what the user said, what the system said in the prototype, and whether that response should be encoded in production.

**Watchout:** The smart practitioner failure mode: the operator tries to "save" off-script user moments by improvising a good response — producing a seamless experience — without flagging the gap. The session feels successful. The design doesn't improve. The gap shows up in production. The operator's job is to improvise AND flag, clearly and immediately, every time they go off-script. A session with many flags is a session that produced valuable findings. A session with no flags usually means the operator was compensating rather than revealing.

**Try This:** Take a conversational flow you're currently designing or planning. Write the dialogue map for the top 3 user scenarios. Then find a colleague and role-play it — one of you as the user, one as the system. The person playing the system should only respond based on the written script, and mark every moment they have to make something up. Each made-up moment is a design gap.

**Proof:** The conversational prototype worked if you have a list of specific dialogue gaps — user inputs the designed system couldn't handle — with decisions about each: should these be added to the happy path, handled as graceful fallbacks, or considered out of scope? The false positive: a session where the user stayed entirely on the happy path. This tells you the happy path works (valuable) but tells you nothing about what happens when users don't (which they always will). Successful conversational testing requires users who diverge, not users who comply.

**Take This Further:** Over the next 3-5 days, run one more script with a different user. Compare the gaps: are they the same gaps or different ones? Patterns across users are design priorities. Unique gaps are edge cases. Write one sentence: what was the most surprising off-script moment, and what does it tell you about the user's mental model of what this system can do?

**After you've run this yourself:** AI can help map the "long tail" of likely user inputs — describe the intended dialogue and ask for variations the user might express at each turn. Use this to stress-test your script before the session. A script that accounts for 80% of user variations will produce more signal in sessions because the operator flags only the genuine gaps.

**What Next:** Conversational prototypes test dialogue logic. When the dialogue is sound and you need to test interaction patterns in a visual interface with more fidelity, read 309f (High-Fidelity Prototype). When the conversation is part of a larger service journey, read 309g (Service Prototype) to test how it fits.
