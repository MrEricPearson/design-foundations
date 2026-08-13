# 309b — Lo-fi Wireframe Prototype
**Tier:** 200 — Practice | **Arc:** Prototyping (see 309-prototyping-arc.md for approach selection) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity), 158 (Task Statement Design), 113 (Defining Success Before You Start) | **Note:** Navigational testing approach — assumes the concept has been validated; see 309a first if concept is still open.

**Goal:** After this piece, you will be able to build a navigable wireframe prototype that tests whether a user can reach their goal — without visual design choices obscuring whether the structure itself works.

**Prior knowledge hook:** The wrong model: visual design choices (color, typography, spacing) communicate priority — and therefore, testing a polished design is more rigorous than testing a stripped-down one, because the fully realized artifact better represents what users will see. The mechanism this model misses: visual design can compensate for structural failures. A beautifully styled interface gives users aesthetic orientation even when the navigation structure is broken — they follow visual cues to the next action rather than structural ones. Strip the visual design and the structure must carry the full cognitive load. If the structure fails without visual guidance, it will fail in production too — just invisibly, until someone asks why users aren't completing tasks.

**Trigger:** Use this approach when the question is navigational: "Can someone get from here to what they need?" or "Is the decision path between states clear?" The concept direction is already validated (or known) and the question is now about structure and flow. If the concept is still open, use 309a first. If the question requires working interaction behavior, use 309c.

**Why this works:** When visual hierarchy is present, users are guided through it — a primary button, a bold heading, a highlighted path — and may navigate successfully due to aesthetic cues rather than structural ones. The navigation structure didn't have to work; the visual design did the work instead. Without visual design, cognitive guidance is purely structural. A participant who navigates correctly through a lo-fi wireframe did so because the structure worked — not because a visual cue directed them. That's the only kind of navigation finding worth acting on before the visual design is built. Lo-fi testing surfaces structural failures that high-fidelity testing hides.

**Method:**
1. **Write the task statement.** Before building anything: write the task a participant would attempt. Per 158 (Task Statement Design) — describe the goal without naming the path: "Find the place where you'd submit a request for equipment." Not "click on the Equipment menu." One task per prototype session.
2. **Map the minimum flow.** List every screen or state the participant must pass through to complete the task, start to finish. Don't design screens that aren't on this path — scope ruthlessly. If you're tempted to add screens for edge cases before anyone has tested the main path, stop.
3. **Build at box-and-label fidelity.** Rectangles for UI elements. Text labels for controls. Boxes with an "X" for images. No styling. No color. No visual hierarchy refinements. If you find yourself adding visual polish, add a text note instead: "visual design goes here." Keep it ugly on purpose — ugly signals "this is still in progress."
4. **Connect the screens.** Create one clickable hot-spot per meaningful interaction in the task path. Label each hot-spot with what it triggers: "tap → goes to screen 3." Don't create hot-spots for things outside the scope of the task. If tapping something leads to a screen that isn't part of the test, label it "out of scope" — don't hide it and don't build it.
5. **Label everything as a prototype.** At the top of every screen: "Wireframe — not final design." This is not optional when stakeholders are in the room. A wireframe that looks like it's waiting for color will be treated as waiting for color. A wireframe labeled as a wireframe will be treated as a test.
6. **Label fake data.** If any screen shows example data, label it "example data — not real" on the screen. Data that looks realistic in a wireframe gets evaluated for accuracy, not for structure.

**Artifact:** A navigable click-through — minimum 3-5 connected states covering the core task path — at box-and-label fidelity, with a documented task statement, all screens labeled as wireframes, and all example data labeled as fake.

**Watchout:** Building beyond the task path before testing the main path. The reason smart practitioners do this: thoroughness is a professional value — a document that covers all cases is more rigorous than one that covers only the main case. Applying that correct principle to a prototype scope creates a test where participants can wander off the task path in multiple directions, where deviation is harder to interpret (was it the structure or the extra screens?), and where the finding on the main path is diluted by findings from paths that haven't been prioritized. The task path is the minimum scope needed to answer the test question. Everything else is test scope that will distort the finding on the question you actually needed to answer.

## When You Don't Have a Design Tool

"Wireframe tool" does not mean "Figma." A navigable click-through can be built in:
- Miro (connect frames with links)
- Google Slides or PowerPoint (connect shapes to other slides with hyperlinks)
- Printed pages, taped to a wall, pointed to during a session
- Any other tool that connects labeled states in a sequence

The artifact is a connected sequence of labeled states. The tool is irrelevant.

## At Enterprise Scale

**Multi-stakeholder review:** If multiple stakeholders need to review the same wireframe prototype and can't be in the same session: record a walk-through (narrate while clicking through it) and share the recording. Stakeholders reviewing a live prototype together tend to debate the prototype; stakeholders reviewing async tend to flag different issues independently — both are valid, and the async approach often surfaces more diverse feedback because people aren't anchoring to what others say first.

**Multi-role flows:** If the task path involves multiple user roles (an approver receives something a requester submits, for example), build one task per role in the same prototype — connected by the state that passes between them. Don't build one "combined" flow that tries to show what everyone experiences simultaneously; that creates a prototype no single person can navigate from their own perspective.

**Try This:** For something you're currently working on, write a task statement. List the screens on the task path — start to finish, main path only. Build boxes-and-labels for each screen. Connect them with one hot-spot per interaction. Show it to one person today: give them the task statement, put the prototype in front of them, and watch without explaining what to do. Note where they hesitate or go the wrong way. Those are the structure problems.

**Proof:** When a participant gets stuck at a specific screen and can't figure out what to tap next — that's navigational confusion the wireframe surfaced before visual design was built. When a participant moves through without hesitation, the structure works.

The false positive: a participant who completes the task because they're familiar with similar products — they navigated by importing mental models from elsewhere, not because your structure worked. A participant who succeeds immediately and confidently without ever hesitating is less diagnostic than one who pauses, considers, and makes the right choice. To distinguish: after the session, ask "what were you thinking when you decided to tap [element] on screen 2?" If the answer is "that's just where I'd expect it to be," the structure succeeded because it matched convention, not because it worked on its own terms. Both outcomes are valuable — but they mean different things.

**Take This Further:** In the next 2-3 days, run the same wireframe with a second participant who has a different level of familiarity with the product area — someone newer to it, or someone with a different role. Write one sentence: what did the second participant get stuck on that the first didn't? What does that tell you about which assumptions in your structure aren't universal?

**After you've run this yourself:** Describe the task path to an AI tool and ask it to play the role of a first-time user: "Starting on screen 1, which says [description], I'm trying to [task]. Where do I go?" Walk through the AI's narration against your click-through and note where the AI's instinct diverges from what your prototype routes them to. Divergences are navigation structure questions worth testing with a real participant.

**What Next:** When the structure is validated, if you need to test the interaction behavior (not just the structure), move to 309c (AI-Generated Prototype) for a functional version. If you're ready to test with a participant in a structured session, read 215a (Moderated Usability Session) or 215b (Unmoderated Usability Testing). If the wireframe reveals confusion at a specific handoff point, read 303 (One Feature, Three Handoffs).
