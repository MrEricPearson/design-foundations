# Design Foundations Manual

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

A practitioner library for product managers, developers, and platform teams. Not a design course — a reference for the design judgment you already need to do your job.

Every piece delivers **one applicable thing** and takes **under five minutes** to read.

**→ [Browse the full library interactively](https://claude.ai/code/artifact/9717a242-e5d9-480f-a988-b8355fbc6d43)** — all 217 pieces, every tier, every cluster, organized for navigation.

---

## The model: three tiers of learning

| Tier | Learning goal | What it looks like |
|---|---|---|
| **100 — Recognize** | Notice this concept in a real situation you're already in | One concept, one signal to watch for, one observational exercise |
| **200 — Practice** | Run this method with something you're working on today | Named steps, a concrete output, one watchout |
| **300 — Orchestrate** | Apply this system to a complex situation and make judgment calls at the seams | Multi-part arc, Judgment Exercise with a real failure case |

No piece requires another piece to make sense. Read what's relevant. Skip what isn't.

---

## Start here by role

**Product Managers →** [`meta/16-start-here-pm.md`](meta/16-start-here-pm.md)

| # | Piece | What it does for you |
|---|---|---|
| 1 | [122 — Starting Questions](100-foundations/122-starting-questions.md) | Pre-work ritual before any project; converts vague asks into checkable claims |
| 2 | [125 — Jobs-to-Be-Done](100-foundations/125-jobs-to-be-done.md) | Reframes requirements from solutions to user situations |
| 3 | [107 — Framing the Problem](100-foundations/107-framing-the-problem.md) | Turns a situation into a testable problem statement |
| 4 | [113 — Defining Success Before You Start](100-foundations/113-defining-success.md) | Prevents post-delivery surprise about what "success" meant |
| 5 | [207 — Premortem](200-methods/207-premortem.md) | Pre-tests a plan against likely failure modes before resources are committed |

---

**Custom Dev teams →** [`meta/17-start-here-custom-dev.md`](meta/17-start-here-custom-dev.md)

| # | Piece | What it does for you |
|---|---|---|
| 1 | [100 — Assumption vs. Fact](100-foundations/100-assumption-vs-fact.md) | Names the thing that causes the most post-launch surprise |
| 2 | [147 — AI as Execution Partner](100-foundations/147-ai-as-execution-partner.md) | Clarifies the judgment/production split in AI-assisted workflows |
| 3 | [132 — Prototype Fidelity](100-foundations/132-prototype-fidelity.md) | Reframes prototyping as a question about what you're testing, not what tool you're using |
| 4 | [123 — What Usability Testing Is](100-foundations/123-what-usability-testing-is.md) | Distinguishes a demo from a test; most applicable before anything ships |
| 5 | [215a — Running a Usability Session](200-methods/215a-moderated-usability-session.md) | Five people, one task, before you ship |

---

**Platform / Non-Custom Dev teams →** [`meta/18-start-here-noncustom-dev.md`](meta/18-start-here-noncustom-dev.md)

| # | Piece | What it does for you |
|---|---|---|
| 1 | [122 — Starting Questions](100-foundations/122-starting-questions.md) | Configuration decisions are project starts — this is the pre-work |
| 2 | [107 — Framing the Problem](100-foundations/107-framing-the-problem.md) | What user problem is this configuration solving? Answering before configuring prevents regret |
| 3 | [202a — Conversational Interview](200-methods/202a-conversational-interview.md) | One conversation with people who'll use the platform before configuration decisions are made |
| 4 | [206c — Assumption-First Proto-Map](200-methods/206c-assumption-first-proto-map.md) | Maps the user experience of the platform you're implementing, including the parts you control |
| 5 | [209 — Design Decision Records](200-methods/209-design-decision-records.md) | Documents why configuration choices were made — essential for platforms that evolve iteratively |

---

## What's in here

```
100-foundations/   133 atomic concepts    Recognize-tier; no prerequisites required
200-methods/        40 practical methods   Practice-tier; builds on 100-level concepts  
300-systems/        38 judgment arcs       Orchestrate-tier; multi-part, audience-specific
standalone/          4 conceptual pieces   No tier; read anytime
meta/                Navigation guides, reading paths, master outline
assets/              Chapter Talk reference materials (internal)
```

**Total: 217 pieces** across all tiers.

---

## What the tiers teach

### Tier 100 — Concepts you can name

Clusters within `100-foundations/`:

- **Foundational thinking** (100–136): Assumption vs. fact, iteration, constraints, self-critique, framing, success definition
- **AI foundations** (147): AI as execution partner — the judgment/production distinction
- **Research and evidence** (148–176): Primary vs. secondary, behavior vs. attitude, synthesis, task statement design, journey maps, prototypes
- **Content architecture** (179–199): Content models, labeling, taxonomy, naming, design systems
- **Visual craft** (187–192): Layout, gestalt, whitespace, reading patterns, typography, color
- **Psychology and bias** (225–232): Self-report bias, confirmation bias, anchoring, loss aversion, social proof, status quo bias
- **Ethics and persuasion** (233–236): Dark patterns, persuasion vs. manipulation, gamification
- **Cognitive interface** (237–243): Cognitive overload, progressive disclosure, accessibility, empty states, error states, onboarding
- **Research methods** (244–246): Qualitative vs. quantitative, mixed methods, sample size
- **Cognitive science** (247–264): Dual process theory, framing effect, loss aversion, sunk cost, Jakob's Law, Hick's Law, correlation vs. causation, survivorship bias
- **Interface cognition & AI shifts** (265–269, upcoming): Cost of novelty, no-UI design goal, serendipity problem in AI-curated interfaces, skeuomorphism vs. abstraction, design style spectrum

### Tier 200 — Methods you can run

Clusters within `200-methods/`:

- **AI-assisted work**: Story mapping in Cursor, grooming with AI, AI for design work
- **Research**: Conversational interview, remote/async research, observational research
- **Synthesis and ideation**: Affinity mapping, structured ideation, premortem
- **Journey and architecture**: Journey mapping (3 approaches), information architecture (2 approaches), service blueprint
- **Evaluation**: Usability testing (moderated + unmoderated), heuristic evaluation, five-second test, competitive scan
- **Measurement and tracking**: UX metrics, design decision records, retrospective for design decisions, Did-It-Work follow-up
- **Craft methods**: Content design, data visualization, accessibility checklist, form design, card sorting, content modeling
- **Prototyping**: 9 approaches from paper sketch to AI-generated to service prototype

### Tier 300 — Systems for complex situations

Arcs within `300-systems/`:

**For Product Managers (317–321, 335):** From vague ask to solvable problem → requirements that survive the build → lightweight validation → prioritizing without false precision → managing the feedback loop → evaluating a design you didn't create

**For Custom Dev (312, 322–325, 336):** Designing what you're building → what's missing from your spec → technical decisions as UX decisions → ship/patch/hold → when things break in production → code review as UX review

**For Platform / Non-Custom Dev (313, 326–329, 337):** UX in a product you didn't build → evaluating vendors before you're locked in → documentation as experience design → running the platform like a product → platform migration as a UX project → when adoption fails

**Cross-audience cognitive science (314–315):** How people actually decide · The psychology of resistance

**Cross-audience evidence and scope (316, 330–334):** Reading data without getting fooled · From findings to decisions · The good-enough evidence problem · Scope as a design decision · Designing handoffs that don't lose information · Solution-first rapid ideation

**Foundational arcs (300–313):** Design debt → persona → AI surprises/agent handoff → handoffs → workshop → service blueprint → dark patterns → designing for AI trust → prototyping → strategic judgment → stakeholder decisions

---

## Navigating the meta layer

| File | What it's for |
|---|---|
| [`meta/10-master-outline.md`](meta/10-master-outline.md) | Complete tiered list of every piece with dependencies; the authoritative source of record |
| [`meta/14-ordering-guide.md`](meta/14-ordering-guide.md) | Prerequisite chains and recommended publishing sequence |
| [`meta/15-capability-calibration.md`](meta/15-capability-calibration.md) | Role-specific reading paths and proactive design signal checklist |
| [`meta/16-start-here-pm.md`](meta/16-start-here-pm.md) | Full PM reading path |
| [`meta/17-start-here-custom-dev.md`](meta/17-start-here-custom-dev.md) | Full custom dev reading path |
| [`meta/18-start-here-noncustom-dev.md`](meta/18-start-here-noncustom-dev.md) | Full non-custom dev reading path |
| [`STATUS.md`](STATUS.md) | Per-piece publish-readiness tracking |
| [`meta/content-strategy-spec.html`](meta/content-strategy-spec.html) | Governing voice, tone, and content craft ruleset — 12 modules with research backing; reference for authors |
| [`meta/layout-system.md`](meta/layout-system.md) | SharePoint layout pattern library — 12 patterns, white space system, image spec format, mobile rules, and publish doc template |
| [`meta/library-design-system.html`](meta/library-design-system.html) | Visual identity reference — all 12 patterns rendered at production fidelity, design tokens, and SharePoint web part mapping |

---

## How to read a piece

Each piece follows a consistent template for its tier. Here's what you'll find:

**Tier 100 pieces include:**
- **Goal** (recognition verb: notice / identify / name / spot)
- **Concept** (what this is and why it matters — with the wrong model named first)
- **You'll see it when** (the situation that makes this visible)
- **The signal** (one checkable sign it's at play)
- **Don't confuse this with** (the adjacent concept most often conflated)
- **Try Noticing** (look for it in work already in front of you)
- **What Next** (where to go from here)

**Tier 200 pieces include:**
- **Goal** (application verb: run / produce / apply / write)
- **Trigger** (when to use this)
- **Method** (exact, unambiguous steps)
- **Artifact** (the tangible output)
- **Watchout** (one honest failure mode)
- **Try This** (5-minute practice with current work)
- **Proof** (how to know it worked)
- **Take This Further** (spaced practice prompt)
- **AI path** (acceleration after you've run it yourself)

**Tier 300 arcs include:**
- Arc-level goal and trigger
- 4 self-contained parts (each with Concept → Method → What you end up with → Proof → Watchout)
- **Try This** and **Take This Further** at arc level
- **Judgment Exercise** (a specific failure case where the arc's key assumption doesn't hold)

---

## What this isn't

This library doesn't teach you to be a designer. It teaches the design judgment that practitioners in every role need to make better decisions with or without a designer in the room. Leadership content is explicitly out of scope — if acting on something requires organizational authority you don't have, it doesn't belong here.

---

&copy; 2026 Eric Pearson. Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use, share, and adapt with attribution.
