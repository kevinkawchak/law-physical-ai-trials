# sub-prompts - Process A output (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Sub-prompts](https://img.shields.io/badge/Sub--prompts-5-4B0082.svg)](.)
[![New stage](https://img.shields.io/badge/New-verify%20stage-000080.svg)](prompt-4-verify-passage.md)
[![Method](https://img.shields.io/badge/Method-Self--learning%20draft%20to%20final-C0C0C0.svg)](.)

This folder is the output of **Process A**: from the single submitted prompt in
[`../prompts/prompt-enactment.md`](../prompts/prompt-enactment.md), five unique,
comprehensive sub-prompts were generated that **Process B** then runs in sequence to
grow the H. R. 9510 passage framework from a colored Mermaid catalog to a
publication-quality manuscript. The method is adapted from the prior adoption build
([`../../adoption/sub-prompts/`](../../adoption/sub-prompts/)) and extended with a
new verification stage between the full and final source files. It is a new paper
topic and does not rewrite the prior adoption framework or review.

## The five sub-prompts

| # | Sub-prompt | Runs in stage | Adapted from (prior sources) |
|:--|:--|:--|:--|
| 1 | [`prompt-1-mermaid.md`](prompt-1-mermaid.md) | `../mermaid/` | `adoption/sub-prompts/prompt-1-mermaid.md`; `adoption/mermaid/` |
| 2 | [`prompt-2-draft-passage.md`](prompt-2-draft-passage.md) | `../draft-framework/` | `adoption/sub-prompts/prompt-2-draft-framework.md`; `adoption/final-framework` (TOC and back matter) |
| 3 | [`prompt-3-full-passage.md`](prompt-3-full-passage.md) | `../full-framework/` | `adoption/sub-prompts/prompt-3-full-framework.md`; `adoption/full-framework` |
| 4 | [`prompt-4-verify-passage.md`](prompt-4-verify-passage.md) | `../verify-framework/` | **New stage** (table and figure double-verification) |
| 5 | [`prompt-5-final-passage.md`](prompt-5-final-passage.md) | `../final-framework/` | `adoption/sub-prompts/prompt-4-final-framework.md`; `adoption/final-framework` |

## What is new in this build (the adaptation)

1. **Target.** Every prompt targets `kevinkawchak/law-physical-ai-trials`,
   `enactment/`, and the single objective of passing H. R. 9510 in both the House
   and the Senate; repository release **v0.3.0**.
2. **Subject.** An evidence-paired passage framework with eight body sections
   (mandate, authority, safety, fiscal, constituents, bipartisanship, coalition,
   passage path), each pairing a legislator's question with a cited fact from the
   bill text, the platform, and the public record.
3. **A new verification stage.** Sub-prompt 4 inserts `verify-framework/` between the
   full and final source files. It runs a table-and-figure audit, performed twice
   for figures, that certifies the uniform `\vspace{-0.75cm}` figure-to-caption gap,
   optimized column widths, no text-box and arrow overlaps, explicit looseness on
   every curved arrow, and even box spacing, before publication polish.
4. **Palette and template.** Figures use only black, grayscales, `#4B0082` (indigo),
   `#000080` (navy), and `#C0C0C0` (silver); the paper template color is `#4B0082`.
   No raster image. Every Mermaid figure is reproduced as colored TikZ.
5. **References.** The author reference set is trimmed to the works that bear on
   legislation, regulation, and the platform; topic references are added with
   working URLs to professional sources and journals.

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Four-stage sub-prompt methodology | [`adoption/sub-prompts/`](../../adoption/sub-prompts/) | all five sub-prompts |
| Template appearance and TikZ primitive | [`adoption/final-framework/publication`](../../adoption/final-framework/publication) | sub-prompts 2, 3, 5 |
| Bill text (most recent version) | `single-prompt-bill/auto-bill-02/final-bill/publication` | sub-prompts 2, 3, 5 |
| Clinical-trial platform scope | `physical-ai-oncology-trials/national-platform/new_paper/final_paper` | sub-prompts 2, 3, 5 |

## License

Released under CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
