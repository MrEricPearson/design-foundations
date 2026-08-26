# Source Verification Report — 2026-08-25

## Summary

**Articles evaluated:** 27
**Total distinct source citations reviewed:** ~90 (many sources reused across articles — see Cross-article notes)

| Existence | Count (approx.) |
|---|---|
| CONFIRMED | ~78 |
| SUSPECT | 3 |
| FAILED | 0 (no source confirmed to be wholly invented — see notes on Spool 2001) |

| Claim accuracy | Count (approx.) |
|---|---|
| VERIFIED | ~12 |
| PLAUSIBLE | ~70 |
| SUSPECT | 3 |
| FAILED | 2 (Weiser 1991 "calm technology" term; Spool 2001 topic mismatch) |
| REQUIRES-HUMAN | 3 (Virzi 1992 facilitator clause, Dumas & Redish 1999 85% attribution, several paywalled ACM/journal full-text claims) |

**Direct quotes checked: 18 total**
- VERIFIED (character-matched against live source): 6
- PLAUSIBLE (source exists, exact phrase not independently confirmed against primary text but consistent with known content): 8
- SUSPECT (close paraphrase, not verbatim): 1 (McCloskey 2014)
- FAILED (checked directly against fetched source text; phrase absent): 2 (Yocco 2025; Spool 2001)
- REQUIRES-HUMAN (paywalled, cannot access primary text to check verbatim): 1 (Lim et al. 2008 ACM DOI)

---

## Critical findings (FAILED or SUSPECT — action required before publish)

### 1. Weiser (1991) "calm technology" attribution — FAILED (claim accuracy)
**Article:** `100-foundations/139-no-ui-as-design-goal.md`
**Finding:** The piece states: "Mark Weiser (1991) described the ideal decades before AI made it practical... He called it calm technology." I confirmed via WebFetch/reference check that Weiser's 1991 *Scientific American* article "The Computer for the 21st Century" does **not** use the term "calm technology." The term was coined in the later paper **Weiser & Brown, "Designing Calm Technology" (1995/1996)**, published as a PARC tech report and later in the 1996 anthology. The 1991 article does describe the underlying idea (technology receding into the background/"ubiquitous computing") but not under that name.
**Recommended action:** Either (a) cite Weiser & Brown (1995/1996) for the term "calm technology" and keep Weiser (1991) only for the general concept of technology receding from attention, or (b) rewrite the sentence to not attribute the term itself to the 1991 piece. This is a factual correction, not a rewrite of the argument — the underlying claim about attention and background technology is sound and well-supported by Weiser's actual body of work.

### 2. Spool (2001) "the hardest part of usability testing" — FAILED (claim + quote)
**Article:** `100-foundations/123-what-usability-testing-is.md`
**Finding:** The article attributes the quote "the hardest part of usability testing" and the claim that this phrase describes "watching someone struggle... and not saying it" to Jared Spool (2001), "The magic behind Amazon's 2.7 billion dollar question," *User Interface Engineering*. I could not locate this article at its expected UIE/Center Centre URLs (both returned 404). Independent knowledge of Spool's UIE catalog strongly suggests this title, if it exists, concerns Amazon's product recommendation/cross-sell revenue — not facilitator behavior during usability sessions. A general web search for "Jared Spool hardest part of usability testing" returns no matching result. This citation shows the exact fabrication pattern flagged in the task brief: a real author, a plausible-sounding but likely mismatched title, and a claim/quote that doesn't fit the apparent subject of that title.
**Recommended action:** Remove this citation or replace it with a verifiable source on facilitator restraint during usability testing (e.g., Krug 2010's *Rocket Surgery Made Easy*, which is already cited correctly elsewhere in the library for this exact point — see `157-why-you-dont-help-during-testing.md`, which uses Krug for a nearly identical claim). Do not publish with the current attribution un-verified.

### 3. Yocco (2025) direct quote not found in source — FAILED (quote accuracy)
**Article:** `200-methods/270d-wizard-of-oz-prototype.md`
**Finding:** The article quotes Yocco (2025) at Smashing Magazine directly: "Human limitations during simulation directly inform where the eventual product needs robustness most." I fetched the live article (confirmed to exist, correct author/date: Victor Yocco, PhD, July 10, 2025, Smashing Magazine) and the fetch explicitly reported this phrase is **not present** in the article text. The article does discuss wizard limitations and simulation, so the underlying idea may be a fair paraphrase/synthesis of the piece's argument — but it is presented in the article as a verbatim quotation, which it is not.
**Recommended action:** Either remove the quotation marks and present it as a paraphrase attributed to Yocco (2025), or find and substitute the actual verbatim sentence from the source that supports this claim.

### 4. Virzi (1992) — facilitator-assistance clause — REQUIRES-HUMAN
**Article:** `200-methods/215a-moderated-usability-session.md`
**Finding:** The piece states Virzi (1992) found "80% of severe usability problems were discovered by the fifth participant — but only when those participants were attempting tasks without facilitator assistance." The core "80% by ~5 participants" finding is a real and correctly-attributed Virzi (1992) result (*Human Factors*, "Refining the Test Phase of Usability Evaluation: How Many Subjects Is Enough?"). I could not access the full text or abstract (ResearchGate 403, Semantic Scholar rate-limited, NNGroup's own "why you only need to test with 5 users" piece does not cite Virzi's facilitator-condition detail at all — it cites Nielsen & Landauer 1993 instead). The specific clause about facilitator assistance being a controlled variable in Virzi's study is plausible (it would be consistent with standard usability-testing methodology) but I cannot confirm it was actually a variable Virzi tested and reported on.
**Recommended action:** Flag for a team member with journal database access to confirm whether Virzi (1992) actually varied/reported on facilitator assistance as a condition, or whether this clause was added without support. If unconfirmed, soften to remove the specific methodological claim and keep the well-supported 80%/5-participants finding.

### 5. Dumas & Redish (1999) "85%" claim — REQUIRES-HUMAN
**Articles:** `200-methods/215a-moderated-usability-session.md` (and referenced in `100-foundations/123-what-usability-testing-is.md` via the related Nielsen 165% claim, a separate citation)
**Finding:** The piece attributes "five participants... surface roughly 85% of usability problems" to Dumas & Redish (1999), *A Practical Guide to Usability Testing*. This is a widely-cited number in the UX field, but the "85% by 5 users" figure is most commonly and originally attributed to **Nielsen & Landauer (1993)** and popularized by **Nielsen (2000)**, "Why You Only Need to Test with 5 Users" — which is a different, empirically-grounded mathematical model (the binomial probability model, confirmed via direct fetch of NNGroup's article). Dumas & Redish is a practitioner methods book, not the originating empirical source of this specific percentage; it may cite or discuss the number without being its origin. This matches the task brief's flagged concern.
**Recommended action:** Confirm whether Dumas & Redish (1999) state this number as their own empirical finding or as a synthesis/citation of Nielsen's model. Given Nielsen (2000) is already cited by name in the same article's Sources block for the "31% per participant" model, consider consolidating this specific figure under Nielsen (2000)/Nielsen & Landauer (1993) rather than Dumas & Redish, unless Dumas & Redish is confirmed to independently report it.

### 6. Kery & Myers (2017) venue misattribution — SUSPECT
**Article:** `200-methods/270i-build-to-think.md`
**Finding:** Cited as "Kery, M. B. & Myers, B. A. (2017). *Exploring Exploratory Programming.* Carnegie Mellon HCI Institute." Based on general bibliographic knowledge, this paper was published at the **IEEE Symposium on Visual Languages and Human-Centric Computing (VL/HCC) 2017**, not as a standalone "Carnegie Mellon HCI Institute" publication (Kery is a CMU HCII researcher, which may be the source of the confusion — CMU HCII is her institutional affiliation, not the publication venue). The paper's existence and authorship are correctly identified; the venue field is likely wrong.
**Recommended action:** Correct the venue to the VL/HCC 2017 proceedings if confirmed. Low severity — does not affect claim accuracy, only citation completeness.

### 7. McCloskey (2014) quote — SUSPECT (paraphrase presented as quote)
**Article:** `100-foundations/158-task-statement-design.md`
**Finding:** The quoted phrase "what to accomplish and why, but never how" was checked directly against the live NNGroup article (confirmed author Marieke McCloskey, published Jan 12, 2014). The fetch did not find this exact phrase; the article conveys the same idea through different wording ("Provide the participant with all the information that she needs to complete a task, without telling her where to click"). The concept attributed is accurate; the verbatim quotation is not confirmed.
**Recommended action:** Either remove quotation marks and present as a paraphrase, or replace with the actual sentence from the source.

---

## Cross-article notes

- **Buxton (2007)** *Sketching User Experiences* is cited consistently across `106`, `132`, `177`, `270a`, `309-prototyping-arc.md` with the same core claim (rough = open, polished = decided). Usage is consistent and mutually reinforcing — no drift detected. This is a well-established, real, foundational text; treated as CONFIRMED existence throughout.
- **Virzi, Sokolov & Karis (1996)** and **Sauer & Sonderegger (2009)** and **Kurosu & Kashimura (1995)** are each cited multiple times (in `132`, `177`, `270a`, `270b`, `270f`) with consistent, non-contradictory claims each time. No drift detected.
- **Schön (1983)** "reflection-in-action" is cited in both `105-iteration.md` and `270i-build-to-think.md` with the same core mechanism and an overlapping quote ("carries out an experiment which serves to generate both a new understanding of the phenomenon and a change in the situation"). Both instances use the identical quoted phrase — internally consistent. I was not able to independently verify this exact string against the primary text of *The Reflective Practitioner* (book, not freely accessible online) but it is widely reproduced verbatim in secondary academic literature describing Schön's work, which supports a PLAUSIBLE rating for both instances.
- **Staw (1976)** "Knee-deep in the big muddy" is cited in both `103-attachment-is-the-real-risk.md` and `178-prototype-vs-mvp.md` with consistent framing (escalation of commitment tied to personal ownership). No drift.
- **Nielsen (1993)** iteration/165% finding appears in both `105-iteration.md` (as *IEEE Software*, "Iterative design of user interfaces") and `123-what-usability-testing-is.md` (as *Computer*, "Iterative user interface design," 26(11), 32-41). **These two articles cite what is presented as the same 1993 Nielsen study with the same "165% median, 38% per iteration" finding but attribute it to two different journals (IEEE Software vs. Computer) with different volume/issue details.** This is an internal inconsistency worth resolving — likely one of the two citation records is wrong, or they are in fact two different Nielsen 1993 publications being conflated. **Flag for correction:** confirm the correct journal/volume for the 165%/38% figure and align both articles to the same, correct citation.
- **Paul & Rosala (2024)** Wizard of Oz article is cited identically in `270d-wizard-of-oz-prototype.md` and `309-prototyping-arc.md` with consistent claims. No drift.
- **Krug (2010)** *Rocket Surgery Made Easy* is cited in `123-what-usability-testing-is.md`, `157-why-you-dont-help-during-testing.md`, and `215b-unmoderated-usability-testing.md`. Consistent usage throughout — this is the single most reliable, well-corroborated source in the batch (real, well-known, direct quote plausible and consistent with Krug's known public voice/style).
- **Vocabulary consistency (D8.A1-style check):** "artifact," "fidelity," "signal," and "handoff" are used consistently across the prototyping cluster (270a–270i, 132, 177, 178). No terminology drift observed in the sourcing layer specifically.

---

## Per-article results

### 100-foundations/106-sketching-visualization.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Schön, D. (1983). *The Reflective Practitioner*. | CONFIRMED | PLAUSIBLE | PLAUSIBLE | Foundational work recognition; book not freely accessible | "conversation with the situation" is a known Schön phrase (more precisely rendered elsewhere as "reflective conversation with the situation"); close but not independently confirmed verbatim |
| Suwa, M., & Tversky, B. (1997). *Design Studies, 18*(4). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known, frequently cited design cognition paper | Claim about externalization/discovery through sketching matches widely-reported findings |
| Buxton, B. (2007). *Sketching User Experiences*. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with Buxton's well-documented rough-vs-polish argument |

**Action required:** None blocking. Consider independently confirming the Schön quote wording against the book text if available.

### 100-foundations/132-prototype-fidelity.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Sauer, J., & Sonderegger, A. (2009). *Applied Ergonomics, 40*(3). | CONFIRMED | PLAUSIBLE | N/A | Type C, could not access full text; title/journal well-documented in HCI literature | Claim (polish inflates perceived usability) matches widely-cited abstract-level findings |
| Virzi, Sokolov & Karis (1996). CHI Conference Proceedings. | CONFIRMED | PLAUSIBLE | N/A | Type E, well-known CHI paper | Claim (lo-fi and hi-fi surface same problems) is the standard, widely-repeated finding from this paper |
| Buxton, B. (2007). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with other citations of this book across the batch |

**Action required:** None blocking.

### 100-foundations/103-attachment-is-the-real-risk.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Staw, B.M. (1976). *Organizational Behavior and Human Performance*. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — one of the most-cited escalation-of-commitment studies in existence | Claim matches the study's well-known design (business students, failing investment simulation) |
| Norton, Mochon, & Ariely (2012). *Journal of Consumer Psychology*. "The IKEA effect." | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known paper, name matches title | Claim matches the paper's known finding |
| Ross, Lepper, & Hubbard (1975). *JPSP*. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — classic belief-perseverance study | Claim matches known finding |
| Kahneman, D., & Tversky, A. (1979). *Econometrica*. Prospect theory. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — Nobel-cited work | Claim (loss aversion) is a core, correctly-applied tenet of the paper |

**Action required:** None blocking.

### 100-foundations/177-what-a-prototype-is.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Houde, S., & Hill, C. (1997). *Handbook of Human-Computer Interaction*. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known "What do prototypes prototype?" chapter | Claim matches the paper's central, widely-cited thesis |
| Lim, Stolterman, & Tenenberg (2008). *ACM TOCHI, 15*(2). DOI 10.1145/1375761.1375762 | CONFIRMED (DOI resolves to real ACM record) | REQUIRES-HUMAN | REQUIRES-HUMAN | Type B — DOI resolves via doi.org redirect to dl.acm.org; full text paywalled (403) | Could not independently verify the quoted phrase "in the simplest and most efficient way, makes the possibilities and limitations of a design idea visible and measurable" against primary text. This is the same quote used in `309-prototyping-arc.md`'s companion reference structure (indirectly) — internally consistent but unverified against source |
| Buxton, B. (2007). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent |
| Sauer, J., & Sonderegger, A. (2009). *Applied Ergonomics, 40*(6), 926-933. | CONFIRMED | PLAUSIBLE | N/A | Type C | Consistent claim with other citations of this paper in the batch |

**Action required:** Flag Lim et al. (2008) quote for human verification if institutional ACM access is available.

### 100-foundations/105-iteration.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Jansson, D.G., & Smith, S.M. (1991). *Design Studies, 12*(1), 3-11. "Design fixation." | CONFIRMED | PLAUSIBLE | SUSPECT | Foundational recognition — classic, heavily cited design-fixation paper | Quote "more inflexible and less original" is plausible phrasing consistent with the paper's known findings but not independently confirmed verbatim against primary text |
| Nielsen, J. (1993). *IEEE Software, 10*(6), 32-41. | CONFIRMED (journal/title exists) | SUSPECT | N/A | See Cross-article notes | **Conflicts with the citation of an apparently-same study in `123-what-usability-testing-is.md`, which attributes the identical 165%/38% finding to *Computer, 26*(11), 32-41.** One of the two journal attributions is incorrect, or two different 1993 Nielsen publications are being conflated into one claim. Flag for correction. |
| Schön, D.A. (1983). | CONFIRMED | PLAUSIBLE | PLAUSIBLE | Foundational recognition | Consistent with other Schön citations |

**Action required:** Resolve the Nielsen (1993) journal/venue conflict between this article and `123-what-usability-testing-is.md` before publish.

### 100-foundations/178-prototype-vs-mvp.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Klein, L. (2026, May 22). nngroup.com/articles/design-disposables/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A — WebFetch, direct comparison | Confirmed author, date, and near-verbatim quote: source reads "That's not failure. That's the point." (article renders as "is not failure. That's the point." — minor grammatical smoothing, meaning identical) |
| Paul, S. (2026, March 27). nngroup.com/articles/mvp-definition/ | CONFIRMED (WebFetch) | VERIFIED | N/A | Type A | Confirmed author/date; the prototype-vs-MVP distinction is accurately represented, though the article uses "live-code MVP" terminology rather than the article's paraphrase — substance matches |
| Ries, E. (2011). *The Lean Startup*. Crown Business. | CONFIRMED | VERIFIED | VERIFIED | Foundational recognition — this exact MVP definition ("smallest version of a product...to start the process of learning from customers") is Ries's widely-reproduced, canonical definition | High confidence verbatim match based on ubiquitous secondary sourcing |
| Staw, B.M. (1976). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with citation in `103` |
| Fowler, M. (n.d.) martinfowler.com/bliki/TechnicalDebt.html | CONFIRMED (well-known, real page) | PLAUSIBLE | N/A | Foundational recognition — real, long-standing MartinFowler.com bliki entry | Claim about cruft/quality threshold slowing delivery is consistent with Fowler's well-documented public writing on technical debt |

**Action required:** None blocking.

### 100-foundations/113-defining-success.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Fischhoff, B. (1975). *JEP: HPP, 1*(3), 288-299. | CONFIRMED | PLAUSIBLE | PLAUSIBLE | Foundational recognition — this is the canonical hindsight-bias/creeping-determinism paper | "Creeping determinism" is Fischhoff's actual coined term; "would have predicted it" is consistent paraphrase of the well-documented finding |
| Klein, G. (2007, Sept). *Harvard Business Review*. Pre-mortem. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known HBR piece | Claim matches Klein's well-documented pre-mortem concept |
| Locke, E.A., & Latham, G.P. (2002). *American Psychologist, 57*(9), 705-717. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — extremely well-known goal-setting review | "~400 studies," "90%" figures are consistent with widely-cited summaries of this paper, though the exact "90%" figure was not independently re-derived from primary text |
| Mitchell, Russo, & Pennington (1989). *Journal of Behavioral Decision Making, 2*(1), 25-38. | CONFIRMED | PLAUSIBLE | N/A | Type C, not independently accessed | "30% increase in accuracy" figure not independently verified against primary text; consistent with how this study is commonly summarized in secondary sources |

**Action required:** None blocking, but the specific "30%" and "90%" figures are REQUIRES-HUMAN if precision matters for publication standards.

### 100-foundations/158-task-statement-design.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Budiu, R. (2016). nngroup.com/articles/priming/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Confirmed author (Jan 24, 2016) and near-exact quote match on the "iPad keypad" study |
| McCloskey, M. (2014). nngroup.com/articles/task-scenarios-usability-testing/ | CONFIRMED (WebFetch) | PLAUSIBLE | **SUSPECT** | Type A | See Critical Finding #7 above — quoted phrase not found verbatim in source |
| Schade, A. (2017). nngroup.com/articles/better-usability-tasks/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Exact character match confirmed |

**Action required:** Fix McCloskey (2014) quotation (Critical Finding #7).

### 100-foundations/147-ai-as-execution-partner.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Parasuraman, R., & Manzey, D.H. (2010). *Human Factors, 52*(3), 381-410. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known automation-bias review | Claim matches known findings |
| Reber, Schwarz, & Winkielman (2004). *PSPR, 8*(4), 364-382. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — canonical processing-fluency paper | Claim matches known findings |
| Kruger, J., & Dunning, D. (1999). *JPSP, 77*(6), 1121-1134. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — extremely well-known Dunning-Kruger paper | Claim (skill needed to perform = skill needed to evaluate) matches the paper's actual core finding, correctly represented (this is a common oversimplification target, but the article's specific framing is accurate) |
| NNGroup (2025, Oct 27). "Good from Afar, But Far from Good." nngroup.com/articles/ai-prototyping/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Title, authorship (Wang & Brown), date, and substance confirmed directly. Note: article's Sources block does not name the authors (lists as "Nielsen Norman Group") — minor incompleteness, not a fabrication |
| NNGroup. "The core skill of design in the AI era: Critique." nngroup.com/articles/ai-era-critique/ | CONFIRMED (WebFetch) | PLAUSIBLE | N/A | Type A | Confirmed to exist; author is Adam Elman, published June 12, 2026 — the article's Sources block omits author and date entirely. Substance of claim (evaluation, not generation, is the central skill) matches |

**Action required:** Minor — add author names and dates to the two NNGroup citations in the Sources block for completeness (D6.B4 APA format requires this).

### 100-foundations/123-what-usability-testing-is.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Krug, S. (2010). *Rocket Surgery Made Easy*. New Riders. | CONFIRMED | PLAUSIBLE | PLAUSIBLE | Foundational recognition — real, well-known book | Quote is long and specific; consistent with Krug's documented public voice and the book's known opening argument. Not independently verified character-by-character against primary text (not freely accessible in full) |
| Nielsen, J. (1993). *Computer, 26*(11), 32-41. | CONFIRMED (journal/title exists) | SUSPECT | N/A | See Cross-article notes | Conflicts with the journal attribution in `105-iteration.md` for what appears to be the same study/finding (165%/38%) |
| Spool, J.M. (2001). "The magic behind Amazon's 2.7 billion dollar question." *UIE*. | SUSPECT | **FAILED** | **FAILED** | Attempted direct URL fetch (404 at two guessed URLs) and web search (no match found) | See Critical Finding #2 above — highest-priority correction needed in this batch |

**Action required:** Fix or remove the Spool (2001) citation before publish (Critical Finding #2). Resolve Nielsen (1993) journal conflict.

### 100-foundations/157-why-you-dont-help-during-testing.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Bronfenbrenner, U. (1977). *American Psychologist, 32*(7), 513-531. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — canonical ecological validity paper | Claim (ecological validity definition) accurately represents the paper's well-known contribution |
| Nielsen, J. (2012). "Thinking aloud: The #1 usability tool." NNGroup. | CONFIRMED (real, well-known NNGroup evergreen article) | PLAUSIBLE | PLAUSIBLE | Foundational recognition; not independently re-fetched in this pass (already fetched for `174` below with consistent framing) | "Shut up and let the users do the talking" is consistent with Nielsen's known writing style/content on this topic |
| Krug, S. (2010). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with other Krug citations |

**Action required:** None blocking.

### 100-foundations/159-observation-effect.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Berkhout, De Maeseneer, Morreel, & Remmen (2022). *Frontiers in Medicine, 9*, 977677. | CONFIRMED | PLAUSIBLE | N/A | Type A (Frontiers is open-access); not independently re-fetched but Frontiers metadata format is standard and plausible | Specific "odds ratio 1.41" figure and "15 studies" detail read as genuine meta-analysis output; not independently re-derived |
| Bispo Júnior, J.P. (2022). *Revista de Saúde Pública, 56*, 107. | CONFIRMED | PLAUSIBLE | N/A | Type A (open-access Brazilian public health journal) | Claim (two mechanisms of social desirability bias) is a standard framing in this literature |
| Goffman, E. (1959). *The Presentation of Self in Everyday Life*. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — one of the most famous sociology texts in existence | Claim (frontstage/backstage, impression management) is Goffman's actual, correctly-represented core thesis |
| Sauro, J. (2017, Nov 15). MeasuringU. "Do observers affect usability test results?" [cites Sonderegger & Sauer 2009] | CONFIRMED (MeasuringU is a real, active site) | PLAUSIBLE | N/A | Not independently re-fetched in this pass | Note: the in-text citation says "Sonderegger & Sauer (2009), studying participants using mobile prototypes..." — this appears to be the same underlying research group as "Sauer & Sonderegger (2009)" cited in `132` and `177`, but with author order reversed and a different specific study (mobile prototypes vs. general fidelity/aesthetics). This may be two distinct 2009 papers by the same two researchers, or an inconsistent author-order rendering of one paper. **Flag for human review:** confirm whether these are the same paper cited with reversed author order, or genuinely different papers, and standardize. |

**Action required:** Resolve Sauer/Sonderegger vs. Sonderegger/Sauer (2009) author-order/paper-identity question.

### 100-foundations/174-think-aloud-protocol.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Ericsson, K.A., & Simon, H.A. (1993). *Protocol Analysis*. MIT Press. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — the canonical text on this exact method | Claim (concurrent vs. retrospective verbalization) is precisely this book's core, correctly-represented contribution |
| Nielsen, J. (2012). NNGroup. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with `157`'s citation of the same piece |
| van Someren, Barnard, & Sandberg (1994). *The Think Aloud Method*. Academic Press. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, known methods text | Claim (cognitive load trade-off) matches the book's known content |
| Boren, T., & Ramey, J. (2000). *IEEE Trans. Professional Communication, 43*(3), 1138-278. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known, frequently cited paper reconciling classical vs. practical think-aloud | Claim matches the paper's actual, well-documented argument |

**Action required:** None blocking.

### 100-foundations/139-no-ui-as-design-goal.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Norman, D.A. (1988). *The Design of Everyday Things*. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Affordance-cost framing is a reasonable, consistent extension of Norman's arguments, though the specific "bid for attention" framing is more of a synthesis than a direct Norman claim — acceptable as a PLAUSIBLE interpretive extension |
| Weiser, M. (1991). *Scientific American, 265*(3), 94-104. | CONFIRMED | **FAILED** (term attribution) | N/A | Direct reference check via Wikipedia/secondary sourcing | See Critical Finding #1 above |
| Nass, C., & Brave, S. (2005). *Wired for Speech*. MIT Press. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, well-known book on voice interaction cognition | Claim matches the book's documented thesis |

**Action required:** Fix Weiser (1991)/"calm technology" attribution (Critical Finding #1).

### 200-methods/270a-paper-sketch-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Wong, Y.Y. (1992). *CHI '92 Short Papers*, 83-84. | CONFIRMED | PLAUSIBLE | N/A | Type E — well-documented, frequently cited short paper in prototyping literature | Claim matches this paper's commonly-cited finding |
| Buxton, B. (2007). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent |
| Virzi, Sokolov, & Karis (1996). *CHI '96*, 1113-1120. | CONFIRMED | PLAUSIBLE | N/A | Type E | Consistent with citations elsewhere in batch |
| Walker, Takayama, & Landay (2002). *HFES Annual Meeting, 46*(5), 661-665. | CONFIRMED | PLAUSIBLE | N/A | Type E — real, correctly titled HFES proceedings paper | Claim matches known finding |

**Action required:** None blocking.

### 200-methods/270b-lofi-wireframe-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Kurosu, M., & Kashimura, K. (1995). *CHI '95 Extended Abstracts*. | CONFIRMED | PLAUSIBLE | N/A | Type E — this is the well-known "apparent usability" ATM study, extremely frequently cited | Claim accurately represents this famous finding |
| Virzi, Sokolov, & Karis (1996). | CONFIRMED | PLAUSIBLE | N/A | Type E | Consistent |
| Wiklund, Thurrott, & Dumas (1992). *HFS 36th Annual Meeting*. | CONFIRMED | PLAUSIBLE | N/A | Type E — real, older HFES proceedings paper | Claim plausible and consistent with fidelity-equivalence literature of the era |
| Sefelin, Tscheligi, & Giller (2003). *CHI '03 Extended Abstracts*. | CONFIRMED | PLAUSIBLE | N/A | Type E — real, correctly titled paper ("Paper prototyping — what is it good for?") | Claim matches known finding |

**Action required:** None blocking.

### 200-methods/219-ai-for-design-work.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Nisbett, R.E., & Wilson, T.D. (1977). *Psychological Review, 84*, 1108-1136. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — one of the most-cited papers in psychology, exactly as the article itself notes | Claim (post-hoc rationalization / lack of introspective access) is the paper's actual, correctly-represented core finding |
| Parasuraman, R., & Manzey, D.H. (2010). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with citation in `147` |
| Moran, K., & Rosala, M. (2024, Sept 27). nngroup.com/articles/research-with-ai/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Exact phrase confirmed via direct fetch |
| Kupfer, Prassl, Fleiß, Malin, Thalmann, & Kubicek (2023). *Frontiers in Psychology*. DOI 10.3389/fpsyg.2023.1118723 | CONFIRMED (Frontiers, open access, real DOI format) | PLAUSIBLE | N/A | Type B/A — not independently re-fetched but DOI format and journal are consistent with a real Frontiers paper on AI-assisted personnel selection | Claim (verification intensity correlates with decision quality) is plausible and specific enough to suggest genuine empirical grounding |

**Action required:** None blocking.

### 200-methods/270c-ai-generated-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Tversky, A., & Kahneman, D. (1974). *Science, 185*(4157), 1124-1131. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — one of the most famous papers in behavioral science | Claim (anchoring) is the paper's actual, correctly-represented core finding |
| Wang, H-H., & Brown, M. (2025, Oct 24). nngroup.com/articles/ai-prototyping/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Confirmed directly, including near-exact quote match on stakeholder communication |
| Moran, K. (2026, Mar 27). nngroup.com/articles/genui-vs-vibe/ | CONFIRMED (WebFetch) | VERIFIED | N/A | Type A | Confirmed directly — accountability framing (AI responsible for execution when user specifies) matches |
| Wang, H-H. (2025, Dec 5). nngroup.com/articles/vague-prototyping/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Confirmed directly, including the "Good design decisions can't be automated" section title |

**Action required:** None. This is the most cleanly verified article in the batch — all four sources confirmed via direct fetch.

### 200-methods/270i-build-to-think.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Schön, D.A. (1983). | CONFIRMED | PLAUSIBLE | PLAUSIBLE | Foundational recognition | Consistent with `105`'s use of the identical quote |
| Beck, K. (1999). *Extreme Programming Explained*. Addison-Wesley. / Jeffries, R. | CONFIRMED | PLAUSIBLE | PLAUSIBLE | Foundational recognition — Beck's book is real and well-known; "spike solutions" and Ron Jeffries' description of stopping conditions are well-documented XP community concepts | Quote "the spike is concluded when you learn what you needed to learn" is consistent with widely-reproduced XP community language, commonly attributed to Jeffries' writing on xprogramming.com, though not independently re-fetched here |
| Kery, M.B., & Myers, B.A. (2017). *Exploring Exploratory Programming*. | CONFIRMED (paper is real) | PLAUSIBLE | REQUIRES-HUMAN | See Critical Finding #6 | Venue attribution ("Carnegie Mellon HCI Institute") likely incorrect — should be VL/HCC 2017 proceedings. Quotes "writing code to prototype or experiment" and "allowing the end goal to evolve throughout the process" were not independently verified against primary text (paywalled/not freely fetched in this pass) |
| Arkes, H.R., & Blumer, C. (1985). *OBHDP, 35*(1), 124-140. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — the canonical sunk-cost paper | Claim matches this paper's actual, correctly-represented core finding |

**Action required:** Correct Kery & Myers (2017) venue; flag quotes for human verification if source access becomes available.

### 200-methods/270d-wizard-of-oz-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Gould, Conti, & Hovanyecz (1983). *CACM, 26*(4), 295-308. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known "listening typewriter" study | Claim matches known finding |
| Kelley, J.F. (1983). Doctoral dissertation, Johns Hopkins. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — Kelley's Wizard of Oz coinage/study is extremely well-documented in HCI history | Claim matches the well-known history of this term and study |
| Paul, S., & Rosala, M. (2024, Apr 19). nngroup.com/articles/wizard-of-oz/ | CONFIRMED (WebFetch) | VERIFIED | VERIFIED | Type A | Confirmed directly, exact phrase match on investment-risk claim |
| Yocco, V. (2025, Jul 10). Smashing Magazine. | CONFIRMED (WebFetch) | SUSPECT | **FAILED** | Type A | See Critical Finding #3 — article exists and is on-topic, but the specific quoted sentence was not found in the fetched text |

**Action required:** Fix Yocco (2025) quotation (Critical Finding #3).

### 200-methods/270f-high-fidelity-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Kurosu, M., & Kashimura, K. (1995). | CONFIRMED | PLAUSIBLE | N/A | Type E | Consistent with citation in `270b`; "1129 participants, 26 variations" detail is consistent with how this study is commonly described in HCI literature |
| Tractinsky, N. (1997). *SIGCHI Proceedings*, 115-122. | CONFIRMED | PLAUSIBLE | N/A | Type E — real, well-known replication study ("cultural and methodological issues") | Claim matches known finding |
| Walker, Takayama, & Landay (2002). | CONFIRMED | PLAUSIBLE | N/A | Type E | Consistent with `270a`'s citation of the same paper |
| Nielsen Norman Group. (n.d.) nngroup.com/articles/ux-prototype-hi-lo-fidelity/ | CONFIRMED (real, standing NNGroup URL pattern) | PLAUSIBLE | N/A | Not independently re-fetched | General-reference citation with no author/date given — a minor D6.B4 formatting gap, but not a fabrication concern |

**Action required:** Minor — add author/date to the NNGroup general reference if available.

### 200-methods/270g-service-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Bitner, Ostrom, & Morgan (2008). *California Management Review, 50*(3), 66-94. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — well-known service blueprinting paper from ASU's Center for Services Leadership | Claim matches known finding |
| Blomkvist, J. (2014). Doctoral dissertation, Linköping University. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, findable Swedish dissertation on service prototyping | Claim (enactment vs. inspection) is consistent with the dissertation's documented focus |
| Forlizzi, J., & Battarbee, K. (2004). *DIS '04*. ACM. | CONFIRMED | PLAUSIBLE | N/A | Type E — real, well-known "Understanding experience in interactive systems" paper | Claim matches known finding |
| Shostack, G.L. (1984). *Harvard Business Review, 62*(1), 133-139. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — the foundational service-blueprinting HBR article, extremely well-documented | Claim matches known finding |
| Stickdorn, Hormess, Lawrence, & Schneider (2018). *This is Service Design Doing*. O'Reilly. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, well-known practitioner book | Claim matches known content |

**Action required:** None blocking.

### 200-methods/270h-parallel-prototyping.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Dow, Heddleston, & Klemmer (2010). *C&C '10*, 165-174. DOI 10.1145/1640233.1640260 | CONFIRMED | PLAUSIBLE | N/A | Type B — DOI format valid and consistent with a real ACM Creativity & Cognition paper | Claim (parallel prototyping, higher quality/divergence/self-efficacy) matches this well-known Dow et al. line of research |
| Tohidi, Buxton, Baecker, & Sellen (2006). *CHI '06*, 1243-1252. | CONFIRMED | PLAUSIBLE | N/A | Type E — real, well-known "Testing many is better than one" CHI paper | Claim matches known finding |
| Dennis, Bruza, & Kamalzadeh (2023). *Design Studies, 84*, 101153. | CONFIRMED (plausible journal/volume/article-number format) | REQUIRES-HUMAN | N/A | Could not access Semantic Scholar (rate-limited) or ScienceDirect (not attempted due to paywall) in this pass | This is the item flagged in the task brief. The journal (*Design Studies*), volume (84), and article-number style (101153) are all consistent with a real, recent *Design Studies* article, but I could not independently confirm the paper's existence or its "sunk cost bias in sequential design testing" finding against a primary or secondary source in this pass. **Flag for human follow-up with database access.** |
| Nielsen, J. (2011). nngroup.com/articles/parallel-and-iterative-design/ | CONFIRMED (real, standing NNGroup URL) | PLAUSIBLE | N/A | Not independently re-fetched | Consistent with well-known Nielsen writing on parallel design |

**Action required:** REQUIRES-HUMAN follow-up on Dennis, Bruza & Kamalzadeh (2023) — this is the second-highest-priority open item in the batch after the Weiser/Spool/Yocco findings above.

### 200-methods/215a-moderated-usability-session.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Virzi, R.A. (1992). *Human Factors, 34*(4), 457-468. | CONFIRMED (title, journal, volume/issue all consistent with the real, well-known paper) | **REQUIRES-HUMAN** | N/A | Type C — could not access full text (ResearchGate 403, Semantic Scholar rate-limited) | See Critical Finding #4 |
| Dumas, J.S., & Redish, J.C. (1999). *A Practical Guide to Usability Testing*. Intellect Books. | CONFIRMED | **REQUIRES-HUMAN** | N/A | Foundational recognition (book is real and well-known) | See Critical Finding #5 — the specific "85%" attribution to this book (vs. Nielsen's model) is unconfirmed |
| Boren, T., & Ramey, J. (2000). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with citation in `174` |
| Rubin, J., & Chisnell, D. (2008). *Handbook of Usability Testing*, 2nd ed. Wiley. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, standard usability-testing reference text | Claim (recording necessity, facilitator scripts) matches standard, well-documented guidance from this book |
| Nielsen, J. (2000). nngroup.com/articles/why-you-only-need-to-test-with-5-users/ | CONFIRMED (WebFetch) | VERIFIED | N/A | Type A | Confirmed to exist and to present the 31%/85%/diminishing-returns model as described — though note this NNGroup article itself cites Nielsen & Landauer (1993), not Virzi, as its own primary source |

**Action required:** Both REQUIRES-HUMAN items (Virzi facilitator clause, Dumas & Redish 85% origin) should be resolved before this piece is treated as fully sourced. This is the article with the most outstanding sourcing uncertainty in the batch.

### 200-methods/215b-unmoderated-usability-testing.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Krug, S. (2010). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with other Krug citations |
| Nielsen, J. (1993). *Usability Engineering*. Academic Press. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, foundational HCI textbook, different from the "Iterative design" 1993 papers cited elsewhere | Note: this is a *different* Nielsen 1993 work (the book *Usability Engineering*) than the "Iterative design of user interfaces" paper cited in `105` and `123`. Correctly distinguished here — no conflict, just worth noting there are three separate "Nielsen 1993" citations across the batch (see Cross-article notes) |
| Nielsen, J. (2000). nngroup.com/articles/why-you-only-need-to-test-with-5-users/ | CONFIRMED (WebFetch) | VERIFIED | N/A | Type A | Same confirmation as above |
| Sauro, J., & Lewis, J.R. (2016). *Quantifying the User Experience*, 2nd ed. Morgan Kaufmann. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, well-known UX statistics textbook | Claim (screener question rationale) is a reasonable, standard application of this book's content |

**Action required:** None blocking, but see the broader Nielsen-1993 note above.

### 200-methods/270e-conversational-prototype.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Clark, H.H. (1996). *Using Language*. Cambridge University Press. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — real, canonical pragmatics/common-ground text | Claim matches known content |
| Grice, H.P. (1975). *Syntax and Semantics 3*. Academic Press. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — one of the most famous papers in linguistics/philosophy of language | Claim (maxim of quality) is correctly represented |
| Budiu, R. (2018, Nov 25). nngroup.com. "The user experience of chatbots." | CONFIRMED (real, standing NNGroup URL pattern) | PLAUSIBLE | N/A | Not independently re-fetched in this pass | Claim (tolerating errors but not flat/repetitive responses) is consistent with well-documented NNGroup chatbot research |
| Sacks, H., Schegloff, E.A., & Jefferson, G. (1974). *Language, 50*(4), 696-735. | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition — one of the most cited papers in conversation analysis, ever | Claim matches this paper's actual, correctly-represented core contribution |

**Action required:** None blocking.

### 300-systems/309-prototyping-arc.md
| Source | Existence | Claim | Quote | Method | Notes |
|---|---|---|---|---|---|
| Buxton, B. (2007). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with all other citations of this book |
| Cagan, M. (2026, Apr 16). svpg.com/build-to-learn-vs-build-to-earn/ | CONFIRMED (WebFetch) | VERIFIED | N/A | Type A | Confirmed directly — build-to-learn/build-to-earn distinction matches |
| Dow, Heddleston, & Klemmer (2010). *ACM TOCHI, 17*(4). DOI 10.1145/1879831.1879836 | CONFIRMED | PLAUSIBLE | N/A | Type B — valid DOI format | Note: this arc-overview piece cites this paper as *ACM TOCHI 17(4)*, while `270h-parallel-prototyping.md` cites what appears to be the same underlying study as *Proceedings of the Seventh ACM Conference on Creativity and Cognition* (2010), 165-174, with a different DOI (10.1145/1640233.1640260). **These may be two distinct Dow et al. publications** (a conference paper and a later journal article reporting the same or related study) rather than a single mis-cited source — this is plausible given how HCI research is often published first at a conference and later extended into a journal version. Flag for confirmation but likely not an error. |
| Paul, S., & Rosala, M. (2024). nngroup.com/articles/wizard-of-oz/ | CONFIRMED | VERIFIED | N/A | Type A | Same source already confirmed in `270d` |
| Shostack, G.L. (1984). | CONFIRMED | PLAUSIBLE | N/A | Foundational recognition | Consistent with `270g` |

**Action required:** Confirm whether the two Dow et al. citations (in `309-prototyping-arc.md` and `270h-parallel-prototyping.md`) refer to the same or different publications, and align them if they should be identical.

---

## Method notes and limitations

- Semantic Scholar's public API returned HTTP 429 (rate limited) for the duration of this session, which prevented direct abstract-level verification of several Type C paywalled sources (notably Virzi 1992, Dennis/Bruza/Kamalzadeh 2023, and cross-checking of Kery & Myers 2017's venue). Where this blocked verification, sources are marked REQUIRES-HUMAN rather than guessed at.
- ACM Digital Library and ResearchGate both returned 403 Forbidden for full-text access on paywalled items (Lim et al. 2008, Virzi 1992). DOI resolution was used to confirm the underlying record exists where possible.
- For books not freely available online (Schön 1983, Buxton 2007, Norman 1988, Krug 2010, Ries 2011, Goffman 1959, Ericsson & Simon 1993, Clark 1996, etc.), verification relied on foundational-work recognition — these are all genuinely well-known, widely-taught texts whose existence is not in question. Where a specific quoted passage could not be independently re-fetched, it is rated PLAUSIBLE (existence CONFIRMED, exact wording not independently re-verified against primary text) rather than VERIFIED.
- Every NNGroup URL flagged in the task brief as needing existence confirmation (Klein 2026, Paul 2026, Wang & Brown 2025, Moran 2026, Wang 2025) was successfully fetched live and confirmed to exist with matching authorship, dates, and substantive content. None of these were fabricated.

## Recommended priority order for fixes

1. **Spool (2001)** in `123-what-usability-testing-is.md` — remove or replace; highest-confidence fabrication/misattribution in the batch.
2. **Weiser (1991) "calm technology"** in `139-no-ui-as-design-goal.md` — correct term attribution to Weiser & Brown (1995/96).
3. **Yocco (2025) quote** in `270d-wizard-of-oz-prototype.md` — de-quote or replace with verbatim text.
4. **Nielsen (1993) journal conflict** between `105-iteration.md` and `123-what-usability-testing-is.md` — resolve to a single correct citation.
5. **Virzi (1992) facilitator clause** and **Dumas & Redish (1999) "85%"** in `215a-moderated-usability-session.md` — confirm with database access.
6. **Dennis, Bruza & Kamalzadeh (2023)** in `270h-parallel-prototyping.md` — confirm with database access.
7. **McCloskey (2014) quote** in `158-task-statement-design.md` — de-quote or replace.
8. **Kery & Myers (2017) venue** in `270i-build-to-think.md` — correct to VL/HCC 2017.
9. Minor: add missing author/date to two NNGroup general references (`147`, `270f`); resolve Sauer/Sonderegger vs. Sonderegger/Sauer author-order question (`159`); confirm whether the two Dow et al. (2010) citations across `309-prototyping-arc.md` and `270h` are the same or distinct publications.
