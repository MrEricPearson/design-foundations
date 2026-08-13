# Design System as Encoded Model
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 179, 194 | **Note:** Prereq for 196; critical for any practitioner working in an organization that uses a shared component library or design system

**Goal:** After this piece, you will be able to recognize what a design system has decided on your behalf — and distinguish between "this component doesn't fit my problem" and "I'm misusing the component."

**Concept:** A design system is not a collection of reusable visual elements. It is an encoded set of decisions about what patterns exist, what they mean, when to use them, and how they relate to each other. Every component in the system embeds assumptions about content, context, and use case. When you use a component, you are inheriting those assumptions — whether you know what they are or not.

A table component assumes the data is tabular: a defined set of columns, consistent rows, comparable values across the same column. Use it for tabular data and it works effortlessly. Use it for content that isn't tabular — varying structure per row, no consistent comparison dimension — and the component will fight you. The fight is a signal: the component's encoded assumptions don't match your content model.

A card component assumes there is an image, a title, a short description, and a primary action. Use it for content with those elements and the design is coherent and fast to produce. Use it for content without an image, or with descriptions of varying length, or with multiple competing actions — and you're fighting the component's assumptions again.

The value the design system provides: consistency and speed when your problem matches its assumptions. You don't make decisions that have already been made well. Buttons look like buttons everywhere. Alerts behave like alerts everywhere. Users don't have to re-learn interaction patterns as they move across the product.

The risk: accepting the design system's encoded decisions without checking whether they fit. The system decided what a card is. If your content isn't really a card — if it doesn't have an image, if the title isn't the primary element, if the action isn't a single clear CTA — using the card component applies decisions that don't fit your content, and the result is a design that looks coherent (it uses the design system correctly) while being structurally wrong for the actual content.

**You'll see it when:** A component is used in a way that requires overriding most of its default styling or adding states the component doesn't support. The effort to make the component work for the use case approaches the effort of building something custom. That is the signal that the design system's encoded assumptions don't match the problem.

**The signal:** A component is "almost right" — it works with some content but requires special cases or overrides for others. A special case inside a component use is usually an assumption mismatch: the component encoded "there is always an image" and this content type doesn't always have an image.

**Don't confuse design system compliance with design system fit** — compliance means using the system's components in the system's prescribed way; fit means those components are the right solution for the problem. You can be perfectly compliant and completely unfit. A design that uses every component as specified but uses the wrong components for the content model is both compliant and broken.

**Try Noticing:** Look at a design or interface built with a design system you know. Find a component that's being used with special cases — a table with cells that merge in unusual ways, a card without images, a form with non-standard validation patterns. For each: what assumption was the component built on that the current use violates? Is the violation incidental (the data doesn't happen to have an image but could) or structural (this content is genuinely not a card)?

**What Next:** Every design system fails at some boundary. Read 196 (Where Design Systems Fail) to understand how to recognize when you've reached that boundary — and what to do when you have.
