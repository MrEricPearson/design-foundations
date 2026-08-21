# Prototyping Arc — Selection and Sequencing
**Tier:** 300 — Orchestrate | **Arc:** Prototyping | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity), 113 (Defining Success Before You Start) | **Parts:** 309a–309i (each publishes separately)

**Arc Goal:** Given a question you need to answer before committing, choose the prototype type that answers it with the least effort — not by familiarity, but by what the question requires.

**Arc Trigger:** You need to test an assumption before committing to what it drives. The question isn't "should we prototype?" but "what are we trying to find out, and what's the minimum artifact that answers it?"

---

The question you're testing determines the prototype you need. Everything else is habit.

Harder to follow than it sounds, because the habit runs deep. You reach for the approach you know — before naming what it's meant to find out. The findings confirm the direction that was already favored. (If you've spent weeks building something a two-hour session could've answered, you've paid the cost this arc prevents.)

The nine approaches differ in what question each answers. They're not a progression — start with the one that fits your question. Before you choose, write that question in one sentence. A prototype without a prior question has no scope.

---

### Paper and sketch → 309a

Paper prototyping answers the earliest question: does this direction make sense? Buxton (2007) showed that rough artifacts signal openness — a sketch reads as "this is still a question," and reviewers engage with direction rather than details. Polished artifacts shift reviewers into refinement mode before direction is confirmed. Use when the concept is unvalidated. When you're unsure which approach fits, start here.

---

### Lo-fi wireframe → 309b

Lo-fi wireframes test navigation. Visual design compensates for structural failure — users follow aesthetic cues even when organization doesn't work. Stripping visual treatment forces structure to carry the full load. A person who navigates correctly through a wireframe did so because the structure worked. That's the only navigation finding worth acting on before visual design is built. Use when concept is clear and the question is flow.

---

### AI-generated → 309c

AI-generated prototypes test interaction behavior, but require a prior specification. Write the question first. AI generates plausible structure from patterns, so output looks right before you've confirmed it is — the question is what you evaluate against. Use when interaction behavior, not concept or structure, is what remains unvalidated.

---

### Wizard of Oz → 309d

Wizard of Oz tests whether automated behavior is valuable before automation is built. A person simulating system responses provides the same utility signal as the system itself. Paul and Rosala (2024) at Nielsen Norman Group describe the method's value as one separation: "is this valuable?" answered before "can we build it?" Use for recommendations, smart defaults, or generated outputs where value is unproven and automation cost is high.

---

### Conversational → 309e

Conversational prototypes test dialogue logic. Systems break where input diverges from what's expected — and a scripted session surfaces those breaks before the system exists. Use when the interaction is primarily language-based: chatbots, guided flows, voice.

---

### High-fidelity → 309f

High-fidelity prototypes test the finished experience — emotional response, interaction feel, visual quality. Fidelity signals completion, shifting reviewers from structural feedback to execution feedback. Use only after concept and structure are sound. Using high-fidelity before both are confirmed gets you polish feedback on an unresolved foundation.

---

### Service → 309g

Service prototypes test seams. Most service failures happen between touchpoints — in handoffs, information transfers, and timing dependencies. Shostack (1984) formalized this: failure points live in backstage dependencies, not the visible moments where failures appear. Use when the experience spans digital and non-digital touchpoints, or when someone could succeed at every individual step and still fail at the journey.

---

### Parallel → 309h

Parallel prototypes test which direction works when you don't know enough to choose. Dow, Heddleston, and Klemmer (2010) at Stanford found that testing multiple directions simultaneously produced better results, more divergent thinking, and higher self-efficacy than developing a single direction. The mechanism is comparative data — which direction worked better, not just whether one can be made to work. Use when you have genuinely divergent intuitions and at least two distinct directions. Variations don't count.

---

### Build to think → 309i

Build to think tests what's actually true at a level of concreteness design artifacts can't reach. Cagan (2026) distinguishes "build to learn" from "build to earn" — functional prototypes with real data reveal behavioral patterns static mockups miss. Use when the question involves dynamic content, complex state, or behavior that's unpredictable until the system is running.

---

### Working with vendor software or third-party systems

You typically can't prototype the interface itself. What you can prototype: onboarding and communication wrapping the tool; configuration decision paths (paper or wireframe works here); and handoffs before and after a user reaches the vendor tool. Those experiences are yours to design.

→ See 220 (Working in Vendor Software) for the full constraint path.

---

**Try This — 20 minutes**

Take something you're working on now with at least one unresolved question about how it will function. Write the question in one sentence. Use the list above to identify the approach that fits. Build the minimum version that answers it — the fastest, not the most complete. Stop when the question is answered.

---

**If it worked:** You have a finding that confirms or challenges an assumption, and you know what to do next because of it.

---

**Over the next 2-5 days,** bring the prototype to one person who'll use what you're building. Let them engage first. Ask: "What did you expect to happen when you did that?" Then write one sentence: what changed your understanding of the question you were testing?

---

**Judgment Exercise**

This arc's key assumption: the prototype exists to answer a specific question, and that question is written before building starts.

Here's where that assumption fails: a prototype built to learn is now treated as a commitment. Teams are asking when they'll get it. Leadership has demoed it. Stakeholders have built expectations around what they saw. The prototype is load-bearing. Unvalidated assumptions still exist, and the cost of surfacing them has risen.

What would you change about your approach — and what would you preserve?

*(A well-formed answer preserves the discipline but changes the audience: the test is now internal, because the development team needs to stay open to findings — not the stakeholders already committed. The arc doesn't undo commitments. It tells you what questions remain inside them.)*

---

**What Next**

When you're ready to test with a real person, read 215a (Moderated Usability Session) or 215b (Unmoderated Usability Testing). If the prototype reveals a cross-team flow, read 303 (One Feature, Three Handoffs). To evaluate the prototype yourself first, read 216 (Heuristic Evaluation).

---

**Sources**

Buxton, B. (2007). *Sketching User Experiences: Getting the Design Right and the Right Design*. Morgan Kaufmann. Rough artifacts signal openness to exploration; high-fidelity prototypes foreclose alternatives prematurely by appearing finished.

Cagan, M. (2026, April 16). Build to learn vs. build to earn. Silicon Valley Product Group. https://www.svpg.com/build-to-learn-vs-build-to-earn/ Functional prototypes with real data generate behavioral learning static mockups cannot produce.

Dow, S., Heddleston, K., & Klemmer, S. (2010). Parallel prototyping leads to better design results, more divergence, and increased self-efficacy. *ACM Transactions on Computer-Human Interaction*, 17(4). https://dl.acm.org/doi/10.1145/1879831.1879836 Teams testing multiple directions simultaneously outperformed teams refining a single direction on design quality, divergence, and self-efficacy.

Paul, S., & Rosala, M. (2024, April 19). The Wizard of Oz method in UX. Nielsen Norman Group. https://www.nngroup.com/articles/wizard-of-oz/ Wizard of Oz prototyping validates utility before building the system that delivers it, lowering investment risk into complex technologies.

Shostack, G. L. (1984). Designing services that deliver. *Harvard Business Review*, 62(1), 133–139. Service blueprinting identified that failure points live in backstage dependencies between touchpoints — not in the customer-facing moments where failures appear.
