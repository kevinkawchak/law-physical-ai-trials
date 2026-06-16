# law-physical-ai-trials

A narrative review that supports the H. R. 9510 (2026) transition to Federal law.

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-EBCB8B.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Release](https://img.shields.io/badge/Release-v0.3.0-8B2E3F.svg)](releases.md)
[![Last Updated](https://img.shields.io/badge/Updated-June%202026-D08770.svg)](CHANGELOG.md)
[![CI](https://img.shields.io/badge/CI-lint%20and%20format-8B2E3F.svg)](.github/workflows/ci.yml)
[![Python](https://img.shields.io/badge/Python-3.10%20%7C%203.11%20%7C%203.12-D08770.svg)](https://www.python.org/)
[![Bill](https://img.shields.io/badge/Bill-H.%20R.%209510%20v5.0-8B2E3F.svg)](https://doi.org/10.5281/zenodo.20619762)
[![Bill DOI](https://img.shields.io/badge/Bill%20DOI-10.5281%2Fzenodo.20619762-EBCB8B.svg)](https://doi.org/10.5281/zenodo.20619762)
[![Review DOI](https://img.shields.io/badge/Review%20DOI-10.5281%2Fzenodo.20685379-D08770.svg)](https://doi.org/10.5281/zenodo.20685379)
[![Adoption DOI](https://img.shields.io/badge/Adoption%20DOI-10.5281%2Fzenodo.20710602-EBCB8B.svg)](https://doi.org/10.5281/zenodo.20710602)
[![Agent](https://img.shields.io/badge/Agent-Claude%20Code%20Opus%204.8%20(1M)-8B2E3F.svg)](https://claude.com/claude-code)
[![Stages](https://img.shields.io/badge/Stages-4-D08770.svg)](review/)
[![Body sections](https://img.shields.io/badge/Body%20sections-8%20pillars-D08770.svg)](review/final-narrative/sections/)
[![TikZ figures](https://img.shields.io/badge/TikZ%20figures-20-8B2E3F.svg)](review/final-narrative/)
[![Palette](https://img.shields.io/badge/Palette-black%20gray%20%2B%203%20theme-D08770.svg)](review/mermaid/)
[![Theme](https://img.shields.io/badge/Theme-%238B2E3F%20preserved-8B2E3F.svg)](review/template/)
[![Media](https://img.shields.io/badge/Media-Tables%20%2B%20ASCII%20%2B%20Mermaid-lightgrey.svg)](review/)
[![Overleaf](https://img.shields.io/badge/Overleaf-pdfLaTeX-8B2E3F.svg)](review/final-narrative/)
[![References](https://img.shields.io/badge/References-12%20%2B%20author%20works-EBCB8B.svg)](review/references/)
[![Contributors](https://img.shields.io/badge/Contributors-4-D08770.svg)](releases.md)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0007--5457--8667-EBCB8B.svg)](https://orcid.org/0009-0007-5457-8667)
[![New](https://img.shields.io/badge/New-adoption%2F%20clinician%20framework-D08770.svg)](adoption/)
[![Confidence questions](https://img.shields.io/badge/Confidence%20questions-8-EBCB8B.svg)](adoption/final-framework/sections/)
[![adoption Mermaid](https://img.shields.io/badge/adoption%20Mermaid-20-8B2E3F.svg)](adoption/mermaid/)
[![New](https://img.shields.io/badge/New-enactment%2F%20passage%20framework-4B0082.svg)](enactment/)
[![Passage questions](https://img.shields.io/badge/Passage%20questions-8-000080.svg)](enactment/final-framework/sections/)
[![Verify stage](https://img.shields.io/badge/New%20stage-verify-4B0082.svg)](enactment/verify-framework/)
[![enactment palette](https://img.shields.io/badge/Palette-%234B0082%20%7C%20%23000080%20%7C%20%23C0C0C0-000080.svg)](enactment/mermaid/)

## What is new in v0.3.0

[Final PDF and Source](https://doi.org/10.5281/zenodo.xxxxxxxx). This v0.3.0 release
adds `enactment/`, a passage framework that answers the eight questions a member of
Congress asks before voting yes on H. R. 9510: mandate, authority, safety, fiscal
score, constituents, bipartisanship, coalition, and the passage path. Each is paired
with a cited fact from the bill and the platform. A new verify stage double-checks
every table and figure.

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':24,'rankSpacing':38,'htmlLabels':true}}}%%
flowchart LR
  Q1["1 Mandate"]:::n1
  Q2["2 Authority"]:::n2
  Q3["3 Safety"]:::act
  Q4["4 Fiscal"]:::n3
  Q5["5 Constituents"]:::n2
  Q6["6 Bipartisan"]:::evid
  Q7["7 Coalition"]:::n3
  Q8["8 Passage"]:::act
  YES["Yes in both<br/>chambers"]:::evid
  Q1 --> Q2 --> Q3 --> Q4 --> Q5 --> Q6 --> Q7 --> Q8 --> YES
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```

The eight questions and the provision or evidence in H. R. 9510 that answers each,
reproduced from the final-framework synthesis table:

| Question | What answers it in H. R. 9510 |
|:--|:--|
| Mandate | Three named gaps in existing law, tied to the record on preventable error |
| Authority | A commerce-power amendment to the FD&C Act adding section 515D, with a savings clause |
| Safety | The ten-gate VVUQ schedule and the three hard catastrophe predicates |
| Fiscal | A 58 million dollar authorization, no net mandatory spending, a 19 to 1 reduction |
| Constituents | A platform scaling to 50 through 100 sites across all regions |
| Bipartisanship | One provision two caucuses can each support on their own terms |
| Coalition | Clinicians, patients, industry, and the States; objections routed to citations |
| Passage path | Regular order in both chambers, known thresholds, a demonstrated platform |

The v0.2.0 and v0.1.0 sections below are unchanged.

## What is new in v0.2.0

[Final PDF and Source](https://doi.org/10.5281/zenodo.20710602). This v0.2.0 release adds `adoption/`, a new clinician-facing companion to the
v0.1.0 review: an eight-question confidence framework (competence, safety,
transparency, oversight, equity, reliability, accountability, workflow) for
deciding when to trust verified Physical AI at the bedside of an oncology trial. Where the v0.1.0 review under `review/` persuades **legislators** through eight
emotional pillars. 

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':24,'rankSpacing':38,'htmlLabels':true}}}%%
flowchart LR
  Q1["1 Competence"]:::n1
  Q2["2 Safety"]:::risk
  Q3["3 Transparency"]:::n2
  Q4["4 Oversight"]:::n2
  Q5["5 Equity"]:::risk
  Q6["6 Reliability"]:::n3
  Q7["7 Accountability"]:::n2
  Q8["8 Workflow"]:::hope
  CT["Calibrated<br/>trust"]:::act
  Q1 --> Q2 --> Q3 --> Q4 --> Q5 --> Q6 --> Q7 --> Q8 --> CT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```

The eight questions and the specific mechanism that answers each, reproduced from
the final-framework synthesis table:

| Question | The mechanism that answers it |
|:--|:--|
| Competence | Local validation and an assurance run (172 of 172 gate tests) |
| Safety | The ten-gate VVUQ examination and the catastrophe-predicate BLOCK |
| Transparency | Explainable output and a hash-chained audit trail |
| Oversight | Human-in-the-loop control, the ESCALATE path, and an override |
| Equity | Subgroup performance reporting and continuous bias surveillance |
| Reliability | Reproducibility checks, drift monitoring, and quantified uncertainty |
| Accountability | Named roles and a signed standard operating procedure |
| Workflow | Integration into the clinic day and consent, with continuous monitoring |

The v0.1.0 narrative review below is unchanged.

## What is new in v0.1.0

[Publication PDF](https://doi.org/10.5281/zenodo.20685379). This v0.1.0 release adds a complete narrative review under `review/` that argues,
through eight emotional pillars, for enacting Physical AI Trial Bill H. R. 9510
v5.0 into Federal law. Built by one Claude Code agent across four stages (21
colored Mermaid figures, then draft, full, and final narratives), it pairs every
appeal with cited evidence, preserves the template theme, and compiles in Overleaf
with no raster images.


## Table of contents

- [What is new in v0.3.0](#what-is-new-in-v030)
- [What is new in v0.2.0](#what-is-new-in-v020)
- [What is new in v0.1.0](#what-is-new-in-v010)
- [The eight body sections](#the-eight-body-sections)
- [Repository structure](#repository-structure)
- [The core mechanism (colored Mermaid)](#the-core-mechanism-colored-mermaid)
- [The eight pillars and the provisions that answer them](#the-eight-pillars-and-the-provisions-that-answer-them)
- [How the build works](#how-the-build-works)
- [Sources used from other repositories](#sources-used-from-other-repositories)
- [Visual media and palette](#visual-media-and-palette)
- [Documentation](#documentation)
- [License](#license)

## The eight body sections

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

## Repository structure

```
law-physical-ai-trials/
  README.md                  (this file)
  CHANGELOG.md               (v0.3.0)
  releases.md                (v0.3.0 + v0.2.0 + v0.1.0 release notes)
  LICENSE
  .github/workflows/ci.yml   (lint-and-format, green)
  review/                    v0.1.0: the legislative narrative review (unchanged)
    README.md
    prompts/                 the submitted prompt + the run output
    sub-prompts/             Process A: four generated sub-prompts
    references/              author_works.bib + narrative_refs.bib
    template/                the reused paper template (unchanged theme)
    mermaid/                 Stage 1: 21 colored Mermaid figures + catalog
    draft-narrative/         Stage 2: scaffold with bracketed source cues
    full-narrative/          Stage 3: rendered manuscript (20 TikZ figs, 8 tables)
    final-narrative/         Stage 4: publication-quality manuscript (9 tables)
  adoption/                  v0.2.0: the clinician confidence framework (new topic)
    README.md
    prompts/                 the submitted prompt + the run output
    sub-prompts/             Process A: four generated sub-prompts
    references/              author_works.bib + framework_refs.bib
    mermaid/                 Stage 1: 20 colored Mermaid figures + catalog
    draft-framework/         Stage 2: scaffold with bracketed source cues
    full-framework/          Stage 3: rendered manuscript (20 TikZ figs, 8 tables)
    final-framework/         Stage 4: publication-quality manuscript (9 tables)
  enactment/                 v0.3.0: the H. R. 9510 passage framework (new topic)
    README.md
    prompts/                 the submitted prompt + the run narrative
    sub-prompts/             Process A: five generated sub-prompts
    references/              author_works.bib (trimmed) + passage_refs.bib
    mermaid/                 Stage 1: 20 colored Mermaid figures + catalog
    draft-framework/         Stage 2: scaffold with bracketed source cues
    full-framework/          Stage 3: rendered manuscript (20 TikZ figs, 6 tables)
    verify-framework/        Stage 4 (new): table and figure audit, verified twice
    final-framework/         Stage 5: publication-quality manuscript (7 tables)
      publication/           the deposit-ready mirror
```

## The core mechanism (colored Mermaid)

Verification before generation, the principle at the center of H. R. 9510: a human
specification is drafted by one agent, reviewed by a second, and admitted only
after ten gates resolve to ACCEPT, ESCALATE, or BLOCK.

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':55,'htmlLabels':true}}}%%
flowchart TB
  SPEC["Clinical specification<br/>human investigators"]:::n1
  GEN["Claude Code<br/>generates candidate code"]:::n2
  REV["Codex<br/>independent peer review"]:::n2
  VVUQ{"VVUQ verification<br/>ten gates"}:::act
  ACC["ACCEPT<br/>execute under audit"]:::hope
  ESC["ESCALATE<br/>return to a qualified human"]:::n3
  BLK["BLOCK<br/>stop before execution"]:::risk
  SPEC --> GEN
  GEN --> REV
  REV --> VVUQ
  VVUQ -->|all gates pass| ACC
  VVUQ -->|uncertain| ESC
  VVUQ -->|catastrophe predicate| BLK
  ESC -.->|human revises| GEN
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```

The argument accumulates across the eight pillars and converges on a single
legislative request.

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':26,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart LR
  P1["1 Compassion"]:::n1
  P2["2 Fear of harm"]:::risk
  P3["3 Moral outrage"]:::risk
  P4["4 Hope"]:::hope
  P5["5 Responsibility"]:::n2
  P6["6 Protection"]:::n2
  P7["7 Trust"]:::hope
  P8["8 Urgency"]:::risk
  ACT["Enact<br/>H. R. 9510"]:::act
  P1 --> P2 --> P3 --> P4 --> P5 --> P6 --> P7 --> P8 --> ACT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
```

## The eight pillars and the provisions that answer them

This synthesis table is reproduced from the final-narrative manuscript.

| Pillar | Provision of H. R. 9510 that answers it |
|:--|:--|
| Compassion | A verified pathway a patient can enter, with consent confirmed and recorded |
| Fear of harm | The mandatory ten-gate verification before any action executes |
| Moral outrage | Subgroup bias surveillance, measured and publicly reported |
| Hope | The authorization that funds a tested national trial platform |
| Responsibility | The conforming amendments that make verification the standard of care |
| Protection | Verified informed consent and a per-subgroup outcome audit |
| Trust | Each gate bound to a published standard, with a hash-chained audit trail |
| Urgency | A defined effective date and a budget-scored, bounded cost of acting |

## How the build works

A single submitted prompt (`review/prompts/prompt-narrative.md`) drives two
processes: Process A generated the four sub-prompts in `review/sub-prompts/`, and
Process B ran them in sequence to grow the manuscript through four stages.

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':30,'rankSpacing':44,'htmlLabels':true}}}%%
flowchart LR
  MP["Master prompt"]:::n1
  SP["Process A<br/>4 sub-prompts"]:::n2
  M1["Stage 1<br/>21 Mermaid figures"]:::n2
  M2["Stage 2<br/>draft-narrative"]:::n3
  M3["Stage 3<br/>full-narrative"]:::act
  M4["Stage 4<br/>final-narrative"]:::act
  REL["v0.1.0 release"]:::hope
  MP --> SP --> M1 --> M2 --> M3 --> M4 --> REL
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```

```
            Master prompt
                 |
       Process A | generate sub-prompts
                 v
   sub-prompts -> mermaid -> draft -> full -> final -> v0.1.0 release
   (4 prompts)   (21 figs)  (scaffold) (prose) (polish)
```

## Sources used from other repositories

| Asset used | Upstream source | Used in |
|:--|:--|:--|
| Paper template (theme, columns, ORCID mark) | `review/template` | every narrative stage |
| Colored Mermaid families and palette discipline | `Clinical-AI-Demos/.../ai-outputs/output-01` | `review/mermaid/` |
| Table of contents and back matter | `cancer-automated/.../papers/VVUQ-02/final-paper` | `draft-narrative` onward |
| Verification evidence (ten gates, 172 tests) | `cancer-automated/.../papers/VVUQ-02` | fear and trust sections |
| Sub-prompt and auto-commit methodology | `single-prompt-bill/.../auto-bill-02` | `sub-prompts/`; build schedule |
| Release and badge conventions | `kevinkawchak/cancer-automated` | this README, `CHANGELOG.md`, `releases.md` |

## Visual media and palette

No raster images are used. The permitted media are full-width white-background
tables, monospace ASCII figures, and colored Mermaid diagrams (native in Markdown,
reproduced as colored TikZ in the compiled LaTeX). The strict palette is black,
grayscales, and `#EBCB8B` (gold, hope), `#D08770` (clay, risk), and `#8B2E3F`
(burgundy, the Act). The `#8B2E3F` paper template theme is preserved.

## Documentation

- [`CHANGELOG.md`](CHANGELOG.md) - the v0.3.0, v0.2.0, and v0.1.0 changelog.
- [`releases.md`](releases.md) - the v0.3.0, v0.2.0, and v0.1.0 release notes.
- [`enactment/README.md`](enactment/README.md) - the v0.3.0 passage framework landing page.
- [`adoption/README.md`](adoption/README.md) - the v0.2.0 clinician framework landing page.
- [`review/README.md`](review/README.md) - the v0.1.0 review landing page.

## License

Released under CC BY 4.0; reproduced public-domain U.S. Government text is used
under 17 U.S.C. § 105. Author: Kevin Kawchak, CEO ChemicalQDevice
([ORCID 0009-0007-5457-8667](https://orcid.org/0009-0007-5457-8667)). DOI left as
[`10.5281/zenodo.xxxxxxxx`](https://doi.org/10.5281/zenodo.xxxxxxxx) pending
deposit.

*Independent research draft. Not enacted law, not pending legislation, and not
legal advice; not endorsed by the FDA, HHS, or any Member of Congress. The
illustrative number "H. R. 9510" is a placeholder. All figures are illustrative or
simulation results unless tied to a cited source.*
