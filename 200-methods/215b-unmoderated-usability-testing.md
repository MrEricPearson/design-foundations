# 215b — Unmoderated Usability Testing
**Tier:** 200 — Practice | **Arc:** Usability Testing | **Prereqs:** 123 (What Usability Testing Is), 113 (Defining Success), 157 (Why You Don't Help During Testing) | **Note:** Use when synchronous access isn't available, when moderation introduces bias, or when you need results from a larger participant pool. If you can run a live session, see 215a (Moderated Usability Session) first.

**Goal:** After this piece, you will be able to run a usability test without being present — and get usable data from participants completing tasks on their own.

**Prior knowledge hook:** Think of the last time you had a prototype or working feature that needed validation but couldn't get anyone in a room for a session. Unmoderated testing solves access — but it transfers the probing work entirely to question design, because no one will be there to follow up.

**Trigger:** You need task completion data from real participants, but synchronous access isn't available — different time zones, high-demand schedules, or a need for a larger participant pool than you can run through individual sessions. Or: moderation bias is a concern (participants behave differently when watched).

**Why this works:** Unmoderated tests decouple the session from the moderator's schedule and timezone. Participants complete tasks in their own environment, at their own pace, which often produces more naturalistic behavior than a scheduled session where a participant knows they're being observed.

**Method:**
1. **Define one task per test.** Same as moderated: a concrete, user-perspective goal with no instructions on how to complete it. The difference: in unmoderated testing, the task statement is doing more work — there's no moderator to clarify ambiguity. Test the task statement with a colleague before deploying it.
2. **Write your follow-up questions in advance.** In a moderated session, you ask follow-up questions based on what you observe. In unmoderated, you write them before the session. Write 2-3 questions for the friction points you most expect to occur: "Was there any moment where you weren't sure what to do? If so, describe it." "What did you expect to happen when you [specific action]?" Your advance questions won't cover every friction point — that's the tradeoff.
3. **Choose your recording approach.** Screen recording with think-aloud instructions is the minimum: "As you complete the task, narrate what you're thinking." A purpose-built unmoderated testing tool (Maze, UserTesting, Lookback, etc.) automates this and adds quantitative data (task completion rates, time-on-task). Either approach works — the tool adds structure, not insight.
4. **Recruit from your actual user population.** Unmoderated testing is easiest to run at scale, which makes it tempting to recruit convenience samples that don't match your actual users. A convenience sample that doesn't represent real users produces data about the wrong people completing the task. Screen for the key characteristics of your actual user before including a participant.
5. **Review recordings for hesitations, restarts, and unexpected paths.** Watch the full recording for at least 3 participants before looking at aggregate data. The aggregate shows where the problem is; the recordings show what it looks like.

**Artifact:** Task completion data — which participants completed the task, where they dropped off, and what they said or did at the points of friction.

**Watchout:** Unmoderated tests can't probe. If a participant takes an unexpected path, you'll see that it happened — but you won't be able to ask why. Design your follow-up questions to cover the most likely unexpected paths, and treat any unexpected path you didn't anticipate as a reason to run a follow-up moderated session.

**When You Can't Run the Full Version**

**If you have no testing tool and limited time:** Set up a screen recording on a shared device, write the task and think-aloud instructions on paper, and have the participant complete the task while recorded. Review the recording asynchronously. This is the minimum unmoderated setup — no platform, no automation. It works; the data is in the recording.

**What you still get:** Behavioral data without synchronous access.

**What you give up:** Quantitative aggregation, automated path tracking, and the efficiency of a purpose-built tool. The insight is the same; the time-to-insight is higher.

**Don't do this:** Don't substitute a survey about the interface for an unmoderated test. Surveys produce attitudinal data ("I thought it was easy"). Unmoderated tests produce behavioral data ("they tried to click the logo to navigate back"). These are different kinds of evidence for different kinds of questions.

**Try This:** Write one task statement for something you're currently working on. Test the statement by handing it to a colleague without context — can they tell you what they're supposed to accomplish without knowing anything about the product? If they need clarification, the task statement is too ambiguous for unmoderated use. Revise until it's self-contained.

**Proof:** If the recordings show hesitations or paths you didn't predict — moments where participants did something different from what you expected — the test produced useful data. If every recording shows participants completing the task directly, either the task was too easy or the participant pool was too similar to the team that built it.

**Take this further:** In the next week, run the same task with 3 additional participants. Write one sentence: what was the most consistent unexpected behavior across participants? That consistency is your primary design direction.

**After you've run this yourself:** Paste your task statement and follow-up questions into an AI tool and ask: "What friction points might participants experience that these follow-up questions wouldn't catch?" Add questions to cover one or two gaps the output identifies.

**What Next:** If the recordings show a specific friction pattern to organize and prioritize, read 214 (Affinity Mapping). If you want to validate the underlying design structure with an expert walk-through rather than user sessions, read 216 (Heuristic Evaluation). For a deeper behavioral investigation of specific friction points, follow up with 215a (Moderated Usability Session).
