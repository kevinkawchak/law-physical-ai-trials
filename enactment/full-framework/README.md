# full-framework - Stage 3: the rendered manuscript (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-3%20full%20(rendered)-4B0082.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-000080.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-6-4B0082.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-4B0082.svg)](.)

This directory is the output of **Stage 3** (sub-prompt
[`../sub-prompts/prompt-3-full-passage.md`](../sub-prompts/prompt-3-full-passage.md)).
The full-framework replaces every bracketed instruction in the draft with finished
prose drawn from the named sources, renders all twenty colored TikZ figures, and
completes every table. It compiles in Overleaf as committed and does not rewrite the
prior `review/` or `adoption/` content.

## Files

```
full-framework/
  README.md              main.tex              passagestyle.sty
  references.bib         prompt-full-passage.md
  output-full-passage.md  full-framework-LaTeX.zip
  sections/
    abstract.tex       q3-safety.tex          q7-coalition.tex
    introduction.tex   q4-fiscal.tex          q8-passage.tex
    q1-mandate.tex     q5-constituents.tex    appendix-figures.tex
    q2-authority.tex   q6-bipartisanship.tex  back_matter.tex
```

## What each section now contains

| Section | Figure | Table |
|:--|:--|:--|
| Introduction | Fig 1 (eight-question path) | Key terms |
| Mandate | Fig 2 (three gaps) | Gaps in existing law |
| Authority | Fig 3 (federalism) | Rule-of-construction map |
| Safety | Fig 4 (verification before generation) | Ten-gate schedule |
| Fiscal | Fig 5 (cost asymmetry) | Authorization schedule |
| Constituents | Fig 6 (national rollout) | Benefit by phase |
| Bipartisanship | Fig 7 (convergence) | -- |
| Coalition | Fig 8 (coalition) | -- |
| Passage path | Fig 9 (capstone) | -- |
| Appendix A | Fig 10 to Fig 20 (eleven exhibits) | -- |

## Palette and figure discipline

Figures use only black, grayscales, `#4B0082`, `#000080`, and `#C0C0C0`. Each figure
keeps a uniform `\vspace{-0.75cm}` between the figure and its caption, every curved
arrow carries an explicit looseness, and box spacing is even. These are audited in
the verify stage.

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Draft scaffold and bracket plan | [`../draft-framework/`](../draft-framework/) | every section |
| Bill text (findings, 515D, financial) | `single-prompt-bill/auto-bill-02/final-bill/publication` | q1 to q4, q7, q8 |
| Platform scope and simulation evidence | `physical-ai-oncology-trials/national-platform/new_paper/final_paper` | q5, q8, Fig 15 |
| Colored Mermaid catalog | [`../mermaid/`](../mermaid/) | all 20 TikZ figures |
| References | [`../references/`](../references/) | `references.bib` |

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

`full-framework-LaTeX.zip` is the Overleaf-ready bundle. No raster image is used.

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
