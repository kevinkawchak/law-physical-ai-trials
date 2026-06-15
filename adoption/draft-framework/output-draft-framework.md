## output-draft-framework

This is the narrative output of Stage 2. The draft-framework is the scaffold: it
fixes the manuscript structure on the reused template theme and, in every body
section, leaves bracketed `[DRAFTING INSTRUCTIONS: ...]` that name the exact
repository files and directories the full-framework and final-framework stages
must process. This is a new paper topic and does not rewrite the prior review.

### What this stage produced

- `frameworkstyle.sty` - the style file built directly on
  `review/template/tmpl20style.sty`, so the template visual appearance is
  preserved (the `#8B2E3F` accent, Linux Libertine body, title rules, accent
  abstract box, and the `L`/`C`/`Y` table columns). It adds the colored TikZ
  `cfwfig` primitive and the themed node styles (`cfact`, `cfhope`, `cfrisk`,
  `cfone`, `cftwo`, `cfthree`, `cfdec`) that reproduce each Mermaid figure
  natively in LaTeX, with no raster image, in the strict palette. The draft uses
  `\flushbottom`; the final stage will switch to `\raggedbottom`.
- `main.tex` - the cover on the template theme, the abstract, the keywords, the
  disclaimer, the Introduction, a clickable `\tableofcontents`, the eight body
  sections, the References, and the back matter.
- `sections/` - one file per section. The Introduction defines the lay terms a
  clinician needs (Physical AI, surgical humanoid, VVUQ, verification before
  generation, Claude Code and Codex, the ten gates, ACCEPT / ESCALATE / BLOCK,
  calibrated trust, automation bias, algorithm aversion) and states the three
  bedside questions. The eight body files map to the CONFIDENCE GOALS in order:
  competence, safety, transparency, oversight, equity, reliability,
  accountability, and workflow.
- `references.bib` - the clinician-confidence references (calibrated trust,
  automation bias, algorithm aversion), the external evidence (To Err Is Human,
  Makary 2016, Obermeyer 2019, Topol 2019, the FDA AI/ML SaMD Action Plan, ASME
  V&V 40-2018), and the author's prior-work lineage including every H. R. 9510
  bill version.

### How the scaffold names its sources

Each body section carries a bracket that points the next stage to the exact file:
the Bill (`author_works.bib` entry `Kawchak2026HR9510Bill`, DOI
10.5281/zenodo.20619762); the verification evidence carried in `review/`; the
clinician references in `framework_refs.bib`; and the colored Mermaid catalog in
`adoption/mermaid/`. Each section also names the Mermaid figure slot and the
body-width table it will carry in the full stage, so no source is left implicit.

### Commit log for this stage

One commit each for `frameworkstyle.sty`, `main.tex`, `references.bib`, the ten
`sections/*.tex` files, `prompt-draft-framework.md`, and this
`output-draft-framework.md`; a second-to-last commit that fixes all errors across
the stage; and a last commit for the directory `README.md` and the
`draft-framework-LaTeX.zip` Overleaf bundle, with the pull request refreshed. The
scaffold compiles in Overleaf with pdfLaTeX as committed.
