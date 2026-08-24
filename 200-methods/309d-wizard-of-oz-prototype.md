# Running AI You Haven't Built
**Tier:** 200 — Practice | **Arc:** Prototyping (309) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity) | **Audience:** General

*Someone just specced an AI feature and nobody's sure yet whether users will actually trust it.*

---

Your team has agreed on a feature. The AI suggests the next action, scores the incoming request, or responds in natural language. You know roughly what it needs to do. What nobody knows: whether users will find its responses useful, trust them, or act on them. The algorithm doesn't exist yet. And if you wait until it does, you're evaluating something that took months to build.

There's a faster path.

---

If you've run a usability session before, you know the basic setup: a user, a task, and something to interact with. This method extends that setup into territory where the thing to interact with includes automated behavior — except the automation is a person, and the user doesn't know it.

Use this when you're building something that produces responses rather than just displaying information. Smart recommendations, AI-generated summaries, a system that classifies inputs and responds accordingly. Any time the feature's value depends on the system doing something intelligent, and you need to know whether that matters to users before you build it. Before building it, not after.

---

Jeff Kelley coined the name at Johns Hopkins in 1983, testing a calendar application that responded to natural language. There was no technology behind it. A person in another room read the user's inputs and responded through the interface in real time. The user believed they were talking to a system. What Kelley found: the conversations users wanted to have were quite different from what the engineering team assumed they'd want. That gap was invisible until someone tested it before building it.

The same year, Gould, Conti, and Hovanyecz (1983) published similar results in Communications of the ACM: a simulated listening typewriter where human operators posed as speech recognition. Their finding was the same. Simulation could reveal whether a technology would be useful to real users, without building it first.

Paul and Rosala (2024) at Nielsen Norman Group describe the current relevance clearly: the method "lowers investment risk into complex, costly technologies such as generative AI" by answering the value question before committing to the implementation.

The mechanism is this: you're not testing the AI. You're testing whether users find AI-like responses useful in this context, with this information, on this task. Those are different questions. Only one of them can be answered before the algorithm exists.

---

**Step 1: Define the scenario.** Write one sentence: what does the user think the system does, and what specific interaction are you testing? "The system suggests a next action after a request is submitted" is testable. "The system is smart" isn't. Two scenarios means two sessions.

**Step 2: Set up the façade.** Build the interface the user sees — whatever makes the interaction feel real without requiring a working backend. A chat window. A form that appears to process. A voice interface piping through a speaker. You're building the surface, not the mechanism.

**Step 3: Prepare the wizard.** The wizard is the person who operates the system in real time, watching inputs and generating the responses users see as system output. Before the session, write down two things: which responses are pre-prepared versus improvised, and what information the wizard is allowed to use. That second item is the constraint. The wizard can only draw on information the real system would have access to. If the real system won't know the user's history outside this session, the wizard doesn't use it either.

**Step 4: Run the session.** The user interacts, the wizard responds, and the facilitator observes. Don't break the illusion. Build in a "processing" indicator if wizard responses take longer than expected. If the wizard can't respond appropriately, log it and use the fallback: "I'm not able to complete that request right now." The moments the wizard hesitates are the data.

**Step 5: Debrief.** Go through every response the wizard gave. Mark each one: confident or hesitant? Did it require information the real system would have, or did the wizard invent something? Where did the user do something unexpected? That list is what you take out of the session.

---

When you're done, you have two columns: responses the wizard gave confidently, and responses where the wizard hesitated, improvised, or couldn't respond. The first column tells you where the algorithm is tractable. The second tells you where it's hard: as a behavior-in-context observation, not an engineering estimate. Yocco (2025) puts it directly: "Human limitations during simulation directly inform where the eventual product needs robustness most." The wizard struggled because they couldn't respond naturally to what the user actually did. The real system faces the same problem.

---

The failure mode that catches experienced teams: the wizard improvises with information the real system would never have. They know the user's intent from context, from a previous conversation, from something outside the session. The response feels right, the user seems satisfied, and the team learns nothing useful. They've tested a system that can't be built.

Before the session, write down exactly what the real system will know at each interaction point. Give that list to the wizard. They stay inside it. (If you've ever watched a wizard give warm, personalized responses during a test of a system that literally won't know the user's name — now you know what that produces.)

---

Pull a feature your team is currently planning that involves automated response, classification, or AI-generated output. Write the scenario sentence. Sketch the surface the user would see. Then run it with a colleague: you're the user, they're the wizard, using only the information on a list you write together beforehand. Run five to ten minutes of interaction. Debrief together: where did they hesitate?

Give the whole setup 30 minutes. You'll have a real finding today.

---

If the debrief produces a short list of wizard-hesitant moments, the interaction pattern is probably well-understood and the algorithm tractable. A long list means you've surfaced the implementation challenge before anyone started building. That's exactly what the session was for.

---

Over the next week, watch for moments in planning when a feature's behavior is getting specced without anyone testing whether users would find it useful. That's the signal. Run the session before the sprint starts, not after. Write one sentence afterward: what did the session reveal that the spec didn't know?

---

After you've run this yourself: AI is useful in the prep phase. Describe the scenario to a language model and ask it to generate ten things users might say that fall outside your expected scope. Have the wizard practice responding to those before the real session. Watch which ones make the wizard pause. Those are it.

---

If the session surfaces confusion about what the system is even doing, 168 (Explainability vs. Transparency in AI) is the next read before speccing the algorithm. If the response format mattered more than expected, 205 (Content Design) covers the content layer of system responses. When you're ready for real participants, 215a (Moderated Usability Session) runs that process.

---

**Sources**

Gould, J. D., Conti, J., & Hovanyecz, T. (1983). Composing letters with a simulated listening typewriter. *Communications of the ACM, 26*(4), 295–308. Finding: Simulating a speech-recognition system with a hidden human operator — before the technology existed — revealed whether the technology would be useful to real users. Even imperfect simulation provided reliable insight into value before any implementation investment.

Kelley, J. F. (1983). *Natural language and computers: Six empirical steps for writing an easy-to-use computer application* [Doctoral dissertation, Johns Hopkins University]. Finding: Testing a natural language calendar application via hidden human simulation revealed that the conversations users wanted to have were substantially different from what the engineering team had designed for — a gap invisible without live user interaction before building.

Paul, S., & Rosala, M. (2024, April 19). The Wizard of Oz method in UX. *Nielsen Norman Group*. https://www.nngroup.com/articles/wizard-of-oz/ Finding: The method lowers investment risk into complex technologies such as generative AI by simulating system behaviors before they can be built; specifically suited for testing chatbots, recommendation algorithms, and real-time information systems.

Yocco, V. (2025, July 10). Unmasking the magic: The Wizard of Oz method for UX research. *Smashing Magazine*. https://www.smashingmagazine.com/2025/07/unmasking-magic-wizard-oz-method-ux-research/ Finding: Human limitations during simulation directly inform where the eventual product needs robustness most; unexpected user inputs and moments where the wizard cannot respond naturally expose the interaction patterns a real system must accommodate.
