# Automation Bias and Calibrated Trust
**Tier:** 100 — Recognize | **Note:** Foundational prereq for 302 (Spotting AI Surprises) and 308 (Designing for AI Trust); pairs with 168 (Explainability vs. Transparency in AI)

**Goal:** Recognize automation bias in yourself and in users — so AI assistance doesn't quietly lower the quality of judgment.

**Concept:** Automation bias is the tendency to over-rely on automated outputs, even when the outputs are wrong and human judgment would catch the error. It's not the result of carelessness — it's a cognitive efficiency mechanism. Trusting automated systems frees attention for other tasks, which is usually sensible. In AI-assisted products, it means users will accept AI outputs they could have corrected, and over time delegate judgment they should retain. The design challenge is calibrating user trust — neither under- nor over-relying on AI outputs.

**You'll see it when:** A user accepts an AI suggestion without reading it carefully because the AI is usually right. Or an AI-generated output becomes the final output without a verification step. The calibration slips from "AI is plausible unless verified" toward "AI is right unless obviously wrong" — and the obvious errors are now the only ones getting caught.

**The signal:** The AI output is accepted without any verification moment — no comparison to known data, no check against what the user already knows, no "does this match what I expected?" pause. The absence of that pause is the signal.

**Don't confuse this with:** Reasonable trust in AI, which is calibrated confidence based on experience with a specific tool on specific types of tasks. Automation bias is uncalibrated trust — trusting AI more than your experience with it warrants. The distinction is whether the trust is specific ("this AI is reliable for X") or general ("AI is usually right").

**Try Noticing:** In the last week, how many AI-generated outputs did you verify before accepting, and how many did you accept on confidence? The ratio is your current calibration for that tool and task type. Is that ratio appropriate given the stakes of the decisions those outputs influenced?

**What Next:** When designing an AI feature and wanting to preserve user calibration, read 302 (Spotting AI Surprises) and 308 (Designing for AI Trust) — both address the structural design of AI outputs in ways that support rather than undermine calibrated trust.
