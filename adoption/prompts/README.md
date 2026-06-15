# prompts - the submitted prompt and the run output

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Topic](https://img.shields.io/badge/Topic-Clinician%20confidence%20framework-8B2E3F.svg)](.)
[![Stages](https://img.shields.io/badge/Stages-Mermaid%20%E2%86%92%20draft%20%E2%86%92%20full%20%E2%86%92%20final-D08770.svg)](.)

This folder holds the single submitted prompt that drives the `adoption/` build
and the markdown output of the run.

| File | Purpose |
|:--|:--|
| [`prompt-adoption.md`](prompt-adoption.md) | The submitted Master prompt verbatim, under a `## prompt-adoption` heading. |
| [`output-adoption.md`](output-adoption.md) | The full markdown output of the run, under a `## output-adoption` heading (the Claude Code narration, not the code files). |

## Relationship to the prior review

This is a **new paper topic** that is analogous in structure to the prior
legislative narrative review in [`../../review/`](../../review/) but does **not**
rewrite it. The prior review argues, through eight emotional pillars, that
legislators should enact the bill. This framework answers a different audience:
the practicing clinician who must decide, at the bedside, when to trust a verified
Physical AI system. The two works share the same verification-before-generation
mechanism, the same `#8B2E3F` template theme, the same strict palette, and the
same four-stage pipeline.

## How the build works

A single submitted prompt (`prompt-adoption.md`) drives two processes:

- **Process A** generated the four unique sub-prompts in
  [`../sub-prompts/`](../sub-prompts/).
- **Process B** runs those sub-prompts in sequence to grow the manuscript through
  four stages: the 20 colored Mermaid figures (`../mermaid/`), then
  `../draft-framework/` (scaffold with bracketed instructions naming exact source
  files), then `../full-framework/` (rendered prose), then `../final-framework/`
  (publication quality).

```
                prompts/prompt-adoption.md
                          |
                 Process A | generate sub-prompts
                          v
   sub-prompts/  ->  mermaid/  ->  draft-framework/  ->  full-framework/  ->  final-framework/
   (4 prompts)      (20 figs)     (scaffold +           (rendered prose,      (publication
                                   bracket cues)         TikZ figures)         quality)
                          |
                          v
            root CHANGELOG.md + releases.md + README.md  (v0.2.0)
```

## License

Released under CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit. Independent research draft; not enacted law and not legal advice.
