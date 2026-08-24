# Conversational Prototype
**Tier:** 200 — Practice | **Part of:** 309 Prototyping Arc (Part 5 of 9) | **Prereqs:** 177, 132, 147, 266 | **Supports:** 308

---

Test dialogue logic before building the system — script the paths a conversation can take, simulate them with a real person, and find where input diverges from expectation.

---

When interaction happens through language rather than visible controls, the interface disappears. No button to click wrong. No dropdown listing the options. What the system says, and how it says it, is the whole product.

If you're building something where the primary interaction is language: a chatbot, a voice assistant, an AI agent interpreting instructions. The team is almost certainly writing conversation flows in code. Questions keep surfacing that nobody can answer without seeing it work. What happens when someone asks two things at once? What does the system say when it doesn't understand? What does confirmation sound like when there's no UI to display it? Building first means discovering these problems after the dialogue logic is locked in.

---

A conversational prototype tests dialogue structure before implementation. You script the paths a conversation can take — what the system says, what users might say back, how the system branches, where it confirms or clarifies. Then you simulate it: one person plays the user, another (the wizard) plays the system by reading scripted responses and choosing which path to follow based on what the user actually says.

Three things surface that code won't show you until it's too late: where users say things you didn't script for, where the system's phrasing creates confusion, and where the conversation needs repair strategies you hadn't planned.

This works because conversation follows structure even when it feels freeform. Sacks, Schegloff, and Jefferson (1974) demonstrated that turn-taking is systematically organized: speakers signal completion, listeners know when to start, and violations feel like interruptions even without literal overlap. Clark (1996) showed that conversations succeed only when both parties work to establish common ground, building shared understanding across turns. Scripting makes those structures visible. When users diverge from your script, that's not user failure. That's your script failing to account for how people actually talk.

---

1. Script the happy path turn by turn. Write exact words, not descriptions. "The system asks for account details" is not a script. "Which account would you like to check — personal checking, business checking, or savings?" is. End when the task is complete.

2. Add one branch for ambiguity. Find the turn where input is most open-ended and write three variations of what the user might say: the expected answer, a clarifying question, and something adjacent but off-script. Pick the three most representative responses.

3. Script the error path. Write what the system says when it doesn't understand, then write what happens next. An error path without a way forward just ends the conversation.

4. Write the confirmation pattern for any action the conversation results in. Grice (1975) called this the maxim of quality: make contributions you have evidence for. In conversational systems, confirmation is how users know the system understood them. Write what the system says to confirm, and what it does if the user says "no, that's not right."

5. Simulate with a real person. One plays the user. Another plays the system, reading scripted responses exactly as written, choosing branches based on what the user says. Don't improvise. If the wizard has to make something up, that's a gap. Mark it.

6. Run it three times with different people as users. Give each person the task goal, not the script. Write down where they said things you didn't script for, where the phrasing confused them, and where conversations broke down completely.

7. Revise based on what broke, then run again. If users asked clarifying questions at the same turn, rewrite that prompt. If they phrased answers you didn't anticipate, add those as branches. The first script is never right.

---

What you end up with is a dialogue script with annotated divergence points: the scripted paths plus notes on where real users went off-script and which system phrasings caused confusion. This becomes the specification for implementation. Your edge cases are named before they're edge cases in production.

---

You'll write system responses that sound fine on paper but feel robotic when spoken aloud. This isn't a writing-quality problem. It's a medium mismatch. Written language leans toward completeness and precision, while spoken language works better short and informal. The simulation catches it: if the wizard reading the script sounds like a terms-of-service document, rewrite it. (If you've ever seen a bot response make a room go quiet in the wrong way, you know exactly what this sounds like.) Raluca Budiu's research at Nielsen Norman Group (2018) found that users tolerated chatbot failures to understand them, but grew annoyed when responses were flat and repetitive, as if nobody was home on the other end. How a conversational system sounds is not a polish concern. It's a trust concern.

---

Pick a task in something you're building that requires back-and-forth: asking for input, confirming a choice, handling an error. Script a three-turn conversation: system prompt, user response, system confirmation or follow-up. Read it aloud to someone and ask them to respond naturally, as if they were the user. Give them the task, not the script. If their first response isn't one you scripted, you just found your first branch point.

---

If the person playing the user responds with something you didn't script and the wizard has to pause to decide what to say next, that's a gap your script needs to cover. If they respond and the wizard reads the scripted reply without hesitating, that path is working.

---

Over the next three days, script and simulate one full conversation flow for a feature with language-based interaction. Run it with at least two different people as users. Afterward, write one sentence: where did both users diverge from your script at the same turn, and what does that turn need to say differently?

---

After scripting and simulating manually, give an AI agent the user's task goal and let it respond to your prompts. Run it twenty times. The patterns in where it diverges show edge cases three manual sessions won't catch. Run the manual simulation first, because AI responses are statistically plausible but not representative of how any real user actually talks. The manual run teaches you what conversational breakdown feels like. The AI run shows how many ways it can happen.

---

Conversational prototypes test dialogue structure. They don't test whether automated conversation is valuable to users in the first place. For that, 309d (Wizard of Oz Prototype) tests system behavior before building automation. If the interface needs no visible UI, 266 (No UI as Design Goal) covers when invisible interfaces are a design decision, not a missing piece. Once the system is built, 308 (Designing for AI Trust) covers calibrating trust when users can't see system state.

---

**Sources**

Clark, H. H. (1996). *Using Language*. Cambridge University Press. Grounding theory: conversation succeeds through the collaborative establishment of common ground — shared understanding built across turns.

Grice, H. P. (1975). Logic and conversation. In P. Cole & J. Morgan (Eds.), *Syntax and Semantics 3: Speech Acts* (pp. 41–58). Academic Press. The cooperative principle and conversational maxims, including the maxim of quality (make contributions you have evidence for), which grounds confirmation patterns in conversational design.

Nielsen Norman Group. Budiu, R. (2018, November 25). The user experience of chatbots. nngroup.com. Usability research on chatbot interaction patterns; key finding: users tolerated chatbot failures to understand input but grew annoyed when responses were flat and repetitive, underscoring that language quality is a usability concern, not a polish concern.

Sacks, H., Schegloff, E. A., & Jefferson, G. (1974). A simplest systematics for the organization of turn-taking for conversation. *Language*, *50*(4), 696–735. Foundational conversation analysis demonstrating that turn-taking follows systematic rules — speakers signal completion, transitions occur at defined points, and violations feel like interruptions even without literal overlap.
