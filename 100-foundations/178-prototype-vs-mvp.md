# Prototype vs. MVP
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 177 (What a Prototype Is), 105 (Iteration) | **Note:** Foundational for all 309 prototyping arc pieces; pairs with 177

**Goal:** After this piece, you will be able to distinguish a prototype from an MVP — and catch the common failure mode of building one when you mean the other.

**Concept:** "MVP" has drifted in meaning until it functions as a synonym for "small, rough, and fast." This drift is expensive. A prototype is small, rough, and fast — but it is also disposable by design. An MVP is the beginning of a product. These are fundamentally different commitments, and conflating them produces a failure mode so common it has a name: the prototype that never gets thrown away.

The actual difference is a commitment to real users and what follows from it. A prototype has no real users. Its job is to answer a question, and when the question is answered, it is discarded. An MVP ships to real users. The moment it ships: it has users who depend on it, who will report problems, whose data it will accumulate, and who will be harmed if it's abandoned. It generates technical debt that must be managed. It creates support obligations. It becomes a system that must be maintained.

The mechanism: the decision to ship is a commitment to all of that, not just to building something small. "MVP" describes the scope of what's built, not a reduced version of the commitment. A minimum viable product is still a product — with all of a product's obligations.

When "MVP" is used to mean "prototype we're going to ship," the team bypasses the prototype's disposability — they've committed to maintaining something before they've learned whether it's worth maintaining. When "prototype" is used to mean "MVP we're going to throw away," they've created users who depend on something that doesn't have a maintenance plan.

**You'll see it when:** a team says they need to "build an MVP to test this idea." If the plan is to throw away the result after learning something, that's actually a prototype — and calling it an MVP commits the team to quality, maintenance, and support expectations that belong to production. The misuse surfaces when the "MVP" becomes customer-facing, goes to leadership as a deliverable, or gets handed to a support team.

**The signal:** ask what happens to the artifact after the learning. If the answer is "we learn from it and then build the real thing," it's a prototype called an MVP. If the answer is "we learn from it and then keep improving it," it's an MVP. If the answer is unclear or no one has thought about it: the commitment decision hasn't been made, and that's the conversation the team needs to have before anything is built.

**Don't confuse this with a pilot** — a pilot is a real, working version of something deployed to a limited audience to validate behavior at scale. A pilot ships to real users, generates real data, and has real obligations. It differs from an MVP in scope of audience, not in commitment level. Prototype → pilot → product is a progression. Conflating any of these steps telescopes the sequence in ways that skip the learning each is designed to generate.

**Try Noticing:** the next time a team commits to "build something small to test," ask: what is this thing's relationship to the users it will reach? Will it be maintained after the test? Who owns it? Which of those answers reflects the actual decision being made, and which reflects a commitment the team may not have explicitly accepted?

**What Next:** when the distinction is clear and you're ready to build a prototype rather than an MVP, read the 309 prototyping arc to choose the right approach. When the decision is to build an MVP instead, read 113 (Defining Success Before You Start) to establish the MVP's success criteria before building begins.
