# 270h — Parallel Prototyping

**Tier:** 200 — Practice | **Arc:** Prototyping (see 309-prototyping-arc.md for approach selection) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity) | **Audience:** General | **Note:** Use when you need comparative data across directions, not optimization data within one direction.

**Goal:** Test multiple directions simultaneously to find which one works better — not just whether one can be made to work.

---

You already know prototyping answers questions. What most practitioners don't realize: the number of prototypes you test at once changes the kind of data you get.

Here's what normally happens. The team picks a direction. You build a prototype. You test it. Users struggle at step three. You fix step three. You test again. They succeed. The prototype works. You ship it. Six months later, engagement is fine but not great, and nobody's sure why — the design passed testing.

The problem wasn't the testing. It was the question. You asked "does this work?" when the real question was "which approach works better?"

---

Use this approach when you have genuinely divergent directions — not variations on the same idea. "Button on the left versus button on the right" isn't parallel prototyping. That's A/B testing. Use parallel when your team has real disagreements about approach: a conversational interface versus a form-based one, a wizard versus a dashboard, a task-first flow versus a browse-first one. If the directions differ only in aesthetics or minor sequencing, you don't need this method.

---

Steven Dow ran an experiment at Stanford (2010) with two groups building social networking features. One group built a single prototype and refined it across iterations. The other built three distinct prototypes in parallel and tested all three before choosing one to refine. Same total time. Same tools. Same task complexity.

The parallel group produced designs that independent evaluators rated significantly higher in quality. Their final designs showed more divergent thinking. And crucially, the designers themselves reported higher confidence in their final solution — not because they'd done more work, but because they'd seen evidence of what worked better.

The mechanism wasn't effort. It was comparison. When you test one prototype, you learn whether it works. When you test multiple simultaneously, you learn which one works better and why. Those are different cognitive outputs. The first gives you a pass/fail signal. The second gives you the underlying principle — the transferrable learning that applies to the next decision.

Tohidi, Buxton, Baecker, and Sellen (2006) confirmed the same pattern: parallel prototyping generated more diverse ideas and better solutions than iterative refinement. But they added something else. Testing multiple prototypes didn't just improve the final output — it reduced fixation. Designers who'd built and refined a single prototype became attached to it, even when testing revealed problems. Designers who'd built multiple stayed open to evidence.

Testing one prototype asks: does this work? Testing multiple asks: which works better? Only the second question generates transferrable principles.

---

1. Define the question all prototypes answer. Write it in one sentence: what do you need to know that these prototypes will test? "Which flow gets users to their first success fastest?" is testable. "Which one is best?" isn't. The question must be the same across all prototypes — otherwise comparison is meaningless.

2. Build two to three distinct prototypes. Each one represents a genuinely different approach to the same problem, built to the same fidelity level. If one is higher fidelity than the others, reviewers will favor it for polish, not structure. Keep them equally rough. Paper and sketch (270a) works well here — building multiple directions at high fidelity burns time before you know which direction deserves it.

3. Test all prototypes with the same participants. Each participant sees all directions in randomized order. Same task for each. Same success criteria. Don't ask which one they prefer — preference is the weakest signal. Watch which one they complete fastest, with the fewest errors, and the least confusion. Behavior tells you what works. Preference tells you what feels familiar.

4. Document performance per prototype. For each one, note: task completion rate, time to completion, points where participants hesitated or backtracked, and questions they asked. You're building a comparative table. The prototype that consistently performs better across participants is the direction that works — not the one the team liked most when you sketched it.

5. Extract the principle. After testing, answer this: what made the better-performing prototype work? Not "it was faster" — that's the outcome. What structural difference caused it to be faster? That principle is the artifact. It applies to the next ten decisions.

---

When you're done, you have three things: a comparative performance table showing which prototype worked better, a documented principle explaining why, and confidence that you chose based on evidence rather than opinion. If two prototypes performed equally well, you've learned that the difference doesn't matter to users — a finding that saves refinement effort on distinctions that won't move outcomes.

---

The failure mode that catches even experienced teams: testing prototypes sequentially instead of simultaneously. You test prototype A, iterate based on feedback, then test prototype B. By the time you reach B, A has been refined through two rounds and the comparison isn't fair. Or worse — you've already committed resources to A, and testing B now feels like a formality to confirm a decision already made.

Sequential testing converts an open question into a sunk cost argument. Teams interpret feedback on later prototypes through the lens of work already invested in earlier ones. They're not comparing directions anymore — they're defending investments.

The fix: all prototypes tested in the same sessions, with the same participants, before any refinement begins. No iteration until you've chosen the direction. It feels inefficient to build multiple things knowing you'll discard most of them. It's more efficient than refining the wrong one.

---

Pull something you're working on where at least two people have genuinely different ideas about the right approach. Not small variations — different structures. Build both as paper sketches (15 minutes each). Then walk one person through both, randomizing the order. Ask them to complete the same task with each. Note which one they completed faster and where they hesitated. Give the whole exercise 45 minutes.

You'll have a comparative finding today.

---

When one prototype consistently outperforms the others across multiple participants, that's the direction. If all prototypes perform about the same, you've learned the choice doesn't matter structurally — pick the one that's easiest to build or best fits technical constraints, because users won't care.

One false positive: participants say they prefer prototype A, but their behavior shows B worked faster with fewer errors. Trust the behavior. Stated preference reflects what feels familiar or socially desirable. Performance reflects what actually works.

---

Over the next three to five days, use the principle you extracted (Step 5) to evaluate one other decision your team is facing. Does the principle apply, or does it break down in this new context? Write one sentence: what did applying the principle reveal that you wouldn't have noticed otherwise?

If you share that sentence in a team channel, you'll see which principles others are finding reusable across contexts.

---

After you've run this yourself: describe both prototypes to an AI tool and ask it to generate five task scenarios that would differentiate them — places where one approach would handle the task better than the other. Use those scenarios as test cases before bringing prototypes to real participants. You'll catch structural differences in your office that would've taken three sessions to surface.

---

Once you've chosen the direction, 270b (Lo-fi Wireframe) or 270f (High-Fidelity Prototype) refines it to the next fidelity level. If the principle you extracted reveals an unstated assumption about who the user is, 301 (From a Vague Ask to a Real Persona) is the next step. When you're ready for a full usability session, 215a (Moderated Usability Session) covers the process.

---

**Sources**

Dow, S. P., Heddleston, K., & Klemmer, S. R. (2010). The efficacy of prototyping under time constraints. *Proceedings of the Seventh ACM Conference on Creativity and Cognition*, 165–174. https://doi.org/10.1145/1640233.1640260 Finding: Teams building and testing multiple prototypes in parallel produced higher-quality designs, more divergent solutions, and reported greater self-efficacy than teams iteratively refining a single prototype. The mechanism was comparative data — teams learned which design worked better, not just whether one could be made to work.

Tohidi, M., Buxton, W., Baecker, R., & Sellen, A. (2006). Getting the right design and the design right: Testing many is better than one. *Proceedings of CHI '06*, 1243–1252. https://doi.org/10.1145/1124772.1124960 Finding: Parallel prototyping generated more diverse ideas and better final solutions than serial refinement. Designers testing multiple directions simultaneously remained more open to evidence. Those refining a single prototype became attached to it even when data suggested problems.


Nielsen, J. (2011). Parallel and iterative design + competitive testing. *Nielsen Norman Group*. https://www.nngroup.com/articles/parallel-and-iterative-design/ Finding: Parallel design followed by competitive testing outperformed purely iterative approaches. The comparative method revealed which design principles transferred across contexts — learning that single-prototype iteration could not produce.

---

**Contributors**

Alberto Zamarron
