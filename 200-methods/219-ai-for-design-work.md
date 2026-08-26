# Before You Use What AI Generated
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** 147 (AI as Execution Partner) | **Wave:** 3

**Goal line:** AI generates fast. Knowing whether to use what it generated takes something else entirely.

---

You get the output back in about thirty seconds. Structured, clean, the sections make sense. It looks like something that would have taken you a couple of hours. So you use it.

Nobody asked whether it was right.

You already know AI generates faster than you do. What's less obvious is where in that process you need to stay in the driver's seat, and what happens when you don't.

---

Use this when you're about to use an AI tool for a design task: interface copy, navigation labels, error message text, a flow structure, a set of options. You want the generation speed. You also want to know whether what comes back is usable.

---

Here's the mechanism. Nisbett and Wilson (1977) showed in one of the most-cited papers in psychology that people don't have direct introspective access to their own decision processes. When they make a choice, they construct an explanation afterward, based on what seems like a plausible reason, not on what drove the decision. They called this post-hoc rationalization. It's durable: people produce confident reasons for choices they made on entirely different grounds.

This shows up immediately when AI output looks polished. The structure is right, the phrasing is professional, the length is appropriate. Your brain reads the form as a quality signal. And when someone asks why you used it, you generate reasons. It covered the main points. Nothing was wrong. It matched what I was going for.

Those aren't evaluations. They're rationalizations.

The fix is simple, and the only requirement is that you do it first. Write down what good looks like before you generate anything. Criteria written before output exist outside the output. They can't be contaminated by it. When you check AI-generated work against criteria you set before seeing it, you're verifying, not rationalizing.

Parasuraman and Manzey (2010) called the version of this that skips the check automation bias, the tendency to accept automated output without independent verification, even among expert users. The full picture is in 147. The relevant part here: polished output signals completion, and the verification step starts to feel redundant. Writing criteria first gives you something to check against before that feeling takes over.

---

The method is five moves.

1. Scope the task before you prompt. Not "help with the error states" but something like "generate three options for the message a user sees when payment processing fails — general timeout scenario, not a declined card." That specificity does two things: it makes the output evaluable, and it forces you to know what you need before you ask.

2. Write criteria before generating anything. Two or three is enough. Write criteria, not preferences. A preference is "it should feel friendly." A criterion is "it says what went wrong and what to do next, in that order, in under fifteen words." Criteria are checkable. You can look at output and say yes or no. Write them first. This step is the whole method.

3. Generate multiple variations. Ask for three to five. The comparison is where evaluation starts. When you're choosing among options, you're thinking about what distinguishes them. One output gives you accept-or-reject. Three give you a real choice.

4. Evaluate each option against your criteria, not against what looks polished. For each variation, check it against what you wrote before generating. Which criteria does it meet? Which doesn't it?

5. Decide. Choose the option that best fits your criteria. Adapt it. AI output almost always needs adjustment for the specific context. Or conclude nothing met the bar, tighten the scope, and run it again.

What you end up with is a decision with a record: what AI generated, what criteria you applied, what you chose and why. Moran and Rosala (2024) at NNGroup were direct about this after studying how practitioners use AI in research and design work: "Never rely on AI tools to perform all your analysis for you." The output is a first pass. Your evaluation is the work.

That record matters beyond the immediate task. It makes your reasoning visible, the decision reviewable, and the next similar task faster, because you've already worked out what criteria matter.

---

The watchout for this method is skipping step 2. The output lands and looks finished, and you think "this is pretty good" and move on without checking it against anything. Kupfer and colleagues (2023) found a direct correlation in their study of AI-assisted personnel decisions: the more thoroughly decision makers reviewed output against explicit information, the better their decisions were. More time spent, more pages examined, better outcomes. The correlation ran the other direction too. Skipping the check wasn't neutral.

(If you've ever shipped interface copy that read perfectly fine in the chat window and wrong in the actual product, you've already paid the tuition on this one.)

---

Take a design task from your current work: interface copy, an error message, navigation labels, an email subject line. Before you open any AI tool, write two things down: exactly what you're asking AI to generate, and two criteria for what good looks like. Then generate three variations and check each against those criteria. Fifteen minutes or less. What you end up with will be something you can explain, not just something that looked right.

---

If you found yourself editing specific things in the output rather than accepting it wholesale, or if you rejected an option that would have passed a gut-check but failed your criteria, the method worked.

---

In the next three days, run this pattern on one more design task. Afterward, write one sentence: what did naming criteria first change about what you caught in the output?

---

After you've run this yourself several times, try a second-order move: use AI to generate the evaluation criteria before you generate the content, then ask whether those criteria were the right ones. That check surfaces assumptions in your own judgment framework, the ones you didn't know you were making.

---

For the foundational thinking behind why the judgment layer matters and can't be delegated, 147 (AI as Execution Partner) covers it in full. For applying this same criteria-first pattern to synthesis work, 214 (Affinity Mapping) has an AI path built on it. For handling AI-generated prototypes, where the output looks especially finished, 132 (Prototype Fidelity) names what to check before treating it as real.

---

**Sources**

Nisbett, R. E., & Wilson, T. D. (1977). Telling more than we can know: Verbal reports on mental processes. *Psychological Review, 84*, 1108–1136. Finding: people lack direct introspective access to their own decision processes and construct post-hoc rationalizations — plausible explanations for choices made on other grounds.

Parasuraman, R., & Manzey, D. H. (2010). Complacency and bias in human use of automation: An attentional integration. *Human Factors, 52*(3), 381–410. Finding: automation bias, the tendency to accept output without independent verification, occurs in expert users. Polished-looking output signals completion and suppresses the impulse to verify.

Moran, K., & Rosala, M. (2024, September 27). Accelerating research with AI. Nielsen Norman Group. https://www.nngroup.com/articles/research-with-ai/ Finding: "Never rely on AI tools to perform all your analysis for you" — AI produces a first pass. Human oversight and review are required at every stage.

Kupfer, C., Prassl, R., Fleiß, J., Malin, C., Thalmann, S., & Kubicek, B. (2023). Check the box! How to deal with automation bias in AI-based personnel selection. *Frontiers in Psychology*. https://doi.org/10.3389/fpsyg.2023.1118723 Finding: verification intensity — time spent reviewing, pages examined — directly correlates with decision quality. Lower verification produced measurably worse outcomes.
