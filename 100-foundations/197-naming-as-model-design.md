# Naming as Model Design
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 183, 179 | **Note:** Core strategic atom; one of the highest-leverage pieces in the library; prereq for 198, 199

**Goal:** After this piece, you will be able to recognize when a naming decision is actually a structural decision — because the name determines what the thing can become.

**Concept:** You've been taught that naming is communication — you name something so others understand what it is. This is partially right and mostly insufficient. Naming is also generative: the name you give a thing determines what affordances it can have, what other things it can relate to, and what capabilities it can enable. The name creates the concept. The concept creates the architecture.

Here is the mechanism: a name is a commitment about what a thing is. That commitment propagates forward. Every decision made after the naming — about what attributes the thing has, what it relates to, how it behaves, where it appears — is made in reference to that initial commitment. When the name is wrong (too narrow, too broad, captures the current instance rather than the general case), everything built on it inherits the wrongness.

The inverse: when the right name is found — the one that accurately captures the concept at the right level of abstraction — it unlocks capabilities that were structurally impossible before. This is not metaphor. Finding that a set of disparate things is actually one thing under a more general concept allows the system to treat them as one thing. Treating them as one thing enables queries, displays, and operations that could not exist when each was treated as separate.

The practical implication: before settling on a name for something in a system — a content type, a feature, a concept in the navigation, a process step — ask: does this name capture the general case, or just the current instance? A name that fits only the current instance will become a constraint as the system evolves. A name that captures the general case will accommodate evolution without structural revision.

The corollary that matters: when you're struggling to design something — when multiple screens solving the "same but different" problem refuse to consolidate, when a filter or search doesn't work the way you want, when a consolidated view seems impossible — consider that the problem may be a naming problem. Finding the right name for the underlying concept may make the architectural problem dissolve.

**You'll see it when:** A system has five different things that are "almost the same" — same purpose, same lifecycle, same attributes — but have different names and are therefore treated as different things in the data model, the code, and the UI. Or: a "simple" consolidation request requires "significant refactoring" because the consolidation reveals that three separate concepts in the current system are actually one concept with a name that hasn't been found yet.

**The signal:** Someone is asked to build a "unified view" of multiple things and the immediate response is "but they're all different" — followed by a list of minor variations. The variations may be real, but they may also be the attributes of one underlying thing, not the evidence that multiple things exist. The reflex to treat difference as separate-concept is the naming failure made visible.

**Don't confuse naming with labeling** — a label is a user-facing word on a screen; a name is a model-level concept that the system reasons about. Labels can be changed at any time without affecting the model. Names are structural commitments. Changing a name after building on top of it requires changing everything that was built in reference to it. Treat naming as a structural decision, not a writing decision.

**Try Noticing:** Look at something you're working on — a design, a data structure, a feature set. Find two or three things that seem related but are treated as separate. Ask: what would you call the concept that encompasses all of them? What attributes would that concept have? What would become possible if the system treated all instances as the same type? If the answer reveals significant new capabilities — filtering, consolidation, cross-context display — you've found a naming opportunity.

**What Next:** The skill of finding the name that unlocks the architecture is the core of strategic design judgment. Read 198 (Pattern vs. Model Problem) to learn how to recognize when you need this kind of structural insight — as opposed to a better implementation of the current structure. Read 199 (Transformation Within Constraints) for how to apply this thinking when the design space is heavily constrained.
