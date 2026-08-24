# What Running Code Tells You That Diagrams Don't

**Tier:** 200 — Practice | **Arc:** 309 (Prototyping) | **Prereqs:** 177, 178, 147 | **Wave:** 4

You're three design reviews into the same feature. Each review ends the same way: "It depends on how the data looks." Somebody sketches a wireframe. Everyone agrees the wireframe looks fine with placeholder numbers. Twelve rows, not the forty thousand that live in production. Nobody knows what happens when the actual dataset shows up.

Somewhere around the fourth review, someone says what everyone has been thinking since the second one: "We should probably just build it and see."

That's not giving up on design. That's instinct catching up to evidence.

---

Some questions about a feature can only be answered by touching the system. Not because you're impatient. Because the answer lives in runtime behavior. Does the API respond fast enough for a live preview to feel real? Does this third-party calendar component handle nested recurring events? Does the filter experience stay manageable when the data is real and enormous rather than small and invented?

Wireframes show what you intend. Running code shows what's true.

You've spent time with prototypes. You know a prototype isn't for shipping: it's for learning something specific. Build to Think applies that same logic directly to code: you write real implementation, to a deliberately shallow depth, specifically to surface the one thing that's been blocking progress. The artifact isn't the code. The artifact is the answer you couldn't get any other way.

---

Use this when design questions keep circling because their answer depends on runtime behavior: real data volume, real API response shape, real state complexity. The pattern that tells you it's time: every design conversation ends with "it depends on..." and what it depends on is something nobody can see in a wireframe. That's the signal.

---

Donald Schön (1983) spent his career studying how professionals generate knowledge, and his finding was uncomfortable for anyone who assumes thinking precedes doing. Understanding doesn't fully precede engagement. It emerges through it. His term was "reflection-in-action": the practitioner runs experiments that "generate both a new understanding of the phenomenon and a change in the situation." What you're thinking shifts as you act.

Software teams figured this out independently. Kent Beck introduced spike solutions in Extreme Programming, time-boxed experiments aimed at learning one specific thing. Ron Jeffries, one of Beck's collaborators on the C3 project, described it plainly: a spike is concluded when you learn what you needed to learn. Not when the code is clean. Not when the feature works. When the question is answered.

Kery and Myers (2017) at Carnegie Mellon confirmed what practitioners already suspected: that "writing code to prototype or experiment" while "allowing the end goal to evolve throughout the process" is a distinct, legitimate mode of inquiry.

Build to Think is a spike with explicit design intent.

---

The discipline starts before a line of code is written. Name what you're trying to learn. "Does the filter stay usable when the result count hits five figures?" "Can we display AI-generated content in a fixed-height card, or does the length variability break the layout?" If the sentence requires "and," it's two questions. Pick one.

Then name your stopping condition: what will count as an answer? What does "learned it" look like? If you can't describe when you'd stop, you don't have a question — you have a direction. And a direction produces a very different kind of build.

Build shallow, using real data and a real endpoint. Implement only what the question requires, and resist everything beyond it. Skip error handling, loading states, styled components. You need the encounter, not a product.

Run it. Use the artifact the way the feature is supposed to be used. Note every moment where behavior diverges from what the design assumed, and what becomes obvious in motion that was unclear on paper. These moments are the data you came for.

Extract the design decisions. Each observation becomes a constraint or a confirmation: "pagination required at scale," "card height must be dynamic with a max and a truncation pattern," "the latency is fine — the loading state is cosmetic, not functional." Write these down before you close the IDE. This document is the artifact. The code is the byproduct.

Then stop. Decide deliberately: foundation for the next iteration, or discarded? Beck's teams planned to throw away the spike. They kept the decisions, not the code.

---

The failure mode looks like progress. You've been building for two hours. The question was answered ninety minutes ago, but the code is working pretty well, and it just needs a few more routes. Maybe some error handling. You're here anyway.

Arkes and Blumer (1985) documented the mechanism behind what happens next: once you've invested in something, continuing it feels necessary — even when the original purpose has already been met. The build feels like forward motion. The stopping condition gets quietly replaced by a new one. (If you've watched a team demo a "prototype" to stakeholders who immediately asked when it would ship, then watched everyone in the room hesitate before answering, you've seen this exact thing.)

The stopping condition isn't optional. It's the whole method.

---

Find a technical question in your current sprint where the answer depends on behavior you haven't seen in a running system. Write it in one sentence. Write the stopping condition in one sentence. Block two hours. Build only what answers the question. Stop at two hours regardless. Extract at least two documented design decisions from what you observed. Then decide deliberately: discard the code and carry the learning forward, or preserve it as a foundation.

---

You'll know it worked if you made at least one design decision after building that you couldn't have made from reviewing static artifacts alone. The false positive: the code went directly into the next PR without a separate decision phase. That's building to ship. The spike was skipped, not run.

---

Over the next week, look at one feature your team shipped in the last quarter. Find the "we realized during development that..." moments. Each one is a question that Build to Think would have answered earlier, at lower cost, before the design direction was locked. Write one sentence: what would you have named as the question, and when in the project would you have run the spike?

If you share it in [the relevant channel], you'll see what others caught too.

---

After you've run this yourself: tools like Cursor or Copilot bring the build step close to zero cost. You can get to the encounter with reality in thirty minutes instead of two hours. This makes the discipline question more important, not less. Cheap building removes the cost barrier. It doesn't remove the need to name the question first, or to stop when it's answered. The tool runs the code. You have to run the thinking.

---

If you're deciding between approaches (paper sketch, AI-generated prototype, or this one), the selection guide lives in the prototyping arc overview (309). If you built something that's working and you're feeling like you should keep it, read 103 before you commit.

---

**Sources**

Schön, D. A. (1983). *The Reflective Practitioner: How Professionals Think in Action.* Basic Books. Professional understanding emerges through action — experiments in practice "generate both a new understanding of the phenomenon and a change in the situation."

Beck, K. (1999). *Extreme Programming Explained.* Addison-Wesley. / Jeffries, R. (XP spike documentation). Spike solutions as time-boxed learning experiments: "The spike is concluded when you learn what you needed to learn." Code is expected to be discarded; the learning is what carries forward.

Kery, M. B. & Myers, B. A. (2017). *Exploring Exploratory Programming.* Carnegie Mellon HCI Institute. Exploratory programming defined by two essential features: "writing code to prototype or experiment" and "allowing the end goal to evolve throughout the process."

Arkes, H. R. & Blumer, C. (1985). The psychology of sunk cost. *Organizational Behavior and Human Decision Processes, 35*(1), 124–140. Once invested in a direction, people continue even when the original objective has been met or abandoned — continuation feels less wasteful than stopping.
