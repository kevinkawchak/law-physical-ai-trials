# prompts - the submitted prompt and its narrative output

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Stage-Bootstrap%20(Process%20A)-8B2E3F.svg)](.)
[![Agent](https://img.shields.io/badge/Agent-Claude%20Code%20Opus%204.8%20(1M)-D08770.svg)](.)

This folder preserves the single submitted Master prompt verbatim and the full
narrative output of the run, following the convention used in the author's prior
builds (`single-prompt-bill/auto-bill-02/master-prompt.md` and the paired
`output-*.md` files). It is the provenance record for the entire
`law-physical-ai-trials/review` narrative project.

## Files

| File | Purpose |
|:--|:--|
| `prompt-narrative.md` | The entire submitted prompt, word for word, under a single `## prompt-narrative` heading. Nothing else is added. |
| `output-narrative.md` | The entire Claude Code markdown output of the run, under a single `## output-narrative` heading (the narrative output, not the source files). Written in the final update. |
| `README.md` | This file. |

## How this folder is used by the rest of the project

The submitted prompt in `prompt-narrative.md` defines the four-stage
SUB-PROMPT SCHEDULE that drives every other directory under `review/`:

1. `../sub-prompts/` - Process A reads this prompt and emits four unique
   sub-prompts.
2. `../mermaid/` - Stage 1 produces the 20+ colored Mermaid figures.
3. `../draft-narrative/`, `../full-narrative/`, `../final-narrative/` - Stages 2,
   3, and 4 grow the manuscript from scaffold to publication quality.

The SECTION GOALS, BACKGROUND, MAIN ACTIONS, and KEY TERMS blocks of the prompt
are the source material for the eight body sections of the narrative paper, and
the references embedded in the BACKGROUND block are carried into
`../references/narrative_refs.bib`.

## License

Released under CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
