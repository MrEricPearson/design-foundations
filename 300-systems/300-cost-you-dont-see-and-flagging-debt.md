# The Cost You Don't See → Flagging Design Debt As You Go
**Tier:** 300 — Orchestrate | **Arc:** Full arc (6 parts) | **Prereqs:** 134 (design debt concept); recommended to publish early as motivational anchor
**Note:** Parts 1-3 = motivational prequel ("The Cost You Don't See"). Parts 4-6 = method ("Flagging Design Debt As You Go"), which also appears in the master outline as a standalone Tier 200 method.

**Goal:** After this arc, you will be able to recognize design debt accumulating in real time, flag it in your existing workflow without slowing down, and identify patterns worth raising.

**Trigger:** you're moving fast on something that feels slightly off but not broken enough to stop for — and you want a habit for catching and tracking that feeling before it compounds.

---

## Part 1: The Restart You Didn't Count

Most rebuilds don't start with a technical problem. They start earlier — at a moment when something wasn't clear enough, and everyone kept moving anyway because stopping felt slower than pushing through.

**A quick way to spot it in your own work:**
1. Think back to the last time something had to be redone significantly.
2. Ask: was there a point, before the rebuild, where someone had a nagging doubt and said nothing?
3. That moment is usually earlier than people think — often before a single line of code.

**What you end up with:** a clearer sense of where your actual restart risk lives — not in execution, but in an unspoken doubt further upstream.

**Proof:** "Was there a moment, before the rebuild, where someone had a nagging doubt and said nothing?" is answerable for any rebuild you've been through. The answer is almost always yes — and the moment it points to is almost always earlier than anyone expected.

**Watchout:** don't turn this into blame-hunting for a past project. The point is noticing the pattern, not finding who to blame for it.

---

## Part 2: What a Demo Actually Proves

A demo that gets applause proves people liked watching it. It doesn't prove the thing works for the people who'll actually use it every day. Those are two different kinds of "yes," and it's easy to mistake one for the other.

**A quick way to tell them apart:**
- Applause tells you the room is comfortable, not that the feature is right.
- Real validation means someone outside the room tried to actually use it, on their own, without you narrating.

**What you end up with:** a habit of asking, after any demo, "did anyone use this without us walking them through it?" — and being honest about the answer.

**Proof:** The question "did anyone use this without us narrating?" has a yes or no answer. A "yes" means you have real validation. A "no" means the applause was real but the validation wasn't — and now you know the difference, rather than mistaking one for the other.

**Watchout:** demos aren't useless — they're good for buy-in and momentum. Just don't let them stand in for the validation they weren't built to provide.

---

## Part 3: The Bar You Didn't Know You'd Set

Every team has an implicit bar for what counts as "good enough to ship." Few ever write it down — it just accumulates from what got let through before.

**A quick self-check:** would your team notice — really notice, out loud — if a shortcut like the one you're about to take happened on someone else's project? If the honest answer is "probably not," that's your current bar, whether anyone chose it on purpose or not.

**What you end up with:** an honest read on where your team's bar actually sits today, not where you'd like it to sit.

**Proof:** The bar your team actually holds is visible in the things that got through, not in the things you'd like to hold. The self-check question surfaces it: if the honest answer to "would we notice this on someone else's project?" is "probably not," that's the bar — chosen or not.

**Watchout:** this isn't about judging your team against some outside standard. Every team's bar is different for good reasons — the point is knowing yours, not matching someone else's.

---

## Part 4: Recognizing Debt in the Moment

Design debt often looks small enough to ignore — a shortcut, a label that doesn't quite make sense, a flow that works but only if you already know the trick. It's easy to walk past it because nothing is technically broken.

**A quick way to catch it:** ask, in the moment, "if a new person hit this today, would they get stuck?" If yes, that's debt, even if it currently works fine for people who already know the workaround.

**What you end up with:** a moment of noticing, which is the entire first step — nothing to fix yet, just to see.

**Proof:** "If a new person hit this today, would they get stuck?" is answerable in the moment. A yes means debt exists, whether or not it's broken. Noticing it explicitly — rather than walking past it — is what makes it capturable in the next step.

**Watchout:** don't try to catch everything at once. Debt-spotting is a habit you build slowly, not a one-time audit.

---

## Part 5: A Lightweight Way to Flag It

Once you notice something, the fastest way to lose it again is to keep it only in your head.

**Method:**
1. Wherever you already track work — a comment, a doc, a shared note — add one line the moment you notice something: what it is, and why it's debt.
2. Don't fix it yet. Just capture it before you move on.
3. Use a consistent marker (a tag, a prefix, whatever's easy) so these are easy to find later.

**What you end up with:** a running, lightweight list of debt, growing in the background without slowing down your actual work.

**Proof:** A consistent marker (tag, prefix, label) in your existing tool means every flagged item is findable in a single search. The list exists and is searchable before you review it — which is the only version of this list that can produce the pattern-finding in Part 6.

**Watchout:** a flag that never gets revisited is just noise. This only works if you actually look at the list again — which is Part 6.

---

## Part 6: Reviewing Your Own Flags

A single flagged item rarely matters much on its own. The value shows up when you look at several of them together.

**Method:**
1. Every so often, read back through what you've flagged.
2. Look for repeats — the same kind of issue showing up more than once.
3. A repeat is a pattern worth raising, even briefly, with whoever can actually address it.

**What you end up with:** a short, evidence-backed observation instead of a vague feeling that "something's off."

**Proof:** A pattern in the flags — the same type of issue appearing three times — is harder to dismiss than a single observation. The repeated flag is evidence; the single flag is a complaint. The review is what converts accumulation into pattern.

**Watchout:** don't wait for a perfect moment to review the list — it'll just keep growing. A quick, regular glance beats a rare deep dive.

---

---

## When You Don't Control the System

This arc assumes you can flag debt to someone with the ability to address it — and that the product is one your team builds. For non-custom dev practitioners working with vendor software or third-party systems, the debt is visible but the path to addressing it is different.

**What you can do:**

**Document with evidence.** Flag debt you observe in a vendor system using the same Part 5 method — write what it is and why it's debt — but address it to a different audience. Documented, specific debt with examples is vendor escalation material. "Users consistently can't find X" with timestamped screenshots and session observations is actionable. "The navigation is confusing" is not.

**Work around at the configuration or workflow layer.** Most vendor systems have configurable elements — custom labels, navigation structures, default settings, help text. Design the configuration to reduce the debt's impact. Document what you configured and why, so the next configuration decision isn't made without context.

**Shape future procurement.** Documented design debt in a current vendor system is evidence for procurement conversations about the next one. A specific, accumulated list of UX gaps — with evidence of their user impact — is the credible input that influences vendor evaluation criteria.

**Know the hard limits.** Some vendor debt is non-negotiable until the vendor addresses it or you change vendors. Name these explicitly. "This can't be fixed at our layer" is a valid conclusion, and naming it clearly prevents the team from repeatedly attempting fixes that aren't available to them.

**What you give up:** The ability to fix the underlying interface. The flagging habit still applies — debt noticed and documented is still more useful than debt noticed and forgotten — but the action it drives is different from the action available in a product you build.

---

**Try This:** open whatever you're working on right now. Ask: "If a new person hit this today, would they get stuck?" If yes, write one line — what it is and why — wherever you already track work. Add a consistent marker (e.g., `[debt]`). That's the habit started.

**Take this further:** in the next week, look back at the flags you've accumulated. Write one sentence: do the patterns that appeared match the restart risks you identified in Part 1, or are they pointing to something different?

**Judgment exercise:** You're three weeks from a hard deadline and the team has zero margin — every sprint is on fire. The arc assumes enough slack to notice and flag debt without stopping the work. What do you do with the habit under crunch? Which parts still apply? What do you cut, and when do you bring the flags back?

**What Next:** if your flags cluster around a specific type of interaction problem (error handling, empty states, labeling), those individual atoms have dedicated content — 116 (Error States), 117 (Empty States), 205 (Content Design). If you want to evaluate accumulated debt systematically rather than in the moment, the 216 (Heuristic Evaluation) method applies the same lens across a full screen.
