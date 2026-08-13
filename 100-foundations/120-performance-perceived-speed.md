# Performance and Perceived Speed
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** none | **Episode:** 8

**Goal:** Recognize when the experience of slowness is a feedback problem, not a performance problem — so you can diagnose whether the fix is technical optimization or interaction design.

**Concept:** The working assumption is that speed is binary — either the system is fast or it's slow, and fast is good. The correction: perceived duration and actual duration are different measurements, and they respond to different interventions. The mechanism: duration perception is governed by feedback signals, not clocks. An action that produces immediate visible confirmation ("loading," a progress bar, an animation) occupies a different psychological category than an action that produces silence. Silence reads as nothing happening. The user's response to silence is to wonder whether the action was received — which creates a second cognitive task on top of waiting. A visible signal converts silence into process, which is cognitively less expensive than uncertainty.

The practical consequence: an interface can feel faster without changing actual performance, and can feel slow despite being technically fast. The 1-second benchmark where responses should feel immediate, the 10-second benchmark where attention wanders without a progress indicator — these are about perception thresholds, not processing time measurements.

**You'll see it when:** Users retry actions (clicking a button twice) because nothing happened after the first click — the action was received but produced no visible acknowledgment. Or users abandon flows at steps with technically acceptable latency but no visible feedback.

**The signal:** An action produces a delay with no signal that the action was received. The user's next behavior is a retry or a question ("did that work?").

**Don't confuse perceived speed with actual performance.** A progress signal makes a wait feel like a process; it doesn't change how long the process takes. A false positive: adding a spinner and declaring the interaction fixed. If the actual processing time is long enough that user attention wanders before the result arrives, the signal manages the wait but doesn't solve the underlying problem — which is that the wait is longer than the task's cognitive engagement span.

**Try Noticing:** Find one interaction in your current product where the user acts and then waits. During the wait: is there any visible signal that the action was received? Does the interface change at all? If not, what would you need to see to know the action had been received?

**What Next:** If the slowness is in an AI-powered interaction, read 308 Part 1 (Make the AI's Behavior Visible) — the visibility principle applies specifically to AI actions and has additional considerations around trust and predictability.
