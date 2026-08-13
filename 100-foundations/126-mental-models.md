# Mental Models
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** none | **Episode:** 3

**Goal:** Recognize when a usability problem is a mismatch between your system's organization and your users' expectations — so you can identify the gap rather than attributing confusion to user error.

**Concept:** The working assumption is that users who can't find things or do things "wrong" need better instructions or a more intuitive design. The correction: every person who uses software arrives with a pre-existing mental model — a map built from prior experience that tells them where things should be, what words mean, and what sequences to expect. When the system's structure conflicts with that map, users get confused. The confusion isn't an error in the user; it's evidence of a gap between two models. The mechanism: the system's model is the designer's or developer's — built on deep familiarity with the system's internal logic. The user's model is built on prior experiences with other systems and their own mental organization of the task. These two models have no particular reason to align, and they routinely don't. Explaining the system better (onboarding, help text) addresses the symptom; aligning the system to users' models addresses the cause.

**You'll see it when:** Users consistently look for a feature in a place where it isn't. Or they call features by names that don't match the labels. Or they complete a task in a sequence different from the one you designed for, and their sequence is internally logical.

**The signal:** Someone uses the product "wrong" in a way that would be correct if the system were organized differently. Their path isn't random — it reflects an expectation that your structure violated.

**Don't confuse mental models with user preferences.** A user who can't find something isn't expressing a preference; they're demonstrating where their expectations diverge from the system's structure. The fix is expectation-matching, not better explanation. A false positive: a user who can find something after reading help text has successfully navigated a mental model gap using a workaround — the gap is still there and will produce the same friction for the next unfamiliar user.

**Try Noticing:** Take one feature or navigation element in something you're working on. Ask someone unfamiliar with it: "Where would you look for [thing]?" Don't show them — just ask. Note whether their answer matches where the thing actually is. The gap is a mental model mismatch.

**What Next:** If the gap is in how information is organized, read 204a (Task-Based IA) for organizing around user goals or 204b (Content-Based IA) for organizing around content types. If the gap is in vocabulary — what things are called — read 205 (Content Design / UX Writing).
