# Layout System — Design Foundations Library

Reference for the write-piece skill. Read during the layout phase (Step 12) to map article sections to patterns and generate the companion `.publish.md`.

Full visual reference: [`meta/library-design-system.html`](library-design-system.html)

---

## Design tokens (abbreviated)

| Token | Value | Use |
|---|---|---|
| Ground | #F5F3EE | Page background |
| Accent | #3B5A9A | Concept panel, step numbers, links, accent chips |
| Amber | #E8A835 | Try This block only |
| Rust | #C4522A | Watchout block only |
| Text-1 | #1C1B18 | Body text, headings |
| Text-2 | #5A5750 | Section headings, secondary text |
| Text-3 | #9A9690 | Labels, metadata, secondary headings |
| Border | #D8D5CE | All dividers and borders |
| T100 badge | #6B82A8 | Tier badge, T100 pieces |
| T200 badge | #3A8A7A | Tier badge, T200 pieces |
| T300 badge | #3B5A9A | Tier badge, T300 pieces |

---

## Column layout (line length fix)

**Problem:** SharePoint's default single-column layout renders text at 90–110 CPL. Research target: 66 CPL (range: 50–75).

**Solution — Flexible Sections (no SPFx needed, mid-2025+):**
- Add section → Flexible section
- Drag left column to ~70% width
- Place all content web parts in the left column (~680px max-width)
- For T300 arcs: place arc navigation Quick Links in the right column
- For T100/T200: leave right column empty

**Fallback — 2-column layout (2/3 + 1/3):** Place all content in the wider column.

**Restricted tenant fallback:** Script Editor web part with `body { max-width: 680px; margin: 0 auto; }` if permitted.

---

## White space system (Spacer web part heights)

| Transition | Spacer height |
|---|---|
| Header (P1) → first section | 32px |
| Concept Panel (P3) → Step Sequence (P4) | 24px |
| Step Sequence (P4) → Watchout (P5) | 16px |
| Watchout (P5) → Try This (P6) | 32px |
| Try This (P6) → Proof (P7) | 0px (Divider only) |
| Proof (P7) → Take This Further | 24px |
| Any section → Source Attribution (P8) | 32px |
| Any section → What Next (P10) | 40px |
| Pull Quote (P11) → next section | 24px |

---

## Section heading hierarchy

Primary sections (Concept, Method, Try This, Watchout, Artifact, Goal): system-ui 700, text-2 color.  
Secondary sections (Prior Knowledge Hook, Trigger, Take This Further, AI Path, Source Attribution): system-ui 600, text-3 color.

Never use template section names in published text — rename each heading to describe its content.

---

## Pattern library

### P1 — Article Header
**Maps to:** Text web part (H1) + Divider  
**Contains:** Tier badge chip · Reading time chip · [Arc position chip — T300 only] · Piece number eyebrow · Title · Goal line (italic Georgia)  
**Rules:**
- Tier badge always first. Reading time chip always present: "4 min read" not "under 5 minutes."
- T300 arcs: arc position chip ("Part 2 of 5") in accent color, between tier badge and reading time
- Title names the recognizable situation, not the technique
- Goal line: one sentence, italic — the promise the piece keeps
- No author, no date, no subtitle

### P2 — Section Block
**Maps to:** Text web part  
**Contains:** Section heading (primary or secondary weight) + body prose  
**Rules:** One idea per section. Georgia body 16px/1.75, max 58ch. Heading weight signals section importance (see hierarchy above).

### P3 — Concept Panel
**Maps to:** Text → Quote or Highlighted (blue tint)  
**Contains:** Blue left border + tinted background + 1–3 sentence concept  
**Rules:** One per piece. The "ah" moment — opens with the situation, not a definition. Pull Quote (P11) typically follows.

### P4 — Step Sequence
**Maps to:** Text → numbered list  
**Contains:** Numbered steps, each one action  
**Rules:** Max 6 steps. Imperative verb opens every step. No explanation inside steps. Each step is one action — split at "and."

### P5 — Watchout Block
**Maps to:** Text → Highlighted (rust/red tint)  
**Contains:** "Watchout" label + paragraph  
**Rules:** One per piece. Names failure mode first. Personal register. Specific to this method.

### P6 — Try This Block
**Maps to:** Text → Highlighted or Banner (amber tint)  
**Contains:** "Try This — [N] minutes" label + prompt  
**Rules:** Most visually distinct block on the page. Names a specific artifact the reader has. Time estimate always present. 32px Spacer before this block.

### P7 — Proof Block
**Maps to:** Text + Divider web part above (not Spacer)  
**Contains:** "If It Worked" label + one sentence  
**Rules:** Immediately after Try This — no gap. One signal, one sentence. Achievable in same sitting.

### P8 — Source Attribution
**Maps to:** Text (compact, 13px) + Spacer (32px) + Divider above  
**Contains:** "Sources" label + source items  
**Rules:** Author + year + publication + specific finding (3 lines max per source). Minimum counts: T100 → 3, T200 → 4, T300 → 5 per arc.

### P9 — Image Block
**Maps to:** Image web part (Full-width setting)  
**Contains:** Image + caption + alt text (required)  
**Rules:** Only when it reduces cognitive load prose cannot. Flat style, no people, library palette. 1360×680px at 2x. Image spec required before production.

### P10 — What Next
**Maps to:** Quick Links or Text links  
**Contains:** Routing chips (1–3 links)  
**Rules:** 40px Spacer before. Chip text: piece number + title. Conditional routing only — never recaps. Min 44px touch height.

### P11 — Pull Quote (research-backed addition)
**Maps to:** Text → Quote style  
**Contains:** Bold top border + italic quote + hairline bottom border  
**Rules:**
- The quotable line required by the writing spec — this is its visual surface
- Placement: immediately after Concept Panel (P3) — captures F-pattern scanners before they reach Method
- Georgia italic 18px, max 52ch
- Bold top border (2px, text-1); hairline bottom border (1px, border)
- One per piece. 24px Spacer after.
- Not used in T100 pieces under 400 words

Research basis: Eye-tracking research shows pull quotes receive fixation before body text — they function as a second headline for scanner-first readers.

### P12 — Check-In (research-backed addition)
**Maps to:** Microsoft Forms (embedded) or Quick Poll web part  
**Contains:** One question + 3 response options  
**Rules:**
- Placement: after Proof (P7), before Take This Further
- One question: "Did you [verb from Try This]?"
- Three options: yes + finding | not yet | doesn't apply
- Required for T200 and T300 pieces. Optional for T100.
- Test in SharePoint mobile app separately from browser
- Link "yes" response to Take This Further channel where applicable

Research basis: Interactive elements increase time-on-task ~36% over static text. Also provides engagement data (completion signal).

---

## Section-to-pattern mapping by tier

### T100 — Recognize
| Section | Pattern |
|---|---|
| Goal | P1 (goal line in header) |
| Concept | P3 (Concept Panel) + P11 (Pull Quote, if piece ≥400 words) |
| You'll See It When | P2 (Section Block, secondary heading) |
| The Signal | P2 (Section Block, secondary heading) |
| Don't Confuse This With | P2 (Section Block, secondary heading) |
| Try Noticing | P6 (Try This Block) |
| Proof/Signal | P7 (Proof Block) |
| What Next | P10 (What Next) |

### T200 — Practice
| Section | Pattern |
|---|---|
| Goal | P1 (goal line in header) |
| Prior Knowledge Hook | P2 (secondary heading) |
| Trigger | P2 (secondary heading) |
| Concept | P3 (Concept Panel) + P11 (Pull Quote) |
| Method | P4 (Step Sequence) |
| Artifact | P2 (primary heading) |
| Watchout | P5 (Watchout Block) |
| Try This | P6 (Try This Block) |
| Proof | P7 (Proof Block) |
| Check-In | P12 (Check-In) |
| Take This Further | P2 (secondary heading) |
| AI Path (optional) | P2 (secondary heading) |
| Source Attribution | P8 |
| What Next | P10 |

### T300 — Orchestrate
Arc header: P1 (with arc position chip).  
Each arc part: P2 (part heading, primary) → P3 (Concept Panel) → P4 (Step Sequence) → P2 (what you end up with) → P7 (Proof) → P5 (Watchout).  
Arc footer: P6 (Try This) → P12 (Check-In) → P2 (Take This Further) → P2 (Judgment Exercise) → P10 (What Next).  
T300 pages: right column navigation listing all arc parts as Quick Links.

---

## Image spec format

```
IMAGE-SPEC
id:           img-001
piece:        [piece-id]
placement:    [after-concept | after-method | after-header | etc.]
purpose:      [one sentence — what cognitive work this image does]
dimensions:   1360x680px (display at 680x340 — 2x for Surface Pro retina)
style:        Flat illustration, no shadows, no people, no gradients, no 3D
palette:      Ground #F5F3EE, Accent #3B5A9A, Amber #E8A835, Text #1C1B18
alt-text:     [full description for screen readers]
gemini-prompt:
  "[Complete Gemini Imagen prompt — must specify: background hex, palette hex values,
  exact visual content, style constraints (no people, flat, no shadows, no gradients),
  dimensions, aspect ratio]"
```

If Gemini results are off: add "vector illustration style, like an editorial icon set" to the prompt and retry.

---

## Mobile and touch rules

- Touch target minimum: 44×44px for all chips, links, and Check-In options
- Body type: never below 16px desktop (renders ~14px in SharePoint mobile — acceptable)
- Color blocks (P3, P5, P6): test in SharePoint mobile app after publishing — rendering differs from desktop
- Two-column layout stacks to single-column on mobile — right navigation column disappears; confirm it contains only navigation links, not content
- Images: set Image web part to "Full width" for mobile scaling
- P12 Check-In: test Forms web part in SharePoint mobile app, not just mobile browser

---

## Companion publish doc format

Every piece generates a `[piece-id].publish.md` at the same folder level as the draft.

```markdown
# Publishing Guide — [Piece ID]: [Title]

## Layout map
| Section | Pattern | SharePoint web part | Notes |
|---|---|---|---|
| [section name] | P[n] | [web part name] | [notes] |

## Spacer schedule
[List each Spacer location and height per the white space system]

## Images
[IMAGE-SPEC blocks — one per image in the piece]

## Check-In question
[The exact question and three response options for P12]

## Publishing checklist
- [ ] Column layout: Flexible Section with content column ~680px
- [ ] Title in H1 — names situation, not technique
- [ ] Reading time chip present (tier badge row)
- [ ] Arc position chip present (T300 only)
- [ ] Concept Panel: blue tint applied
- [ ] Pull Quote: present immediately after Concept Panel
- [ ] Try This Block: amber tint applied, 32px Spacer before
- [ ] Watchout Block: rust tint applied
- [ ] Proof Block: Divider (not Spacer) above, no gap from Try This
- [ ] Check-In: embedded form present, tested in mobile app
- [ ] All images uploaded at 1360x680px, alt text present, Full-width setting
- [ ] What Next links verified and working, 40px Spacer before
- [ ] Source attribution block present
- [ ] All Spacer heights set per white space schedule
- [ ] Page reviewed in SharePoint mobile app
- [ ] Piece linked from LIBRARY-MAP and relevant Start Here docs
```
