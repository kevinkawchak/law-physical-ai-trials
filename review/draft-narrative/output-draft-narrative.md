## output-draft-narrative

This is the narrative output of Stage 2. The draft-narrative is the scaffold: it
fixes the manuscript structure on the reused template theme and, in every body
section, leaves bracketed `[DRAFTING INSTRUCTIONS: ...]` that name the exact
repository files and directories the full-narrative and final-narrative stages
must process.

### What this stage produced

- `narrativestyle.sty` - the style file built directly on
  `review/template/tmpl20style.sty`, so the template visual appearance is
  preserved (the `#8B2E3F` accent, Linux Libertine body, title rules, accent
  abstract box, and the `L`/`C`/`Y` table columns). It adds the colored TikZ
  `narrativefig` primitive and the themed node styles (`nfact`, `nfhope`,
  `nfrisk`, `nfone`, `nftwo`, `nfthree`, `nfdec`) that reproduce each Mermaid
  figure natively in LaTeX, with no raster image, in the strict palette.
- `main.tex` - the cover on the template theme, the abstract, the keywords, the
  disclaimer, the Introduction, a clickable `\tableofcontents`, the eight body
  sections, the References, and the back matter.
- `sections/` - one file per section. The Introduction defines the lay terms a
  medical-AI legislator needs (Physical AI, surgical humanoid, VVUQ, verification
  before generation, Claude Code and Codex, the ten gates, ACCEPT / ESCALATE /
  BLOCK) and states the three guiding questions. The eight body files map to the
  SECTION GOALS in order: compassion, fear of preventable harm, moral outrage,
  hope, responsibility and duty, protection of vulnerable people, trust and
  reassurance, and urgency.
- `references.bib` - the advocacy-science references from the prompt BACKGROUND
  block, the external evidence (To Err Is Human, Makary 2016, Obermeyer 2019,
  Topol 2019, the FDA AI/ML SaMD Action Plan, ASME V&V 40-2018), and the author's
  prior-work lineage including every H. R. 9510 bill version.

### How the scaffold names its sources

Each body section carries a bracket that points the next stage to the exact file:
the Bill (`author_works.bib` entry `Kawchak2026HR9510Bill`, DOI
10.5281/zenodo.20619762); the verification evidence in
`cancer-automated/papers/VVUQ-02`; the advocacy references in
`narrative_refs.bib`; and the colored Mermaid catalog in `review/mermaid/`. Each
section also names the Mermaid figure slot and the body-width table it will carry
in the full stage. Each section already includes a simple palette TikZ
placeholder figure, which the full and final stages expand and refine.

### Carried forward to the full-narrative

The full-narrative replaces every bracket with finished prose drawn from the named
files, renders the colored TikZ figures from `review/mermaid/`, adds the
body-width tables, and weaves in the MAIN ACTIONS and KEY TERMS. The
final-narrative then applies the senior-author corrections identified from the
full stage.
