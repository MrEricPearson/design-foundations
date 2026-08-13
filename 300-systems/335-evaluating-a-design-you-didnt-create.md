# Evaluating a Design You Didn't Create
**Tier:** 300 — Orchestrate | **Arc:** Full arc (4 parts) | **Audience:** PM primary | **Prereqs:** 107 (Framing the Problem), 113 (Defining Success Before You Start), 115 (Giving and Receiving Feedback), 136 (Critique vs. Feedback), 317 (From a Vague Ask to a Solvable Problem), 318 (Writing Requirements That Survive the Build)

**Goal:** Judge whether a design solves the stated problem — and name concerns in a way that preserves the designer's domain.

**Trigger:** You've received a design for review — from an embedded designer, a vendor mockup, or a self-service tool output. The trigger is not "the designer asked for feedback." It is "you are now the person responsible for deciding whether this design answers the question that was defined."

---

## Part 1 — What You're Actually Evaluating

**Concept:** The PM's review job is to assess whether the design gives users a clear path to the outcome defined in the brief — not whether it looks good or is technically feasible. Those are real questions, but they belong to other people in other conversations. When a PM evaluates aesthetics, they're doing the designer's job. When they evaluate implementability, they're doing the developer's job. Neither protects the user.

**Method:**
1. Before opening the design, re-read the problem statement and success criteria from the brief (317 and 318 if you used them)
2. Write one sentence: "A user needs to be able to [task] so that [outcome]"
3. Open the design and trace that task: can a user complete it without instruction? How many decisions does it ask them to make? Where does the path stall or break?
4. Note every point where the path is unclear or requires knowledge the user won't have — these are your structural concerns

**What you end up with:** A task-centered lens on the review, not an aesthetic or technical one. One question anchoring everything: does this design give the user a clear path to the outcome we defined?

**Proof:** If your review notes contain observations about colors, spacing, or implementation approach, you reviewed the wrong thing. If your notes describe the user's path and where it breaks or stalls, you reviewed the right thing.

**Watchout:** The design may look great and still not answer the right question. Substitution is the most common failure mode — teams design for a version of the problem that was easier to solve, not the one that was defined. Evaluating visual quality doesn't catch substitution.

---

## Part 2 — Structure Before Style

**Concept:** Structural concerns (does this give users a path?) and stylistic concerns (does this look right?) require different expertise to evaluate and should be separated. Structure is within the PM's scope; style is not. Conflating them produces feedback that's hard for designers to act on and erodes trust in the review process.

**Method:**
1. Run the information-only check: mentally strip the visual styling and focus on what's underneath
2. Ask for every element: what can a user do with this? In what order? What decision are they being asked to make?
3. Ask: what information does the user need to make that decision? Is it present in the design, or would they have to know it already?
4. Write two lists: structural concerns (gaps in the user's path, missing information, unclear next steps) and style observations (layout, colors, visual hierarchy)
5. Surface only the structural list in the review; defer or drop the style observations unless the designer asks

**What you end up with:** Two distinct feedback categories — structural (within scope) and stylistic (outside scope). You surface the structural concerns and hold the stylistic ones.

**Proof:** If a designer can act on every item in your feedback without re-explaining the problem to you, the feedback was well-scoped. If they respond "but that was a design decision" to any item, you crossed into their domain.

**Watchout:** "This doesn't look like our brand" is a style note. "Users may not recognize this as an action they can take" is a structural note. The difference is whether the concern is about appearance or about user capability.

---

## Part 3 — The Problem Statement Check

**Concept:** Many designs answer a slightly different question than the one that was stated — usually one that was easier to design for. The PM's job is to catch this substitution before implementation. Once development starts, the cost of re-aligning on the right problem grows exponentially.

**Method:**
1. For each primary action in the design, write the sentence from the problem statement it serves — the specific user need or goal that action addresses
2. If you can't find a sentence in the problem statement that the action clearly serves, mark it: this action needs explanation before the review ends
3. Count the unmarked vs. marked actions — if most actions trace cleanly, the design is aligned; if several can't be traced, the design has drifted
4. For each marked action, write the question to raise in the review: not "why is this here?" but "which user need is this serving that I'm not seeing?"

**What you end up with:** Evidence that the design is or isn't answering the problem that was defined — before implementation locks in the direction.

**Proof:** If you can draw a direct line from every primary user action to a sentence in the problem statement, the design is coherent. If two or more actions require explanation to connect to the problem, the design has drifted and the drift is worth naming before the review ends.

**Watchout:** "Users asked for this" doesn't mean it belongs in the design — it means someone expressed a preference. The question is whether the preference serves the actual defined goal, or whether it served a different goal that felt adjacent.

---

## Part 4 — Naming the Concern, Not the Fix

**Concept:** PMs who leave design reviews having prescribed solutions rather than named problems create two problems: they undermine the designer's domain, and they lock in solutions prematurely. A concern named as a problem opens the design space. A concern named as a fix closes it.

**Method:**
1. For each structural concern from Parts 1–3, write it as a question rather than a prescription
2. Check: does the question name a potential user failure without telling the designer how to address it? If yes, it's well-formed. If the question contains a "should" or implies a specific change, rewrite it
3. Distinguish between questions about user capability ("Will users know what to do next after submitting?") and questions about design choices ("Why isn't the button blue?") — only the first belongs in the review
4. Bring the question list into the review session; let the designer respond with their reasoning or a proposed change; don't resolve the questions yourself

**What you end up with:** A list of problem-framed questions that open the design space for the designer to address — not solution prescriptions that close it.

**Proof:** If the designer takes your feedback and proposes a solution you didn't anticipate — one that solves the concern better than what you would have prescribed — the feedback was well-formed. If they implement exactly what you described verbatim, the question was probably functioning as an instruction.

**Watchout:** If you find yourself using the word "should" in feedback, you've crossed into prescribing. Restate as a question. "The button should be blue" is a prescription. "Will users see this as the primary action?" is a concern.

---

**Try This:** Take a design you reviewed in the last month. Apply Part 3's problem statement check: for each primary user action in the design, write the sentence from the problem statement it serves. Where can't you find one? Write that concern as a question — not a fix.

**Take This Further:** In your next design review, name one concern as a problem-framed question rather than prescribing a solution. After the review, write one sentence: did the designer's response tell you the concern was real, or that your framing of it was off?

**Judgment Exercise:** You're reviewing a design that's visually polished, clearly implementable, and the team is excited about it. When you trace the primary user task, it requires four steps where two would suffice — but every one of the four steps is individually useful and individually defensible. The design doesn't do anything wrong; it just does more than the user needs to accomplish the goal. What is your concern, and how do you name it without prescribing a redesign? What would change about your answer if the extra steps served a business need the brief didn't capture?

**What Next:** 321 (Managing the Design Feedback Loop) for turning this review capability into a decision-producing meeting. 311 (Psychology of Stakeholder Decisions) when stakeholder reaction to the feedback needs managing. 318 (Writing Requirements That Survive the Build) to trace the design back to the requirements it was built against.
