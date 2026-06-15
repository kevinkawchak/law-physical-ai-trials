# draft-framework - Stage 2: the scaffold

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-2%20draft%20(scaffold)-8B2E3F.svg)](.)
[![Sections](https://img.shields.io/badge/Body%20sections-8%20questions-D08770.svg)](sections/)
[![Figures](https://img.shields.io/badge/Placeholder%20figures-10-8B2E3F.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-8B2E3F.svg)](.)

This directory is the output of **Stage 2** (sub-prompt
[`../sub-prompts/prompt-2-draft-framework.md`](../sub-prompts/prompt-2-draft-framework.md)).
The draft-framework is the scaffold: it lays out the full manuscript structure on
the reused template theme and, in every body section, leaves bracketed
`[DRAFTING INSTRUCTIONS: ...]` that name the exact repository files and directories
the full-framework and final-framework stages must process. It compiles in Overleaf
as committed and does not rewrite the prior review under `review/`.

## How the scaffold works

Each body section opens with a short framing of the confidence question, then a
bracket that points the next stage to the exact source (a `framework_refs.bib` key,
an `author_works.bib` key, the verification evidence carried in `review/`, the
Mermaid figure slot to reproduce, and the body-width table to build), then a
labeled placeholder `cfwfig` figure with a caption. The full-framework replaces
every bracket with finished, cited prose and renders the real figures and tables.

## Files

```
draft-framework/
  README.md                  main.tex             frameworkstyle.sty
  references.bib             prompt-draft-framework.md
  output-draft-framework.md  draft-framework-LaTeX.zip
  sections/
    introduction.tex   q3-transparency.tex   q6-reliability.tex
    q1-competence.tex  q4-oversight.tex      q7-accountability.tex
    q2-safety.tex      q5-equity.tex         q8-workflow.tex
    back_matter.tex
```

## The eight body sections (CONFIDENCE GOALS)

| # | File | Confidence question |
|:--|:--|:--|
| 1 | `q1-competence.tex` | Is it actually good at this, or only good on paper? |
| 2 | `q2-safety.tex` | What stops it before it hurts someone? |
| 3 | `q3-transparency.tex` | Can I see why it did that? |
| 4 | `q4-oversight.tex` | Am I still in control? |
| 5 | `q5-equity.tex` | Does it work for the patient in front of me? |
| 6 | `q6-reliability.tex` | Will it be the same tomorrow, at 3 a.m.? |
| 7 | `q7-accountability.tex` | Who is responsible when it is wrong? |
| 8 | `q8-workflow.tex` | Does it fit how I actually work? |

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Visual theme, columns, abstract box | `review/template/tmpl20style.sty` | `frameworkstyle.sty` |
| TOC and back matter conventions | `review/final-narrative` | `main.tex`, `sections/back_matter.tex` |
| Colored Mermaid figure slots | `../mermaid/diagrams/` | placeholder `cfwfig` figures and bracket cues |
| Clinician and evidence references | `../references/framework_refs.bib` | `references.bib`, bracket cues |
| Author works and bill versions | `../references/author_works.bib` | `references.bib`, bracket cues |
| Verification evidence (ten gates, 172 tests) | `review/` | `q1`, `q2`, `q6` bracket cues |

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

`draft-framework-LaTeX.zip` is the Overleaf-ready bundle (main.tex,
frameworkstyle.sty, references.bib, and sections/). No raster image is used; the
text-based ORCID mark needs no file.

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit.
