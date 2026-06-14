# review - narrative review supporting the H. R. 9510 transition to law

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Bill](https://img.shields.io/badge/Bill-H.%20R.%209510%20v5.0-8B2E3F.svg)](https://doi.org/10.5281/zenodo.20619762)
[![Stages](https://img.shields.io/badge/Stages-Mermaid%20%E2%86%92%20draft%20%E2%86%92%20full%20%E2%86%92%20final-D08770.svg)](.)
[![Sections](https://img.shields.io/badge/Body%20sections-8%20emotional%20pillars-8B2E3F.svg)](.)
[![Media](https://img.shields.io/badge/Media-Tables%20%2B%20ASCII%20%2B%20colored%20Mermaid-lightgrey.svg)](.)
[![Agent](https://img.shields.io/badge/Agent-Claude%20Code%20Opus%204.8%20(1M)-D08770.svg)](.)
[![Bill DOI](https://img.shields.io/badge/Bill%20DOI-10.5281%2Fzenodo.20619762-EBCB8B.svg)](https://doi.org/10.5281/zenodo.20619762)

[Publication PDF](https://doi.org/10.5281/zenodo.20685379). This directory holds the entire narrative review that supports the transition of
Physical AI Trial Bill **H. R. 9510 v5.0** into a new Federal AI law. The review
is a single, growing manuscript written for legislators in medical AI who have
neither robotics experience nor Claude Code and Codex application experience. 

## How the build works

A single submitted prompt (`prompts/prompt-narrative.md`) drives two processes:

- **Process A** generated the four unique sub-prompts in `sub-prompts/`.
- **Process B** runs those sub-prompts in sequence to grow the manuscript through
  four stages: the 20+ colored Mermaid figures (`mermaid/`), then
  `draft-narrative/` (scaffold with bracketed instructions naming exact source
  files), then `full-narrative/` (rendered prose), then `final-narrative/`
  (publication quality).

```
                prompts/prompt-narrative.md
                          |
                 Process A | generate sub-prompts
                          v
   sub-prompts/  ->  mermaid/  ->  draft-narrative/  ->  full-narrative/  ->  final-narrative/
   (4 prompts)      (21 figs)     (scaffold +          (rendered prose,      (publication
                                   bracket cues)        TikZ figures)         quality)
                          |
                          v
            root CHANGELOG.md + releases.md + README.md  (v0.1.0)
```

## The eight body sections (SECTION GOALS)

| # | Section | Emotional pillar | Guiding appeal |
|:--|:--|:--|:--|
| 1 | Compassion and empathy | care for the patient | "What happens if we do nothing?" |
| 2 | Fear of preventable harm | avoidance of loss | "Without this law, more people will suffer." |
| 3 | Moral outrage | fairness | "This should not happen in America." |
| 4 | Hope | opportunity | "We can save lives if we act." |
| 5 | Responsibility and duty | obligation | "You have the power to prevent this." |
| 6 | Protection of vulnerable people | protection | bias, consent, and subgroup safety |
| 7 | Trust and reassurance | confidence | "This technology can be trusted." |
| 8 | Urgency | timeliness | "Patients are waiting now." |

## Directory map

```
review/
  README.md                  (this file)
  prompts/                   the submitted prompt and the run output
    prompt-narrative.md      (verbatim Master prompt)
    output-narrative.md      (full markdown output, written in the release update)
    README.md
  sub-prompts/               Process A output (four sub-prompts)
    prompt-1-mermaid.md      prompt-3-full-narrative.md
    prompt-2-draft-narrative.md  prompt-4-final-narrative.md
    README.md
  references/                shared bibliography
    author_works.bib         (the author's prior works and every bill version)
    narrative_refs.bib       (advocacy science + accurate external evidence)
    README.md
  template/                  the reused paper template (unchanged visual theme)
  mermaid/                   Stage 1: 21 colored Mermaid figures + catalog
  draft-narrative/           Stage 2: scaffold with bracketed source cues
  full-narrative/            Stage 3: rendered manuscript
  final-narrative/           Stage 4: publication-quality manuscript
```

## Sources used from other repositories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Paper template (theme, columns, ORCID mark) | `law-physical-ai-trials/review/template` | every narrative stage |
| Colored Mermaid families and palette discipline | `Clinical-AI-Demos/.../ai-outputs/output-01` | `mermaid/`; every figure |
| Table of contents and back matter conventions | `cancer-automated/.../papers/VVUQ-02/final-paper` | `draft-narrative/` onward |
| Verification evidence (ten gates, 172 tests) | `cancer-automated/.../papers/VVUQ-02` | `s2`, `s7` body sections |
| Sub-prompt and auto-commit methodology | `single-prompt-bill/.../auto-bill-02` and its `sub-prompts/` | `sub-prompts/`; the build schedule |
| Author works and every bill version | `review/references/author_works.bib` | the evidence-to-law lineage |

## Visual media and palette

No raster images are used. The permitted media are full-width white-background
tables, monospace ASCII figures, and colored Mermaid diagrams (native in
Markdown, reproduced as colored TikZ in the compiled LaTeX). The strict palette
is black, grayscales, and `#EBCB8B` (gold, hope), `#D08770` (clay, risk), and
`#8B2E3F` (burgundy, the Act). The `#8B2E3F` paper template theme is preserved.

## License

Released under CC BY 4.0; reproduced public-domain U.S. Government text is used
under 17 U.S.C. § 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit. Independent research draft; not enacted law and not legal advice.
