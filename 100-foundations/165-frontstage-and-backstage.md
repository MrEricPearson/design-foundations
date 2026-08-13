# Frontstage and Backstage
**Tier:** 100 — Recognize | **Note:** Foundational prereq for 306 (Service Blueprint)

**Goal:** Recognize the frontstage/backstage distinction in any product or service — so you know what users see versus what enables what they see.

**Concept:** Frontstage is everything the user can see and interact with: the interface, the message, the output. Backstage is everything that makes the frontstage work: the systems, the teams, the data flows, the processes users never see. A frontstage problem that keeps coming back is usually a backstage problem that was never addressed.

**You'll see it when:** A user-facing issue keeps getting "fixed" at the interface level but returns. The fix is applied to what's visible; the cause lives in what isn't. Until the backstage is examined, the frontstage fix is treating the symptom.

**The signal:** If solving the problem requires changing something the user never sees — a system, a process, a data model, a team handoff — the backstage is involved. If the entire solution is visible in the interface, it's a frontstage fix.

**Don't confuse this with:** Frontend/backend in software architecture, which is a technical distinction. Frontstage/backstage is about user visibility, not code location. A backend computation that determines what a user sees is frontstage in effect if its output is what the user experiences. A frontend element that users never interact with because it's hidden by default is practically backstage. The question is: does the user perceive it?

**Try Noticing:** Think of a product you're working on. Pick one user-facing step and ask: what has to happen behind the scenes — in any system or team — for this step to work correctly? What you named is backstage. Its existence isn't visible to users, but its failure is.

**What Next:** When you're ready to map the backstage that supports a user's journey, read 306 (Service Blueprint). The blueprint is the tool for making backstage dependencies visible before they cause frontstage failures.
