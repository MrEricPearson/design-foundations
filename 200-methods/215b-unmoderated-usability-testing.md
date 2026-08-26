# Unmoderated Usability Testing

**Tier:** 200 — Practice | **Prereqs:** 123 (What Usability Testing Is), 159 (Observation Effect) | **Companion:** 215a (Moderated Usability Session)

**Goal:** Run unmoderated usability testing to find out where people get stuck without watching them in real time.

---

Most people think usability testing means sitting in a room with someone while they use your thing. You watch them click around, you take notes, maybe you ask follow-up questions when they hesitate. That's moderated testing, and it works — but it's also slow, it requires scheduling, and it only scales as far as your calendar allows. If you need to talk to 30 people, you're looking at weeks of coordination.

Unmoderated testing flips this. You write the tasks, you send the link, people do it on their own time. You get recordings of every session — what they clicked, where they paused, what they said out loud while they were trying to figure it out. No scheduling. No live facilitation. You trade real-time observation for scale and speed.

---

You'd use this when you've built something people will interact with on their own — a prototype, a working feature, a flow you're not sure makes sense yet — and you want to know where it breaks down before you ship it. If you're wondering whether people can actually complete the core tasks without help, this gets you that answer faster than any other method.

It works because you're measuring behavior under realistic conditions. When no one's watching, people don't perform for you. They don't narrate their confusion politely. They just try to get the thing done, and when they can't, the recording shows you exactly where the model in their head diverged from the model in your interface (Nielsen, 1993). The task you wrote becomes the control — same instructions for everyone — and the variance in how people attempt it becomes the signal.

---

Pick the thing you're testing. It needs to be something someone can interact with in a browser — a clickable prototype, a staging link, even a production feature if you're testing a change. If it's not live yet, tools like Figma prototypes or anything with working links will do the job. Write down the URL.

Write three tasks. Each task should describe what someone would actually try to accomplish, not how to do it. Don't say "click the blue button in the top right." Say "find out how much shipping costs to your address." The task should feel like something they'd do on their own, not instructions you're giving them (Krug, 2010). If you're testing a sign-up flow, the task might be "create an account using your work email." If you're testing navigation, it might be "find the page that explains how refunds work." Three tasks is enough to surface the biggest problems without overwhelming people.

Write a screener question. You need one question that filters for the people who would actually use this. If you're building something for project managers, ask "Do you currently manage software projects as part of your job?" If the answer is no, they don't get the test. The screener keeps you from testing with people who have no reason to care whether your thing works (Sauro & Lewis, 2016).

Set up the test in an unmoderated testing tool. Tools like UserTesting, Maze, or Lookback let you define tasks, add the screener, and generate a link people can click to start the session. You'll paste in your URL, type in your three tasks, add the screener question, and set a target number of participants. Ten people is usually enough to catch the patterns — more than that and you start seeing the same problems repeat (Nielsen, 2000).

Send the link. You can recruit through the tool's panel (they'll find people who match your screener), or you can send the link directly to people you already know fit the profile. If you're using the tool's panel, you'll get results in a few hours. If you're sending it yourself, you'll get results as people have time to click through.

Watch the recordings. Each video shows you someone attempting your tasks — their screen, their voice if they're thinking aloud, their clicks and scrolls. You're looking for two things: where they hesitated, and where they gave up. If someone spent 40 seconds hunting for a button that should've been obvious, that's a findability problem. If they clicked something that didn't do what they expected, that's a labeling or affordance problem. If they completed the task but took a path you didn't anticipate, that's information about how they're thinking about the structure.

Write down what blocked them. For each task, note which step caused confusion and how many people hit the same problem. If six out of ten people couldn't figure out how to start the return process, that's not a people problem — it's a design problem. If only one person struggled and nine didn't, that's probably an edge case you can defer. You're not trying to fix everything. You're trying to find the places where the current design is costing people effort they shouldn't have to spend.

---

What you end up with: a set of session recordings showing where people got stuck, how long it took them to recover, and whether they completed the task at all. You'll have notes on which problems showed up repeatedly and which ones were one-offs. You'll know whether the core flows work without intervention, or whether you need to redesign before anyone else tries to use this.

---

The failure mode here is writing tasks that teach people how to succeed instead of letting them figure it out. If your task says "click the blue button labeled 'Start' in the top navigation," you've just told them exactly where to look — you won't learn whether they could've found it on their own. The task should describe the goal, not the path. If you catch yourself writing instructions, stop and rewrite it as an outcome. "Find the page that shows pricing options" will tell you whether your navigation works. "Click 'Pricing' in the menu" won't.

---

Pull up something you're working on right now — a prototype, a feature branch, anything someone could click through in a browser. Write one task for it. Not how to do it, just what someone would try to accomplish if they landed on that page with a goal in mind. If you're building a form, the task might be "submit a request for time off next Friday." If you're building a dashboard, it might be "find out how many support tickets were closed last week." Write it down. Read it out loud. If it sounds like instructions, rewrite it as a goal.

---

If the task reads like something you'd say to a coworker who's never seen this before — and they'd know what to try — it's working. If reading it makes you realize you've been assuming people know where things are, that's the thing to fix before you run the test.

---

In the next two days, write tasks for the other two core things someone would try to do with this. Don't build the full test yet — just write the tasks. Then pick one person who fits your user profile and send them the tasks over email or Slack. Ask them to tell you, in one sentence, what they'd try first for each one. If their answer matches what you expected, your tasks are clear. If it doesn't, you've just learned something about how they're thinking about the problem. Write one sentence: what surprised you about what they said they'd do first?

If you share it in the Platform Excellence channel, you'll see what others noticed too.

---

After you've written tasks, watched people attempt them, and fixed the biggest blockers: you can use AI to speed up the pattern-spotting step. Upload your session notes (the blockers and timestamps, not the full videos) and ask it to group the problems by type — findability issues, labeling mismatches, task failures, recovery paths people took. It won't catch things you didn't write down, but it'll surface which categories of problem cost people the most time. That gives you a prioritized fix list faster than reading through ten sets of notes manually.

---

If people completed the tasks without major friction, run the test with a bigger group to confirm the pattern holds. If you found repeated blockers in the same step, redesign that part of the flow, then test again with a new group to confirm the fix worked. If the tasks felt too easy or too hard, revisit how you're scoping the scenario — you may need to test a harder decision point or a simpler entry task first. When you're ready to run a live session with a facilitator present, 215a (Moderated Usability Session) covers that method.

---

## Sources

Krug, S. (2010). *Rocket surgery made easy: The do-it-yourself guide to finding and fixing usability problems.* New Riders. Source for the task-writing standard this piece applies throughout: a task should describe what someone would actually try to accomplish, not the steps to get there.

Nielsen, J. (1993). *Usability engineering.* Academic Press. Foundational grounding for observing behavior under realistic, unmoderated conditions — the basis for this piece's claim that recordings reveal where a participant's mental model diverges from the interface without anyone narrating politely for an observer.

Nielsen, J. (2000). Why you only need to test with 5 users. *Nielsen Norman Group.* https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/ Established that a small number of participants is enough to catch the majority of usability problems before findings start repeating — the basis for this piece's recommendation that around ten unmoderated sessions is usually sufficient.

Sauro, J., & Lewis, J. R. (2016). *Quantifying the user experience: Practical statistics for user research* (2nd ed.). Morgan Kaufmann. Supports this piece's use of a screener question to filter for participants who genuinely match the intended user profile, rather than testing with people who have no stake in whether the thing works.
