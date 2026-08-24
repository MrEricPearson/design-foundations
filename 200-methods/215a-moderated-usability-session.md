# Run a Moderated Usability Session

**Tier:** 200 — Practice | **Prereqs:** 123 (What Usability Testing Is), 157 (Why You Don't Help), 159 (Observation Effect), 174 (Think-Aloud Protocol) | **Companion:** 215b (Unmoderated Usability Testing)

**Goal:** Run a moderated usability session with a working build — so you learn where people get stuck without your help.

**Goal line (for article header):** You need to know if people can actually use what you built.

---

Most demos show what your build can do. A usability session shows what someone can do with your build when you're not there to explain it.

You already know the difference between showing someone your work and watching them try to use it. The first tells you whether your logic makes sense to you. The second tells you whether the interface communicates that logic to someone who doesn't already understand it. That gap is what a moderated usability session measures.

Run this when you have something interactive — a working build, a clickable prototype, even a staging environment — and you need to know whether people can complete real tasks with it before you ship it to everyone.

---

The mechanism is structured observation with minimal intervention. You're creating conditions where someone attempts a task you've defined, thinks aloud while working, and encounters the interface as they would in real usage — without you jumping in to clarify, redirect, or reassure. The structure gives you repeatable data across participants. The non-intervention gives you honest data about what the interface actually communicates.

Virzi (1992) tracked defect detection rates across usability testing and found that 80% of severe usability problems were discovered by the fifth participant — but only when those participants were attempting tasks without facilitator assistance. Sessions where facilitators intervened to help participants proceed detected far fewer problems, because intervention masks the exact points where the design fails to support independent use.

That's the thing people get wrong most often: they think the goal is helping participants succeed. It's not. The goal is learning where the design doesn't help them succeed. Every time you intervene, you're learning about your ability to mediate. You're not learning about the interface.

---

Start by writing task statements for what you need participants to attempt. Pick 3–5 realistic tasks someone would actually try to complete with this build. Each task statement should name a goal without naming the path: "Find last month's invoice" instead of "Click Reports, then Billing, then filter by date." "Turn off email notifications" instead of "Go to Settings and uncheck the email box."

The task statement gives the participant intent but not instruction. That's the whole point. You want to see which path they take when the interface is their only guide.

For each task, write down what success looks like: the specific outcome that tells you they completed it. "They've opened the invoice PDF" or "Email notifications are toggled off and they've confirmed the change." Don't skip this step. You need an unambiguous completion marker so you know whether someone finished the task or just thinks they did.

Recruit 5 participants. Not users you've worked with before — people who match your target audience but haven't been trained on this build. Dumas and Redish (1999) documented that five participants, each attempting the same task set, surface roughly 85% of usability problems in a design. Going beyond five yields diminishing returns unless you're comparing across distinct user types.

Schedule 45–60 minutes per session. That gives you time for introduction (5 min), tasks (30–40 min), and a brief post-session debrief (5–10 min). Build in 15-minute buffers between sessions so one that runs long doesn't cascade.

Set up screen recording and audio capture. You will not remember what happened in the third task of the fourth session without a recording. You'll remember the spectacular failure and maybe one delightful moment, but you won't remember the quiet hesitation that happened six times across five people — which is actually the more useful pattern. OBS Studio, Loom, QuickTime with system audio, whatever works. Just record it.

Write a facilitator script for yourself. It doesn't need to be formal, but it needs to exist. Write out the introduction you'll give, the task statements exactly as worded, and the prompts you'll use when someone goes quiet. This keeps you consistent across participants. If you ad-lib differently with each person, you're introducing variance that makes patterns harder to see.

Your introduction should normalize struggle. Tell participants, "This is a test of the interface, not a test of you. If something is confusing, that's useful information — it tells us what to fix. There are no wrong answers, and you can't break anything." Then explain think-aloud: "As you work, please say what you're thinking, what you're looking for, or what you're trying to do. It helps us understand your reasoning."

That framing matters. Boren and Ramey (2000) found that participants who understood the session as evaluating the interface (not evaluating them) produced more honest struggle behavior and narrated confusion more openly than participants who felt they were being tested. The more a participant feels judged, the harder they'll work to hide confusion — which means you miss the data.

During the session, give one task at a time. Read the task statement aloud, then let them work. Don't clarify it unless they explicitly ask, and even then, restate it identically — don't paraphrase or add detail. If they ask "what should I do?" say "whatever seems right to you." If they ask "is this the right place?" say "what do you think?" Redirect the question back without answering it.

Watch. Take notes. Do not help. If they're silent for more than 10–15 seconds, prompt them: "What are you thinking right now?" or "What are you looking for?" That's not intervention — it's a facilitation move that keeps think-aloud going without giving information. You're asking them to narrate. You're not telling them what to do.

When they complete a task — or when they're clearly stuck and have stopped trying — move to the next task. If they didn't complete it, note that. Don't tell them they didn't finish. Just move on. "Okay, next task: [read the next task statement]."

After all tasks, spend 5 minutes asking open retrospective questions: "What was easiest?" "What was most confusing?" "Was there anything you wanted to do but couldn't figure out how?" These aren't the primary data — observation is the primary data — but they'll surface things participants noticed that they didn't vocalize during the task.

---

You'll end up with 5 recordings, 5 sets of notes, and a list of where each participant struggled, succeeded, or gave up. That's your artifact: a session log documenting what happened at each task for each participant, plus the recordings for review.

The log should capture: participant ID, task attempted, whether they completed it, where they hesitated or went wrong, what they said when confused, and how long it took. You don't need a formal template. A spreadsheet with columns for [Participant, Task, Completed?, Observations, Time] works fine.

---

You'll know you ran this correctly if you did not answer a single "where do I...?" or "is this...?" question during any task attempt. Every time you wanted to help and didn't, you captured a design problem. That discomfort is the signal that the method is working.

If participants thanked you afterward for being patient while they "figured it out," that's another good sign. They felt safe enough to struggle in front of you, which means the session framing worked and the data is honest.

The false positive: participants succeeded at every task without hesitation. That's possible — maybe the interface really is that clear — but it's more often a sign that your tasks were too easy, your participants were too experienced with this type of interface, or you intervened without realizing it. If everyone succeeds smoothly, review your recordings and count how many times you clarified, confirmed, or redirected. You might have been helping more than you thought.

---

In the next two days, watch the recording of one session all the way through. As you watch, write down every moment where the participant paused, backtracked, or said something confused. You're building a list of friction points the interface created.

Afterward, write one sentence: what would you do differently in the next round of sessions?

---

After you've run a few rounds of moderated sessions and you're confident in the method, you can use AI to help with analysis. Record the session, transcribe it, then prompt: "This is a usability session transcript. Identify every moment where the participant expressed confusion, hesitated, backtracked, or failed to complete the task. For each moment, quote what they said and describe what they were trying to do." That'll give you a structured first pass you can validate against the video.

---

If you're testing something that isn't built yet — a wireframe, a sketch, a printout — read 216 (Paper Prototype Testing). If you want to test without being present during the session, read 215b (Unmoderated Usability Testing). If you're getting consistent task failures across participants and need to redesign, read 211 (Fixing What Failed in Testing).

---

**Sources**

Virzi, R. A. (1992). Refining the test phase of usability evaluation: How many subjects is enough? *Human Factors, 34*(4), 457–468. — Documented that 80% of severe usability problems are detected by the fifth participant when tasks are attempted without facilitator intervention; sessions with facilitator assistance mask failure points and reduce defect detection rates; structured observation with minimal intervention produces repeatable, comparable data across participants.

Dumas, J. S., & Redish, J. C. (1999). *A Practical Guide to Usability Testing.* Intellect Books. — Five participants attempting the same task set surface approximately 85% of usability problems in a design; additional participants yield diminishing returns unless testing across distinct user types; task statements should specify goal without path to measure whether the interface alone communicates procedure.

Boren, T., & Ramey, J. (2000). Thinking aloud: Reconciling theory and practice. *IEEE Transactions on Professional Communication, 43*(3), 261–278. — Participants who understood the session as evaluating the interface rather than their performance produced more honest struggle behavior and narrated confusion more openly; framing the session as "testing the design, not you" reduces social desirability bias and observation effects; light prompting ("what are you thinking?") maintains think-aloud verbalization without introducing intervention bias.

Rubin, J., & Chisnell, D. (2008). *Handbook of Usability Testing: How to Plan, Design, and Conduct Effective Tests* (2nd ed.). Wiley. — Screen and audio recording are not optional; patterns of hesitation and quiet confusion across participants are not reliably recalled without recordings; facilitator scripts reduce cross-session variance and make problems easier to identify as patterns rather than isolated incidents.

Nielsen, J. (2000). Why you only need to test with 5 users. *Nielsen Norman Group.* — Elaborates the diminishing returns curve: first participant reveals roughly 31% of problems, each additional participant reveals fewer new problems, by the fifth participant you've found approximately 85% of issues; testing beyond five makes sense only when comparing distinct user segments or when testing reveals insufficient problem density to justify design changes.
