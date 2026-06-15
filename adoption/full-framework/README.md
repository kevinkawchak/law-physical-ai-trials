# full-framework - Stage 3: the rendered manuscript

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-3%20full%20(rendered)-8B2E3F.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-D08770.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-8-8B2E3F.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-8B2E3F.svg)](.)

This directory is the output of **Stage 3** (sub-prompt
[`../sub-prompts/prompt-3-full-framework.md`](../sub-prompts/prompt-3-full-framework.md)).
The full-framework processes every bracketed `[DRAFTING INSTRUCTIONS: ...]` left in
[`../draft-framework/`](../draft-framework/) and replaces it with finished, cited
prose drawn from the exact named sources. Every body section now carries a real
colored TikZ figure and a body-width table; no scaffolding bracket remains. It
compiles in Overleaf as committed and does not rewrite the prior review.

## What changed from the draft

| Draft (Stage 2) | Full (Stage 3) |
|:--|:--|
| Bracketed `[DRAFTING INSTRUCTIONS]` naming sources | Finished, cited prose drawn from those sources |
| Placeholder figures | 20 colored TikZ figures (2 introduction, 8 body, 10 appendix) |
| No tables | 8 body-width tables (`tab:competence` to `tab:workflow`), `\autoref` |
| Abstract as a bracket | A real abstract under 250 words |
| MAIN ACTIONS and KEY TERMS named | Adoption actions and key terms woven into the prose |

## Files

```
full-framework/
  README.md                 main.tex             frameworkstyle.sty
  references.bib            prompt-full-framework.md
  output-full-framework.md  full-framework-LaTeX.zip
  sections/
    abstract.tex        q3-transparency.tex   q7-accountability.tex
    introduction.tex    q4-oversight.tex      q8-workflow.tex
    q1-competence.tex   q5-equity.tex         appendix-figures.tex
    q2-safety.tex       q6-reliability.tex    back_matter.tex
```

## The eight body sections and their evidence

| # | Section | Figure | Table | Anchored in |
|:--|:--|:--|:--|:--|
| 1 | Competence | 3 | `tab:competence` | `topol2019high`; the assurance run (172 of 172) |
| 2 | Safety | 4 | `tab:safety` | `kohn2000toerr`; `makary2016medical`; the ten gates |
| 3 | Transparency | 5 | `tab:transparency` | `fda2021samd`; the hash-chained audit trail |
| 4 | Oversight | 6 | `tab:oversight` | `lee2004trust`; `goddard2012automation` |
| 5 | Equity | 7 | `tab:equity` | `obermeyer2019dissecting`; subgroup performance |
| 6 | Reliability | 8 | `tab:reliability` | `asme2018vv40`; drift and uncertainty |
| 7 | Accountability | 9 | `tab:accountability` | the signed SOP; the CFR and ICH adaptions |
| 8 | Workflow | 10 | `tab:workflow` | `dietvorst2015algorithm`; the patient journey |

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Visual theme and TikZ primitive | `review/template`; `../draft-framework/frameworkstyle.sty` | `frameworkstyle.sty` |
| Bracketed source cues to process | `../draft-framework/sections/` | every section |
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

`full-framework-LaTeX.zip` is the Overleaf-ready bundle. No raster image is used.

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit.
