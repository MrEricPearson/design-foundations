# The Fastest Way to Test the Wrong Thing
**Tier:** 200 — Practice | **Arc:** Prototyping (309) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity), 147 (AI as Execution Partner), 158 (Task Statement Design) | **Audience:** General

*It generated fast. Nobody stopped to ask whether it was generating the right thing.*

---

You ran the session. People reacted to the prototype: someone noted the button placement, another flagged the error state, two said it felt intuitive. Forty minutes in, someone raised a concern about the overall flow. The room moved on. The debrief was waiting.

What nobody confirmed: whether the prototype was testing the question you actually needed to answer. The session gave you feedback on what AI built. That's not the same thing.

---

If you've used AI for drafts, outlines, or code scaffolding, you know the generate-then-evaluate approach: generate first, then refine. That works in most contexts. The instinct to apply it to prototyping is right. What it produces there is a specific, predictable failure mode. Knowing it in advance is what keeps the method from inverting on you.

Use this approach when the question requires interaction behavior to test: something that responds, not just something that looks like it responds. A paper sketch (270a) handles conceptual direction. A lo-fi wireframe (270b) handles navigational structure. Come here when you need real interaction: a filter that updates, a form that validates, a modal that fires.

---

AI compresses the production step. What takes hours of coded UI takes minutes of prompting. That speed is real and useful. The risk is in what happens cognitively the moment you see the output.

Tversky and Kahneman (1974) showed the mechanism: people estimate from an initial value and adjust, but the adjustment is never enough. The anchor dominates. In prototyping, when AI generates something visually finished before you've confirmed the structure is right, that polished output becomes the reference point for everything that follows. Wang and Brown (2025) at Nielsen Norman Group confirmed the consequence: showing polished AI prototypes "without proper framing may sabotage your stakeholder communication." The polish changes the kind of thinking people bring to the room.

The discipline that protects against it is one sentence, written before you open any tool.

---

Step 1: Write the question. On paper — not in the prompt window. "This prototype will test [specific question]." One sentence. Two sentences means two questions. Plan two tests. AI fills a vague scope with what's typical. What's typical isn't always what you're testing.

Step 2: Define the scope. List: one user goal, the minimum screens required to test it, and what you'll explicitly exclude. Without clear scope, AI generates comprehensive rather than targeted: a full product when you needed one flow.

Step 3: Prompt for function, not aesthetics. Describe what the interaction needs to do: "A prototype that lets a user [goal] across: [list each screen and what happens]." Huei-Hsin Wang (2025) found that vague prompts reliably produce poor layouts: excessive elements, poor visual hierarchy. Describe the function, not the appearance.

Step 4: Evaluate against the question. Before doing anything else: does what was generated test what you wrote in step 1? If the flow routes users somewhere you didn't intend, revise the prompt — not the question. The question is the specification. The prompt is your attempt to communicate it.

Step 5: Label every screen. At the top of each generated screen: "Prototype — not final design." Visible, not small. AI-generated UI looks finished enough that stakeholders who weren't present during generation may treat it as a product preview. The label keeps the session in learning mode.

---

When you're done: a working prototype with a documented question, a scope written down, every screen labeled, and a list of what's simulated. That last item matters when sharing with anyone who wasn't present during generation. What the prototype doesn't do should be visible before the session starts.

---

The failure mode that catches experienced practitioners: opening the tool before writing the question. It's not carelessness. Generate-then-evaluate works in nearly every other AI-assisted context. They've applied it correctly dozens of times, and so they apply it here. The generated prototype looks real, feels navigable, and revising it to test a different question feels like waste. The question gets shaped around the artifact rather than the artifact around the question. (If you've watched a team debate a generated layout before anyone asked what it was supposed to answer, you've seen this.)

Kate Moran (2026) at NNGroup puts the accountability clearly: when you specify what to build, AI is responsible for execution quality. What to test, and whether the output actually tests it — that's yours. Write the question before you generate anything. Every time, in that order.

---

For a feature or flow you're currently working on: write the question on paper before opening any tool. List the minimum screens. Prompt for function: "a prototype that lets a user [goal] across these screens: [list]." Evaluate the output against your question: does it actually test what you wrote? Label every screen. Show it to one person and watch what they do. Note where the generated behavior did something you didn't expect. That's where AI's interpretation of your prompt diverged from your intent.

Give the whole process 45 minutes. You should have a testable prototype today.

---

You've preserved the judgment layer if you can answer, before sharing: "What question was this prototype designed to test?" If you can answer clearly, you're ready. If the honest answer is "I'm not sure," the prototype ran ahead of you.

The false positive: a session where participants react, decisions get made, and it looks like success. What it didn't confirm: whether you were testing the right structure. A productive-looking session can still not answer your question.

---

Over the next few days, show the same prototype to someone with less context. Watch for when they treat it as a finished product. Write one sentence: at what point did the realism stop being useful and start creating the wrong expectation?

---

This approach is the AI path. The generation in step 3 is what AI contributes. If you've defined the question, scoped the minimum interaction, and evaluated whether the output tests it, the judgment layer was yours throughout. That was the point.

---

When you're ready to test with a real participant, read 215a (Moderated Usability Session) for a live facilitated session, or 215b (Unmoderated Usability Testing) if participants work independently. If the prototype surfaces a consistent pattern across multiple states, read 216 (Heuristic Evaluation) to map it to a known structural principle. If the prototype reveals a deeper uncertainty about who you're designing for, read 301 (From a Vague Ask to a Real Persona).

---

**Sources**

Tversky, A., & Kahneman, D. (1974). Judgment under uncertainty: Heuristics and biases. *Science, 185*(4157), 1124–1131. Finding: people estimate uncertain quantities by starting from an initial value and adjusting — but the adjustment is systematically insufficient. The anchor dominates even when the estimator knows it's arbitrary and is motivated to set it aside.

Wang, H-H., & Brown, M. (2025, October 24). Good from afar, but far from good: AI prototyping in real design contexts. Nielsen Norman Group. https://www.nngroup.com/articles/ai-prototyping/ Finding: showing polished AI-generated prototypes without proper framing "may sabotage stakeholder communication." AI tools lack the judgment and nuance of an experienced practitioner. The approach works best with people who already understand the craft.

Moran, K. (2026, March 27). GenUI vs. vibe coding: Who's designing? Nielsen Norman Group. https://www.nngroup.com/articles/genui-vs-vibe/ Finding: when practitioners specify what to build, AI is responsible for execution quality. The distinct failure modes are poor execution (vibe coding) vs. poor judgment (genUI). Design decision authority determines which failure mode applies.

Wang, H-H. (2025, December 5). Prompt to design interfaces: Why vague prompts fail and how to fix them. Nielsen Norman Group. https://www.nngroup.com/articles/vague-prototyping/ Finding: vague prompts produce "Frankenstein layouts" — excessive elements, poor hierarchy, redundant components, counterintuitive information flows. "Good design decisions can't be automated," and AI remains a tool requiring human judgment and expertise.
