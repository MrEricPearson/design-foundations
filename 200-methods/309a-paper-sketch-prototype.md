# 309a — Paper/Sketch Prototype
**Tier:** 200 — Practice | **Arc:** Prototyping (see 309-prototyping-arc.md for approach selection) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity), 106 (Sketching/Visualization), 113 (Defining Success Before You Start) | **Note:** Widest-reach approach — no tools required. Right starting point for any unvalidated concept.

**Goal:** After this piece, you will be able to build a paper prototype of a conceptual direction in under 30 minutes — without any tools — and get feedback from it the same day.

**Prior knowledge hook:** Here is the model most practitioners carry about getting feedback: the more polished the artifact, the more useful the feedback — because stakeholders take it seriously and can evaluate it properly. This model has a hidden cost it never reveals: when something looks polished, every person in the room registers "this is what we're building." Their brain shifts from directional evaluation (is this the right direction?) to refinement evaluation (how do we improve this direction?). Directional feedback requires a signal that direction is still open. Roughness is that signal.

**Trigger:** Use this approach when the question is conceptual: "Does this direction make sense?" or "Is this flow logical?" If the question is about navigation specifics or fine-grained interaction, see 309b (Lo-fi Wireframe). If you need something that functions rather than just looks like it functions, see 309c (AI-Generated).

**Why this works:** Fidelity is a commitment signal. A polished artifact — a high-quality mockup, a functional prototype, a styled deck — communicates to everyone in the room that decisions have been made. Their cognitive mode shifts: instead of "should we go this direction?", they're asking "how do we improve what we've decided?" A sketch communicates the opposite: this is a question, not an answer. Those two registrations produce entirely different kinds of feedback. Only the second gives you the feedback you need at the concept stage. The roughness of a paper sketch is not a limitation — it is the mechanism by which the prototype earns directional feedback instead of refinement feedback.

**Method:**
1. **Write the question.** At the top of a blank page, write the one question this prototype will answer. "Does this sequence make sense to someone who hasn't seen it before?" One question. If you have two questions, plan two separate tests — don't combine them into one prototype.
2. **Sketch one state per page.** One page = one screen or one moment. Use boxes for UI elements, text labels for controls, arrows for connections. Stick figures are fine for people. Text is fine instead of drawings. No tools, no rulers — sketches should look like sketches.
3. **Leave visible gaps.** If you don't know what a step looks like, write "?" or "unknown" in that space and move on. Don't fill gaps with guesses you haven't labeled as guesses.
4. **Annotate every simulated interaction.** For each tap target, button, or transition: write what happens when a user interacts with it. "Tapping this area shows page 3." "This triggers a confirmation state." Annotation is the method — a sketch without annotation is just a drawing.
5. **Number the pages and draw the path.** Indicate which page follows which by numbering them and drawing connecting arrows, or by writing the destination page number next to each annotated interaction.

**Artifact:** A set of annotated sketches — minimum 3 pages covering the core task path — with the question written at the top of page 1, numbered pages, labeled simulated interactions, and visible gaps marked as unknown.

**Watchout:** The consistent failure mode is digitizing the sketches before getting feedback — moving them into Figma, Miro, or slides to "make them clearer for stakeholders." The reason smart practitioners do this: they've learned that rough work isn't taken seriously in professional contexts. In most work, polish signals quality. They're applying that correct principle in a context where it works against them. A digitized sketch raises the fidelity signal before the question is answered, converting directional feedback into refinement feedback — and the artifact now looks like it cost something, which makes changing direction feel like waste. The rule: paper until one round of feedback on the question you wrote at the top. Only then consider whether higher fidelity answers a different question.

## When You Can't Run the Full Version

**If participants can't be in the same room:** Photograph the sketches (straight-on, good lighting) and share them as images with numbered annotations. Walk through them in a video call or asynchronous video — narrating what each sketch represents and asking the participant what they'd expect to happen at each decision point. The feedback quality is lower than in-person, but the method still works.

**What you still get:** concept-level feedback on whether the direction makes sense and where the biggest gaps in the mental model are.

**What you give up:** the ability to put the sketch in someone's hands and watch them physically interact with it — which often reveals confusion points that verbal narration doesn't.

**Don't do this:** digitize the sketches to make them look "professional" before getting feedback. The roughness is doing communication work. A digitized version of a paper sketch is worse than the paper sketch for testing — it looks like a decision, not a question.

## At Enterprise Scale

When multiple stakeholders need to review the same prototype: photograph the sketches and present them in a shared session rather than distributing images asynchronously. Stakeholders reviewing sketches independently tend to evaluate them as finished proposals; stakeholders reviewing them together in a walk-through tend to engage with them as questions. Narrating what each sketch represents — "this is the state after someone has filled in the form" — keeps the conversation in question mode rather than approval mode.

**Try This:** For something you're currently working on, write the question at the top of a page. Sketch the states — one per page — that someone would pass through to answer it. Annotate every interaction. Photograph it when you're done. Show it to one person today and ask: "Walk me through what you think is happening here." Notice where they need to be corrected — those are the gaps the prototype revealed.

**Proof:** When the person you're testing with asks about specific steps ("wait, so what happens here when I tap this?") rather than evaluating the visual design ("the colors are off"), the fidelity is calibrated correctly. Questions about how something works are signal at this stage; comments about how it looks are noise.

The false positive: a participant who says "I think I understand it" but cannot predict what happens at the next step. Understanding at the concept level means being able to predict the next state — not just recognizing what they saw. Ask: "What do you think would happen if you tapped here?" If they can't predict it, the concept hasn't been understood yet. Verbal confirmation without predictive accuracy is not validation.

**Take This Further:** In the next 2-3 days, take the same sketches to a second person with a different perspective on the problem (a different role, a different relationship to the flow). Ask: "What did you expect to happen here that didn't?" Write one sentence: what assumption did you discover you were making that you now know isn't shared?

**After you've run this yourself:** Describe the sketch to an AI tool in words — "A paper prototype with [number] pages: page 1 shows [description], page 2 shows [description]..." — and ask it to list questions a first-time user would have about the concept. Use that list to add annotations to the sketches before the next review session, or to pre-empt the gaps you haven't addressed.

**What Next:** Once the concept is validated, move to 309b (Lo-fi Wireframe) to test the navigational structure at higher fidelity. If the question is answered and you're ready to test with a real participant in a structured session, read 215a (Moderated Usability Session). If the sketch reveals assumptions that haven't been tested about who the user is, read 301 (From a Vague Ask to a Real Persona).
