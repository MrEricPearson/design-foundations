# Q3 Prototyping Enablement — Content Model

## Purpose
- Q3 goal: a platform-wide Prototyping microlearning series (Teams + SharePoint) reinforcing that everyone on the platform supports dev outcomes and can improve clarity/stakeholder alignment through visualizing ideas.
- Plus one interactive talk per specialist chapter: Product Managers, Custom Dev, Non-Custom Dev (3rd party).
- Underlying (not surfaced) purpose, in priority order: (1) teach people to do this themselves, building appreciation through doing; (2) let them know design is available when it gets hard. Design should act as a force multiplier — stepping in only where teams can't do it themselves or with AI.
- AI is the bridge that closes the "onboarding a designer costs more than doing it myself" objection.
- Audience: functional/practitioner workers ONLY. No leadership content — cut entirely, not just deprioritized.
- Tone: first-person, peer/practitioner voice ("here's what I tried"), never authoritative or talking down. Modeled on a respected dev publishing a how-to on AI orchestration. Content stays silent on the AI-adoption mandate/consequences — that's leadership's message, not this content's job.
- Constraint: every piece (arc part or standalone) is under 5 minutes and self-contained toward ONE goal. Arcs should form a real narrative where order adds value — not just a badge on a loosely related topic cluster. Every part should still stand alone if read out of order.
- No illustrative examples/anecdotes in the actual published content — too risky, feels like calling out real situations. Present info directly instead.

## Org context this content responds to (informs framing, not stated directly)
- Org is agile but wants deep AI integration everywhere. Resistance = lack of AI knowledge/confidence, fear of job loss, fear of the unknown, reluctance to learn new things.
- Design is engaged haphazardly — sometimes early-through-delivery but tapers before benefits show; sometimes only as last-resort firefighting; often fades in/out. No universal assumption that design is "part of the process."
- Dev teams have wide latitude on HOW they work; validate mostly through demos framed as seeking approval ("love our stuff, please?") rather than real testing.
- Work is frequently delayed by lack of requirements — ironically the same underlying barrier as AI adoption (both need foundational clarity to function), but teams tend to restart repeatedly rather than build that clarity first.
- Teams self-report doing discovery/iteration/testing, but not in an unbiased, success-driven way.
- Few teams stay engaged post-MVP; work moves into Hypercare, often run by a 3rd party.
- Core perception problem: design is seen as a barrier/weight — "by the time I onboard them I could've done it myself."

## Content format (locked)
Every piece follows: **Trigger** (when to use it) → **Method** (exact steps) → **Artifact** (tangible output) → **Proof** (that it works, without a narrative anecdote) → **Watchout** (one line — this pattern's honest failure mode).

## Sequencing philosophy
No single correct order. Discovery-to-solution, delivery-to-discovery-to-solution, and everything in between are valid. Arcs are a **pattern library** — tools to reach for based on the risk in front of you — not a mandated pipeline.

---

## Locked Arc Structure

### 0. The Risk in What You Assume (foundational arc, 5 parts) — DRAFTED, see /01-drafts/
1. Assumption vs. fact
2. Not all assumptions are equal (impact × uncertainty)
3. Bias is just an assumption you don't know you're making
4. Attachment is the real risk, not the starting point
5. Your derisking toolkit (visibility, recognizing bias, iteration, co-creation — presented as a pattern library, not a sequence)

The four tools map onto the arcs below:
- Visibility → Story Mapping in Cursor
- Recognizing bias → From a Vague Ask to a Real Persona
- Iteration → Mocking and Testing an Agent Handoff
- Co-creation → Running One Workshop, Start to Finish

### 1. The Cost You Don't See (3 parts) → Flagging Design Debt As You Go (3 parts)
Motivational on-ramp establishing why debt is worth flagging, then the method for flagging it as a personal habit (not a team-management tool).

### 2. From a Vague Ask to a Real Persona (5 parts)
1. Start with your proto-persona — naming assumptions honestly
2. A role is not a persona
3. From proto to real — a confidence gradient, not a single validation event
4. One person, many roles — a quick reality check
5. Carrying it forward honestly
(Persona hierarchy/specialist nesting and multiple-personas-per-person systems-thinking depth: parked as too advanced for this series — potential bonus/standalone later.)

### 3. Story Mapping in Cursor (5 parts)
1. Mapping the backbone
2. Breaking activities into real steps
3. Adding the detail layer (walking skeleton)
4. Slicing your MVP line (a risk decision, not a scope cut)
5. Walking the map with someone else

### 4. Grooming with AI (3 parts)
1. Right-sizing stories
2. Writing acceptance criteria with AI
3. Running the grooming pass itself

### 5. Spotting Where AI Surprises People (2 parts) → Mocking and Testing an Agent Handoff (3 parts)
1. Keep a running log of AI-surprise moments
2. Turn the log into patterns
3. Mock the handoff moment before writing agent logic
4. Test the mock with a real teammate
5. What changed as a result

### 6. One Feature, Three Handoffs (4 parts)
One feature's journey through PM → Dev → 3rd-party, each part a single moment:
1. Vocabulary gap (MVP means 3 things in this room)
2. The missing brief sentence
3. Handoff / design QA moment
4. Signaling theory — what a polished mockup accidentally promises

### 7. Running One Workshop, Start to Finish (5 parts)
1. Is it even needed
2. Opening safely
3. Handling a skeptic
4. Closing the session
5. Following up weeks later

### Standalone thread (loose, no sequence, no numbering)
- Environment Setup for Discovery Work in Cursor
- Desire paths as literal user research
- Broken windows and the one unfixed thing wrecking culture
- Tragedy of the commons and shared design systems
- Film review culture for design critique
- Error states as a trust system
- Empty states
- Edge/boundary states
- Performance and perceived speed
- Data visualization for decision-makers
- A practitioner's checklist for accessible enterprise forms

---

## Watchouts (by piece)

**Foundational arc**
1. Assumption vs. fact — don't turn this into a gotcha game for other people's language; it's self-awareness, not correction.
2. Impact × uncertainty — "low risk" can become an excuse to never validate anything.
3. Bias — naming a bias isn't the same as fixing it.
4. Attachment — "stay flexible" can become an excuse to never commit to a direction.
5. Toolkit — this is a menu, not a mandatory checklist to run every time.

**Persona arc**
1. Proto-persona — presenting it as fact instead of "proto" is the exact failure this prevents.
2. Role ≠ persona — don't turn this into bureaucracy; it's a lens, not a new deliverable.
3. Proto → real — more data isn't automatically better data.
4. Many roles — don't use this as an excuse to avoid picking a primary persona.
5. Carrying forward — a stale, unrevisited persona becomes a liability.

**Story Mapping**
1. Backbone — map what people actually do, not the aspirational process.
2. Steps — going too granular too early kills momentum.
3. Detail layer — this is a first pass, not the final map.
4. MVP line — it's a risk decision, not a deadline-driven scope cut.
5. Validate — a nodding colleague isn't validation; find someone who'll push back.

**Grooming with AI**
1. Right-size — AI produces plausible stories that hide missing context; you still own the call.
2. Acceptance criteria — don't accept criteria you don't fully understand just because it sounds thorough.
3. Grooming pass — speed can create false confidence; leave room for real disagreement.

**AI Surprises / Agent Handoff**
1. Log — log surprising successes too, not just failures.
2. Patterns — a few examples isn't a pattern yet.
3. Mock — an overly polished mock creates the same false confidence as a demo.
4. Test — someone too close to the project won't catch what fresh eyes would.
5. What changed — a test without a follow-through change is just theater.

**One Feature, Three Handoffs**
1. Vocabulary — nodding isn't alignment; check definitions explicitly.
2. Brief sentence — doesn't replace a real conversation when stakes are high.
3. Handoff/QA — matching the spec doesn't catch what the spec itself got wrong.
4. Signaling — too-low fidelity can mislead too; match fidelity to the decision.

**Workshop**
1. Is it needed — can become an excuse to skip alignment entirely.
2. Opening safely — don't let it feel forced or HR-flavored.
3. Skeptic — don't shut them down; they're often naming a real risk.
4. Closing — a rushed close loses commitments people forget by tomorrow.
5. Follow-up — the step most likely to quietly get skipped.

**Standalone thread**
- Desire paths — not every workaround is a signal worth designing around.
- Broken windows — don't ignore bigger structural debt while chasing small stuff.
- Tragedy of the commons — naming it doesn't fix it; someone still has to own upkeep.
- Film review critique — can feel surveillance-y without buy-in.
- Error states — don't bury real problems in reassuring copy.
- Empty states — a clever one doesn't fix a genuinely confusing first run.
- Edge states — chasing every edge case can stall shipping.
- Perceived speed — tricks can't substitute forever for fixing real performance.
- Data viz — a persuasive chart isn't the same as an accurate one.
- Accessibility checklist — passing it isn't the same as working for a real assistive-tech user.

---

## Chapter Talks (separate track — see areas file for full task breakdown)
Structure differs from the series: **Cold open (function-specific pain) → one Method+Trigger explored deeply → live exercise using the unit's provided test → debrief tying back to the platform goal.** No stage-setter/conclusion — the session is both hook and proof. Three chapters: PM, Custom Dev, Non-Custom Dev — each needs a unit contact, a selected method, a shaped test/exercise, and a scheduled session.
