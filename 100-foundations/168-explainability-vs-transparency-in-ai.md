# Explainability vs. Transparency in AI
**Tier:** 100 — Recognize | **Note:** Foundational prereq for 302 (Spotting AI Surprises) and 308 (Designing for AI Trust); pairs with 167 (Automation Bias)

**Goal:** Recognize the difference between an AI that explains its outputs and one that is transparent about how it works — so you know which one a user actually needs.

**Concept:** Explainability is the AI's ability to describe why it produced a specific output: "I recommended this because your last three actions matched this pattern." Transparency is the AI's ability to describe how it works in general: "I use collaborative filtering across anonymized user behavior." Users almost never need transparency in the algorithmic-disclosure sense. They almost always need explainability — "why this, for me, right now?" Designing for transparency when the user needs explainability is a common design misdirection: the team reveals how the system works rather than why it produced the specific thing the user is questioning.

**You'll see it when:** An AI product team debates how much to "expose the algorithm" or "show the confidence score" when what users are actually asking is "why did it tell me this?" The question is about a specific output — that's an explainability question, not a transparency question.

**The signal:** The user's question is about a specific output ("why this recommendation?"), not about the system in general ("how does the recommendation engine work?"). Explainability answers the first; transparency answers the second. A design that answers the second in response to the first has misread what the user needs.

**Don't confuse this with:** Disclosure — a legal and ethical concept about data collection, usage, and consent. Disclosure obligations can be met alongside either explainability or transparency; they're about informing users of data practices, not about giving visibility into AI reasoning on a specific output.

**Try Noticing:** Look at the last AI feature you used that felt opaque or surprising. What question did you want answered about it? Was it "why did it say this specifically?" or "how does this system work in general?" That question is the design requirement that an explainability or transparency feature would address.

**What Next:** When designing explainability into an AI feature, read 308 (Designing for AI Trust) — Part 3 (Explanation Structures) covers the design decisions that make AI outputs feel legible to users at the output level.
