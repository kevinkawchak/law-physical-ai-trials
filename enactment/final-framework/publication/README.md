# publication - the deposit-ready manuscript (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-5%20final%20(publication)-4B0082.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-000080.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-7-4B0082.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-4B0082.svg)](.)
[![Enactment Paper DOI](https://img.shields.io/badge/Enactment%20DOI-10.5281%2Fzenodo.20726461-000080.svg)](https://doi.org/10.5281/zenodo.20726461)

[Final PDF and Source](https://doi.org/10.5281/zenodo.20726461). This directory is the deposit-ready mirror of the final-framework: the
submission-quality source a senior author would sign. It is identical to the parent
`final-framework/` source and is bundled separately as `LaTeX Source Files.zip` for
upload to Overleaf or a repository deposit. It does not rewrite the prior `review/`
or `adoption/` content. Note: a fifth AI generated \publication, pdf, and source code files were generated but were identical to the prior final version. A copy of the pdf is included in /enactment/pdfs/claude_code_manuscripts.  

## The eight questions and the provisions that answer them

This synthesis is reproduced from `tab:synthesis` in the manuscript.

| Question | The provision or evidence that answers it |
|:--|:--|
| Mandate | Three named gaps in existing law, tied to the record on preventable error |
| Authority | A commerce-power amendment to the FD&C Act adding section 515D, with a savings clause |
| Safety | The ten-gate VVUQ schedule and the three hard catastrophe predicates |
| Fiscal | A 58 million dollar authorization, no net mandatory spending, a 19 to 1 cost reduction |
| Constituents | A platform scaling to 50 through 100 sites across all regions |
| Bipartisanship | One provision two caucuses can each support on their own terms |
| Coalition | Clinicians, patients, industry, and the States; objections routed to citations |
| Passage path | Regular order in both chambers, known thresholds, a demonstrated platform |

## Files

```
publication/
  README.md         main.tex          passagestyle.sty
  references.bib    sections/         LaTeX Source Files.zip
```

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

No raster image is used; the ORCID mark is text-based and every figure is colored
TikZ in the strict palette black, grayscales, `#4B0082`, `#000080`, `#C0C0C0`.

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Certified figures and tables | [`../../verify-framework/`](../../verify-framework/) | every section |
| Finished prose | [`../../full-framework/`](../../full-framework/) | every section |
| Bill text and platform scope | `single-prompt-bill/...` and `physical-ai-oncology-trials/...` | citations |
| References | [`../../references/`](../../references/) | `references.bib` |

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending deposit.
