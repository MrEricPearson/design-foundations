# Decision Inventory
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** None | **Note:** Gateway to the decision landscape cluster; prereq for 194, 195; pairs with 182

**Goal:** After this piece, you will be able to recognize when you are designing inside a set of decisions that have already been made — and stop treating inherited decisions as your starting point without examining them first.

**Concept:** You don't start with a blank slate. Nobody does. By the time you open a design file or write the first line of code, a set of decisions has already been made that constrains what you can build. The development framework was chosen. The design system was selected. The database schema was defined. The vendor software was purchased. The AI tool generated a first-pass structure. The team decided to use this component rather than build a custom one. Each of these is a decision. None of them are neutral.

The failure mode: treating inherited decisions as the starting point without auditing them. If you accept the framework, the design system, the vendor's IA, the AI's first draft, and the previous team's component choices as given, you have accepted their assumptions as yours — including the wrong ones. You've built your work on a foundation you haven't examined.

The practice: before designing, inventory the decisions that have already been made. For each: who made it, when, on what basis, and is it still valid given the current problem? This is not a challenge to every decision — most inherited decisions are fine and should stand. It is a deliberate assessment that separates "this is a real constraint" from "this is a decision we haven't revisited."

The mechanism underneath: invisible decisions are still decisions. They shape what's possible, what looks expensive but isn't, and what looks cheap but will cost dearly when a constraint that was accepted without review turns out to be wrong. Making them visible doesn't add work. It eliminates wasted work on paths that were never available — and identifies paths that look closed but aren't.

**You'll see it when:** A team is told "we can't do that" and accepts it — then a different team does it. The constraint wasn't real; it was an unexamined inherited decision that someone treated as immovable. Or: a design goes through weeks of revision constrained by a technical or content decision that nobody questioned, and then someone asks "wait, why do we have to do it this way?" and the answer is "I don't know, that's how it's always been."

**The signal:** A sentence starting with "we can't because..." without the speaker knowing specifically why or when that decision was made. The "can't" is being treated as a constraint when it may be an unexamined inherited decision.

**Don't confuse a decision inventory with a requirements document** — requirements describe what the thing should do; a decision inventory describes what has already been decided about how it should work. Requirements are forward-looking; the decision inventory is backward-looking. You do the inventory to understand what space you're designing in before specifying what should happen in that space.

**Try Noticing:** Take something you're working on or working toward. Spend 5 minutes listing every decision that has already been made that constrains it — technology choices, tool choices, structural choices, vendor relationships, prior design decisions that current work has been built on. For each one: do you know why that decision was made? Is it still valid? If you can't answer "why" for a decision that significantly shapes your work, that's an unexamined constraint.

**What Next:** Once you can see the decisions that have been made, you need vocabulary for distinguishing between them. Read 194 (Three Constraint Types) to understand which inherited decisions are fixed, which are fixed but changeable, and which only appear to be fixed.
