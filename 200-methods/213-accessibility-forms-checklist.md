# A Practitioner's Checklist for Accessible Enterprise Forms
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** None. Pairs with 116 (error states), 117 (empty states)

**Goal:** After this piece, you will be able to run a basic accessibility pass on a form and name what passes and what fails — without specialist tools.

**Prior knowledge hook:** Think of the last form you filled out where you couldn't tab between fields in a predictable order — or where an error message appeared in red text and said nothing useful about what to do next.

**Trigger:** you're about to ship a form with several fields, especially in a dense or complex tool.

**Why this works:** keyboard navigability and clear error messaging aren't edge-case accessibility concerns — they're the floor below which a form stops working for a measurable portion of users. The tab test takes three minutes and catches the failures that affect everyone who doesn't use a mouse.

**Method:** check, at minimum — can you tab through every field in a logical order? Does every field have a visible label? Are errors announced clearly, not just shown in color?

**Artifact:** a short pass/fail check on your current form.

**Watchout:** passing this checklist isn't the same as it working for a real assistive-tech user — test with one when you can.

**Try This:** open a form you're building right now. Put down the mouse. Tab through it without clicking. Note: did you reach every field? Were the labels visible? Trigger one error — was it announced clearly or only shown in color?

**Proof:** Tab through your own form right now without using a mouse. If you can reach every field in a logical order, confirm every label is visible, and trigger an error to see how it's announced, you've run the check. A pass means the floor is covered. A fail means something specific broke — and you know what it is.

**Take this further:** in the next week, run the same tab test on a form in a product you use regularly, not one you built. Write one sentence: what fails that you'd never have noticed without the test?

**What Next:** If the error announcement fails the check, read 116 (Error States) for how to write accessible error messages. If the form handles high-stakes or sensitive data, read 237 (Cognitive Overload) to reduce cognitive load at moments of peak user anxiety, and 240 (Form Design Principles) for sequencing and label clarity under pressure.
