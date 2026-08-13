# Taxonomy Design Basics
**Tier:** 100 — Recognize | **Arc:** Standalone | **Prereqs:** 183, 184 | **Note:** Controlled vocabulary foundation; prereq for 222 (IA arc); pairs with 184 (labeling systems)

**Goal:** After this piece, you will be able to recognize the difference between a taxonomy that was designed to serve users and one that was designed to serve the organization — and why those produce different navigation outcomes.

**Concept:** A taxonomy is a controlled vocabulary — a defined set of terms with clear relationships, scope, and meaning within a specific domain. "Controlled" is the operative word: the terms are fixed, their meanings are agreed upon, and adding or changing a term is a deliberate act that has consequences for everything classified under it.

The failure pattern in practice: taxonomies get designed by asking the people who own the content to name their categories. This produces an org-facing taxonomy — one that reflects how the organization thinks about and groups its content internally. The team responsible for "legal and compliance" names their section "legal and compliance." The team responsible for "customer support resources" names their section "customer support resources." Each section accurately reflects how the owning team categorizes their content. None of it reflects how a user navigating to find something would categorize what they need.

The mechanism: users approach navigation with a task. They want to do something or find something. Their query — mental or actual — is task-shaped, not org-chart-shaped. A user who wants to "update my billing address" is not going to navigate to "account management." They are going to look for something related to billing, payment, or account settings — and "account management" will require an additional inference step: "I guess updating my address falls under account management." That inference step is cognitive load added by the taxonomy mismatch. Multiply it by every navigation choice on every page visit.

The test: can someone unfamiliar with your organization's structure navigate to what they need using only the taxonomy terms, without prior knowledge of how your org is structured? If the answer requires knowing your org chart, the taxonomy is org-facing.

**You'll see it when:** Navigation testing reveals that users can't find things — not because the content is missing, but because they're looking in a different section than where it lives. The content is in "financial management" and they're looking in "billing." Or: users succeed at finding things faster after a rebrand or IA redesign that didn't change the content — only the labels and organization. The content was always there. The taxonomy was blocking it.

**The signal:** Navigation section names are also department names or function names from inside the organization. When the org chart and the site map look structurally similar, the taxonomy is org-facing.

**Don't confuse a taxonomy with a site map** — a site map shows the hierarchy of pages; a taxonomy defines the vocabulary of terms used to organize and classify content. A site map could implement any number of underlying taxonomies. Two sites with identical site map structures can serve users completely differently depending on whether the taxonomy reflects user language or org language. Fixing the site map without fixing the taxonomy produces the same problem with a new layout.

**Try Noticing:** Open a navigation system — a product, an intranet, a website in your domain. Look at the top-level navigation terms. For each term: would a user who has never worked in this organization choose that word to navigate to what lives there? Or does it require knowing what the organization calls this domain? The count of terms that require organizational knowledge is a rough measure of how org-facing the taxonomy is.

**What Next:** Building a taxonomy that reflects user language requires understanding that language — which is research. Read 115 (Card Sorting) for the method most useful for discovering user-native taxonomy. Read 222 (IA Arc) for how to apply this in a full IA design process.
