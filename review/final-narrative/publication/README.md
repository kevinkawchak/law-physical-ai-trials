# final-narrative edits - Stage 4: the publication manuscript

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-4%20final%20(publication)-8B2E3F.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-D08770.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-9-8B2E3F.svg)](sections/)
[![Compiles](https://img.shields.io/badge/Overleaf-pdfLaTeX-8B2E3F.svg)](.)
[![Review DOI](https://img.shields.io/badge/Review%20DOI-10.5281%2Fzenodo.20685379-D08770.svg)](https://doi.org/10.5281/zenodo.20685379)


[Publication PDF](https://doi.org/10.5281/zenodo.20685379). This directory is the output of **Stage 4** (sub-prompt
[`../sub-prompts/prompt-4-final-narrative.md`](../sub-prompts/prompt-4-final-narrative.md)).
The final-narrative carries the full-narrative to publication quality by
implementing the corrections identified from the full stage. It is the
submission-ready manuscript and compiles in Overleaf as committed.

## Corrections applied from the full-narrative

| Correction | What was done |
|:--|:--|
| Vertical white bands | `\raggedbottom` replaces `\flushbottom` so the page bottom is natural, not stretched |
| Stranded tables | `\needspace` before every table |
| Pillar to provision | A synthesis table maps all eight pillars to the exact provision of H. R. 9510 |
| Figure routing | Cleaner feedback-arrow routing and a width safety margin on the widest figure |
| Symbols and dashes | Verified "§" (never "SS") and single hyphens only |
| Even spacing | `\sloppy`, `\emergencystretch`, `microtype`, maximal widow and club penalties |

## Files

```
final-narrative/
  README.md                     main.tex             narrativestyle.sty
  references.bib                prompt-final-narrative.md
  output-final-narrative.md     final-narrative-LaTeX.zip
  sections/
    abstract.tex          s3-moral-outrage.tex   s7-trust.tex
    introduction.tex      s4-hope.tex            s8-urgency.tex
    s1-compassion.tex     s5-responsibility.tex  appendix-figures.tex
    s2-fear-of-harm.tex   s6-protection.tex      back_matter.tex
```

## Sources used from other directories (Rule 6)

| Asset | Upstream source | Used in |
|:--|:--|:--|
| Visual theme and TikZ primitive | `review/template`; the full-narrative `narrativestyle.sty` | `narrativestyle.sty` |
| Finished prose and figures | `review/full-narrative/` | every section |
| Colored Mermaid figures | `review/mermaid/diagrams/` | the 20 colored TikZ figures |
| Advocacy and evidence references | `review/references/narrative_refs.bib` | citations |
| Author works and bill versions | `review/references/author_works.bib` | lineage and the synthesis table |
| Verification evidence | `cancer-automated/.../papers/VVUQ-02` | fear and trust sections |

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
