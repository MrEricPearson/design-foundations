# 215a — Moderated Usability Session
**Tier:** 200 — Practice | **Arc:** Usability Testing | **Prereqs:** 123 (What Usability Testing Is), 113 (Defining Success), 157 (Why You Don't Help During Testing), 174 (Think-Aloud Protocol) | **Note:** Use when you can run a live, synchronous session with a participant. If synchronous access isn't available or moderation introduces bias, see 215b (Unmoderated Usability Testing).

**Goal:** After this piece, you will be able to find out whether a real person can complete a specific task with your interface — before it ships — without the session moderator's presence distorting the result.

**Prior knowledge hook:** Think of a feature you shipped confident users would understand — and then watched someone use it without the context you had, attempting something completely different from what you expected. That gap between your confidence and their experience is what this method surfaces before it becomes a shipped problem.

**Trigger:** You have something testable — a prototype, working interface, or even a paper sketch — and want to know whether a real person can complete a specific task without guidance. You have access to at least one person unfamiliar with this specific interface.

**Why this works:** Internal review is done by people who already know what the interface is supposed to do. That knowledge fills in the gaps the interface leaves, making internal review a poor proxy for user experience. A usability session puts someone without that knowledge in front of the interface — and their confusion is the data.

**Method:**
1. **Define one task.** Write a concrete goal from the user's perspective: "Find your most recent invoice." Not "explore the dashboard." One specific, observable thing.
2. **Recruit one person who hasn't seen this interface.** This doesn't need to be formal. A colleague from a different team, a friend — anyone unfamiliar with the specific UI works for most purposes.
3. **Set up the session.** Say: "I'm going to ask you to try to do something. Think out loud as you go — say whatever you're noticing. I can't answer questions during the task; that's what we're testing." This is the think-aloud prompt (174).
4. **Give the task in writing, then observe without helping.** When they hesitate: silence. When they're stuck: "what are you looking for?" — never "you'd click here." When they ask a direct question: "what would you expect to happen?" (157 explains why this boundary matters.)
5. **Write what you observe.** Where they hesitated, what they tried first, what they said, where they gave up. The observation is the data; your interpretation of why it happened is not.
6. **After the task: one question per friction point.** "What did you expect to happen when you [specific action]?" Ask in order, about the moments you noted. Don't ask about general impressions — specific friction points produce specific improvement directions.
7. **Run five sessions.** Five participants will surface most recurring problems in an interface.

**Artifact:** A ranked list of task failure points — where users hesitated, what they tried instead, what they expected — ordered by how many of your five participants hit the same friction.

**Watchout:** The urge to explain is the hardest thing to suppress. Every explanation you give during a session hides a design problem from your findings. "Oh, that's a bug we're fixing" removes a data point. Stay quiet until the task ends.

**When You Can't Run the Full Version**

**If you're in a regulated environment (no recording, restricted participant pools, legal constraints):** Run the session without any recording. Take notes by hand during the session — every hesitation, every verbal statement, every action sequence. The evidence is in your notes, not in the recording. One unrecorded session with hand notes is significantly more useful than no session. Consult your organization's guidance on participant consent forms in regulated contexts before recruiting.

**If you can only run one session:** One session surfaces specific friction points. It can't surface patterns. Treat one session as a "worst-case finder" — if something goes wrong once, it will go wrong again. Prioritize fixing anything that completely blocked the participant before fixing anything that just slowed them down.

**What you still get:** Direct observation of friction that internal review doesn't surface.

**What you give up:** Pattern data (which friction points are universal vs. participant-specific). Five sessions are the minimum for pattern-level confidence.

**Don't do this:** Don't use a think-aloud session to test whether users like the interface. Preference is not the question — task completion is. A participant who says "I like this design" while failing the task has given you attitudinal data that conflicts with your behavioral data. The behavioral data is what matters.

**Try This:** Pick one thing a user is supposed to be able to do with something you're working on. Find one person who hasn't used it. Give them the task in writing. Don't say anything until they're done. Write down every moment they weren't sure what to do.

**Proof:** If you finish sessions and find yourself thinking "I need to fix [specific thing] before this ships," the method worked. If you find only confirmation that everything works as intended, either the task was too easy or the participants were too close to the team that built it. Try someone further removed.

**Take this further:** In the next week, run one additional session with a different participant. Write one sentence: did the same friction points come up, or different ones? Recurring friction is the finding; divergent friction means either noise or that your user types vary more than expected.

**After you've run this yourself:** Use an AI tool to draft the task statement — describe the user goal and ask for a written task prompt that's specific enough to test without leading. Check the output: if the prompt tells the user how to complete the task, it's leading. A well-formed task prompt gives only the end-state goal.

**What Next:** If you have multiple observed friction points to organize, read 214 (Affinity Mapping). If you want an evaluation method that doesn't require recruiting, read 216 (Heuristic Evaluation). If participants can't be available synchronously, read 215b (Unmoderated Usability Testing).
