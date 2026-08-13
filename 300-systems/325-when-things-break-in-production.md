# When Things Break in Production
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** Custom Dev primary | **Prereqs:** 100 (Assumption vs. Fact), 113 (Defining Success Before You Start), 126 (Mental Models), 249 (Loss Aversion), 253 (Sunk Cost Fallacy), 259 (Cognitive Dissonance)

**Goal:** Respond to production failures in a way that protects users, supports the team, and produces learning — by separating the incident response from the post-incident analysis, communicating with appropriate transparency, and generating findings that prevent recurrence rather than assigning blame.

**Trigger:** Something in production broke, and the team is in reactive mode. Users are affected. The pressure is to fix it fast and explain it minimally. What's needed is the opposite: clear-headed response that protects users now, honest communication that maintains trust, and analysis afterward that produces durable learning.

---

## Part 1 — The Incident Response: Users First

**Concept:** When something breaks in production, two things need to happen in parallel: technical remediation (diagnose and fix the problem) and user communication (tell affected users what's happening). These are often treated as sequential — fix it, then communicate. The problem with this sequence is that users experiencing the failure are not waiting quietly. They're forming a mental model of what happened based on what they're seeing: nothing works, nothing tells me why, and I don't know when it will be fixed. That mental model — formed in the absence of communication — tends toward the most alarming interpretation.

The technical team's primary instinct during an incident is to diagnose. The user's primary need during an incident is to know what's happening, whether their data is safe, and when they can expect resolution. Meeting the user's need doesn't require a complete diagnosis. It requires honesty about what's known now.

**Method:**
Within the first 15 minutes of a confirmed production incident:
1. Identify the user-facing impact: who is affected, what specifically are they unable to do, is there any risk to data?
2. Write a status communication that states: what's happening (in user terms, not technical terms), what users should or shouldn't do right now, that the team is aware and working on it
3. Publish the status communication to wherever affected users will look for it — the product itself (if it's still accessible), the team channel, a status page, email
4. Set a cadence for updates: even if there's nothing new to report, "we're still working on it, estimated resolution is [time]" is more trust-preserving than silence

**What you end up with:** A user-facing communication stream that runs parallel to the technical response — so users aren't left to interpret silence.

**Proof:** After an incident, the question "what did we tell users during the incident?" should have a specific, timestamped answer. If the answer is "nothing until it was fixed," the user communication didn't happen.

**Watchout:** The instinct to wait until there's more information before communicating produces a gap between the incident and the first user communication. Every minute of that gap is a minute users are forming their own interpretation. An early, honest "we know something is wrong and we're investigating" is better than a complete explanation that arrives late.

---

## Part 2 — Restoring Service Without Creating New Risks

**Concept:** The pressure during an incident is to restore service as fast as possible. Fast restoration is important. But speed and stability trade off — a quick fix that addresses the symptom without the cause creates the conditions for a recurrence, and a recurrence is worse than the original incident because it signals that the first incident was not fully understood. The restoration decision is also a risk decision: what are we confident this change accomplishes, and what might it affect that we haven't tested?

The cognitive trap during an incident: the team is under pressure, Loss Aversion is active (the current broken state feels costly), and there's a strong pull toward any action that might resolve it. This produces the risk of taking too many actions simultaneously — making several changes at once makes it impossible to know which one fixed the issue and which ones may have introduced new issues.

**Method:**
During remediation:
1. Form a hypothesis about the cause before taking action: "we believe the issue is caused by X, evidence Y, predicted fix Z"
2. Make one change at a time, with a defined check after each change — this preserves the ability to attribute which action had which effect
3. After each change: verify the intended effect and check for unexpected effects before the next change
4. Before declaring the incident resolved, verify the fix addresses the root cause hypothesis — not just that the symptom has stopped

**What you end up with:** A remediation process that restores service with confidence in the cause and minimal side-effect risk.

**Proof:** If the incident recurs within 24 hours of the "fix," the fix addressed the symptom without the cause. That's not a failure of process — it's a signal that the root cause hypothesis needs more investigation, not more patches.

**Watchout:** Some incidents require immediate symptom relief (rollback, traffic reroute) before root cause is understood. That's acceptable. The critical discipline is labeling it correctly: "we've stopped the immediate failure but the root cause is still under investigation" — not "the incident is resolved."

---

## Part 3 — Post-Incident Communication: Transparency Without Over-Disclosure

**Concept:** After an incident is resolved, there are typically two failure modes in communication: too little (users learn nothing about what happened, trust erodes) and too much (every technical detail is disclosed, the communication produces anxiety or confusion without providing useful information). The goal is transparency that serves users — information that helps them understand what happened, whether they need to take any action, and what the team is doing to prevent recurrence.

User communication about incidents is not about absolution (making the team look better than they were) or excessive honesty (disclosing technical details that users can't act on). It's about the information users need to make decisions about whether to trust the system and whether to take any action with their data.

**Method:**
After an incident is resolved, write a post-incident summary for affected users that covers:
1. **What happened:** in user terms — which features were affected, for what period, and what users experienced
2. **Impact:** were any user actions, data, or workflows affected beyond the downtime? If so, what specifically?
3. **What was done:** a brief, plain-language description of the fix — not the technical implementation, but what changed and why it should prevent recurrence
4. **What users should do:** if there's any action users need to take (check something, re-submit something, expect a delay in processing), name it specifically; if there's nothing to do, say so explicitly ("no action required on your end")
5. **What the team is doing to prevent recurrence:** one sentence about the systemic change being made, not a promise that this will never happen again

**What you end up with:** A post-incident communication that serves users — honest about what happened, clear about impact, actionable where action is needed.

**Proof:** A user who reads the post-incident summary should be able to answer: "did this affect me? Do I need to do anything? Is it safe to use the product now?" If those three questions can't be answered from the summary, it needs revision.

**Watchout:** "We apologize for the inconvenience" is not communication — it's a placeholder. Apologies belong in the summary, but they don't substitute for the information users need. And promising that the issue "will never happen again" is a promise that can't be kept; "we're implementing X to significantly reduce the risk of recurrence" is both honest and more credible.

---

## Part 4 — The Post-Mortem: Learning, Not Blame

**Concept:** A post-mortem that ends with "who made the error" has failed its purpose. Incidents are almost never the product of a single person doing something wrong — they're the product of system conditions that made the error possible. Finding the person who made the last action before the failure is easy and produces nothing useful: the system conditions that made that action possible remain unchanged, and the next person in that role will encounter the same conditions.

A post-mortem that produces learning identifies the system conditions that contributed to the incident — the gaps in testing, the missing monitoring signal, the process step that was skipped, the assumption that wasn't validated — and changes those conditions. The question is not "what did the person do wrong" but "what would have had to be different for this incident not to have happened."

**Method:**
Within 48 hours of incident resolution, conduct a structured post-mortem:
1. **Reconstruct the timeline:** what happened, in what sequence, with approximate timestamps — this is factual reconstruction, not interpretation
2. **Identify contributing conditions:** for each event in the timeline, what system conditions made that event possible? Missing monitoring? Insufficient testing coverage? An assumption that wasn't validated? A process step that wasn't followed because it was unclear?
3. **Distinguish contributing conditions from contributing causes:** contributing conditions are things the system could change; contributing causes are individual human actions, which are not changeable by systemic intervention
4. **Write specific, actionable follow-up items for each contributing condition:** "add monitoring for [specific signal]," "add test coverage for [specific case]," "revise the deployment checklist to include [specific check]" — not "improve our testing" or "be more careful"
5. **Assign each item a specific owner and a specific date**

**What you end up with:** A set of specific, owned improvements to system conditions — the things that will make a recurrence less likely, not a narrative about what went wrong.

**Proof:** A post-mortem that produces no action items didn't find the contributing conditions. A post-mortem that produces 15 action items found too many contributing conditions to address — prioritize to the 3 that would have had the most impact.

**Watchout:** Post-mortems in environments where blame is the cultural norm will produce blame-driven findings even with a "no blame" framing. The format doesn't change the culture. If the post-mortem is used to build a case against a person, the learning value is destroyed along with the team's willingness to be honest in future post-mortems.

---

**Try This:** Review the last production incident in your context — even a small one. Write a post-mortem using Part 4's structure. Identify the contributing conditions (not the contributing cause). Write three specific, actionable follow-up items. Do any of those items represent changes that would have prevented the incident?

**Take This Further:** After your next incident, write the post-incident user communication from Part 3 before publishing it, and test it against the three questions: "did this affect me? Do I need to do anything? Is it safe to use the product now?" Revise until all three are answerable. Write one sentence afterward: what did the test reveal that you would have published without the check?

**Judgment Exercise:** Your post-mortem has identified a contributing condition: a testing gap that was known before the incident but wasn't addressed because the feature was under time pressure. The contributing cause (in timeline terms) was a code change that wasn't caught because the test coverage was missing. The developer who made the change is junior and wasn't aware the coverage gap existed. What do you write in the post-mortem, who are the action items assigned to, and what do you say to the developer?

**What Next:** 324 (Ship / Patch / Hold) for the pre-launch decision framework that reduces incident risk. 300 (Design Debt) for tracking the systemic improvements that post-mortems generate.
