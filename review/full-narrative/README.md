# full-narrative - Stage 3: the rendered manuscript

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-3%20full%20(rendered)-8B2E3F.svg)](.)
[![Figures](https://img.shields.io/badge/TikZ%20figures-20-D08770.svg)](sections/)
[![Tables](https://img.shields.io/badge/Body--width%20tables-8-8B2E3F.svg)](sections/)

This directory is the output of **Stage 3** (sub-prompt
[`../sub-prompts/prompt-3-full-narrative.md`](../sub-prompts/prompt-3-full-narrative.md)).
The full-narrative processes every bracketed instruction left in the draft and
replaces it with finished prose drawn from the exact named sources. No
scaffolding brackets remain. It compiles in Overleaf as committed.

## What changed from the draft

- Every `[DRAFTING INSTRUCTIONS: ...]` is now finished, cited prose.
- Each body section carries one colored TikZ figure and one body-width table, and
  the appendix reproduces the remaining catalog diagrams, for 20 figures in the
  manuscript (plus the 21 in the Markdown catalog).
- The MAIN ACTIONS (advocacy, coalition building, policy entrepreneurship,
  reconciliation) and KEY TERMS (testimony, committee hearings, markup) are woven
  into the responsibility and fear sections.
- Each emotional appeal is paired with a cited fact and closes on a specific
  provision of H. R. 9510.

## Files

```
full-narrative/
  README.md                    main.tex            narrativestyle.sty
  references.bib               prompt-full-narrative.md
  output-full-narrative.md     full-narrative-LaTeX.zip
  sections/
    abstract.tex          s3-moral-outrage.tex   s7-trust.tex
    introduction.tex      s4-hope.tex            s8-urgency.tex
    s1-compassion.tex     s5-responsibility.tex  appendix-figures.tex
    s2-fear-of-harm.tex   s6-protection.tex      back_matter.tex
```

## Sources used from other directories (Rule 6)

| Section | Sources processed |
|:--|:--|
| Introduction | `Kawchak2026HR9510Bill`; Mermaid 01, 02; `novak2020patient`, `moreland2015hearing` |
| 1 Compassion | `Kawchak2026CancerPatientsJourney`; `novak2020patient`; Mermaid 11 |
| 2 Fear of harm | `kohn2000toerr`, `makary2016medical`; VVUQ-02; Mermaid 04, 20 |
| 3 Moral outrage | `obermeyer2019dissecting`; `Kawchak2026PatientPriorityProposedU`; Mermaid 15 |
| 4 Hope | `topol2019high`; simulation lineage; Mermaid 06 |
| 5 Responsibility | `moreland2015hearing`; MAIN ACTIONS, KEY TERMS; Mermaid 03, 14 |
| 6 Protection | `obermeyer2019dissecting`, `fda2021samd`; CFR Part 50; Mermaid 15 |
| 7 Trust | `asme2018vv40`; VVUQ-02 ten gates; Mermaid 10, 07, 17 |
| 8 Urgency | `kok2013finding`, `fda2021samd`; Mermaid 16, 21 |

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
