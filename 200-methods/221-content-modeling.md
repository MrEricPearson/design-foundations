# Content Modeling
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** 179, 180, 181, 183 | **Wave:** 3

**Goal:** Run a content modeling session that produces a named set of content types with defined attributes and relationships — before any screen design begins.

**Prior Knowledge Hook:** You've probably started a design project by asking what the screens should look like. The frame that produces better outcomes earlier: ask what the system knows about first. A content model is not a prerequisite to design — it is the foundation that design is a representation of. When it doesn't exist before design starts, it will be reverse-engineered under pressure during implementation, one unexpected content problem at a time.

**Trigger:** Use this method when starting a new product or feature, when a feature request reveals that the underlying data model is unclear, when multiple teams are naming the same things differently, or when design iterations keep failing because the content "doesn't fit" the designed containers.

**Why this works:** Every design decision about display depends on what exists to display. A filter requires an attribute to filter on. A sort requires a comparable value. A related content panel requires a defined relationship. Running content modeling before design reveals what capabilities the design can actually specify — and what would require structural work that looks invisible in the design but surfaces as a gap during implementation. Doing this before design means structural surprises become decisions rather than crises.

**Method:**

**Step 1: Name the things.** List every distinct type of thing the system needs to know about. Not screens — things. A product, a user, an order, an article, a location. Each distinct type of thing is a content type candidate. Stop when you've named everything you can think of. This step prevents the mistake of designing around unlabeled things that show up later as "content that doesn't fit."

**Step 2: Define attributes for each type.** For each content type, list every named property instances of that type have. Include attributes whether they're currently stored, planned, or needed. Mark each: Is it required (every instance has it) or optional? Is the value free-form (user-entered text) or structured (a defined set of values, a date, a number, a reference to another type)? This step prevents the mistake of designing features on attributes that don't exist.

**Step 3: Name the relationships.** For each content type, ask: what other types does this relate to? An article has an author (a reference to a user type). An order contains products (a reference to a product type, multiple). A location has a region (a reference to a region type). Draw the relationship as: [Type A] + [relationship verb] + [Type B], and note cardinality (one-to-one, one-to-many, many-to-many). This step prevents the mistake of designing cross-type views on relationships that haven't been defined.

**Step 4: Test against the required capabilities.** List the top 5-10 things the system must be able to do: filter, sort, display, relate, search. For each capability, trace it back to the attribute or relationship it requires. Does the attribute exist in the model? Is it structured (not free-form)? Is the relationship defined? Where capabilities can't be traced back to the model, either add the missing structure or acknowledge the capability gap explicitly. This step prevents the mistake of specifying features the model can't support.

**Step 5: Name the gaps.** Document explicitly: what did you need that isn't in the model? What's in the model but needs structural work before it can support the intended capabilities? These are the known risks in the current design. Naming them doesn't solve them, but it means the team knows what's decided and what isn't. This step prevents the mistake of leaving structural unknowns implicit.

**Artifact:** A content type map — a named set of content types, each with its attribute list (with structured/free-form designation and required/optional status), plus a relationship diagram (or table) showing how types connect. This is the shared model the design, development, and content teams are working from.

**Watchout:** Content modeling produces completeness pressure — the feeling that the model must account for everything before proceeding. Most smart, thorough practitioners fail here: they treat incompleteness as a problem to solve before continuing. This is backwards. Incomplete models are expected and fine. What you're producing is the current best understanding, explicitly marked with what's known and what's still open. Premature completeness pressure produces two failure modes: (1) the model session never ends because someone always has one more attribute to add, or (2) the model is closed too early with false confidence that it's complete. The correct stance: this is what we know now, and here are the explicit gaps. Design proceeds from what's defined.

**Try This:** Take a feature or screen you're currently designing or working toward. Without looking at any existing designs: list the types of things it needs to know about. For each type, list 5-7 attributes. Then identify 2-3 relationships between types. Now compare to what the system actually supports: do those attributes exist? Are they structured? What's missing? What would need to exist before the feature could work as designed?

**Proof:** The content model is working when a new design request can be evaluated against it: "does the model support this?" becomes an answerable question. The false positive: a model that's complete but unchecked — it exists, but it hasn't been tested against the actual design requirements. A model isn't verified until at least one design decision has been traced back to a specific attribute in the model that you confirmed exists.

**Take This Further:** Over the next 3-5 days, find one feature in a product you work on where "the data doesn't support it" or "we'd have to check the content manually." Trace back: what attribute or relationship is missing? Could it be added to the current model, or would it require structural work? Write one sentence: what would change about the design if that attribute existed?

**After you've run this yourself:** AI can help expand an initial content type list quickly — describe the domain and the intended capabilities, ask for content type candidates with attributes. Use it to surface types you may have missed. Then validate: does each type it named represent a thing the system actually needs to know about, or is it a screen (which is not a content type)?

**What Next:** Once you have a content model, the IA work — how content is organized, navigated, and accessed — is constrained by what the model contains. Read 222 (IA Methodology) for how to build navigation and organization from a defined content model. For how classification decisions within the model compound over time, revisit 183 (Classification Decisions Compound).
