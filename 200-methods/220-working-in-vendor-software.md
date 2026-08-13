# Working in Vendor Software
**Tier:** 200 — Practice | **Arc:** Standalone | **Prereqs:** 134 (Design Debt) | **Audience note:** Written for non-custom dev practitioners responsible for vendor/third-party systems where the interface can't be modified. Pairs with 300 (Design Debt arc) for the flagging habit this piece feeds.

**Goal:** After this piece, you will be able to apply design thinking to a system you didn't build and can't redesign — reducing the UX gap at the layers you can change, and documenting what you can't change in a way that's actionable.

**Prior knowledge hook:** Think of a product you're responsible for that you didn't build — a vendor platform, a third-party tool, a licensed system. Design problems exist in it. Some of those problems are visible and frustrating. But you can't change the interface. That constraint doesn't end the design work; it changes where the design work happens.

**Trigger:** A design problem has been identified in a vendor or third-party system — navigation doesn't match user task logic, labels use the vendor's terminology rather than users' language, a critical workflow is five steps when it should be two. You're responsible for user outcomes with this system, but you didn't build it and can't modify the core interface.

**Why this works:** Vendor systems have layers of mutability — some things are genuinely fixed, and some things look fixed but aren't. The design leverage available to you is always larger than it first appears, once you've separated what's configurable from what's locked. And what genuinely can't be changed isn't design dead-end; it's evidence — for the vendor relationship, for procurement decisions, and for user communication that sets expectations correctly.

**Method:**
1. **Map the layers of what you can and cannot change.** For the vendor system, separate three categories:
   - **Fixed:** core interface elements the vendor controls and won't change (navigation structure, data model, primary workflows, system-generated terminology)
   - **Configurable:** elements the vendor exposes for configuration (custom labels, navigation order, default settings, visible modules, role-based access controls, help text, notification content)
   - **Adjacent:** elements outside the system that shape how users experience it (onboarding materials, training, contextual documentation, communication to users before and after they use the system, support processes)

2. **Apply design thinking to the configurable and adjacent layers.** For each configurable element, ask: does the current configuration serve the user's mental model and task logic, or is it still at the vendor's default? For adjacent elements, ask: are users entering this system with the context they need to succeed, and are they leaving it with the support they need when it breaks?

3. **Document the UX gaps in the fixed layer.** For each fixed design problem you've identified, write: what the user is trying to do, what the system makes them do instead, and what the measurable cost is (time, errors, workarounds, support requests). This documentation has two uses: it becomes the evidence for vendor escalation, and it becomes the rationale for future procurement decisions.

4. **Identify the escalation path.** For each documented gap, name who owns the relationship with this vendor and what the path is for surfacing design feedback. Gaps without an escalation path become organizational shrug — visible but unaddressable. A named path (even a slow one) keeps the gap actionable rather than resigned.

**Artifact:** A vendor constraint map — four sections:
1. What's fixed (with documented UX gaps and their costs)
2. What's configurable (with current configuration vs. recommended configuration)
3. What's adjacent (with current state and design opportunities)
4. Escalation path (who owns the vendor relationship, how to surface feedback)

**Watchout:** The most common failure mode in vendor software is treating the vendor's defaults as design decisions rather than starting points. Many configurable elements are left at vendor defaults by teams who didn't know they were configurable. Before concluding a layer is fixed, check the vendor documentation — specifically the administration and configuration sections — because what looks like a locked interface may have user-facing or admin-level customization that wasn't used at implementation.

**When You Can't Run the Full Version**

**If you can't produce the full constraint map:** Start with section 3 only — the adjacent layer. What happens before and after users interact with the system is usually entirely within your control, regardless of what the vendor locks. Better onboarding, better documentation, better support processes, and better expectation-setting often reduce the user impact of fixed design problems by more than the problems themselves would suggest.

**What you still get:** Reduced friction at the entry and exit points of the system, without touching the vendor interface at all.

**What you give up:** The systemic view of what's fixed, configurable, and adjacent — which means the configurable layer improvements don't get made, and the fixed layer gaps don't get documented for escalation.

**Don't do this:** Don't attempt to work around fixed design problems by training users to expect them. "That's just how the system works — you have to remember to click the second tab first" is a training-as-workaround pattern that absorbs user frustration without reducing it. Document the gap instead, set expectations explicitly, and pursue the escalation path.

**Try This:** Pick one design problem in a vendor system you're responsible for. Classify it: is it fixed, configurable, or adjacent? If configurable — what's the current configuration, and what would the configuration be if you optimized it for user task logic? If fixed — write one sentence about what the gap costs users: how often they encounter it and what they have to do as a result. That sentence is the start of your escalation documentation.

**Proof:** If the constraint map has at least one item in the "configurable" section that wasn't optimized at implementation — a label, a default, a module setting — the mapping exercise produced a design improvement opportunity that didn't require any vendor interaction. If every item is in the "fixed" section with no escalation path, either the map is incomplete (check configurable and adjacent again) or this system has been fully design-optimized at the available layers (unlikely for a recently implemented vendor system).

**Take this further:** In the next week, share the documented fixed-layer gaps with whoever owns the vendor relationship. Write one sentence: did they know these gaps existed and were being documented, or was the documentation new information to them? The answer tells you whether the gap has an active escalation path or whether building one is the next step.

**After you've run this yourself:** Share the documented UX gaps (what users are trying to do, what the system makes them do instead, what it costs) with an AI tool and ask it to generate possible workarounds at the configurable and adjacent layers. Treat the output as a starting prompt list — not a complete solution — since workarounds depend on specifics about your vendor's configuration options that AI doesn't have.

**What Next:** If the constraint map reveals systemic design debt in the vendor system, read 300 (Design Debt arc) for the habit of flagging and tracking debt over time — including the specific guidance for vendor contexts in the "When You Don't Control the System" section. If the gaps revealed suggest the system isn't fit for purpose, that's the beginning of a vendor evaluation conversation — which requires the documented gap evidence this method produces.
