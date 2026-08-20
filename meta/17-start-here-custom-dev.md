# Start Here — Custom Dev
**Type:** Audience orientation meta-piece | **Not published** — referenced from library introduction and capability calibration guide

## The problems this reading path addresses

Custom development teams commonly encounter: building to spec without a shared understanding of user experience context; discovering usability or navigability problems post-launch when they're expensive to fix; technical correctness that doesn't translate to actual use; and validation through demos that produce approval rather than task-based evidence.

This reading path targets the gap between "it works" and "people can use it."

## What custom dev audiences have that accelerates learning

Dev teams building custom software are already practiced at prototyping in code — they understand iteration, tradeoffs, and building disposable things to answer a question. The design methods most immediately useful to them are the conceptual frames for what questions a prototype should answer, and the lightweight methods for getting outside their own mental model before committing to an implementation.

AI is already part of custom dev workflows. 147 (AI as Execution Partner) makes explicit what they're already doing — using AI to accelerate production while retaining judgment — and clarifies where the judgment still lives.

## Recommended starter sequence (5 pieces)

| Order | Piece | Why this one first |
|---|---|---|
| 1 | 100 — Assumption vs. Fact | Names the thing that causes the most post-launch surprise: building against assumptions treated as facts |
| 2 | 147 — AI as Execution Partner | Clarifies the judgment/production split for AI-assisted workflows — directly relevant to how this audience already works |
| 3 | 132 — Prototype Fidelity | Reframes prototyping as a fidelity decision, not a tool decision; applicable to code-based prototyping |
| 4 | 123 — What Usability Testing Is | Distinguishes demo from testing; most immediately applicable before any user-facing feature ships |
| 5 | 215 — Running a Usability Session | The first evaluative method — five people, one task, before you ship |

After these five, a dev team member can externalize a design assumption before building and test it with one real person before writing production code.

## Tier context for this audience

Custom dev typically enters at **Tier 100** for conceptual reframing, but moves quickly to **Tier 200** for the practical methods. The 300-level arcs most relevant are 302 (Spotting AI Surprises → Agent Handoff) for AI-feature work and 300 (Cost You Don't See → Flagging Design Debt) for ongoing quality decisions.

## Audience-specific T300 arcs

**312 — Designing What You're Building** is the primary T300 arc for this audience. It packages the evaluative distance methods (self-critique, mental model mapping, unmoderated testing, edge state design) into a build-time system for teams with no dedicated designer in the loop. Prereqs: 103, 111, 126, 123 — all T100/T200 pieces in the starter sequence or close to it.

Four extended arcs address the full custom dev workflow from spec-reading to production incidents:

| Arc | What it delivers |
|---|---|
| 322 — What's Missing From Your Spec | Read an incoming spec with the lens that finds what it doesn't say: silent assumptions, undefined edge states, missing user context, and decisions left to implementation |
| 323 — Technical Decisions as UX Decisions | Recognize when data model choices, async patterns, and error handling become user experience decisions — and make them with the user in front of mind |
| 324 — The Ship / Patch / Hold Decision | Make confident launch decisions by defining the quality threshold before testing, evaluating known issues by user impact, and choosing a launch path with appropriate risk controls |
| 325 — When Things Break in Production | Respond to production incidents in a way that protects users, communicates transparently, and produces learning through blameless post-mortems |
| 336 — Code Review as UX Review | Evaluate a pull request for experience implications — not just technical correctness — using four questions that surface what code review typically misses |

322 pairs naturally with 312 as build-time self-review. 323 is the most novel arc — addresses the class of UX failures that emerge from implementation decisions nobody thought of as design decisions. 324 and 325 form a launch/post-launch pair.

## Next steps

See meta/15-capability-calibration.md Section B for the full custom dev reading path. For AI-specific work, the arc sequence is 147 → 302 → 308 (AX trust design). For the cross-audience arcs with high custom dev relevance: 334 (Solution-First Rapid Ideation) pairs well with the build-to-think prototyping approach (309i).
