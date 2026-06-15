# references - shared bibliography for the adoption framework

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Author works](https://img.shields.io/badge/Author%20works-43-8B2E3F.svg)](author_works.bib)
[![Framework refs](https://img.shields.io/badge/Framework%20refs-14-D08770.svg)](framework_refs.bib)

This directory holds the two master bibliographies used by every stage of the
clinician confidence framework. Each framework stage
(`../draft-framework/`, `../full-framework/`, `../final-framework/`) ships its own
`references.bib` that is the concatenation of these two files, so each Overleaf
bundle compiles standalone with `\nocite{*}`.

| File | Contents | Entries |
|:--|:--|:--|
| [`author_works.bib`](author_works.bib) | The author's prior works and every H. R. 9510 bill version. Reused verbatim from [`../../review/references/author_works.bib`](../../review/references/author_works.bib); the engineering lineage is identical across both papers. | 43 |
| [`framework_refs.bib`](framework_refs.bib) | The clinician-confidence literature: calibrated trust, automation bias, and algorithm aversion; accurate external evidence (To Err Is Human, Makary 2016, Obermeyer 2019, Topol 2019, FDA AI/ML SaMD Action Plan, ASME V&V 40-2018); and the advocacy and communication science set. | 14 |

## What is new versus the prior review

The prior review's `narrative_refs.bib` is oriented to legislative advocacy. This
framework keeps the accurate external evidence and the advocacy-science set, drops
the budget-process reference that does not bear on a clinician's decision, and adds
the three landmark references that define this framework's organizing concept of
**calibrated trust**:

| Added reference | Why it anchors the framework |
|:--|:--|
| Lee and See (2004), *Trust in Automation* | Defines appropriate reliance: trust proportioned to demonstrated capability. |
| Dietvorst, Simmons, and Massey (2015), *Algorithm Aversion* | The under-trust failure mode the framework guards against. |
| Goddard, Roudsari, and Wyatt (2012), *Automation Bias* | The over-trust failure mode, reviewed specifically in clinical decision support. |

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Author works and bill versions | `review/references/author_works.bib` | `author_works.bib` (verbatim) |
| External evidence and advocacy set | `review/references/narrative_refs.bib` | `framework_refs.bib` (carried, re-scoped) |

## License

CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
