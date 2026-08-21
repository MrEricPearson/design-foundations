# When Your Task Statement Gives Away the Answer
**Tier:** 100 — Recognize | **Note:** Prereq for 215a (Moderated Usability Testing) and 215b (Unmoderated Usability Testing); pairs with 174 (Think-Aloud Protocol) and 157 (Why You Don't Help During Testing)

**Goal:** Recognize when a usability task statement reveals the interface path — because a task that names the answer tests memory, not usability.

*You wrote it to be clear. What you wrote was a hint.*

---

The participants in your last usability test found the feature quickly. What you might not know is that your task told them where to look.

When you write "Use the filter to find all tickets assigned to your team," you've named the feature. The participant isn't finding "filter" — they're following an instruction that already contains the word. Those are different cognitive tasks. One produces data about whether the interface is clear. The other confirms that people can read.

A usability task statement's job is to describe what the person wants to accomplish without describing how the interface accomplishes it. The quality of your task determines the quality of what you learn. A task that names a feature, a button label, or a menu item has done the participant's navigation work before the session starts. The participant finds the thing. You record a success. And you walk away with a much more confident answer to a much less useful question.

Raluca Budiu (2016) at Nielsen Norman Group studied this mechanism directly. In one study, participants were asked to find an "iPad keypad" — a less common way to say keyboard. Most typed "keypad" into the search box, even though the interface used "keyboard." The task's word stuck. Participants didn't navigate to the right label. They searched for the term the task had just handed them. The test measured whether the label in the task matched a label in the interface. Not whether anyone would find the feature on their own.

Amy Schade (2017), also at NNGroup, names the failure plainly. Tasks that contain interface terminology test "reading comprehension and ability to find matching words, rather than your labels and navigation." The study runs. Participants find what you asked them to find. You conclude the feature is discoverable. But what you've confirmed is narrower: that people can follow an instruction containing the right word. Which isn't the same thing, and isn't what the test was for.

---

You'll recognize this pattern once you know what to look for. A leading task reads like directions: "Go to Account Settings and update your notification preferences." A goal-oriented task reads like a situation: "You've been getting too many email notifications. Take care of that." One tells participants where to go. The other lets the interface tell them. The difference is everything the test is supposed to measure.

The same problem appears in softer forms: naming a section, a workflow stage, a status label, a tab. Any noun in the task that exists as a visible label on screen becomes a waypoint. Participants move toward those terms rather than exploring how the interface structures itself. You get completion rates. You lose the data that would make those rates meaningful.

(If you've written task scripts that look more like step-by-step tutorials than situations, you've done this. Most people do, the first few times. The tasks feel specific and helpful, which is the exact property that makes them less useful.)

---

The signal is one question. Read the task. Does any word in it appear as a visible label somewhere in the interface? Button text, menu item, section heading, feature name, status badge, tab label. Every match is doing the participant's work. The test is measuring label-matching, not discoverability. That's the sentence to hold onto.

Marieke McCloskey (2014) at NNGroup frames the standard directly: effective tasks specify "what to accomplish and why, but never how." The "how" lives in the interface labels, the navigation structure, the button text. The goal lives in what the participant cared about before they opened the screen.

---

This isn't an argument for vague tasks. Vague tasks produce vague data, and "do something with a document" is not a usability task. Specific tasks are what you're after — specific about the person's situation and goal, not about the interface path they should take to get there.

"Find the January invoice for Acme Corp and download a PDF of it" is specific. It names a document, a company, a file format. None of those appear as labels in most invoicing interfaces. The participant still has to find where invoices live. That's the test.

The false positive: thinking any concrete detail in a task is a hint. It isn't. Dates, amounts, names, document titles: these add context the participant needs. They don't reveal interface structure. A menu label does. The check is always the same: does this word appear on screen?

---

Pull up your next session's task list, or the last one you ran. For each task, find every word that also appears as a visible label somewhere in the interface: menu items, button text, section headings, status labels, feature names. Every match is doing the participant's navigation for them. The test is measuring word-matching for those terms, not whether the interface communicates on its own.

Then rewrite each flagged task from the participant's goal. What did they want to accomplish before they knew this interface existed? That question is the task. The interface is supposed to answer it, and the test's only job is to make sure nothing else does it first.

If you found matches, those tasks were coaching the answer. That's not a flaw in how you've been testing — it's just the thing you now know to check.

---

When you're ready to run a live session, 215a (Moderated Usability Testing) covers session structure and how to handle participants who ask clarifying questions about the task itself. When you're planning unmoderated testing — where no one can step in to clarify — 215b (Unmoderated Usability Testing) covers what self-contained task statements require when there's no facilitator in the room.

---

**Sources**

Budiu, R. (2016). Priming and User Interfaces. Nielsen Norman Group. https://www.nngroup.com/articles/priming/

McCloskey, M. (2014). Turn User Goals into Task Scenarios for Usability Testing. Nielsen Norman Group. https://www.nngroup.com/articles/task-scenarios-usability-testing/

Schade, A. (2017). Write Better Qualitative Usability Tasks. Nielsen Norman Group. https://www.nngroup.com/articles/better-usability-tasks/
