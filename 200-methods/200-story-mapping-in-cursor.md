# Story Mapping in Cursor
**Tier:** 200 — Practice | **Arc:** Full arc (5 parts) | **Prereqs:** 106 (sketching), 107 (framing), 109 (weighing tradeoffs); pairs with 147 (AI as Execution Partner) | **Tool note:** The method in this arc is tool-agnostic — the five parts work with sticky notes, a whiteboard, Miro, a spreadsheet, or any shared doc. The "Cursor" in the title refers to using Cursor as the shared working environment for the AI-assisted layer in "After you've run this yourself." If you're not using Cursor: run the backbone (Part 1) and steps (Part 2) in any shared doc or whiteboard tool, use AI to generate a first-pass backbone via any AI chat tool, and walk the map with another person in whichever tool you both have open.

**Goal:** After this arc, you will be able to map a complete user journey from backbone to MVP slice — in a working file, with another person's input — before breaking anything into tickets.

**Prior knowledge hook:** Think of the last time a sprint or release contained work that felt disconnected — individual tickets that were technically done but didn't add up to something a user could actually complete. That's the gap story mapping addresses.

**Trigger:** you're about to break a feature into tickets without a shared picture of how all the work fits together first.

**Why this works:** stories mapped to a user journey stay grounded in the user's actual path — the map makes gaps and dependencies visible before any ticket exists, so decisions about scope are made against what the user needs rather than what seems buildable.

---

## Part 1: Mapping the Backbone

Before breaking anything into tickets, map the shape of what people actually do — the big activities, in the order they happen.

**Method:**
1. List the major activities someone goes through to accomplish their goal, left to right, in sequence.
2. Keep it high level — verbs, not features. "Finds a product," not "clicks the search bar."
3. Stop once you've covered the full journey, start to finish.

**What you end up with:** a single row of activities — the backbone of the map everything else builds on.

**Proof:** If the backbone can be written as a sequence of verb phrases that someone unfamiliar with the project can follow start to finish, it's working. If it can't — if it assumes knowledge or skips steps — the gap is visible in the row, not buried in a ticket.

**Watchout:** map what people actually do today, not the aspirational process you wish they followed.

---

## Part 2: Breaking Activities Into Real Steps

Each backbone activity is really a handful of smaller steps. This is where the map starts to get useful.

**Method:**
1. Under each backbone activity, list the concrete steps someone takes to complete it.
2. Stay at the level of "what they do," not "what we'll build" — that comes later.
3. Don't worry about being exhaustive yet — capture the obvious steps first.

**What you end up with:** a second row under your backbone, showing the real steps inside each activity.

**Proof:** Each step should be expressible as something a person does, not something a system does. If a step can only be written as "system processes X," it's a technical detail, not a user step — and it belongs elsewhere.

**Watchout:** going too granular too early kills momentum. Stay loose here — you can always add detail later.

---

## Part 3: Adding the Detail Layer

Now add the variations, edge conditions, and specifics under each step — the "walking skeleton" that makes the map feel real instead of idealized.

**Method:**
1. For each step, note the different ways it might actually happen (a returning user vs. a new one, a happy path vs. an error).
2. Keep each note short — a phrase, not a paragraph.
3. This is still a first pass, not a final spec.

**What you end up with:** a fuller map that captures real variation, not just the ideal path.

**Proof:** The detail layer is working when the map feels slightly uncomfortable — when you've added at least one variation you weren't originally planning to handle. An idealized map has no variations. A real one does.

**Watchout:** don't chase completeness here. This is a working draft, not the final map — perfectionism at this stage just delays the more useful step next.

---

## Part 4: Slicing Your MVP Line

Now decide what's truly necessary for a first release versus what can wait. This is a risk decision, not just a scope cut.

**Method:**
1. Draw a horizontal line across your map.
2. For everything above the line: ask what happens if we ship without it — is that a real, tolerable risk, or does the whole thing fail without it?
3. Adjust the line based on that answer, not based on what fits a deadline.

**What you end up with:** a release scope grounded in actual risk, not just arbitrary time pressure.

**Proof:** For each item above the line, the question "what happens if we ship without this?" should have a tolerable answer. If any item above the line can't pass that check, the line needs to move — and now you know exactly where and why.

**Watchout:** the line is a risk decision, not a deadline-driven scope cut — if you're only slicing to hit a date, you're not using this tool the way it's meant to be used.

---

## Part 5: Walking the Map With Someone Else

A map you built alone only reflects what you already know. Walking it with someone else is where you find out what you missed.

**Method:**
1. Pick someone who'll actually push back — not just nod along.
2. Walk them through the map, activity by activity, and ask where it doesn't match their experience.
3. Update the map based on what surfaces.

**What you end up with:** a map that's been stress-tested by at least one other perspective before you build on it.

**Proof:** A walk-through that produces zero pushback means you chose the wrong person to walk it with. One that produces at least one update means the map is already more accurate than it was. The update is the proof — not the session itself.

**Watchout:** a nodding colleague isn't validation. Choose someone likely to disagree with at least part of it.

**Try This:** open a file right now and write the backbone for something you're currently working on — just the activity row, in sequence, left to right. Stop at 10 activities. Does it cover start to finish?

**After you've run this yourself:** describe the user's goal and context to an AI tool and ask it to generate a first-pass backbone of activities — then review it against what you know actually happens, correct anything that doesn't match, and walk Part 2 yourself.

**Take this further:** in the next week, use the map you built to run a grooming session. Afterward, write one sentence: what did the room change that the map got wrong? That delta is the map's most honest feedback.

**What Next:** once you have a slice and a stress-tested map, take it to 201 (Grooming with AI) to turn it into properly scoped tickets.
