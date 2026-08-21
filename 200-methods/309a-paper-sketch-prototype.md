# 309a — Paper / Sketch Prototype

**Tier:** 200 — Practice | **Arc:** Prototyping (see 309-prototyping-arc.md for approach selection) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity), 106 (Sketching / Quick Visualization), 113 (Defining Success Before You Start) | **Audience:** General | **Note:** Widest-reach approach — no tools required. Right starting point for any unvalidated concept.

**Goal:** Build and test a paper prototype of a concept in under thirty minutes, with no tools, and get feedback from it the same day.

---

You already know that feedback catches problems. The question is whether you're getting the right kind of feedback — or just the kind visible in what you showed.

Here's the trap. You spend time on a concept. The flow makes sense in your head. You know what question you need answered: does this direction work? You show it in the meeting. And the room tells you how to refine the thing you showed them, not whether you should be building it at all. You walked in with a question. You walked out with a polish list.

This happens because of fidelity. Not fidelity as a quality measure: fidelity as a signal.

---

Y.Y. Wong (1992) studied what happens when people evaluate design artifacts of different levels of finish. The finding was specific: polish signals finished. Rough signals open. When something looks refined, everyone in the room registers it as a decision — their cognitive mode shifts from "is this the right direction?" to "how do we improve this direction?" You can't turn that shift off. Nobody chooses it. It's how artifacts register.

Bill Buxton (2007) makes the distinction this way: a sketch asks a question. A finished artifact answers one. The moment something looks polished enough to take seriously as an answer, you've lost the room's ability to give you directional feedback — even if the direction isn't decided yet. Walker, Takayama & Landay (2002) confirmed this: paper sketches and browser-rendered HTML prototypes on identical tasks produced the same usability findings. Finish level doesn't change what gets caught. It changes what gets said.

This is why a paper sketch works. Not because it's faster (it is), and not because it's cheaper (it is). Because the roughness itself is the mechanism. Roughness tells the person looking at it: this is a question, not an answer. Those two words change everything about what they say next.

> **Polish signals finished. Rough signals open. Those two registrations produce entirely different kinds of feedback.**

---

Use this approach when the question is conceptual: "Does this direction make sense?" or "Is this flow logical?" If the question has moved past direction into navigation specifics or fine-grained interaction, see 309b (Lo-fi Wireframe). If you need something that functions rather than just looks like it functions, see 309c (AI-Generated). Paper is for the moment before those questions. Use it when you're still asking whether you're headed somewhere worth going.

---

**Step 1: Write the question.** At the top of a blank page, write the one question this prototype will answer. "Does this sequence make sense to someone who hasn't seen it before?" One question. If you have two, plan two separate tests — combining them into one prototype is how you end up with feedback that answers neither.

**Step 2: Sketch one state per page.** One page equals one screen or one moment in the flow. Boxes for UI elements, text for controls, arrows for connections. No tools, no rulers. Stick figures are fine. Sketches should look like sketches. That's the point.

**Step 3: Leave visible gaps.** If you don't know what a step looks like, write "?" or "unknown" and move on. Don't fill a gap with a guess you haven't labeled. Visible gaps tell your reviewer exactly where to focus.

**Step 4: Annotate every simulated interaction.** For each tap target, button, or transition, write what happens. "Tapping this shows page 3." "This triggers a confirmation state." The annotation is the method. A sketch without annotation is just a drawing — the annotation tells your reviewer what to imagine.

**Step 5: Number the pages and draw the path.** Indicate which page follows which. Number them, draw connecting arrows, or write the destination page number next to each annotated interaction. The path is the prototype. The sketches are the pages in it.

---

When you're done, you have a set of annotated sketches — minimum three pages covering the core task path — with the question written at the top of page 1, numbered pages, labeled interactions, and visible gaps marked as unknown. That's the artifact. Thirty minutes to build.

(And yes, it will look like something your twelve-year-old made in a free period. That's correct. You drew it right.)

---

The consistent failure mode is digitizing the sketches before getting feedback. Moving them into Figma, Miro, or a slide deck to "make them clearer for stakeholders." Smart practitioners do this because they've learned that rough work isn't taken seriously in professional contexts — and in most work, that's a correct principle. They're applying it in a context where it backfires.

A digitized sketch raises the fidelity signal before the question is answered. It converts directional feedback into refinement feedback. The artifact now looks like it cost something, which makes changing direction feel like waste. Virzi, Sokolov & Karis (1996) found that paper prototypes catch the same usability problems as polished ones — including the most serious ones. You're not losing resolution by keeping it rough. You're preserving the signal that keeps feedback honest.

The rule: paper until one round of feedback on the question you wrote at the top. Only then decide whether higher fidelity would answer a different question.

When multiple stakeholders need to see the same sketches, run a walk-through together rather than distributing images for individual review. Narrating what each page represents ("this is the state after someone fills in the form") keeps the conversation in question mode.

---

For something you're working on right now, write the question at the top of a page. A feature, a flow, a process change you're currently figuring out — pick one. Sketch the states someone would move through to answer it. Annotate every interaction. Give it thirty minutes.

When you're done, photograph the sketches straight-on and show them to one person today. Ask: "Walk me through what you think is happening here." Don't explain. Listen for where they need to be corrected — those are the gaps the prototype revealed.

If the person can't be in the same room: photograph the sketches and walk through them on a video call, narrating what each page represents. You get directional feedback on whether the concept makes sense. That's the only question paper needs to answer.

---

When they ask about specific steps — "wait, what happens when I tap this?" — rather than the visual design, the fidelity is calibrated correctly. Questions about how something works are signal at this stage. Comments about how it looks are noise. Separate them clearly.

One false positive: a participant who says "I think I understand it" but can't predict what happens at the next step. Ask: "What do you think would happen if you tapped here?" Verbal confirmation without predictive accuracy isn't validation.

---

In the next two to three days, take the same sketches to a second person with a different perspective on the problem: a different role, a different relationship to the flow. Ask: "What did you expect to happen here that didn't?" Afterward, write one sentence: what assumption did you discover you were making that you now know isn't shared?

If you share that sentence in a team channel, you'll see what others noticed too.

---

After you've run this yourself: describe the sketch to an AI tool in words — "a paper prototype with [N] pages: page 1 shows [description], page 2 shows..." — and ask it to list questions a first-time user would have about the concept. Use that list to add annotations before the next review session, or to identify gaps you haven't addressed.

---

Once the concept is validated, 309b (Lo-fi Wireframe) tests the navigational structure at higher fidelity. If you're ready for a structured session with a real participant, 215a (Moderated Usability Session) covers running it. If the sketch revealed assumptions about who the user is that haven't been tested, 301 (From a Vague Ask to a Real Persona) is the next move.

---

**Sources**

Wong, Y.Y. (1992). Rough and ready prototypes: Lessons from graphic design. *Short Papers Proceedings of ACM CHI '92*, 83–84.

Buxton, B. (2007). *Sketching user experiences: Getting the design right and the right design.* Morgan Kaufmann.

Virzi, R.A., Sokolov, J.L., & Karis, D. (1996). Usability problem identification using both low- and high-fidelity prototypes. *Proceedings of ACM CHI '96*, 236–243.

Walker, M., Takayama, L., & Landay, J.A. (2002). High-fidelity or low-fidelity, paper or computer? Choosing attributes when testing web prototypes. *Proceedings of the Human Factors and Ergonomics Society Annual Meeting, 46*(5), 661–665.
