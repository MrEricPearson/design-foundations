# Card Sorting for IA Validation
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** 204-information-architecture | **Note:** Evaluative complement to 204; tree testing is the navigational variant — add IA-validation coverage through card sorting before investing in a dedicated tree testing tool

**Goal:** After this piece, you will be able to find out whether users organize information the way your navigation assumes they do.

**Prior knowledge hook:** Think of a navigation menu you designed that made perfect sense to you and your team — and then watched users scan every category multiple times before picking the wrong one.

**Trigger:** you've structured navigation or an information architecture and want to know whether it matches what users expect — before building it.

**Why this works:** users navigate by the mental model they already have, not by yours — card sorting makes the gap between those two models visible before you build the wrong structure into production, where it costs far more to fix.

**Method:**
1. Write each navigation item or content category on a card — one item per card, no hierarchy shown. Aim for 30–40 items maximum; more becomes unwieldy.
2. Run an open sort (for discovery): ask 5–8 participants to group the cards however makes sense to them, then label each group themselves. Don't suggest groups — their groupings are the data.
3. After all participants have sorted: compare groupings. Look for consensus clusters (3+ people grouped these together) and persistent outliers (items that never landed in the same group twice).
4. Consensus clusters = your navigation categories; they reflect real mental models. Persistent outliers = items that need different labeling, deeper nesting, or may not belong in navigation at all.
5. Optional closed sort (for validation): once you have a proposed structure, ask participants to sort cards into your predefined categories. Where they can't find a home for something — or put it somewhere you didn't expect — is where your category labels aren't matching their mental models.

**Artifact:** a grouping comparison table showing which items were consistently grouped together and which were divergent — with at least one revised navigation structure based on the consensus clusters.

**Watchout:** card sort results are mental models, not optimal structures — what users expect isn't always what's most correct or complete. Use results to understand user expectations, then combine with domain knowledge to decide. Don't implement groupings mechanically when they produce incomplete or incoherent categories.

**Try This:** take your current navigation items, write each on a sticky or doc line, and send them to three people with the instruction "group these however makes sense to you and name each group." Compare the three groupings — what lands together consistently, and what gets placed differently every time?

**Proof:** If you revise your navigation structure based on the sort results and participants in a follow-up closed sort can place cards into categories with less hesitation and fewer errors, the method worked. The shift from "where would you put this?" confusion to confident placement is the signal.

**Take this further:** in the next week, share the grouping results with one team member who didn't run the sort. Write one sentence: what surprised them about how users categorized things?

**After you've run this yourself:** describe your navigation items to an AI tool and ask it to generate three possible grouping structures with different label approaches — use this to pressure-test your current structure before running the actual sort.

*Tree testing note: tree testing is the navigational complement to card sorting — you show the proposed structure and ask users to find specific items within it. Run card sorting first to build the structure; tree testing to validate navigation paths once the structure exists. Dedicated tools (Maze, Optimal Workshop) are required for tree testing; card sorting can be run with physical cards, sticky notes, or a shared document.*

**What Next:** if the sort reveals that your IA structure is off, return to 204a (Task-Based IA) if users are grouping by task logic, or 204b (Content-Based IA) if by content type. If the sort is complete and you want to test whether users can navigate to specific items, that's a tree test — flag it to your embedded designer or use a tool like Maze.
