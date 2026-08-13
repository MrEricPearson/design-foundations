# Status Quo Bias
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 101, 229 | **Episode:** 3

**Goal:** Recognize when resistance to a change is driven by preference for the current state itself — independent of the new state's actual quality — so you can distinguish "this design isn't good enough" from "any change faces this headwind."

**Concept:** The working assumption is that users and stakeholders evaluate proposed changes based on the merits of the change. The correction: the current state has a systematic advantage over any alternative, because change introduces uncertainty and any loss from the transition weighs more heavily than equivalent gains.

The mechanism: the current arrangement is the reference point (see 228 — Anchoring). Changing from it requires accepting certain transition costs in exchange for uncertain future benefits. Loss aversion (229) makes certain costs feel heavier than uncertain gains. The result is a systematic preference for the existing state that is independent of whether it is better or worse than the alternative.

Status quo bias is distinguishable from informed preference for the current state: a user who has evaluated both options and prefers the current one is not showing status quo bias. A user who has not evaluated the alternative, or who acknowledges the alternative is better but still resists the change, is showing status quo bias.

For design, this creates a specific asymmetry: new features that replace existing functionality face a steeper adoption curve than additive features, even when users acknowledge the new approach is superior. Default settings are disproportionately maintained even when users say they'd prefer a different configuration. Opt-in flows underperform equivalent opt-out flows because the current state (not opted in) has the status quo advantage.

**You'll see it when:** A user acknowledges a new feature or approach is better but doesn't change their current workflow to use it. Or when a design change that users agreed would improve the product shows low adoption in practice. The gap between stated preference and actual behavior is the fingerprint.

**The signal:** Resistance to a better option is framed as preference for keeping what's already there, rather than a specific deficiency in the new option.

**Don't confuse this with:** Rational conservatism — legitimate caution about changes that involve learning cost, workflow disruption, or risk. Status quo bias is irrational resistance to a change that users themselves acknowledge would produce better outcomes. The diagnostic: ask "is the resistance about the new state, or about the transition?" Rational conservatism resists specific costs. Status quo bias resists the change itself, even when specific costs are addressed.

**Try Noticing:** Look at a feature in your current product that was designed to replace an existing way of doing something. What is the adoption rate? Now identify: do users who haven't adopted it typically give specific reasons (the new version doesn't do X) or general reasons (I'm used to the current way)? Specific reasons point to design problems. General reasons point to status quo bias — a different problem requiring a different response.

**What Next:** Read 232 (Cognitive Dissonance) — when users have adopted something despite status quo resistance, cognitive dissonance explains why they may rationalize the new state as what they wanted all along. Read 233 (Dark Patterns) for how status quo bias is exploited through dark patterns that make the current state feel like the only safe option.
