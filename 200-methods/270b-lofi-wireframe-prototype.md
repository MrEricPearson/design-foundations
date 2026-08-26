# 270b — Lo-fi Wireframe Prototype
**Tier:** 200 — Practice | **Arc:** Prototyping | **Prereqs:** 177, 132, 158, 113

**Goal:** After this piece, you can build a navigable wireframe prototype that tests whether a user can reach their goal — without visual design choices obscuring whether the structure itself works.

---

You already know that different fidelity levels serve different questions. That's the problem. What's easy to miss is that visual design doesn't just change how a prototype looks — it changes what the test can actually measure.

---

Use this when the question is navigational: can someone get from where they start to what they need? The concept direction is already validated. What's still open is whether the path through it is clear. If the concept is still uncertain, you're not ready for this yet. If the question requires working interaction behavior — data loading, conditional states, error handling — you need something functional. This sits between those two: a connected structure, testable today, before any visual work has happened.

---

When visual hierarchy is present, participants use it. A primary button, a bold heading, a highlighted path — these guide users through an interface even when the navigation structure underneath is ambiguous or wrong. Kurosu and Kashimura (1995) established this directly: the correlation between aesthetics and *perceived* ease of use is stronger than the correlation between aesthetics and *actual* ease of use. Users experience an attractive interface as more usable than it is. In a test, that means a participant can navigate successfully because a visual cue pointed them forward — not because your structure worked.

Strip the visual design, and you remove that compensation. The structure has to carry the full cognitive load. (If you've ever polished a prototype to have it ready for a stakeholder review, then watched users completely miss the main action — you've seen this exact dynamic.) Virzi, Sokolov, and Karis (1996) compared paper prototypes and high-fidelity versions of the same products and found substantially the same usability problems in both conditions. Lo-fi testing doesn't produce weaker findings. It surfaces structural failures without visual design covering them first.

**Strip the visual design and you find out if the structure works.**

---

Start with the task statement. Before anything gets drawn: write the task a participant would attempt. It describes a goal, not a path: "find where you'd submit a request for equipment," not "click on Equipment." The task statement is the scope of the prototype. Everything in it either serves the task or doesn't belong there.

From the task, map the minimum flow. List every screen or state a participant must pass through to complete the task — start to finish, main path only. Stop. Don't build screens that aren't on this path. The temptation to cover edge cases before testing the main route is real, but a prototype that branches in five directions makes it much harder to interpret where someone went wrong.

Build at box-and-label fidelity. Rectangles for UI elements. Text labels for controls. No color. No styling. No visual hierarchy. If you catch yourself adding polish, write a note instead: "visual design goes here." Keep it rough — participants engage with structure rather than react to aesthetics.

Connect the screens. One clickable hot-spot per meaningful interaction in the task path. Label each with what it triggers: "tap → screen 3." Don't build hot-spots for things outside the task scope. If something leads somewhere not being tested, label it "out of scope" and move on.

Label every screen as a prototype. At the top: "Wireframe — not final design." This isn't optional when stakeholders are present. A wireframe without a label gets treated like it's waiting for color. A labeled wireframe gets treated like a test.

Label any example data. Data that looks real in a wireframe gets evaluated for accuracy rather than for the structural question you're actually testing.

---

What you end up with: a navigable click-through, 3–5 connected states at box-and-label fidelity, covering the core task path. It includes the documented task statement, all screens labeled as wireframes, and any example data marked as fake. Research consistently supports this format regardless of tool: Wiklund, Thurrott, and Dumas (1992) found no meaningful difference in error rates across prototypes of varying fidelity compared to an actual product, and Sefelin, Tscheligi, and Giller (2003) found that both paper and computer-based lo-fi prototypes surface all major issue categories. The tool is irrelevant. Build in Figma, Miro, PowerPoint, or with printed pages on a table. The connected structure is the artifact.

---

One failure mode reliably breaks the test before it starts: building beyond the task path before testing the main path. Thoroughness is a real professional value, and a more complete prototype feels more rigorous. Applying that instinct to prototype scope creates a test where participants can wander off in multiple directions, deviation is harder to read, and the finding on the main path gets diluted by findings from paths that weren't prioritized. The task path is the minimum needed to answer the actual test question. Everything else distorts the finding you needed most.

---

For something you're currently working on: write a task statement for one core flow. List the screens on the task path — main path only. Build boxes-and-labels for each screen. Connect them with one hot-spot per interaction. Show it to one person today: give them the task statement, put the prototype in front of them, and watch without explaining anything. Note where they hesitate or go the wrong direction. Those are the structural problems.

This takes about 30–45 minutes to build and 20 minutes to run.

---

If a participant gets stuck at a specific screen and can't figure out what to do next, the wireframe found a structural problem before visual design was built. One thing to watch: a participant who completes the task immediately and confidently, without pausing, may have navigated by importing mental models from other products rather than by following your structure. After the session, ask what they were thinking at a key decision point. "That's just where I'd expect it to be" and "I followed the label" mean different things.

---

In the next 2–3 days, run the same wireframe with a second participant who has different familiarity with the product area. Write one sentence. What did the second participant get stuck on that the first didn't? What does that tell you about which structural assumptions aren't universal?

After you've run this yourself: describe the task path to an AI tool and ask it to play the role of a first-time user. "Starting on screen 1, which shows [description], I'm trying to [task], where do I go?" Walk the AI's narration against your click-through. Where its instinct diverges from what your prototype routes them to: navigation questions worth testing with a real participant.

---

When the structure is validated and the question shifts to interaction behavior — what happens when states change, data loads, or conditions aren't met — move to 270c. If you're ready to run a structured session with a participant, read 215a (Moderated Usability Session) or 215b (Unmoderated Usability Testing). If the wireframe surfaces confusion at a specific handoff between roles or systems, read 303 (One Feature, Three Handoffs).

---

**Sources**

Kurosu, M., & Kashimura, K. (1995). Apparent usability vs. inherent usability: Experimental analysis on the determinants of the apparent usability. *CHI '95 Extended Abstracts on Human Factors in Computing Systems*. ACM. Found the correlation between aesthetics and perceived ease of use is stronger than the correlation between aesthetics and actual ease of use — the finding this piece uses to explain why visual hierarchy can mask a broken structure during testing.

Virzi, R. A., Sokolov, J. L., & Karis, D. (1996). Usability problem identification using both low- and high-fidelity prototypes. *Proceedings of the CHI Conference on Human Factors in Computing Systems*. ACM. Compared paper prototypes and high-fidelity versions of the same products and found substantially the same usability problems in both — cited here as evidence that stripping visual design doesn't weaken what a wireframe test can catch.

Wiklund, M. E., Thurrott, C., & Dumas, J. S. (1992). Does the fidelity of software prototypes affect the perception of usability? *Proceedings of the Human Factors Society 36th Annual Meeting*. Found no meaningful difference in error rates across prototypes of varying fidelity compared to the actual product — supports this piece's claim that the tool or fidelity level used to build a wireframe doesn't change what it reveals.

Sefelin, R., Tscheligi, M., & Giller, V. (2003). Paper prototyping — what is it good for? A comparison of paper- and computer-based low-fidelity prototyping. *CHI '03 Extended Abstracts on Human Factors in Computing Systems*. ACM. Found that both paper and computer-based lo-fi prototypes surface all major issue categories — cited alongside Wiklund et al. to show the connected structure, not the tool, is what makes a wireframe the right artifact.
