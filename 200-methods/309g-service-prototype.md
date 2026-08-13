# Service Prototype
**Tier:** 200 — Practice | **Arc:** 309 (Prototyping) | **Prereqs:** 177, 132, 113 | **Wave:** 4

**Goal:** Run a service prototype session that tests the end-to-end user experience across digital and non-digital touchpoints — at a moment when the digital interface alone can't answer the question.

**Prior Knowledge Hook:** The frame most practitioners bring to prototyping: we're testing the interface. The interface is the design. The test tells us whether the design works. This frame is accurate for products where the complete user experience is contained in the digital interface. It fails for services, where the experience spans the interface plus human interactions, physical environments, wait times, support flows, and cross-channel handoffs. In these contexts, testing the interface alone is like testing one act of a three-act play and declaring the play ready.

**Trigger:** Use a service prototype when: the user's full journey includes interactions outside the digital product (phone calls, physical visits, email exchanges, third-party handoffs); when the failure mode you're trying to prevent involves breakdown at the seams between touchpoints (the user knows how to use the app, but the app leads them to a process that fails them); or when users report satisfaction with individual touchpoints but dissatisfaction with the overall experience. The service prototype tests the seams.

**Why this works:** Most user experience failures in service contexts don't happen within touchpoints — they happen between them. The app works. The email confirmation arrives. The support rep is helpful. But the information in the email contradicts what the app shows. The support rep can't see what the app displays. The physical location doesn't know what the online system promised. These seam failures cannot be tested by any prototype that tests a single touchpoint in isolation — they require staging the full journey and observing what happens where the handoffs occur.

The mechanism: service prototypes expose the hidden communication assumptions between touchpoints. Every seam in a service journey is a communication protocol: touchpoint A assumes touchpoint B knows X; touchpoint B assumes the user already has Y; the system assumes a time window that the physical environment makes impossible. Making these assumptions explicit by staging the full journey reveals which ones are wrong before building the supporting infrastructure.

**Method:**

**Step 1: Map the service journey end to end.** Identify every touchpoint a user encounters from initial trigger to final resolution. For each touchpoint: what channel (digital, phone, physical, email), what the user needs, what the service provides, and what carries from this touchpoint to the next. This is your service blueprint at prototype fidelity.

**Step 2: Identify the seams.** Mark every point where information, intent, or context must transfer from one touchpoint to another. These are the highest-risk points in the service. If the information transfer fails (or never happens), the user experience at the next touchpoint degrades. Circle these seams — they are the primary test targets.

**Step 3: Assign roles to the service team.** Each touchpoint needs a person or resource to represent it in the prototype session. Digital interfaces: use an existing prototype or the live system. Phone or human interactions: a team member plays the role, scripted. Physical environment: staged or described. Each role-player knows their script and, critically, knows what information they're supposed to receive from the previous touchpoint and what they're supposed to pass forward.

**Step 4: Run the user through the full journey.** The user experiences the service as if it were real — as close to real as you can stage. Facilitator follows alongside. Do not interrupt the journey; observe what happens at each seam. Does the information transfer? Does the user have to repeat themselves? Does anything break between touchpoints?

**Step 5: Debrief at the seams.** After the session, focus analysis on every seam: was the information transferred correctly? Did the user experience continuity or disruption? Did the role-playing service team have what they needed to serve the user? Each seam failure is a design gap in the service infrastructure.

**Artifact:** An annotated service journey map showing: what worked at each touchpoint, what broke at each seam, and what information assumptions were revealed as wrong. These findings are the design requirements for the service layer — the infrastructure, communications, and protocols that support the digital interface.

**Watchout:** The failure mode that is almost universal in service prototype sessions: the prototype becomes a demo of how it's supposed to work rather than a test of whether it does. Role-players know the designed protocol. The user, playing along cooperatively, follows the designed flow. Nobody breaks. The session passes. The actual seam failures — the ones that happen when users don't cooperate with the designed protocol, or when the information transfer fails in real conditions — aren't revealed because the session is too clean. Real service prototypes require real complexity: unpredictable users, constrained role-players, and deliberate attempts to surface the assumptions that break.

**Try This:** Think of a product or service you work on that involves at least one touchpoint outside the digital interface — a phone call, an email, a physical step. Map the journey end to end for one user scenario. Identify the two seams you trust least — the handoffs where you suspect information doesn't transfer reliably. What would a 30-minute staged test of those two seams look like? What would you need to stage and what would you learn?

**Proof:** The service prototype worked if you found at least one seam failure you did not already know about. The false positive: a session where every seam worked as designed, because the role-players and user were all cooperating with the design. A service prototype that reveals no gaps is almost always a staged demonstration rather than a genuine test. Real service journeys have friction; a prototype that produces no friction either eliminated real failure modes (the design is exceptional) or eliminated the conditions that produce failure modes (the staging was too cooperative).

**Take This Further:** Over the next week, audit one failure or complaint in a service you work on. Trace it back to its seam: which handoff failed, what information was missing, and what assumption was wrong? Write one sentence: what would have been required in the service prototype to surface this failure before it happened to a real user?

**After you've run this yourself:** AI can help map the information that must transfer at each seam — describe the service journey and ask what data, context, or confirmations each touchpoint needs to receive from the previous one. Use this checklist to verify your service blueprint before running the prototype.

**What Next:** Service prototypes test the full journey. When the question is specifically about what happens when multiple design directions are explored simultaneously before committing to one, read 309h (Parallel Prototyping). When you need to prototype quickly to understand a technical or interaction constraint by building it, read 309i (Build to Think).
