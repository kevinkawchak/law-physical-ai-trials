# Published final-framework - Stage 4: the publication-quality manuscript

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-4%20final%20(publication)-8B2E3F.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-D08770.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-9-8B2E3F.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-8B2E3F.svg)](.)

[Final PDF and Source](https://doi.org/10.5281/zenodo.20710602). This directory is the output of **Stage 4** (sub-prompt
[`../sub-prompts/prompt-4-final-framework.md`](../sub-prompts/prompt-4-final-framework.md)).
The final-framework carries the full-framework to publication quality by
implementing the corrections identified from the full stage. It is the
submission-ready manuscript and compiles in Overleaf as committed. It does not
rewrite the prior review under `review/`.

## Corrections applied from the full-framework

| Correction | What was done |
|:--|:--|
| Vertical white bands | `\raggedbottom` replaces `\flushbottom`; `\tolerance` lowered to 1800 |
| Synthesis | A ninth table (`tab:synthesis`) maps all eight questions to the mechanism that answers each |
| Stranded tables | `\needspace` guard before every table (synthesis uses `\needspace{12\baselineskip}`) |
| Figure routing | The widest appendix figure (Figure 17) pulled inward to sit within the body measure |
| Symbols and dashes | Verified `\S` (never "SS") and single hyphens only; `--` only as TikZ edges |
| Even spacing | `\sloppy`, `\emergencystretch`, `microtype`, maximal widow and club penalties |

## Files

```
final-framework/
  README.md                  main.tex             frameworkstyle.sty
  references.bib             prompt-final-framework.md
  output-final-framework.md  final-framework-LaTeX.zip
  sections/
    abstract.tex        q3-transparency.tex   q7-accountability.tex
    introduction.tex    q4-oversight.tex      q8-workflow.tex
    q1-competence.tex   q5-equity.tex         appendix-figures.tex
    q2-safety.tex       q6-reliability.tex    back_matter.tex
```

## The eight questions and the mechanisms that answer them

This synthesis is reproduced from `tab:synthesis` in the manuscript.

| Question | The mechanism that answers it |
|:--|:--|
| Competence | Local validation and an assurance run (172 of 172 gate tests) |
| Safety | The ten-gate VVUQ examination and the catastrophe-predicate BLOCK |
| Transparency | Explainable output and a hash-chained audit trail |
| Oversight | Human-in-the-loop control, the ESCALATE path, and an override |
| Equity | Subgroup performance reporting and continuous bias surveillance |
| Reliability | Reproducibility checks, drift monitoring, and quantified uncertainty |
| Accountability | Named roles and a signed standard operating procedure |
| Workflow | Integration into the clinic day and consent, with continuous monitoring |

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Visual theme and TikZ primitive | `review/template`; `../full-framework/frameworkstyle.sty` | `frameworkstyle.sty` |
| Finished prose and figures | `../full-framework/` | every section |
| Colored Mermaid figures | `../mermaid/diagrams/` | the 20 colored TikZ figures |
| Clinician and evidence references | `../references/framework_refs.bib` | citations |
| Author works and bill versions | `../references/author_works.bib` | citations and the lineage |
| Verification evidence (ten gates, 172 tests) | `review/` | `q1`, `q2`, `q6` |

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

`final-framework-LaTeX.zip` is the Overleaf-ready bundle. No raster image is used.

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit.
