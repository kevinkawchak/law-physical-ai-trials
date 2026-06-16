# prompts - the submitted prompt and the run output (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Stage](https://img.shields.io/badge/Process-A%20%2B%20B%20driver-4B0082.svg)](.)
[![Topic](https://img.shields.io/badge/Topic-H.R.%209510%20passage%20framework-000080.svg)](.)

This folder holds the single prompt that drives the entire `enactment/` build and
the markdown narrative of the run, mirroring `adoption/prompts/` and
`review/prompts/`.

## Files

| File | Contents |
|:--|:--|
| [`prompt-enactment.md`](prompt-enactment.md) | The submitted Master prompt, verbatim, under a `## prompt-enactment` heading. |
| [`output-enactment.md`](output-enactment.md) | The markdown narrative of the run (reasoning and build schedule), under an `## output-enactment` heading. Not the source files. |
| `README.md` | This file. |

## How the prompt drives the build

```
prompts/prompt-enactment.md
          |
 Process A | generate five sub-prompts
          v
sub-prompts/ -> mermaid/ -> draft-framework/ -> full-framework/ -> verify-framework/ -> final-framework/
          |
          v
 root CHANGELOG.md + releases.md + README.md  (v0.3.0)
```

Process A reads the submitted prompt and writes the five sub-prompts in
[`../sub-prompts/`](../sub-prompts/). Process B runs them in sequence to grow the
passage framework from a colored Mermaid catalog to a publication-quality
manuscript, adding a new `verify-framework/` stage between the full and final
source files that double-checks every table and figure.

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Prompt-and-output convention (`## heading` + verbatim text) | [`adoption/prompts/`](../../adoption/prompts/) | this folder |
| Two-process build methodology (Process A and Process B) | [`adoption/`](../../adoption/) and [`review/`](../../review/) | the whole build |

## License

Released under CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
