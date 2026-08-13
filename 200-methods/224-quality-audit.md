---
tier: 200
type: practice
piece: 224
title: Quality Audit
goal: Place a specific product or feature on the quality ladder and identify the one action that would move it up one level.
prereqs: [137, 138]
pairs_with: [112, 116, 215a, 215b, 216]
episode: 19
status: drafted
---

## Goal

Place a specific product or feature on the quality ladder and identify the one action that would move it up one level.

## Prior Knowledge Hook

You already evaluate products intuitively — "this is clunky," "this is fine," "this actually works." This method makes that intuition explicit, locatable, and actionable.

## Trigger

Before a release decision. After a usability test round. When a product is working correctly but adoption is disappointing. When a team disagrees about whether something is "good enough."

## Concept

Each quality threshold has a specific diagnostic question. Answering them in sequence locates exactly where a product currently sits. The first question that answers "no" tells you which level you're at — and that level's friction type tells you what to address. You cannot skip levels: a product that isn't yet usable will not become trusted by adding trust-level polish.

## Method

**State the primary user task in one sentence.** Not the feature's function — the user's goal. If you can't write it in one sentence, the scope is too large; narrow it until you can.

**Q1 — Functional threshold:** Can a prepared user complete this task without assistance, workarounds, or failure? If no → the product is at functional. The friction is capability or reliability. Fix: identify the specific failure mode and remove it before anything else.

**Q2 — Usable threshold:** Can a user with reasonable context complete the task without sustained active attention — without having to stop, think, search, or decide in ways unrelated to their actual goal? If no → the product is at usable. The friction is comprehension or decision overhead. Fix: reduce the number of decisions the interface asks the user to make; apply progressive disclosure.

**Q3 — Efficient threshold:** Do users reach for this product when the task arises — by choice, not by assignment? Do they build it into their workflow rather than around it? If no → the product is at efficient. The friction is reliability or unpredictability. Fix: identify the trust failure — the moment where the product surprised the user in a bad direction — and make that moment predictable.

**Name one action.** Not a feature list. One specific change that addresses the friction at your current level. If you find yourself writing a list, you've found the real gap — and the audit worked.

## Artifact

A quality placement statement:

> "This [feature / product] is currently at [level] because [specific evidence — one sentence]. To reach [next level], the most direct action is [one specific change]."

## Watchout

The audit reveals the current level, not all the levels simultaneously. A team that discovers they're at functional should not try to design for trust. Each threshold has to be crossed in sequence — rushing to trust-level decisions on a product that isn't yet usable produces things nobody uses elegantly. Start at the first "no."

## Try This

Pick one feature in your current work. Write the user task sentence. Answer Q1, Q2, and Q3 in order. Stop at the first "no." Write the quality placement statement — level, evidence, one action.

## Proof

If your "one action" turns into a list, the audit surfaced something real: the product has more friction at that level than you expected. A single specific action is the right output. A list means you're at a lower level than you thought — revisit which "no" answer is actually the first one.

## Take This Further

In the next three days, share your quality placement statement with one other person working on the same product. Ask whether they'd place it at the same level. Disagreement on placement is itself a finding — it reveals where the team's model of "good enough" diverges. Afterward, write one sentence: *What did the disagreement reveal about what we each think the product is for?*

## AI Path

After you've run the audit yourself: paste your placement statement into a conversation with an AI and ask it to challenge your evidence for the level placement. Strong placements survive the challenge; weak ones reveal the next question you need to answer. Do not use AI to run the audit for you — the diagnostic questions require direct knowledge of how the product behaves with real users.

## What Next

- At **functional** → focus on error and edge state design: **116, 117, 118**
- At **usable** → reduce cognitive overhead: **237 Cognitive overload**, **238 Progressive disclosure**
- At **efficient** → address the trust gap: **Testing What You Built (Ep22)**
- At **trusted** → focus on maintenance: **134 Design debt**, **135 Leading vs. lagging indicators**
