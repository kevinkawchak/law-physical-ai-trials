# draft-narrative - Stage 2: the scaffold

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-2%20draft%20(scaffold)-8B2E3F.svg)](.)
[![Sections](https://img.shields.io/badge/Body%20sections-8-D08770.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-8B2E3F.svg)](.)

This directory is the output of **Stage 2** (sub-prompt
[`../sub-prompts/prompt-2-draft-narrative.md`](../sub-prompts/prompt-2-draft-narrative.md)).
The draft-narrative is the scaffold: it sets the manuscript structure on the
reused template theme and, in every body section, leaves bracketed
`[DRAFTING INSTRUCTIONS: ...]` that name the exact repository files the
full-narrative and final-narrative stages must process. It compiles in Overleaf
exactly as committed.

## Files

```
draft-narrative/
  README.md                    (this file)
  main.tex                     (cover, abstract, TOC, \input lines)
  narrativestyle.sty           (template theme + colored TikZ Mermaid primitive)
  references.bib               (advocacy + evidence + author lineage; 55 entries)
  prompt-draft-narrative.md    (the generating sub-prompt, verbatim)
  output-draft-narrative.md    (the narrative output of this stage)
  draft-narrative-LaTeX.zip    (the Overleaf bundle)
  sections/
    introduction.tex           s4-hope.tex          s8-urgency.tex
    s1-compassion.tex          s5-responsibility.tex back_matter.tex
    s2-fear-of-harm.tex        s6-protection.tex
    s3-moral-outrage.tex       s7-trust.tex
```

## One section file per section

| Section file | Body section (SECTION GOAL) |
|:--|:--|
| `sections/introduction.tex` | Introduction and definitions |
| `sections/s1-compassion.tex` | 1. Compassion and empathy |
| `sections/s2-fear-of-harm.tex` | 2. Fear of preventable harm |
| `sections/s3-moral-outrage.tex` | 3. Moral outrage |
| `sections/s4-hope.tex` | 4. Hope |
| `sections/s5-responsibility.tex` | 5. Responsibility and duty |
| `sections/s6-protection.tex` | 6. Protection of vulnerable people |
| `sections/s7-trust.tex` | 7. Trust and reassurance |
| `sections/s8-urgency.tex` | 8. Urgency |
| `sections/back_matter.tex` | Acknowledgments, Ethics, Rights, Cite, Data |

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Visual theme, columns, abstract box | `review/template/tmpl20style.sty` | `narrativestyle.sty` |
| TOC and back-matter conventions | `cancer-automated/.../VVUQ-02/final-paper` | `main.tex`, `sections/back_matter.tex` |
| Colored Mermaid figures | `review/mermaid/diagrams/` | every section figure placeholder |
| Advocacy science and external evidence | `review/references/narrative_refs.bib` | bracketed cues; `references.bib` |
| Author works and bill versions | `review/references/author_works.bib` | bracketed cues; `references.bib` |
| Verification evidence (ten gates, 172 tests) | `cancer-automated/.../papers/VVUQ-02` | `s2`, `s7` bracketed cues |

## Compile (Overleaf, pdfLaTeX)

```
pdflatex main
bibtex   main
pdflatex main
pdflatex main
```

## License

CC BY 4.0. Reproduced public-domain U.S. Government text is used under 17 U.S.C.
§ 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
