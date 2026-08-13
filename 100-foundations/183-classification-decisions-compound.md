# Classification Decisions Compound
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 179, 182 | **Note:** Prereq for 184, 186, 197; bridges bolt-on cost to naming and taxonomy

**Goal:** After this piece, you will be able to recognize when a naming or classification decision is creating compounding constraints — before those constraints have been built on top of.

**Concept:** Every time you name something, you make a claim about what it is. That claim is not just descriptive — it is generative. It determines what the thing can be related to, how it can be grouped, how it can be searched, and what other decisions can be made in reference to it. The name creates the concept. The concept becomes the foundation. The foundation accumulates structure on top of it.

When the same thing is called different names in different parts of a system — "task" in one phase, "request" in another, "item" in a third, "work order" in a fourth — the classification has fragmented. Four names means four things. Four things means four data structures, four displays, four sets of filters, four status systems, and zero ability to reason across them. The fragmentation is not a naming problem; it is a structural problem that expresses itself as a naming problem.

The inverse mechanism: when you recognize that four different names refer to the same underlying thing, giving that thing one name makes cross-phase reasoning possible. One name, one content type, one status system, one consolidated view. What was four screens becomes one. This is not a refactoring of names — it is a restructuring of what the system knows about, made available by the recognition that the classification was wrong.

Classification compounds in the other direction too. The more decisions made on the assumption that "task" and "request" are different things — the more code, the more content, the more workflow — the more expensive it becomes to unify them. The classification decision is a seed. Every piece of work done in its reference is fertilizer. The compounding is exponential in the worst cases.

**You'll see it when:** Different teams use different words to describe what is, when examined, the same underlying thing — the same deliverable, the same process step, the same record type. Or: a request to build a "simple" cross-phase view meets resistance because "the data is organized differently in each phase." The organization reflects the classification; the classification reflects the assumption that these are different things.

**The signal:** When you ask "how does a [thing] move from one phase/team/system to another?" and the answer is "we communicate manually" or "we have a handoff document" or "they get a notification" — there is almost certainly a classification problem underneath. The manual handoff exists because the system doesn't have a concept that spans both phases. It doesn't have that concept because the classification stopped at the phase boundary.

**Don't confuse this with terminology preference** — if two teams prefer different words for the same thing but the underlying system treats it as the same thing, that's a terminology gap, not a classification problem. A classification problem means the system itself treats them as different things — different tables, different workflows, different filters. Terminology can be solved with a glossary. Classification requires structural change.

**Try Noticing:** Find a handoff point in your work — where output from one phase becomes input to the next. Ask: what does one side call the thing being handed off? What does the other side call it? If the names differ, look underneath: does the system treat them as the same thing or different things? If different, what has been built on the assumption that they are different? That is the accumulated structure of the classification decision.

**What Next:** Naming as a structural act is explored more deeply in 197 (Naming as Model Design), which covers when a new name can unlock a new architecture. For how to build a vocabulary that prevents classification drift from the start, read 186 (Taxonomy Design Basics).
