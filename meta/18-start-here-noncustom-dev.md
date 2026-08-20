# Start Here — Non-Custom Dev / 3rd-Party / Configuration
**Type:** Audience orientation meta-piece | **Not published** — referenced from library introduction and capability calibration guide

## The problems this reading path addresses

Teams working with vendor software, SaaS platforms, or third-party tools commonly encounter: configuration decisions with no documented rationale that can't be explained later; getting buy-in for new tools or changed configurations without a user-centered argument; user adoption gaps after deployment; and the assumption that because the vendor built the UI, the user experience isn't configurable or improvable.

Design methods apply fully in vendor-software contexts — not to the UI itself, but to configuration choices, adoption strategy, onboarding design, and the user experience of how the platform is implemented. This is the library's response to the documented perception gap: "design can't help with SaaS."

## What non-custom dev audiences have that accelerates learning

These teams often have strong systems thinking — they understand platform constraints, integration dependencies, and configuration tradeoffs. They are typically closer to the end-user than product or engineering because they own the implementation and, often, support. The design methods most useful to them are the ones that bring user experience evidence into configuration and rollout decisions.

## Recommended starter sequence (5 pieces)

| Order | Piece | Why this one first |
|---|---|---|
| 1 | 122 — Starting Questions | Configuration decisions are project starts — the pre-work questions apply directly |
| 2 | 107 — Framing the Problem | What user problem is this configuration solving? Answering before configuring prevents post-launch regret |
| 3 | 202 — Lightweight Research Mechanics | One conversation with the people who'll use the platform before configuration decisions are made |
| 4 | 206 — Journey Mapping | Maps the full user experience of the implemented platform, including the parts the vendor doesn't control |
| 5 | 209 — Design Decision Records | Documents why configuration choices were made — essential for platforms that get modified iteratively |

After these five, a non-custom dev team member can document user context before configuration starts, and create a decision record that explains why the system was set up the way it was.

## Tier context for this audience

Non-custom dev typically enters at **Tier 100** for conceptual frames and moves to **Tier 200** for the research and mapping methods. The Tier 300 arcs most relevant are 303 (One Feature, Three Handoffs) for vendor implementations that cross multiple teams, and 306 (Service Blueprint / Dependency Map) for mapping the full system including vendor components.

## Audience-specific T300 arcs

**313 — UX in a Product You Didn't Build** is the primary T300 arc for this audience. It applies design judgment to the decisions you actually control in a vendor or SaaS implementation: configuration choices grounded in user mental models, pre-implementation heuristic evaluation, scenario-driven configuration rationale, and adoption strategy based on Status Quo Bias and Loss Aversion rather than training. Builds directly on pieces 4 and 5 in the starter sequence above (206 Journey Mapping, 209 Design Decision Records). Prereqs: 126, 255, 250, 124, 110, 130 — all T100/T200 pieces.

Four extended arcs address the full non-custom dev workflow from pre-adoption evaluation to ongoing platform management and migration:

| Arc | What it delivers |
|---|---|
| 326 — Evaluating Vendor Products Before You're Locked In | Heuristic review + mental model fit assessment + non-configurable risk documentation — before configuration investment begins |
| 327 — Documentation as Experience Design | Write task-organized documentation that closes the support loop; test it before publishing; maintain it so it doesn't become a trap |
| 328 — Running the Platform Like a Product | Apply product thinking to platform management: define outcome-level success metrics, gather systematic signal, make configuration decisions with the same rigor as product decisions |
| 329 — Platform Migration as a UX Project | Treat migrations as user experience transitions: map what users are actually losing, design the transition period, communicate in a way that builds trust not anxiety |
| 337 — When Adoption Fails | Diagnose which of four failure modes is driving low adoption after deployment — and choose a response matched to the actual cause, not the visible symptom |

326 is the highest-priority extension — most impactful before any new tool adoption. 327 addresses ongoing adoption gaps. 328 addresses platform management for teams with an ongoing stewardship role. 329 applies when a migration is planned.

## Next steps

See meta/15-capability-calibration.md Section B for the full non-custom dev reading path. For adoption strategy specifically, 305 (Generalized Did-It-Work Follow-Up Habit) + 206c (Assumption-First Proto-Map) is the sequence — start with the assumption-based map since research access is typically unavailable. For the cross-audience arcs with high non-custom dev relevance: 330 (From Findings to Decisions) and 315 (Psychology of Resistance) both apply directly to adoption and configuration challenges.
