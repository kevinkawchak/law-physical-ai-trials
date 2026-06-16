# verify-framework - Stage 4: the table and figure audit (v0.3.0, new stage)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-4%20verify%20(new)-4B0082.svg)](.)
[![Figures audited](https://img.shields.io/badge/Figures%20audited%20twice-20-000080.svg)](verification-report.md)
[![Tables audited](https://img.shields.io/badge/Tables%20audited-6-4B0082.svg)](verification-report.md)

This directory is the output of **Stage 4** (sub-prompt
[`../sub-prompts/prompt-4-verify-passage.md`](../sub-prompts/prompt-4-verify-passage.md)),
a stage that is **new to the v0.3.0 build** and has no analogue in the prior
`adoption/` pipeline. It is inserted between the full and final source files to
double-verify that every table and every figure is correct before the manuscript is
carried to publication quality. It does not rewrite the prior `review/` or
`adoption/` content.

## What this stage produces

- [`verification-report.md`](verification-report.md): the full audit, table by table
  and figure by figure, with a verdict for each test and each figure verified twice.
- The corrected source files: `main.tex`, `passagestyle.sty`, `references.bib`, and
  the twelve `sections/*.tex`, identical in prose to the full stage but with the
  certified figure and table fixes applied.
- `verify-framework-LaTeX.zip`: the Overleaf-ready bundle of the corrected sources.

## The three figure checks (each figure, twice)

| Check | What it confirms |
|:--|:--|
| (a) No text box and arrow overlaps | No connector passes through a node and no label sits on a box |
| (b) Explicit looseness on every curved arrow | Every `to[...]` curve carries a `looseness=` value appropriate to the bend |
| (c) Proper spacings between boxes | Node pitch is even and no two boxes touch |

Plus the uniform `\vspace{-0.75cm}` figure-to-caption gap and the strict palette.

## Corrections certified

| Item | Fix |
|:--|:--|
| Figure 1 (eight-question path) | Rerouted as a serpentine; the wrap is a short straight vertical link, so no edge crosses a box |
| Figure 16 (two-chamber strategy) | Node pitch evened to 3.7 throughout |
| Figure 19 (objection handling) | Vertical box pitch widened 1.0 to 1.4 so two-line boxes do not touch |
| Table `tab:terms` | Term column widened to 3.6 cm |
| Table `tab:gates` | Gate column widened to 3.75 cm, numeric columns trimmed |

All other figures and tables passed both checks unchanged.

## Files

```
verify-framework/
  README.md                  verification-report.md
  main.tex                   passagestyle.sty
  references.bib             prompt-verify-passage.md
  output-verify-passage.md   verify-framework-LaTeX.zip
  sections/  (the twelve corrected section files)
```

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Rendered prose, figures, and tables (input to the audit) | [`../full-framework/`](../full-framework/) | every file |
| Figure and table instructions | [`../sub-prompts/prompt-4-verify-passage.md`](../sub-prompts/prompt-4-verify-passage.md) | the audit |

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

## License

CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
