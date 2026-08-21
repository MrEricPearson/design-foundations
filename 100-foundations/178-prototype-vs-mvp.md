# Prototype vs. MVP
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 177 (What a Prototype Is), 105 (Iteration) | **Audience:** General | **Note:** Foundational for all 309 prototyping arc pieces; pairs with 177

**Goal:** After this piece, you can tell the difference between a prototype and an MVP — and catch the common failure mode of building one when you mean the other.

**Goal line (for publish doc):** Nobody plans to keep the prototype forever. It just happens.

---

Something shifts when a team says "let's build an MVP to test this idea." The word *minimum* does a lot of work in that sentence: minimum fidelity, minimum effort, minimum investment — and somewhere in the logic, minimum commitment slips in too. That last part is the problem.

"MVP" has drifted. In most conversations, it's shorthand for "small, rough, and fast." Prototypes are also small, rough, and fast. So the two terms have collapsed into each other in daily use, and teams have stopped noticing that they describe fundamentally different commitments.

The difference isn't fidelity. It isn't feature scope, or how polished the interface is. The difference is what happens the moment someone outside your team starts using it.

---

A prototype has no real users. Not as a limitation. As a definition. Its job is to answer a question: does this approach make sense, does this flow work, does this concept land? When the question is answered, the prototype is done. You throw it away and build the real thing. NNGroup's Laura Klein (2026) described this as making "design disposables": artifacts you create not to deliver to anyone, but to help yourself think. When they've done that job, throwing them away "is not failure. That's the point."

An MVP ships to real users. Sara Paul at NNGroup (2026) drew this distinction with useful precision: a prototype tests whether an idea has value, while an MVP tests whether a specific implementation will succeed by measuring real behavior — what people actually do, not what they say they'll do.

Real users means real data. It also means real obligations.

The moment your product reaches real users, it has users who depend on it. It accumulates data that needs managing, generates support requests someone has to answer, and creates technical debt. Ward Cunningham coined that term in 1992 to describe what accrues when code ships faster than it's properly built, and Martin Fowler has since shown what it costs: teams who rush below a quality threshold end up delivering later, not sooner, as cruft piles up and slows every subsequent change. Ship a prototype to real users and call it an MVP, and you've started that clock without the foundation to service what's now ticking on it.

---

You'll see this confusion most clearly when a team says "we want to build something small to test the concept, then throw it away if it doesn't work." That's a prototype. But if the plan is to show it to customers, collect real feedback, and iterate from there, that's an MVP, whatever anyone calls it. The word matters because the commitment it encodes matters.

The signal is one question: what happens to this thing after the learning?

Ask it about whatever your team is about to build, and notice where the discussion goes. When the answer is "we learn from it and then build the real thing from scratch," that's a prototype — disposable by design, exactly as intended. When the answer is "we learn from it and keep shipping improvements," that's an MVP. No clear answer means the commitment decision hasn't been made yet, and everything that follows depends on it: quality standards, maintenance expectations, and how users experience what gets shipped.

Eric Ries (2011) defined the MVP in the Lean Startup as "the smallest version of a product you can use to start the process of learning from customers." Learning *from* customers: not from internal testers, not from a simulation. Real customers means a real product, with real product obligations. Ries was describing the minimum viable start of something you're committed to, not a rough draft you might discard.

---

Don't confuse this with a pilot. A pilot is a real, working version of something deployed to a limited audience to validate behavior at scale. It has real users, real data, real obligations, the same as an MVP. The difference between a pilot and an MVP is the scope of the audience, not the level of commitment. A prototype is the only one of these three designed to be thrown away.

(Teams sometimes discover they've been running a "pilot" for eighteen months with no handoff plan. Different problem. Different piece.)

---

The failure mode worth watching for: the prototype that never gets thrown away.

It usually starts with someone saying "let's just ship this to a few users to get real data." Often that's a reasonable call, if the decision to create real users has been made explicitly. But it usually hasn't. The team thinks they're running a prototype. From the user's seat, they're using a product with nobody behind it. That gap is where support debt, maintenance debt, and trust debt accumulate at once.

Barry Staw (1976) found that people invest the most in a failing course of action when they were personally responsible for starting it. They double down to justify the original decision rather than walk away from it. A prototype turned product, built by the same team now responsible for maintaining it, will attract continued investment well past the point where scrapping it would have been smarter. The prototype becomes the product not because anyone decided it should. Because nobody decided it shouldn't.

Staw called this escalation of commitment. In product work, it disguises itself as iteration.

---

The next time someone proposes "building something small to test this," notice the two questions that would answer what this thing actually is: who will use it, and what happens to it after the test? When those have clear answers, the commitment decision has been made. When they don't, that conversation is worth more than whatever gets built first. Start there.

---

**What Next:** When the decision is to build a prototype, the 309 prototyping arc covers nine approaches and how to choose among them. When the decision is to build an MVP instead, read 113 (Defining Success Before You Start) to establish what the MVP needs to prove before the build begins.

---

**Sources**

Klein, L. (2026, May 22). The case for design disposables. *Nielsen Norman Group.* https://www.nngroup.com/articles/design-disposables/

Paul, S. (2026, March 27). Minimum viable product (MVP): Definition. *Nielsen Norman Group.* https://www.nngroup.com/articles/mvp-definition/

Ries, E. (2011). *The Lean Startup.* Crown Business.

Staw, B. M. (1976). Knee-deep in the big muddy: A study of escalating commitment to a chosen course of action. *Organizational Behavior and Human Performance, 16*(1), 27–44.

Fowler, M. (n.d.). Technical debt. *MartinFowler.com.* https://martinfowler.com/bliki/TechnicalDebt.html [cites Ward Cunningham, OOPSLA 1992]
