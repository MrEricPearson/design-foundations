# Progressive Disclosure
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 237 | **Episode:** 8

**Goal:** Recognize when information or options could be sequenced to match user readiness, so that earlier stages don't burden working memory with decisions that only become relevant later.

**Concept:** The working assumption is that progressive disclosure means hiding advanced features from novice users — a feature flag or "show advanced settings" toggle. The correction: progressive disclosure is a structural principle about when information is presented relative to when the user needs it to make a decision. The hiding and revealing is incidental; the structure is about load timing.

The mechanism: every piece of information presented before it's needed occupies working memory without contributing to the current decision. Information presented after it's needed forces the user to backtrack, re-read, or make decisions without context they'll need later. The well-timed disclosure matches the arrival of information to the moment the user is making the decision that requires it — not earlier, not later.

This is a structural property of a flow, not a visual property of a screen. A clean, minimal screen can still violate progressive disclosure if it surfaces a decision that depends on context the user won't establish for several more steps. A dense screen might honor progressive disclosure if every element on it is relevant to the current decision and nothing is carrying information forward unnecessarily.

Three patterns to recognize:

**Staged commitment:** Ask for low-stakes information first, higher-stakes later. Each stage should produce enough value to motivate continuing. (Email → account → payment, in that order — not the reverse.) Early stages that don't produce value before asking for the next stage of commitment will see abandonment at that stage.

**Contextual surfacing:** Options, settings, or information appear when the user is in the state that makes them relevant — not always present as a permanent interface element that carries visual and cognitive weight even when irrelevant.

**Just-in-time explanation:** Instructions, error states, and help content appear at the moment of need, not as a preamble to be read before beginning. Preambles are skipped; JIT explanations are read because the user is in the problem state the explanation addresses.

**You'll see it when:** A form asks for information before the user understands why it's needed. Or when an onboarding flow presents all options before the user has any context for evaluating them. Or when a flow's most complex decision arrives before the user has built any orientation in the product.

**The signal:** Users frequently abandon a flow at the point where the most cognitively demanding decision is asked — not at the end, and not at a step that is objectively harder. The abandonment point is where load peaks relative to context.

**Don't confuse this with:** Removing information to make the interface simpler. Progressive disclosure doesn't reduce the total information — it sequences it. All the same decisions and explanations can exist; they arrive when the user is ready for them rather than all at once. The simplification that results from hiding information permanently is a different design move, with a different trade-off.

**Try Noticing:** Map the decision points in a user flow you're currently working on in order of when they appear. Now map them again in order of how much context the user needs to make each one well. Are the highest-context decisions appearing before or after the user has built that context? Where the two orderings diverge is where progressive disclosure is being violated.

**What Next:** Read 240 (Form Design Principles) — forms are the context where progressive disclosure is most consequential and most frequently violated, because form design tends to be done field-by-field rather than as a staged disclosure flow.
