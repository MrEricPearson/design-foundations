# Where Design Systems Fail
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 195, 194 | **Note:** Pairs with 195; critical for practitioners building on top of vendor-provided or enterprise design systems

**Goal:** After this piece, you will be able to recognize the two signals that mean you've reached the boundary of a design system — and know what to do at each.

**Concept:** A design system was designed for anticipated use cases. The team or vendor who built it had a set of problems in mind. They made good decisions for those problems. The system works well inside its design envelope. At the boundary of that envelope — where your problem diverges from what the system anticipated — the system creates friction rather than reducing it. Learning to read that friction correctly is one of the most practically valuable skills in working with design systems.

The friction appears in two distinct ways, and they require different responses.

**Signal 1: The component is being overridden or extended to fit.** You're spending disproportionate effort making the component behave differently from its default — suppressing properties it always shows, adding properties it doesn't support, overriding styles that don't fit the context. The system is doing work against you. This signal means: you may be outside the design envelope for this component. The question to ask: is the override compensating for a genuine misfit (the component's assumptions don't match the content model), or correcting for an incorrect application (you're using the wrong component for this content type)?

If it's a genuine misfit: the decision is whether the design system needs extending (which has maintenance cost and coordination cost) or whether a custom solution is warranted (higher build cost, but stays out of the shared system). Neither is inherently right.

**Signal 2: The design system doesn't have a component for this.** The system has cards, tables, lists, and forms. The problem needs something the system hasn't anticipated — a complex multi-state visualization, a custom interactive pattern, a domain-specific display that doesn't fit any existing component. The system doesn't fail here; it simply stops. The question is: build custom within the design system's design language (consistent look and feel, inconsistent interaction pattern library), or accept a broader inconsistency.

The decision framework: how often will this pattern appear? A pattern that appears once is probably fine as a custom build. A pattern that will appear dozens of times across the product is worth the investment in extending the design system properly — the consistency payoff compounds over reuse. A one-off pattern built correctly is far cheaper than a recurring pattern treated as one-off and rebuilt inconsistently each time.

**You'll see it when:** A design review reveals that multiple teams have solved the same problem differently because the design system didn't have a component for it — so each team built their own. The result is visual and behavioral inconsistency across the product, for a use case that could have been standardized. This is the design system's failure to anticipate a recurring use case, surfaced after the fact.

**The signal:** The phrase "we built a custom version of [component] for this" appearing more than once, independently, in more than one place in the product. When teams are building the same custom thing independently, it wasn't custom — it was a missing component.

**Don't confuse a design system gap with a design problem** — a gap means the system doesn't have what's needed; a design problem means the team is using the system incorrectly. These have different solutions. Filling a gap requires extending the system (or accepting the gap deliberately). Fixing incorrect usage requires training and tooling that reinforces correct use. Treating a gap as incorrect usage leads to poor workarounds. Treating incorrect usage as a gap leads to a design system cluttered with specialized components that exist because someone didn't know what to use.

**Try Noticing:** Look at a product you work on or use frequently. Find one interaction pattern that appears more than twice. Is it implemented consistently — same component, same behavior, same visual treatment — every time? If not: is the inconsistency because the design system doesn't have a component for it (a gap), or because different teams made different choices about which existing component to use (a usage problem)? The distinction tells you where to intervene.

**What Next:** Recognizing a design system's limits is the first step toward working at the right level — sometimes extending the system, sometimes building custom, sometimes reframing the problem so it fits what already exists. For how to make deliberate decisions about which path to take, read 198 (Pattern vs. Model Problem) and 199 (Transformation Within Constraints).
