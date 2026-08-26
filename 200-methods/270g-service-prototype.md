# Testing the Seams Before They Break
**Tier:** 200 — Practice | **Arc:** Prototyping (309) | **Prereqs:** 177 (What a Prototype Is), 132 (Prototype Fidelity), 113 (Defining Success Before You Start) | **Audience:** General

*Every step worked. The journey failed anyway.*

---

Someone calls the support line and gets the right answer. They navigate the app and submit the form correctly. They receive the confirmation email on time. Three weeks later, they call again: the thing they submitted never happened.

Every touchpoint succeeded. Nothing carried forward.

---

You've probably run prototypes before — screens connected in sequence, someone clicking through. That works when the experience lives in one place. This method is for when it doesn't.

Use this when you're designing something that spans digital and non-digital touchpoints. An onboarding flow that includes a phone call. A request that moves through three systems. A purchase that requires someone in another department to do something specific before the user's next step can happen. When the experience depends on information moving between places — and you need to know whether those handoffs will actually work before the first real user hits them.

---

Shostack (1984) formalized the problem in Harvard Business Review: most service failures don't happen where users see them. They happen backstage, in dependencies users never observe. The checkout works. The warehouse can't fulfill it. The user experiences delay. Where things break and where failures appear are different places.

Bitner, Ostrom, and Morgan (2008) later extended this into a full design framework at Arizona State's service research institute: service blueprinting forces visibility into everything behind the interface — the handoffs, the information transfers, the dependencies that must resolve for the frontstage experience to hold together. The mechanism is explicit: draw what happens backstage and where it touches what users see. Failures live at those connection points.

Forlizzi and Battarbee (2004) described why prototyping services is harder than prototyping products: a product prototype sits in front of you. A service prototype requires enacting a series of moments in time. You're not testing whether one thing works. You're testing whether the sequence holds when time passes and people hand things off. That's the question service prototypes answer.

Stickdorn and colleagues (2018) gave this definition: a service prototype tests the orchestration. The individual moments might all function. What's unvalidated is whether they connect. A person could succeed at every individual step and still fail at the journey if one handoff loses information or timing falls out of sync.

The wrong model: prototyping is for interfaces. That's where it breaks. The interface is one moment. The service is the whole sequence. Testing one screen at a time misses the seams.

---

1. Map the full journey as written. List every touchpoint the user encounters from start to finish, across all channels. Email, app screen, phone call, physical location, paper form. Include wait states: "User waits 2 days for approval." The map includes everything, not just what you control.

2. Add the backstage layer. Below each user-facing touchpoint, write what must happen behind it for that moment to work. When a user submits a form, someone reviews it. When they receive a confirmation, a system generated it based on data from another system. Write those dependencies explicitly. This is the blueprint: frontstage on top, backstage below.

3. Mark the handoffs. Draw a line connecting each place information moves from one system, person, or channel to another. Label what's being transferred: "approval decision," "user's equipment request," "account number." Those lines are the failure points. Shostack's finding holds: if the service breaks, it breaks at a line, not at a box.

4. Build the minimum enactment. Pick the riskiest handoff — the one where you're least confident information will transfer correctly or timing will hold. Prototype just that segment: the two touchpoints it connects and the backstage dependency between them. Use whatever makes it real enough to test. A real email. A spreadsheet standing in for a system. A phone call. If the user would wait three days, compress it to three minutes but keep the waiting period. The enactment includes time passing.

5. Run it with roles. One person plays the user, another plays each backstage role. Walk through the segment. The user acts, the backstage person responds based only on what the handoff gave them. Stop when something doesn't carry forward. Document it: what information was expected that didn't arrive? What timing assumption broke?

6. Fix the handoff, then extend. Redesign the transfer so the missing piece gets captured or communicated. Re-run that segment. If it holds, prototype the next handoff. Repeat until the full journey is enacted end to end without a break.

---

What you end up with: a blueprint showing every touchpoint and dependency, and a documented list of handoff failures you found and fixed before anyone built the real service. The artifact is the blueprint with annotations: "Fixed: approval decision now includes equipment type" or "Added: confirmation email tells user what happens next and when."

Blomkvist (2014) compared service prototypes to product prototypes at Linköping University and found that service prototypes must be evaluated through enactment — walking through time — because service quality emerges from sequencing and timing, not from static inspection. You can't look at a service blueprint and know it works. You have to run it.

---

The failure mode that catches teams who've prototyped interfaces before: building the frontstage touchpoints in high fidelity before testing whether the backstage can actually support them. The screens look polished. The user journey appears complete. Then someone runs it and discovers the confirmation email can't be generated because two systems don't share the field it needs to display. High-fidelity frontstage with untested backstage dependencies produces a prototype that looks finished and can't be built. Test the seams before you polish what they connect.

---

Take something you're working on now that crosses at least two systems or involves a handoff to another person. Map the user's journey: every touchpoint, frontstage. Add the backstage layer: what must happen behind each moment for it to work? Mark one handoff where you're not completely confident the information will transfer cleanly. Prototype just that handoff with a colleague: one of you is the user, one is the system or person on the other side. Use a real email, a shared doc, whatever makes it concrete. Run it. Note what didn't carry forward.

This takes about 45 minutes to map and 20 minutes to enact one segment.

---

If you discover something that should transfer but doesn't — a field, a decision, a piece of context — the prototype worked. That's the finding: the handoff needs redesign before it's built. One thing to watch: the person playing the backstage role filling in gaps with knowledge they have from outside the prototype. "Oh, I'd just assume that means X." The real system won't assume. Constraint the backstage player: they only know what the handoff explicitly gave them.

---

Over the next week, pick one more handoff from the same journey. Map it, enact it, document what breaks. Then write one sentence: what pattern do the two handoff failures share? If both broke because of missing context, that's a design rule for every handoff in this service. If both broke because timing wasn't explicit, every touchpoint needs to tell users what happens next and when.

---

After you've run this yourself: AI can generate the first-draft blueprint from a journey description. Describe the user's path across touchpoints, ask the tool to map likely backstage dependencies and flag handoffs where information might not transfer cleanly. Use that as the starting map, then validate it by enacting the flagged segments. The AI won't catch everything — backstage dependencies are specific to your systems — but it'll surface the handoffs worth testing first.

---

When the service prototype reveals that one touchpoint isn't clear about what the user should do next, 205 (Content Design) covers how to write interface copy that sets expectations across time. If timing dependencies are the issue — users waiting without knowing what's happening — 120 (Performance and Perceived Speed) addresses how to make wait states feel deliberate instead of broken. When you're ready to test the full enacted service with a real user, 215a (Moderated Usability Session) applies to service walkthroughs just as it does to interface testing.

---

**Sources**

Bitner, M. J., Ostrom, A. L., & Morgan, F. N. (2008). Service blueprinting: A practical technique for service innovation. *California Management Review, 50*(3), 66–94. Finding: Service blueprinting forces visibility into backstage processes and their connection points with frontstage customer touchpoints. Failures consistently occur at the interface between what customers see and the support processes that must function behind them.

Blomkvist, J. (2014). *Representing future situations of service: Prototyping in service design* [Doctoral dissertation, Linköping University]. Finding: Service prototypes must be evaluated through enactment rather than inspection because service quality emerges from sequencing and timing across touchpoints. Static examination of a service blueprint cannot reveal whether the orchestration will hold under real conditions.

Forlizzi, J., & Battarbee, K. (2004). Understanding experience in interactive systems. *Proceedings of the 2004 Conference on Designing Interactive Systems*. ACM. Finding: Product prototypes can be physically examined. Service prototypes require enactment across time because services are experienced as sequences of interactions, and the quality of the whole depends on how individual moments connect when time passes and roles hand things off.

Shostack, G. L. (1984). Designing services that deliver. *Harvard Business Review, 62*(1), 133–139. Finding: Service failures consistently occur in backstage dependencies — the operational processes and information transfers that support customer-facing moments — not in the frontstage touchpoints where failures become visible to users.

Stickdorn, M., Hormess, M. E., Lawrence, A., & Schneider, J. (2018). *This is service design doing*. O'Reilly Media. Finding: A service prototype tests orchestration rather than individual touchpoints. Users may succeed at every discrete interaction and still experience failure if handoffs lose information, timing breaks, or dependencies don't resolve correctly between moments.
