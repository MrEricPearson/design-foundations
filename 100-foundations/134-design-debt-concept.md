# Design Debt
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 113 | **Episode:** 15

**Goal:** Recognize when a design decision is creating ongoing user cost that will compound over time — so you can name it explicitly before it gets buried.

**Concept:** The working assumption is that design debt is like technical debt — something engineers track, and not a design team concern. The correction: design debt is orthogonal to technical debt, and it's invisible precisely because it doesn't live in the code. The mechanism: technical debt fails builds and throws errors. Design debt accumulates in user behavior — in workarounds, support tickets, abandonment at specific screens, and confusion that users stop reporting because they've adapted. Unlike a bug, design debt doesn't present as an error state. It presents as friction that seems tolerable until you measure its actual cost across users and sessions.

A decision that created design debt was usually a deliberate one made under real constraint — time, information, competing priorities. The debt isn't the decision; it's the ongoing cost the decision creates for users over time, with interest as the product scales and the inconsistency accumulates.

Three forms:
- **Consistency debt** — the same action, pattern, or concept works differently in different parts of the product
- **Communication debt** — the interface relies on users knowing something it never told them (an unlabeled action, an unexplained status)
- **Coverage debt** — states the interface should handle (errors, empty states, edge cases) that are missing or broken

**You'll see it when:** A support question appears repeatedly about the same interaction. Usability sessions produce the same hesitation at the same screen across participants. A team proposes a workaround for a user behavior rather than addressing the underlying interaction.

**The signal:** A known design problem that hasn't been addressed because it's "not a bug." The team can describe exactly what's confusing and exactly why it was never fixed.

**Don't confuse design debt with unfinished work.** Unfinished work hasn't been done yet. Design debt was done — it just created an ongoing cost when it was. A false positive: a long list of design issues that the team acknowledges feels like documented design debt. But if none of the items have a named user cost (what exactly is the recurring friction?) and a named cleanup effort (what would it take to fix?), the list is awareness without accountability. Both are needed.

**Try Noticing:** Name one interaction in a product you work with that you know is confusing. Can you trace it to a specific decision made under constraint? What is the ongoing user cost? What would cleanup require? That structure — original decision, current user cost, cleanup effort — is a named debt item.

**What Next:** To learn how to track and flag design debt as it forms, read the 300 arc (The Cost You Don't See → Flagging Design Debt). To understand how emotional attachment to existing decisions creates debt, read 103 (Attachment Is the Real Risk).
