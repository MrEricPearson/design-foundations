# Heuristic Evaluation
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** 124-nielsens-heuristics | **Note:** Pairs with 215-usability-session, 211-quick-comparative-scan

**Goal:** After this piece, you will be able to produce a severity-rated usability problem list for any interface — without recruiting users.

**Prior knowledge hook:** Think of a UI you looked at and thought "something's off here" but couldn't articulate what — so you either said nothing, or gave feedback that was too vague for anyone to act on.

**Trigger:** you need to identify usability problems in an interface and don't have users available, or you want to find problems before putting real users in front of something.

**Why this works:** heuristic evaluation gives a named vocabulary for what "off" means — when you can name the violated principle, the finding becomes specific, prioritizable, and fixable rather than a subjective reaction that's easy to dismiss.

**Method:**
1. Walk through the interface screen by screen, simulating the primary user task. Stay in the user's flow — don't jump to settings or edge cases until you've covered the main path.
2. For each screen: note any element that violates one of the 10 heuristics (124). Write it as: "[element] violates [heuristic] because [specific behavior]."
3. Rate each violation by severity: 0 = not actually a problem, 1 = cosmetic (low priority, fix if time), 2 = minor (should fix), 3 = major (fix before ship), 4 = catastrophic (fix immediately — blocks core task).
4. List violations ordered by severity, not by screen order. Severity 4 and 3 items are the report.
5. Repeat with a second evaluator if possible. Two independent evaluations find roughly twice the problems a single evaluator finds, and a merged severity list is more defensible.

**Artifact:** a severity-rated violation list with the specific location, the violated heuristic, and the reason for the severity rating — for all Severity 2, 3, and 4 items.

**Watchout:** heuristic evaluation finds different kinds of problems than usability testing — it catches interface-level issues well, but misses task-level failures that only appear when a real person tries to accomplish something specific with unclear context. Use it as a complement to usability testing, not a replacement.

**Try This:** take one screen you're working on right now. Walk through it using heuristics 1, 3, 5, and 9 only (status visibility, user control, error prevention, error recovery). Write every violation you find with a severity rating. That's a quick four-heuristic scan.

**Proof:** A severity-rated list converts "this feels bad" into "this is a Severity 3 violation of Heuristic 9 that blocks error recovery." The first is an opinion; the second is a prioritized, fixable, arguable finding. If you can walk out of a review with a ranked list that the team didn't need to argue about which things mattered, the method worked.

**Take this further:** in the next week, run the same four-heuristic scan on a different screen in the same product. Write one sentence: are the violations consistent across screens, or does one screen have a concentrated problem?

**After you've run this yourself:** describe a screen's content and layout to an AI tool and ask it to identify violations of each of the 10 heuristics — then check each violation against the actual interface, since AI without visual access can only work from your description. For interfaces with screenshots, some AI tools can evaluate visually.

**What Next:** if you want to validate your findings with real task behavior, run 215a (Moderated Usability Session) — it will confirm which Severity 3/4 items are actually blocking users. If participants need to work independently without a facilitator, use 215b (Unmoderated Usability Testing) instead. If you want to compare against a competitor, read 211 (Quick Comparative Scan).
