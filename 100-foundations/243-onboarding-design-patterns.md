# Onboarding Design Patterns
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 238, 241 | **Episode:** 9

**Goal:** Recognize which onboarding pattern a product is using and whether that pattern matches what new users actually need to reach first value — so you can identify onboarding failures at the structural level rather than at the copy or visual level.

**Concept:** The working assumption is that onboarding is a welcome screen and a product tour — an orientation sequence that explains what the product does before users start using it. The correction: explaining a product and demonstrating its value are different things, and onboarding fails most commonly when it does the former instead of the latter.

The mechanism: new users arrive with varying levels of sophistication and clarity about what they want the product to do for them. What they have in common is that they haven't yet experienced the product producing value. The onboarding's job is to get them to that first moment of value as quickly as possible — because before that moment, the user is deciding whether to continue, and they're deciding based on the effort they're putting in relative to nothing concrete yet.

"Time to value" is the design variable that predicts onboarding success better than any other. Product tours that explain features before value is felt, profile completion flows that require extensive input before anything works, and tutorial sequences that teach the product before demonstrating it all increase time to value. They also increase the perceived cost of continuing before the user has any evidence that the cost is worth paying.

Four onboarding patterns and when each applies:

**Blank slate onboarding:** The user lands in the empty product and discovers value through exploration. Works when the product is familiar enough in category that users know what to do, or when the value is immediately apparent from a small first action. Fails when users don't know what to try first and the empty state doesn't guide them.

**Sample data onboarding:** The user arrives to a pre-populated product that demonstrates what a working state looks like. Works when the value requires context that users can't create in a first session — showing an analytics dashboard with real-looking data demonstrates the product in a way an empty dashboard cannot. Fails when sample data is so obviously fictional that it doesn't produce belief, or when it's hard to clear before real use.

**Guided setup flow:** A structured sequence walks the user through the minimum configuration needed for the product to work. Works for products where a configuration decision must be made before any value is possible (integrating a data source, defining a team structure). Fails when the flow requires information users don't have yet, or asks for decisions that only make sense after some product experience.

**Progressive onboarding:** The product reveals capabilities and guidance contextually as users reach the relevant state — not in an upfront sequence. Works for complex products where the full scope is too large to demonstrate upfront. Fails when contextual prompts arrive before users understand the context that makes them relevant.

**You'll see it when:** New user activation drops sharply at a specific onboarding step — the step is asking for something the user doesn't have yet, or is requiring effort before demonstrating any value. Or when users who complete onboarding have similar activation rates to users who skip it — the onboarding didn't accelerate time to value.

**The signal:** Users who complete the onboarding sequence but then don't perform a core product action within the first session. The onboarding oriented them without getting them to value.

**Don't confuse this with:** Onboarding being the only lever for new user activation. Onboarding addresses the interface and flow. Pre-signup expectations (set by marketing), product-market fit, and the product's inherent usability all affect activation independently of onboarding quality. A well-designed onboarding on a product that doesn't solve a real problem will not produce strong activation — but it will make the failure clearer.

**Try Noticing:** Walk through your product's onboarding as a new user — ideally in an incognito session or fresh account. Time how long it takes from first landing to your first experience of the product doing something useful for you. That is your current time to value. Now identify what, if anything, is between landing and that moment that doesn't contribute to reaching it.

**What Next:** Read 241 (Empty States) — the moment after onboarding ends and the user arrives at the empty product proper is the second inflection point in new user experience. Onboarding and empty state design together determine whether a new user reaches genuine first value.
