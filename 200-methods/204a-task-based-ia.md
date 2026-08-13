# 204a — Task-Based Information Architecture
**Tier:** 200 — Practice | **Arc:** Information Architecture | **Prereqs:** 119 (Progressive Disclosure), 133 (Visual Hierarchy) | **Note:** Use when people are trying to accomplish tasks and the primary question is "what am I trying to do?" For content-heavy structures where the primary question is "what type of content am I looking for?", see 204b (Content-Based IA). Pairs with 218 (Card Sorting) for validation.

**Goal:** After this piece, you will be able to organize and label a navigation structure around the tasks users are trying to accomplish — not the way your team thinks about the system internally.

**Prior knowledge hook:** Think of a product where you never know where to find the thing you need. Scanning every nav item, trying different groupings — that experience is a broken information architecture. The nav is organized around how the product thinks about itself, not how users think about what they're trying to do.

**Trigger:** People are getting lost trying to find things. The navigation structure exists but isn't matching how users look for them — and the structure reflects internal taxonomy rather than user task logic.

**Why this works:** People navigate by mental model, not by a system's logic. When groupings and labels match what users already know how to look for, navigation becomes invisible — they find the thing. When the structure matches internal taxonomy instead, every navigation step is a translation problem that requires insider knowledge to decode.

**Method:**
1. **List every destination.** Write down everything a user might need to find or do in the system. Don't organize yet — just get everything out.
2. **Group by task, not by department.** For each item, ask: "what task is someone trying to accomplish when they come here?" Items that serve the same task belong together, even if they come from different internal systems or teams. Items that serve different tasks stay separate, even if they're technically part of the same system.
3. **Label in user language.** Name each group using the words a user would use when they're trying to find it — not the words your team uses internally. Test the label: would someone outside the team immediately understand what's in this group?
4. **Limit top-level choices.** Seven or fewer top-level items is the practical ceiling for navigation that can be scanned at a glance. If you have more, apply progressive disclosure (119) — show the most common destinations, hide the rest until needed.

**Artifact:** A grouped navigation structure with labels in plain user language.

**Watchout:** The urge to organize by how your team works — grouping content by the department that owns it, by the system it lives in, or by the order in which your team built it — is the most common IA failure. If a user has to know your org chart to navigate the product, the structure has been built inside-out.

**When You Can't Run the Full Version**

**If you're inheriting a legacy IA you can't restructure:** Work within the existing structure and improve the labels without changing the groupings. Better labels reduce the translation cost even when the grouping is imperfect. Document the grouping-level problems alongside the label improvements so the underlying structure can be addressed when access to change it opens up.

**If the top-level choice count can't be reduced (too many mandatory destinations):** Apply progressive disclosure (119) to surface the 5-7 most common destinations at the top level and route the rest through secondary navigation. The task-frequency data that drives this decision can come from analytics or from asking users what they're looking for most often.

**What you still get:** Navigation that at least uses user language at the label level, even if the groupings are constrained.

**What you give up:** The structural match between task logic and navigation grouping — which is the larger share of the navigational improvement.

**At Enterprise Scale**

Enterprise products often serve multiple distinct user roles whose tasks share a surface but don't share a structure. A single task-based IA that works for one role produces the wrong navigation for another.

**Multi-role navigation:** Before building the task-based IA, map which tasks belong to which roles. Roles with significantly different task sets need different entry points into the same system — not different navigation systems, but a role-aware top-level that routes each role to their primary tasks without requiring them to navigate past each other's top-level items. This is the "personalized navigation" pattern; the IA is still task-based per role, but the top-level is role-aware.

**Deeply nested hierarchies:** When the content volume forces 4-5 levels of navigation, task-based IA alone is insufficient — users lose track of where they are and what's at adjacent levels. Add breadcrumbs (so users know their location at all times), progressive disclosure (so only the current level is visible at full depth), and a search path as an always-available alternative to navigation.

**Legacy enterprise systems:** Many enterprise products have accumulated IA from multiple teams over many years, producing structures that reflect organizational history rather than task logic. In these systems, full IA restructuring is typically a project, not a method. Focus task-based IA on the highest-traffic destinations first — the 20% of navigation that serves 80% of users' tasks — and improve from there.

**Try This:** List every top-level navigation item in something you're building. For each one, ask: does a user who doesn't know your team's internal structure immediately understand what's in here? Rename any that require insider knowledge.

**Proof:** Ask someone unfamiliar with the system where they'd look for one specific thing. If they navigate to the right group without guidance, the labels are working. If they hesitate or look elsewhere first, the structure reflects internal taxonomy, not user task logic.

**Take this further:** In the next week, ask one person who uses the product (not one who built it) to find three things. Watch where they look first, without guiding them. Write one sentence: which label or group caused the most hesitation?

**After you've run this yourself:** List your navigation items to an AI tool and ask it to suggest groupings a first-time user might expect, based on common mental models for that type of software. Cross-reference with what you know about your actual users. Treat the output as a prompt list for what to test, not as a validated structure.

**What Next:** Once you have a proposed structure, validate it with real users using 218 (Card Sorting). If the navigation serves content-heavy destinations — document libraries, knowledge bases, research archives — where users are asking "what type of content am I looking for?" rather than "what task am I trying to accomplish?", read 204b (Content-Based IA) as a companion approach.
