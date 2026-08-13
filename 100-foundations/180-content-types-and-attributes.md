# Content Types and Attributes
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 179 | **Note:** Core vocabulary for all content architecture work; prereq for 182, 184, 221

**Goal:** After this piece, you will be able to recognize what a content type is and what its attributes are — so you can describe what a system knows about its things precisely, instead of treating "content" as one undifferentiated material.

**Concept:** Content is not a monolith. A system that shows multiple kinds of things contains multiple content types — each a named category of thing with a defined set of attributes. An article has a title, a body, an author, a publish date, and a set of tags. A product has a name, a price, variants, an inventory count, and images. A user has an email, a role, and a history. These are different content types; they are not different amounts of the same thing.

Attributes are the slots that instances of a content type fill. When you define that a product has a "price" attribute, you can display that price, sort by it, filter on it, compare it. When the price lives in the body field as text — "costs $50" — you can only display it. You can't filter, sort, or compute. The same information exists in both cases, but only the structured attribute version can be reasoned about by the system.

This is the underlying mechanism of why structured content is worth defining: an attribute is not just a field — it is a capability. Every attribute you name is something the system can select for, filter by, display in context, or reference from another type. Every piece of content buried in a blob field is a capability the system permanently doesn't have.

**You'll see it when:** A stakeholder asks for a feature — "show the five most recent articles by this author" — and the answer is "we'd have to check the articles manually because the author isn't stored as a separate field." The capability was assumed. The attribute never existed. The information may be present somewhere in the content, but not in a form the system can act on.

**The signal:** Someone is asked to display or filter content and cannot, not because the information is missing, but because "it's all in there somewhere" — meaning it exists in unstructured text rather than as a named attribute. The content exists. The attribute doesn't.

**Don't confuse an attribute with a field label in a form** — a field label is a UI element; an attribute is a data definition. You can rename a field label without changing the attribute. You can change the attribute and break every piece of content that depended on it. The confusion matters because people often "add a field to the form" when what they're actually doing is defining a new attribute — which has consequences for every existing piece of content, every query that runs against the data, and every display that shows the attribute.

**Try Noticing:** Pick something you use frequently — a task manager, a content platform, an internal tool. Choose one type of thing in it — a task, an article, a record. List every attribute you can observe: what named properties does this thing have that the system treats differently (can filter by, can sort by, can display distinctly)? Now look for information that exists in the "body" or "description" or "notes" field that could be an attribute but isn't. What can the system not do because of that — and what would it be able to do if those things were attributes?

**What Next:** Once you can identify content types and their attributes, read 182 (The Bolt-On Cost) to understand what happens when you try to add attributes after the content architecture is already built. If you're about to define new content, read 221 (Content Modeling Method) for how to run the definition process systematically.
