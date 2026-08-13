# 204b — Content-Based Information Architecture
**Tier:** 200 — Practice | **Arc:** Information Architecture | **Prereqs:** 119 (Progressive Disclosure), 133 (Visual Hierarchy) | **Note:** Use when people are looking for content by type — documents, records, knowledge base articles — and the primary question is "what kind of content am I looking for?" For task-driven navigation where the primary question is "what am I trying to do?", use 204a (Task-Based IA). Pairs with 218 (Card Sorting) for validation.

**Goal:** After this piece, you will be able to organize a content-heavy structure around the categories users actually think in — not the categories your organization thinks in.

**Prior knowledge hook:** Think of a knowledge base, document library, or content portal you've used that required you to understand the publisher's internal organization before you could find what you needed. That translation from "what I'm looking for" to "what category this lives in here" is the IA cost — and it's higher in content-heavy systems than in task-driven ones because content doesn't have an obvious functional home.

**Trigger:** You're organizing a system that's primarily about finding and consuming content — documents, articles, records, reference material — and the primary user question is "what kind of content am I looking for?" rather than "what task am I trying to accomplish?"

**Why this works:** Content-heavy systems fail differently than task-based systems. Task-based IA fails when tasks are mapped to the wrong section. Content-based IA fails when the taxonomy doesn't match how users mentally classify what they're looking for — which is rarely the same as how the content was produced or stored internally.

**Method:**
1. **List every content type the system contains.** Not every individual document — the types of content. Reports, policies, templates, guides, case files, product specs, training materials — whatever applies to your system.
2. **Group by how users talk about content, not by how it was produced.** Users look for "how-to guides" and "reference material" — not "documentation produced by the enablement team" or "assets from Q2 initiative." Group content by the user-facing category first, then map organizational ownership internally.
3. **Test the categories with language.** For each category, complete this sentence: "I'm looking for a [category name] that helps me [do what]." If the sentence doesn't complete naturally — if users wouldn't use that category name in that sentence — the category reflects internal thinking, not user thinking.
4. **Provide two paths to the same content.** Content-heavy systems benefit from browse paths (organized by category) and search (keyword-based). Build both. The browse path serves users who are exploring or don't know exactly what they need; the search path serves users who know what they're looking for. Don't assume one path is enough.

**Artifact:** A content taxonomy — category structure with user-language labels — plus guidance on browse vs. search path availability.

**Watchout:** Content taxonomies collapse under the weight of "and also..." categories. "Other resources," "general," "miscellaneous" are IA failure signals — content that doesn't fit any category is content for which the taxonomy hasn't been fully thought through. Investigate what's in the miscellaneous bucket before naming it.

**When You Can't Run the Full Version**

**If you're inheriting existing content that's already organized by someone else's taxonomy:** Don't restructure the underlying organization — restructure the labels and surface navigation only. A different label on the same groupings reduces user translation cost without requiring a full content migration. Document the taxonomy-level problems for future resolution.

**If you can't validate the categories with users before launch:** Run the "I'm looking for a [category] that helps me [do what]" test with internal stakeholders who are close to the user type. It's not the same as user validation, but it surfaces obvious category mismatches before launch. Plan for card sorting (218) post-launch as the validation method.

**What you still get:** A labeled structure that at least reduces the most visible translation problems, even without full validation.

**What you give up:** Confidence that the categories match actual user mental models. Post-launch validation (218: Card Sorting) becomes more important when pre-launch validation wasn't possible.

**At Enterprise Scale**

Enterprise content systems often have multiple user roles with different content needs. A single taxonomy that serves all roles produces a top-level that's too broad for any individual to navigate efficiently.

**Role-filtered browse paths:** Build browse paths filtered by role — an admin's view of the same content library surfaces different categories than a field user's view. The underlying taxonomy stays the same; the browse path surfaces only the categories relevant to each role.

**Governance for ongoing content:** Content-based IA degrades over time as content is added without attention to taxonomy fit. Build a light-touch governance layer: every new content item is categorized at time of creation by the person who creates it, with the category options shown in the taxonomy at that moment. This keeps the IA current without requiring periodic restructuring audits.

**Try This:** List every type of content in a system you're working on. Complete the sentence "I'm looking for a [type] that helps me [do what]" for each type. Find any type that doesn't complete the sentence naturally — that type's label is reflecting internal thinking rather than user thinking. Rename it.

**Proof:** Ask someone unfamiliar with the system where they'd look for a specific piece of content by describing what they need ("I need a guide that explains how to do X"). If they navigate to the right category without guidance, the content taxonomy is matching user mental models. If they search instead of browsing, either the browse path isn't working or search is genuinely the better path — both outcomes are information.

**Take this further:** In the next week, watch one person try to find two different pieces of content in the system. Write one sentence: at what point did they switch from browsing to searching, and what does that signal about where the browse path breaks down?

**After you've run this yourself:** Share your content taxonomy with an AI tool and ask it to describe how a first-time user would interpret each category label. Where the interpretation differs from what the category actually contains, the label is working against the user.

**What Next:** Validate the taxonomy with real users using 218 (Card Sorting) — have them sort content items into groups and label the groups themselves. The resulting taxonomy reflects user mental models, not team assumptions. If the system serves multiple user roles with different content needs, apply the role-filtered browse path pattern described in the enterprise scale section above.
