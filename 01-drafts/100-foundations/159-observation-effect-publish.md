# 159 Observation Effect — Publish Layout Map

**Piece ID:** 159-observation-effect.md  
**Tier:** T100 Recognize  
**Format:** Standalone atom  
**Target length:** ~1000 words (actual: 1,040 words)  
**Prereq chip:** "Builds on: [157 Why You Don't Help During Testing](157-why-you-dont-help-during-testing.md)"

---

## Layout Annotations

### Header Block
- **Title:** Notice When Being Watched Changes How Someone Acts
- **Subtitle/Goal line:** Recognize when observation itself changes participant behavior during testing
- **Prereq chip placement:** Below title, above first paragraph
  - Text: "Builds on: [157 Why You Don't Help During Testing](157-why-you-dont-help-during-testing.md)"
  - Style: Blue info chip, left-aligned

### Body Structure

**Opening (Concept)** — Paragraphs 1-3
- Opens in the moment: participant being too careful during testing
- Defines observation effect: behavioral shift from being watched, not facilitator influence
- Anchors to Mayo's Hawthorne studies (1920s) as source credibility
- Distinguishes from observer bias immediately
- Connects to Nielsen's usability methodology
- Visual break: `---` horizontal rule before "You'll see it when"

**You'll See It When** — Paragraph 4
- Single paragraph, no header
- Names the situation: testing with awareness of observation
- Visual break: `---` horizontal rule after

**The Signal** — Paragraphs 5-6
- Two concrete signals: apologizing/explaining, and narrating everything
- Real-user behavior contrast embedded in each signal
- Visual break: `---` horizontal rule after

**Don't Confuse This With** — Paragraphs 7-9
- Three-paragraph disambiguation section
- Para 7: observation effect vs. observer bias (action vs. presence)
- Para 8: How to tell them apart (concrete test)
- Para 9: observation effect vs. social desirability bias (doing vs. saying)
- Visual break: `---` horizontal rule after

**Try Noticing** — Paragraphs 10-12
- Three observational prompts, each building on previous
- Para 10: apologies and retries (observed vs. natural behavior gap)
- Para 11: narration as performance indicator
- Para 12: session arc — relaxation vs. sustained performance
- Visual break: `---` horizontal rule after

**What Next** — Paragraph 13
- Conditional routing with two paths
- Path 1: caught observation effect in real session → 215a (moderated usability session)
- Path 2: haven't run test yet → 157 (observer bias)
- Both paths hyperlinked
- Visual break: `---` horizontal rule after

**Sources Block** — End matter
- Three sources, APA citation format
- Mayo (1933): Hawthorne studies, original observation effect documentation
- Nielsen (1993): think-aloud protocol, usability methodology authority
- Webb et al. (1966): reactivity and nonreactive research, behavioral research foundation
- Style: Standard reference block, gray background or indented

---

## Visual Design Notes

**Blue panel treatment:** Opening paragraph (the "you're watching someone" moment) could be pulled into a blue highlight panel if visual emphasis needed — but not required. The narrative flow works as continuous prose.

**Amber block treatment:** None needed. "Don't Confuse This With" section has enough weight in prose; visual highlighting would over-emphasize.

**Horizontal rules (`---`):** Six breaks total, marking template boundaries:
1. After Concept (para 3) → before You'll See It When
2. After You'll See It When (para 4) → before The Signal
3. After The Signal (para 6) → before Don't Confuse This With
4. After Don't Confuse (para 9) → before Try Noticing
5. After Try Noticing (para 12) → before What Next
6. After What Next (para 13) → before Sources

**Hyperlinks:**
- All "What Next" routing links active
- All source citations in Sources block formatted as hanging indent
- Prereq chip in header links to piece 157

---

## Template Element Compliance Check

| Element | Present | Location |
|---------|---------|----------|
| Goal | ✓ | Header subtitle line |
| Concept | ✓ | Paragraphs 1-3 |
| You'll see it when | ✓ | Paragraph 4 |
| The signal | ✓ | Paragraphs 5-6 |
| Don't confuse this with | ✓ | Paragraphs 7-9 (three-part disambiguation) |
| Try Noticing | ✓ | Paragraphs 10-12 (three observational prompts) |
| What Next | ✓ | Paragraph 13 (conditional routing, two paths) |
| Sources (min 3) | ✓ | Mayo 1933, Nielsen 1993, Webb et al. 1966 |

---

## Cross-Reference Map

**Incoming prereqs:**
- 157-why-you-dont-help-during-testing.md (observer bias — facilitator influence)

**Outgoing connections:**
- 215a-moderated-usability-session.md (T200 method, uses observation effect mitigation techniques)
- Referenced in What Next conditional routing

**Testing branch position:**
- Part of Testing concept cluster
- Follows 157 (observer bias)
- Feeds into 215a (moderated session method)

---

## Publish Checklist

- [ ] Prereq chip placed and linked
- [ ] All What Next paths hyperlinked to correct files
- [ ] Six horizontal rule breaks preserved in layout
- [ ] Sources block formatted with hanging indent
- [ ] Title and subtitle match exactly as written
- [ ] No section headers added (narrative flow only)
- [ ] Visual design (blue panel / amber block) applied per notes above
- [ ] Cross-reference map confirmed against 10-master-outline.md
- [ ] Word count noted in metadata (1,040 words)
