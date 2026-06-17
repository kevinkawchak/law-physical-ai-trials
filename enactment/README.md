# enactment - the H. R. 9510 passage framework (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Topic](https://img.shields.io/badge/Topic-H.R.%209510%20passage%20framework-4B0082.svg)](.)
[![Stages](https://img.shields.io/badge/Stages-Mermaid%20%E2%86%92%20draft%20%E2%86%92%20full%20%E2%86%92%20verify%20%E2%86%92%20final-000080.svg)](.)
[![Questions](https://img.shields.io/badge/Passage%20questions-8-4B0082.svg)](final-framework/sections/)
[![Mermaid figures](https://img.shields.io/badge/Mermaid%20figures-20-000080.svg)](mermaid/)
[![New stage](https://img.shields.io/badge/New-verify%20stage-4B0082.svg)](verify-framework/)
[![Palette](https://img.shields.io/badge/Palette-indigo%20%7C%20navy%20%7C%20silver-C0C0C0.svg)](.)
[![Agent](https://img.shields.io/badge/Agent-Claude%20Code%20Opus%204.8%20(1M)-4B0082.svg)](https://claude.com/claude-code)
[![Enactment Paper DOI](https://img.shields.io/badge/Enactment%20DOI-10.5281%2Fzenodo.20726461-000080.svg)](https://doi.org/10.5281/zenodo.20726461)

[Final PDF and Source](https://doi.org/10.5281/zenodo.20726461). This directory holds a **new paper topic** (repository release v0.3.0) built with the
same staged pipeline as the v0.1.0 review under [`../review/`](../review/) and the
v0.2.0 framework under [`../adoption/`](../adoption/), but it does **not** rewrite
either. The work is *Earning the Congress's Vote: An Eight-Question Passage Framework
for Enacting H. R. 9510 in the House and Senate*, written for the staffer, the
member, and the committee counsel who must decide whether to mark up, cosponsor, and
vote for the bill in both chambers.

## Three audiences, one mechanism

| | `review/` (v0.1.0) | `adoption/` (v0.2.0) | `enactment/` (v0.3.0) |
|:--|:--|:--|:--|
| Audience | Legislators in medical AI | Practicing clinicians | Members, staff, committee counsel |
| Organizing frame | Eight emotional pillars | Eight confidence questions | Eight passage questions |
| Register | Advocacy narrative | Clinical and operational | Legislative and budgetary |
| Goal | Enact the bill into law | Calibrated trust at the bedside | Pass H. R. 9510 in both chambers |
| Shared spine | Verification before generation; ten VVUQ gates; ACCEPT / ESCALATE / BLOCK | same | same |

## The eight passage questions

| # | Question | Answered by |
|:--|:--|:--|
| 1 | Mandate: is the problem real enough to need a statute? | Three gaps in existing law; the record on preventable error |
| 2 | Authority: is this within Congress's power and consistent with existing law? | A commerce-power amendment to the FD&C Act (section 515D); a savings clause |
| 3 | Safety: what in the bill protects patients? | The ten-gate VVUQ schedule and the three hard catastrophe predicates |
| 4 | Fiscal: what does it cost, and is it paid for? | A 58 million dollar authorization; no net mandatory spending; a 19 to 1 reduction |
| 5 | Constituents: who does this help back home? | A platform scaling to 50 through 100 sites across all regions |
| 6 | Bipartisanship: can one caucus support it without losing the other? | One provision two caucuses can each support on their own terms |
| 7 | Coalition: who is behind it, and is opposition manageable? | Clinicians, patients, industry, and the States; objections routed to citations |
| 8 | Passage path: can it move through both chambers and then work? | Regular order, known thresholds, a defined runway, a demonstrated platform |

## How the build works

A single submitted prompt
([`prompts/prompt-enactment.md`](prompts/prompt-enactment.md)) drives two processes:
Process A generated the five sub-prompts in [`sub-prompts/`](sub-prompts/), and
Process B ran them in sequence to grow the manuscript through five stages, adding a
new verification stage between the full and final source files.

```
                prompts/prompt-enactment.md
                          |
                 Process A | generate five sub-prompts
                          v
   sub-prompts/ -> mermaid/ -> draft-framework/ -> full-framework/ -> verify-framework/ -> final-framework/
   (5 prompts)     (20 figs)   (scaffold + cues)   (rendered prose)    (table/figure audit)  (publication)
                          |
                          v
            root CHANGELOG.md + releases.md + README.md  (v0.3.0)
```

## Directory map

```
enactment/
  README.md                  (this file)
  prompts/                   the submitted prompt and the run output
  sub-prompts/               Process A output (five sub-prompts)
  references/                author_works.bib (trimmed) + passage_refs.bib
  mermaid/                   Stage 1: 20 colored Mermaid figures + catalog
  draft-framework/           Stage 2: scaffold with bracketed source cues
  full-framework/            Stage 3: rendered manuscript (20 TikZ figs, 6 tables)
  verify-framework/          Stage 4 (new): table and figure audit, verified twice
  final-framework/           Stage 5: publication-quality manuscript (7 tables)
    publication/             the deposit-ready mirror
```

## What is new in this build

1. **A new verification stage.** `verify-framework/` sits between the full and final
   source files and double-verifies every table and figure: a uniform
   `\vspace{-0.75cm}` figure-to-caption gap, column widths optimized to the text per
   column, and a twice-repeated figure audit (no text-box and arrow overlaps, an
   explicit looseness on every curved arrow, even box spacing).
2. **A new palette and template color.** Figures use only black, grayscales,
   `#4B0082` (indigo), `#000080` (navy), and `#C0C0C0` (silver); the paper template
   color is `#4B0082`.
3. **A trimmed reference set.** The less relevant author references were removed and
   important topic references were added with working URLs to professional sources
   and journals.

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Staged pipeline and sub-prompt methodology | [`adoption/sub-prompts/`](../adoption/sub-prompts/) | `sub-prompts/`; the build schedule |
| Template appearance, TikZ primitive, table columns | [`adoption/final-framework/publication`](../adoption/final-framework/publication) | every framework stage |
| Colored Mermaid families and palette discipline | [`adoption/mermaid/`](../adoption/mermaid/) | `mermaid/`; every figure |
| Most recent bill version (findings, 515D, financial) | `single-prompt-bill/auto-bill-02/final-bill/publication` | every body section |
| Clinical-trial platform scope | `physical-ai-oncology-trials/national-platform/new_paper/final_paper` | mandate, constituents, passage |
| Author works (then trimmed) | [`adoption/references/author_works.bib`](../adoption/references/author_works.bib) | `references/author_works.bib` |

## Visual media and palette

No raster image is used; the ORCID mark is text-based. The permitted media are
full-width white-background tables and colored Mermaid diagrams (native in Markdown,
reproduced as colored TikZ in the compiled LaTeX). The strict palette is black,
grayscales, `#4B0082` (indigo, authority and the bill), `#000080` (navy, evidence and
support), and `#C0C0C0` (silver, cost and caution). The `#4B0082` template theme is
used throughout.

## License

Released under CC BY 4.0. Reproduced public-domain U.S. Government text is used under
17 U.S.C. § 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending deposit.
Independent research draft; not enacted law and not legal advice. The number
"H. R. 9510" is illustrative.
