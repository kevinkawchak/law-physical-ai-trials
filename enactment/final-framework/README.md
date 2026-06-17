# final-framework - Stage 5: the publication-quality manuscript (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-5%20final%20(publication)-4B0082.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-000080.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-7-4B0082.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-4B0082.svg)](.)
[![Enactment Paper DOI](https://img.shields.io/badge/Enactment%20DOI-10.5281%2Fzenodo.20726461-000080.svg)](https://doi.org/10.5281/zenodo.20726461)

[Final PDF and Source](https://doi.org/10.5281/zenodo.20726461). This directory is the output of **Stage 5** (sub-prompt
[`../sub-prompts/prompt-5-final-passage.md`](../sub-prompts/prompt-5-final-passage.md)).
The final-framework carries the verify-stage sources to publication quality. It is
the submission-ready manuscript and compiles in Overleaf as committed. It does not
rewrite the prior `review/` or `adoption/` content.

## Finishing applied from the verify stage

| Correction | What was done |
|:--|:--|
| Vertical white bands | `\raggedbottom` replaces `\flushbottom`; `\tolerance` lowered to 1800 |
| Synthesis | A ninth table (`tab:synthesis`) maps all eight questions to the provision that answers each |
| Certified figures | The twenty figures keep the geometry the verify stage certified (serpentine path, even pitch, widened spacing) |
| Caption gap | The uniform `\vspace{-0.75cm}` figure-to-caption gap is preserved |
| Symbols and dashes | Section symbol (never "SS") and single hyphens only; `--` only as TikZ edges |
| Citations | `ieeetr` with `\nocite{*}` so every entry renders with a clickable resolver |

## Files

```
final-framework/
  README.md              main.tex             passagestyle.sty
  references.bib         prompt-final-passage.md
  output-final-passage.md  final-framework-LaTeX.zip
  sections/
    abstract.tex       q3-safety.tex          q7-coalition.tex
    introduction.tex   q4-fiscal.tex          q8-passage.tex
    q1-mandate.tex     q5-constituents.tex    appendix-figures.tex
    q2-authority.tex   q6-bipartisanship.tex  back_matter.tex
  publication/           the deposit-ready mirror (+ LaTeX Source Files.zip)
```

## The eight questions and the provisions that answer them

This synthesis is reproduced from `tab:synthesis` in the manuscript.

| Question | The provision or evidence that answers it |
|:--|:--|
| Mandate | Three named gaps in existing law, tied to the record on preventable error |
| Authority | A commerce-power amendment to the FD&C Act adding section 515D, with a savings clause |
| Safety | The ten-gate VVUQ schedule and the three hard catastrophe predicates |
| Fiscal | A 58 million dollar authorization, no net mandatory spending, a 19 to 1 reduction |
| Constituents | A platform scaling to 50 through 100 sites across all regions |
| Bipartisanship | One provision two caucuses can each support on their own terms |
| Coalition | Clinicians, patients, industry, and the States; objections routed to citations |
| Passage path | Regular order in both chambers, known thresholds, a demonstrated platform |

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Certified figures and optimized tables | [`../verify-framework/`](../verify-framework/) | every section |
| Finished prose | [`../full-framework/`](../full-framework/) | every section |
| Template appearance and TikZ primitive | [`adoption/final-framework/publication`](../../adoption/final-framework/publication) | `passagestyle.sty` |
| Bill text and platform scope | `single-prompt-bill/...`; `physical-ai-oncology-trials/...` | citations |
| Colored Mermaid catalog | [`../mermaid/`](../mermaid/) | the 20 colored TikZ figures |
| References | [`../references/`](../references/) | `references.bib` |

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
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
