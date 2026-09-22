# Notice When Being Watched Changes How Someone Acts

**Goal:** Recognize when observation itself changes participant behavior during testing.

---

You're watching someone use your prototype. They're moving carefully, double-checking everything, narrating their thoughts like they're performing surgery instead of clicking through a form. Something feels off — they're being too deliberate, too careful, too good at this.

That's the observation effect showing up.

The observation effect is the shift in behavior that happens when someone knows they're being watched. It's not about you influencing them (that's observer bias, covered separately). It's about them performing for you — trying harder, being more careful, self-censoring frustration — because there's an audience. Mayo's original Hawthorne studies in the 1920s found this with factory workers: productivity went up not because of better lighting or rest breaks, but because workers knew researchers were watching them. The attention itself changed the work.

In usability testing, this shows up constantly. Participants try to succeed at tasks they'd abandon in real life. They soldier through confusing interfaces without complaint because they don't want to seem difficult. They narrate politely even when they're genuinely lost. The behavior you're seeing isn't fake — they're really doing those things — but it's not the behavior you'd see if they were alone at their desk on a Tuesday afternoon with three other tabs open and a Slack notification chiming in.

Jakob Nielsen built an entire usability methodology around working with this reality. The think-aloud protocol asks participants to narrate their thoughts specifically because silence hides too much — but it also intensifies observation effect. You're not just watching them anymore; you're asking them to perform their thinking out loud. Some people rise to that and get more deliberate. Others freeze up entirely.

---

You'll see observation effect when someone is using your product with you in the room — or on a call, or recording themselves, any situation where they know their actions are being captured. The format doesn't matter. The awareness does. If they know someone will see this, observation effect is in play.

The clearest signal: they apologize for struggling, or they explain why they're confused, or they try harder than anyone would in real life. "I'm probably just missing something obvious" is observation effect talking. So is "Let me try that again" after a single failed attempt. Real users don't do that. Real users close the tab and try something else. But in a test session, people try to be good participants. They try to give you data. They try not to waste your time. And all of that trying changes what they do.

Another version: they narrate everything, even when you haven't asked them to. "Okay, so I'm clicking here... and now I'm reading this... and I think I need to scroll down..." That's not how people use software alone. That's performance. It's not dishonest — they're genuinely trying to help you understand their process — but it's a version of their behavior that only exists because you're watching.

---

Don't confuse observation effect with observer bias. Observer bias is when *you* influence the participant — when you help them, hint at the answer, or react to their struggles in ways that change what they do next. That's your behavior affecting theirs. Observation effect is when *awareness of being watched* changes their behavior, even if you're sitting perfectly still saying nothing. One is about what the facilitator does. The other is about what the participant feels.

Here's how to tell them apart: if the participant is trying harder because you made a face when they struggled, that's observer bias. If they're trying harder because someone's in the room and they don't want to look bad, that's observation effect. Observer bias requires action from you. Observation effect just requires your presence.

This also isn't the same as social desirability bias, though they're related. Social desirability is about what people *say* — answering survey questions in ways that make them look good, claiming they'd use a feature they'd never actually touch. Observation effect is about what people *do* — the extra care, the extra effort, the behavior that only shows up when they know they're being studied. One distorts self-report. The other distorts action. You see social desirability in post-session interviews when someone says "yes, I'd definitely use this" while their actual behavior during the session showed them avoiding it entirely.

---

Try noticing it in your next test session. Watch for the moment someone apologizes for being slow, or explains why they're confused, or tries something a second time after it fails once. That's observation effect. Now imagine them alone — no moderator, no recording, no one watching. Would they still try again, or would they bail? If the answer is bail, you're seeing the gap between observed behavior and natural behavior.

You can also catch this in how people narrate. If they're explaining every click like they're teaching you how the interface works, that's performance. Real users don't narrate. Real users scan, click, swear quietly when it doesn't work, and try something else. The narration only exists because you're there.

One more place to look: the very beginning of the session. Some participants start out tentative and careful, then relax as the session goes on. Others stay in performance mode the whole time. The ones who relax are letting observation effect fade. The ones who don't are still performing. Both are useful data, but only if you notice which mode they're in.

---

**What next:** If you caught observation effect in a real test session — someone being too careful, too polite, too persistent — you're ready for [215a-moderated-usability-session.md]. That piece walks through moderating a full session and includes techniques for reducing observation effect: framing the test to lower stakes, normalizing failure, and pacing the session so participants stop performing and start just using the thing.

If you haven't run a test session yet, start with [157-why-you-dont-help-during-testing.md]. That covers observer bias — the other side of this coin, where your behavior changes theirs. You'll want both concepts in place before moderating your first session.

---

**Sources:**

Mayo, E. (1933). *The Human Problems of an Industrial Civilization*. New York: Macmillan. (Original Hawthorne studies documenting observation effects in workplace productivity research.)

Nielsen, J. (1993). *Usability Engineering*. Boston: Academic Press. (Establishes think-aloud protocol and addresses participant behavior in usability testing methodology.)

Webb, E. J., Campbell, D. T., Schwartz, R. D., & Sechrest, L. (1966). *Unobtrusive Measures: Nonreactive Research in the Social Sciences*. Chicago: Rand McNally. (Foundational work on reactivity and observation effects in behavioral research.)
