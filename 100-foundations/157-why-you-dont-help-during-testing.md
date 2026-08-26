# Why You Don't Help During Testing
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** none | **Episode:** 21

**Goal:** Recognize when helping a participant changes the evidence you're collecting — so you can spot the moment your instinct to help starts producing false confidence instead of real findings.

*The participant is going in circles and you know exactly what to tell them. You can't.*

---

You're watching someone use the thing you built. They pause. They squint at the screen. They hover the cursor over three different buttons without clicking any of them.

Every part of you wants to jump in.

It's "that button does X," or "try clicking here," or just "what are you looking for?" in a way that hands them the answer. The silence feels terrible. Watching someone struggle with your work feels worse. You know exactly what would fix this, and you know it takes five words.

But here's the thing: the moment you help is the moment the test stops measuring whether someone can use this without help. In the real situation, when nobody's watching and nobody's there to guide them, those five words aren't available.

---

The instinct to help isn't wrong. It's just answering a different question.

When you step in, you're answering: can this person complete the task if someone who knows the system is standing next to them? That's a useful question in training. It's not useful in usability testing.

Usability testing produces a specific kind of evidence: whether someone unfamiliar with your work can complete a task without coaching. The method only works if the conditions of the test match the conditions of real use closely enough that what happens in the test predicts what happens when the product is out in the world. Research methods call this ecological validity — the degree to which the test environment mirrors the environment where the design actually gets used (Bronfenbrenner, 1977). The closer they match, the more you can trust what you observed. The wider the gap, the less the test tells you.

Your participant is confused because your interface is confusing. That confusion is the data. The moment you step in and explain, you've closed the gap between "the interface alone" and "the interface with your help," and erased the finding.

Jakob Nielsen (2012) put it directly: shut up and let the users do the talking. He wasn't being harsh. He was naming the discipline that makes the method work. Every sentence you say changes what happens next. After you've spoken, the participant isn't just responding to the interface anymore. They're responding to you, to what they think you want to hear, to the social pressure of performing correctly in front of someone who clearly knows the system. You can't separate those influences afterward. The evidence becomes uninterpretable.

---

You'll feel this pull most clearly at the moments it matters most. The participant looks up from the screen and asks, "Am I doing this right?" A task runs twenty minutes over and you're watching the clock. Someone's frustration has crossed from productive into visibly distressing. Those are exactly the moments where the test is producing its most valuable signal. Someone who's frustrated found a real problem. That's a finding. Someone who can't finish in the expected time just told you something accurate about how the design performs under real conditions.

The hardest version is a direct question: "Should I click this?" The right answer is a non-answer. "What would you normally do?" or "What are you looking for?" Keep them thinking aloud without teaching them anything about how the interface works. (If you've ever said "well, it depends on what you're trying to do" because you thought it was neutral — you helped them anyway. You both knew it.) This is harder than it sounds, and it's why practiced facilitators are more useful here than knowledgeable ones. Knowing the product well is almost a liability. The discipline is sitting with the silence while someone struggles with something you could explain in ten seconds.

---

You've crossed the line the moment you start a sentence with "Actually, what that does is—" or "Try looking at—" or "Most people click on—." If the participant's next attempt is easier because of something you said, that's not facilitation. That's contamination.

---

None of this means never speaking. Usability testing isn't silent observation. You're in the room, and total silence from you would be its own kind of distraction. You'll prompt participants to keep thinking aloud when they go quiet — a simple "keep talking" or "what are you thinking right now?" works. Ask what surprised them, what they expected, what they were looking for. If someone is so lost and so frustrated they're about to abandon the session altogether, step in and redirect.

The line runs here: prompts that keep someone talking about their own thought process are fine. Anything that teaches them how the interface works invalidates the test. Steve Krug (2010) documents this tension directly in *Rocket Surgery Made Easy*: the facilitator's urge to help is real, it's strong, and it doesn't disappear with experience. What improves with practice is the ability to redirect it. Save the useful information for the debrief. During the test, the participant's struggle isn't a problem to solve. It's the point.

---

Take two minutes with this. Think back to the last time you watched someone use something you built: a prototype in review, a demo with a stakeholder, a document someone was reading in real time. Replay the moment when they got confused or stuck.

Did you help them? What specifically did you say or do? If you'd stayed quiet, what would that silence have revealed that your help covered up?

You don't need a formal session for this to matter. Any time someone's encountering your work for the first time in front of you, you're collecting evidence. Whether that evidence reflects what you built, or what you built plus your help, is a choice you're making in real time.

---

If you're getting ready to run a live session, 215a (Moderated Usability Session) covers the full facilitation method, including when and how to intervene without biasing what you're observing. To understand what to listen for while you're staying quiet, 174 (Think-Aloud Protocol) covers the verbal behavior that makes silence productive. If you want the foundational concept behind why unfamiliarity matters here, 151 (Self-Report vs. Observed Behavior) is where that sits.

---

**Sources**

Bronfenbrenner, U. (1977). Toward an experimental ecology of human development. *American Psychologist*, 32(7), 513–531. Introduced ecological validity as the degree to which research environments approximate real-world conditions — foundational to understanding why artificially assisted test conditions undermine the generalizability of findings.

Nielsen, J. (2012). *Thinking aloud: The #1 usability tool.* Nielsen Norman Group. Core facilitation guidance includes the instruction to "shut up and let the users do the talking" — the discipline of silence that preserves behavioral evidence during sessions.

Krug, S. (2010). *Rocket surgery made easy: The do-it-yourself guide to finding and fixing usability problems.* New Riders. Documents the facilitator tension directly: the urge to help participants who are struggling is real and powerful, but acting on it transforms what you're measuring.
