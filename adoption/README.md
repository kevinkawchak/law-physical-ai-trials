# adoption - the clinician confidence framework (v0.2.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Topic](https://img.shields.io/badge/Topic-Clinician%20confidence%20framework-8B2E3F.svg)](.)
[![Stages](https://img.shields.io/badge/Stages-Mermaid%20%E2%86%92%20draft%20%E2%86%92%20full%20%E2%86%92%20final-D08770.svg)](.)
[![Questions](https://img.shields.io/badge/Confidence%20questions-8-8B2E3F.svg)](final-framework/sections/)
[![Mermaid figures](https://img.shields.io/badge/Mermaid%20figures-20-EBCB8B.svg)](mermaid/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-9-D08770.svg)](final-framework/)
[![Concept](https://img.shields.io/badge/Concept-calibrated%20trust-EBCB8B.svg)](.)
[![Agent](https://img.shields.io/badge/Agent-Claude%20Code%20Opus%204.8%20(1M)-8B2E3F.svg)](https://claude.com/claude-code)

[Final PDF and Source](https://doi.org/10.5281/zenodo.20710602). This directory holds a **new paper topic** built with the same four-stage pipeline
as the v0.1.0 review under [`../review/`](../review/), but it does **not** rewrite
it. The work is *Earning the Clinician's Trust: An Eight-Question Confidence
Framework for Verified Physical AI in Oncology Trials*, written for the clinicians
who will supervise autonomous Physical AI at the bedside of an oncology clinical
trial and who must decide when that reliance is earned.

## Review versus adoption: two audiences, one mechanism

| | `review/` (v0.1.0) | `adoption/` (v0.2.0) |
|:--|:--|:--|
| Audience | Legislators in medical AI | Practicing clinicians and trial staff |
| Organizing frame | Eight emotional pillars | Eight confidence questions |
| Register | Advocacy narrative | Clinical and operational |
| Goal | Enact the bill into law | Place calibrated trust at the bedside |
| Shared spine | Verification before generation; ten VVUQ gates; ACCEPT / ESCALATE / BLOCK; the `#8B2E3F` template theme; the strict palette | same |

## The eight confidence questions (CONFIDENCE GOALS)

| # | Question | Answered by |
|:--|:--|:--|
| 1 | Competence: is it actually good at this? | Local validation and the assurance run (172 of 172 gate tests) |
| 2 | Safety: what stops it before it hurts someone? | The ten gates and the catastrophe-predicate BLOCK |
| 3 | Transparency: can I see why it did that? | Explainable output and a hash-chained audit trail |
| 4 | Oversight: am I still in control? | Human-in-the-loop control, ESCALATE, and override |
| 5 | Equity: does it work for the patient in front of me? | Subgroup performance and bias surveillance |
| 6 | Reliability: will it be the same tomorrow? | Reproducibility, drift monitoring, uncertainty |
| 7 | Accountability: who is responsible when it is wrong? | Named roles and a signed SOP |
| 8 | Workflow: does it fit how I actually work? | Integration into the clinic day and consent |

## How the build works

A single submitted prompt ([`prompts/prompt-adoption.md`](prompts/prompt-adoption.md))
drives two processes: Process A generated the four sub-prompts in
[`sub-prompts/`](sub-prompts/), and Process B ran them in sequence to grow the
manuscript through four stages.

```
                prompts/prompt-adoption.md
                          |
                 Process A | generate sub-prompts
                          v
   sub-prompts/  ->  mermaid/  ->  draft-framework/  ->  full-framework/  ->  final-framework/
   (4 prompts)      (20 figs)     (scaffold +           (rendered prose,      (publication
                                   bracket cues)         TikZ figures)         quality)
                          |
                          v
            root CHANGELOG.md + releases.md + README.md  (v0.2.0)
```

## Directory map

```
adoption/
  README.md                  (this file)
  prompts/                   the submitted prompt and the run output
  sub-prompts/               Process A output (four sub-prompts)
  references/                author_works.bib + framework_refs.bib
  mermaid/                   Stage 1: 20 colored Mermaid figures + catalog
  draft-framework/           Stage 2: scaffold with bracketed source cues
  full-framework/            Stage 3: rendered manuscript (20 TikZ figs, 8 tables)
  final-framework/           Stage 4: publication-quality manuscript (9 tables)
```

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Paper template (theme, columns, abstract box) | `review/template` | every framework stage |
| Sub-prompt and four-stage methodology | `review/sub-prompts/` | `sub-prompts/`; the build schedule |
| Colored Mermaid families and palette discipline | `review/mermaid/` | `mermaid/`; every figure |
| TOC and back-matter conventions | `review/final-narrative` | `draft-framework/` onward |
| Verification evidence (ten gates, 172 tests) | `review/` | `q1`, `q2`, `q6` sections |
| Author works and every bill version | `references/author_works.bib` | the engineering lineage |

## Visual media and palette

No raster images are used. The permitted media are full-width white-background
tables, monospace ASCII figures, and colored Mermaid diagrams (native in Markdown,
reproduced as colored TikZ in the compiled LaTeX). The strict palette is black,
grayscales, and `#EBCB8B` (gold, confidence), `#D08770` (clay, risk), and `#8B2E3F`
(burgundy, verification and clinician authority). The `#8B2E3F` template theme is
preserved.

## License

Released under CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit. Independent research draft; not enacted law and not legal or clinical
advice.
