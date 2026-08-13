# Spotting Where AI Surprises People → Mocking and Testing an Agent Handoff
**Tier:** 300 — Orchestrate | **Arc:** Full arc (5 parts) | **Prereqs:** 106 (sketching, for Part 3+), 147 (AI as execution partner), 167 (Automation Bias and Calibrated Trust), 168 (Explainability vs. Transparency in AI), 169 (Affordance)
**Note:** Master outline lists Parts 1-2 ("Spotting AI Surprises") and Parts 3-5 ("Mocking and Testing an Agent Handoff") as separate Tier 200 methods. Single-source treatment applied here. Prereq for 308 (Designing for AI Trust).

**Goal:** After this arc, you will be able to identify where an AI-assisted workflow breaks user expectations, build a low-fidelity mock of the handoff moment, and run a short test to find the gaps before they're baked in.

**Trigger:** you're using AI in a workflow and want to catch where it surprises people — before those surprises are expensive to fix or baked into agent logic.

---

## Part 1: Keep a Log

When an AI does something unexpected — good or bad — that moment is worth capturing before it's forgotten.

**Method:**
1. Keep a simple running list — wherever's easiest — of moments an AI's output surprised you or a teammate.
2. Note both directions: things that went wrong, and things that worked better than expected.
3. A sentence is enough. Don't overthink the entry.

**What you end up with:** a growing record of real AI behavior, not just your general impression of it.

**Proof:** A log entry written in the moment is more accurate than a memory of the same moment reviewed later. The log exists and can be searched; a general impression can't. Surprises that go unlogged disappear; ones that are logged become the raw material for Part 2.

**Watchout:** log surprising successes too, not just failures. Both reveal assumptions that turned out to be wrong.

---

## Part 2: Turn the Log Into Patterns

A single surprising moment doesn't tell you much. A cluster of similar ones does.

**Method:**
1. Every so often, reread your log.
2. Group similar entries together — do certain kinds of tasks keep producing surprises?
3. Use that pattern to decide where you need tighter guardrails or more testing before trusting the output.

**What you end up with:** a short list of places where your AI-assisted process needs more caution, based on real evidence.

**Proof:** A cluster of similar log entries means the same kind of task is consistently surprising people. That pattern is actionable — it tells you specifically where to add guardrails or more explicit testing. A single entry doesn't; a cluster does.

**Watchout:** a handful of examples isn't a pattern yet. Resist generalizing from just one or two entries.

---

## Part 3: Mock the Handoff Moment

Before writing any actual agent logic, mock the moment where a human would receive the AI's output — what it looks like, what it says, how a person is expected to react.

**Method:**
1. Sketch or write out the handoff moment as if it already exists — what does the AI hand back, and how?
2. Keep it rough — a wireframe, a written script, whatever's fastest.
3. Don't build any real logic yet — this is still a guess you're about to test.

**What you end up with:** a low-cost mock of the moment that matters most, before any real engineering investment.

**Proof:** A rough mock that someone can react to is worth more than an unbuilt vision of what you plan to build. The roughness is intentional — a polished mock produces reactions to the polish, not to the handoff. A rough one produces reactions to the handoff itself.

**Watchout:** an overly polished mock creates the same false confidence as a demo. Keep it rough on purpose.

---

## Part 4: Test the Mock With a Real Teammate

Walk someone through the mock as if it's real, and watch what actually happens.

**Method:**
1. Show the mock to a teammate without over-explaining it first.
2. Watch where they hesitate, get confused, or do something you didn't expect.
3. Capture what surprised you — this feeds directly back into your surprise log.

**What you end up with:** real reactions to the handoff moment, before it's expensive to change.

**Proof:** A hesitation, a confused look, or an unexpected click during the test is direct evidence — not an inference. That reaction existed before the test; the test just made it visible before any engineering was locked in.

**Watchout:** someone too close to the project won't catch what a fresher set of eyes would. Pick a tester who isn't already deep in the context.

---

## Part 5: What Changed

The test only matters if it actually changes something.

**Method:**
1. Compare what you expected against what actually happened in the test.
2. Identify at least one concrete change to make based on the gap.
3. Make the change before moving forward — don't just note it for later.

**What you end up with:** a handoff moment that's actually been improved by what you learned, not just observed.

**Proof:** The gap between what you expected and what happened in the test is specific and checkable. If at least one concrete change addresses that gap before you move forward, the test changed something. If nothing changed, the test only produced observation — which is useful, but not what this step is for.

**Watchout:** a test without a follow-through change is just theater. If nothing changes afterward, the test didn't do its job.

---

---

## Before Deployment: When You Have No History to Learn From

Parts 1 and 2 assume a log of real AI behavior to find patterns in. If you're designing an AI feature from scratch with nothing yet deployed, the arc still applies — but the input changes.

**Design the visibility, control, and explanation structures in advance** — before any AI behavior is locked in — based on the AI behaviors you intend to produce. Work from your documented intended behaviors: "The AI will [do X] under [condition Y]." For each intended behavior, design what the user sees, what control they have over it, and how the AI explains itself.

**Test with simulated outputs.** Mock the AI's output at its expected confidence range — not just the happy path. If the AI will sometimes be wrong, mock what a wrong output looks like to the user and test how people respond to it. Surprises at deployment come from behaviors that weren't tested; simulated outputs let you test the behavior before the behavior exists.

**Log intended behaviors as a starting point for your real surprise log.** When the feature ships, your pre-deployment design decisions are the first entries — hypotheses about where users might be surprised. The real log confirms or revises them.

**The Judgment Exercise** ("No surprises have happened because there are no users yet") names this constraint. This section is the answer: design from intended behaviors, test from simulated outputs, log from day one.

---

**Try This:** find one moment in a current project where an AI takes action on a user's behalf or returns a result they didn't explicitly request. Write one sentence about what you think the user expects to happen at that moment — then write one sentence about what actually happens. That gap is your first log entry.

**Take this further:** in the next week, add five more entries to your surprise log. Write one sentence: did a pattern emerge that wasn't visible from your first entry alone?

**Judgment exercise:** You're designing an AI feature from scratch — nothing's shipped yet. No surprises have happened because there are no users yet. Parts 1 and 2 assume a log of real behavior to find patterns in. What do you use instead? How do you run the arc when you have no history to learn from?

**What Next:** once you've identified and tested the handoff moment, 308 (Designing for AI Trust) gives you the design system for addressing what you found — visibility, override, explainability, graceful failure, and calibration testing.
