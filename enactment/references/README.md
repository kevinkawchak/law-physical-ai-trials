# references - the evidence base for the passage framework (v0.3.0)

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-C0C0C0.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Author works](https://img.shields.io/badge/Author%20works-21%20(trimmed)-4B0082.svg)](author_works.bib)
[![Topic refs](https://img.shields.io/badge/Topic%20refs-24-000080.svg)](passage_refs.bib)

Two BibTeX files supply every citation in the `enactment/` manuscript. They are
copied into each stage's `references.bib` so each stage compiles standalone.

## Files

| File | Contents |
|:--|:--|
| [`author_works.bib`](author_works.bib) | The author's prior works that bear on passage: every bill version, the National Platform and its standards (USL, national MCP, federated learning), the regulatory adaptations (21 CFR Part 50, Part 312, ICH), the surgical-humanoid and adverse-event assurance works, and the oncology-AI lineage anchor. |
| [`passage_refs.bib`](passage_refs.bib) | Legislative process and budget rules, the FD&C Act and precedent statutes, the consensus safety standards the bill binds the gates to, external evidence on medical error and algorithmic bias, and the advocacy science on how evidence moves a legislature. |

## What was removed, and why (the trim)

The prompt directs that less relevant author references be removed. From the prior
`adoption/references/author_works.bib` set, this topic drops the works that do not
bear on legislation, regulation, or the platform: the chemistry and spectrometry
preprints (paclitaxel biosynthesis, monoclonal-antibody bioprocess, large multimodal
spectrometry, chemical document retrieval) and the stand-alone drug-synergy and
single-procedure simulation demonstrations. Those works are not deleted from the
repository; they remain in `adoption/references/author_works.bib`, which this build
does not rewrite. What remains here is the bill, the platform, the regulatory
adaptations, and the assurance lineage that a legislator would actually cite.

## What was added, and why (the topic references)

Per the prompt, important references for this topic were added with working URLs to
professional sources and journals:

| Group | Examples | Used in |
|:--|:--|:--|
| Legislative process and budget rules | How Our Laws Are Made; CBO cost estimates; Statutory PAYGO Act; Unfunded Mandates Reform Act; House Rules (CutGo) | Authority, Fiscal, Passage |
| Statute and precedent | FD&C Act; 21st Century Cures Act; Open Payments; CMS Medicare Advantage AI rule; S. 1399; EO 14179 | Mandate, Authority, Bipartisanship |
| Consensus safety standards | ASME V&V 40; ISO 14971; ISO/TS 15066; FDA SaMD Action Plan; UL 4600 | Safety, Authority |
| External evidence | To Err Is Human; Makary 2016; Topol 2019; Obermeyer 2019 | Mandate, Safety, Constituents |
| Advocacy and evidence-to-policy science | Moreland-Russell 2015; Brownson 2006; Cairney 2016 | Bipartisanship, Coalition |

All journal entries carry DOIs that resolve to the article of record; all
government and standards entries link to the issuing body's page.

## Sources used from other directories (Rule 6)

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| The starting author reference set (then trimmed) | [`adoption/references/author_works.bib`](../../adoption/references/author_works.bib) | `author_works.bib` |
| The external-evidence and advocacy entries (carried and extended) | [`adoption/references/framework_refs.bib`](../../adoption/references/framework_refs.bib) | `passage_refs.bib` |
| Bill text and DOIs | `single-prompt-bill/auto-bill-02/final-bill/publication` | both `.bib` files |

## License

Released under CC BY 4.0. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)).
