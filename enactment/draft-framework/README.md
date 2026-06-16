# draft-framework - Stage 2: the scaffold (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-2%20draft%20(scaffold)-4B0082.svg)](.)
[![Sections](https://img.shields.io/badge/Body%20sections-8-000080.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-4B0082.svg)](.)

This directory is the output of **Stage 2** (sub-prompt
[`../sub-prompts/prompt-2-draft-passage.md`](../sub-prompts/prompt-2-draft-passage.md)).
The draft-framework is the scaffold: it lays out the full manuscript structure for
the H. R. 9510 passage framework and leaves bracketed `[DRAFTING INSTRUCTIONS: ...]`
in every body section naming the exact files the full, verify, and final stages
process. It compiles in Overleaf as committed and does not rewrite the prior
`review/` or `adoption/` content.

## Files

```
draft-framework/
  README.md              main.tex              passagestyle.sty
  references.bib         prompt-draft-passage.md
  output-draft-passage.md  draft-framework-LaTeX.zip
  sections/
    abstract.tex       q3-safety.tex          q7-coalition.tex
    introduction.tex   q4-fiscal.tex          q8-passage.tex
    q1-mandate.tex     q5-constituents.tex    appendix-figures.tex
    q2-authority.tex   q6-bipartisanship.tex  back_matter.tex
```

## The eight passage questions (one section each)

| # | Section | The question it answers |
|:--|:--|:--|
| 1 | `q1-mandate.tex` | Is the problem real enough to need a Federal statute? |
| 2 | `q2-authority.tex` | Is this within Congress's power and consistent with existing law? |
| 3 | `q3-safety.tex` | What in the bill actually protects patients? |
| 4 | `q4-fiscal.tex` | What does it cost, and is it paid for? |
| 5 | `q5-constituents.tex` | Who does this help back home? |
| 6 | `q6-bipartisanship.tex` | Can one caucus support it without losing the other? |
| 7 | `q7-coalition.tex` | Who is behind it, and is the opposition manageable? |
| 8 | `q8-passage.tex` | Can it move through both chambers and then work? |

## Palette and figure discipline

The accent is `#4B0082` (indigo); figures use only black, grayscales, `#4B0082`,
`#000080` (navy), and `#C0C0C0` (silver). The `psgfig` TikZ primitive reproduces each
Mermaid figure with no raster image, and `\psgcaption` places a uniform
`\vspace{-0.75cm}` between every figure and its caption.

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Template appearance, TikZ primitive, table columns | [`adoption/final-framework/publication/frameworkstyle.sty`](../../adoption/final-framework/publication/frameworkstyle.sty) | `passagestyle.sty` |
| TOC and back-matter conventions | [`adoption/final-framework`](../../adoption/final-framework) | `main.tex`, `back_matter.tex` |
| Bill text (sections and appendices) | `single-prompt-bill/auto-bill-02/final-bill/publication` | every body section's bracket |
| Platform scope | `physical-ai-oncology-trials/national-platform/new_paper/final_paper` | q1, q5 brackets |
| Colored Mermaid catalog | [`../mermaid/`](../mermaid/) | figure slots |
| References | [`../references/`](../references/) | `references.bib` |

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

`draft-framework-LaTeX.zip` is the Overleaf-ready bundle. No raster image is used.

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
