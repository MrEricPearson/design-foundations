# You're Getting Feedback on the Wrong Thing
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 106 | **Episode:** 13

*When the prototype looks finished, people stop questioning whether the direction is right.*

---

You show something you've been working on. A few people look at it. Comments start coming — a detail here, an edge case there, something specific they noticed. The meeting has energy. Forty minutes later it ends. Nobody asked whether the direction itself was right.

That's a fidelity mismatch. And the reason it happens isn't because the people in the room were unhelpful. It's because of what your demo told them.

---

There's a working assumption most people bring to prototype reviews: fidelity is about production quality. How finished something looks. How much time went into making it. The correction is simpler and more useful. Fidelity is about match — specifically, whether the prototype's level of detail is appropriate for the question you're trying to answer.

That distinction matters because of how people read visual polish. When something looks finished, they treat it as finished. They shift from strategic mode to tactical mode: what would I change about this specific thing? Whether the direction is right starts to feel like an already-settled question. Sauer & Sonderegger (2009) documented exactly this: increased visual polish led participants to rate products as more usable than lower-polish equivalents, even when the underlying functionality was identical. The same effect runs in prototype reviews. Polish doesn't just change what people think of the design — it changes what they feel safe saying about it.

The rough prototype sends the opposite signal: it tells the room the direction is still open, and that questioning it is on the table. Choosing the right level is how you control that signal.

---

Three question types map to three fidelity levels, and often the mismatch happens when people skip the first one.

If the question is "does this direction make sense?" — a rough sketch is the right tool. Labeled boxes, arrows, stick figures. (I mean that without irony.) The question is strategic, so the prototype should look strategic. Anything more polished signals that the strategic question has already been answered, which is exactly the wrong message when you haven't confirmed it yet.

Move up a level: "can someone find what they need?" This is where wireframes and basic click-throughs belong. Labels matter here because they carry the conceptual model. Color and visual style don't. They pull attention from structure to surface.

The third question earns the high polish: "does this feel like a finished product?" You're testing the actual experience of something close to final. Virzi, Sokolov & Karis (1996) showed that low- and high-fidelity prototypes surface substantially the same usability problems — which means you don't need to polish most things to test them. But when the visual design is itself the question, rough won't give you a real answer.

The skill is knowing which question you're actually in.

---

There's an AI wrinkle worth naming, because this is where I see the mismatch happen most often now. An AI tool can generate a polished-looking screen from a rough prompt in seconds. That's genuinely useful when you're in the visual stage. But it's a trap when you're not. You describe what you want, the AI produces something that looks finished, and then you show it to someone for feedback on the underlying concept — and they give you feedback on the execution. It's the design equivalent of showing up to a rough-draft review with a leather-bound manuscript. The tool produced polish quickly. The question didn't require it.

Roughness, again, is not about production time. A thing that took three minutes to generate can still carry the wrong signal.

---

You'll notice a fidelity mismatch by watching what feedback you get. If reviewers are digging into button labels and icon sizing when your question was about flow, the prototype already told them the direction was settled. When a session ends without anyone questioning the navigation because the screen looked final, that's the same thing.

The check is simple: does the feedback address the question the prototype was designed to answer? If not, the fidelity was higher than the question required.

---

Don't confuse fidelity with how rough something looks. A wireframe can look rough and still be high fidelity for a navigational question. An AI-generated screen can look finished and be low fidelity for a conceptual question — because the polish doesn't match what you're trying to learn.

The false positive to watch for: you run a session with a wireframe (no color, no imagery) and assume you've matched the fidelity correctly. But the wireframe has realistic copy, complete navigation logic, and working labels. It's navigational fidelity, not conceptual. The visual roughness masked the functional completeness. "Rough-looking" and "appropriate fidelity" are not the same thing.

---

Look at the last prototype or mockup you showed to someone. Write the question it was designed to answer. Now ask: was the fidelity appropriate for that question? If it was higher than needed, what specifically prompted the extra polish — a stakeholder presentation, a tool that generates it automatically, habit?

The next time you're about to show something, write the question first. Then check: does this prototype's level of detail match that question, or is it ahead of it? If it's ahead, pull back. The rougher version will get you better feedback. That's the whole move.

---

This piece is part of the Prototyping cluster in the Design Foundations Library. The arc overview at 309 (Prototyping: Choosing the Right Approach) maps fidelity to specific methods. When you're ready to test a prototype with real users, read 215a (Moderated Usability Session) or 215b (Unmoderated Usability Testing) — both build on fidelity awareness as a starting assumption. To evaluate a prototype without recruiting participants, 124 (Nielsen's Heuristics) is a structured alternative.

---

*Sources: Sauer, J., & Sonderegger, A. (2009). The influence of prototype fidelity and aesthetics of design in usability tests. Applied Ergonomics, 40(3) — increased visual polish led participants to rate products as significantly more usable even with identical functionality; the effect changes what reviewers feel safe saying. Virzi, R.A., Sokolov, J.L., & Karis, D. (1996). Usability problem identification using both low- and high-fidelity prototypes. CHI Conference Proceedings — low- and high-fidelity prototypes surface substantially the same usability problems; polish is not required for most testing questions.*
