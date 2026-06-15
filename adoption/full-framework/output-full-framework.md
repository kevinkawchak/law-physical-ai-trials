## output-full-framework

This is the narrative output of Stage 3. The full-framework is the rendered
manuscript: every bracketed `[DRAFTING INSTRUCTIONS: ...]` left in the
draft-framework is replaced with finished, cited prose drawn from the exact files
it named, and each body section now carries a real colored TikZ figure and a
body-width table. No scaffolding bracket remains. This is a new paper topic and
does not rewrite the prior review under `review/`.

### What this stage produced

- `main.tex` - the cover on the template theme, the abstract (`sections/abstract`),
  the disclaimer, the keywords, the Introduction, a clickable `\tableofcontents`,
  the eight body sections, an appendix figure compendium, the References, and the
  back matter.
- `sections/abstract.tex` - a single paragraph under 250 words, no citations,
  stating the mechanism, the eight questions, calibrated trust, and the three
  recurring questions.
- `sections/introduction.tex` - defines the lay terms (Physical AI, verification
  before generation, Claude Code and Codex, VVUQ, the ten gates, ACCEPT / ESCALATE
  / BLOCK, calibrated trust, automation bias, algorithm aversion) and carries
  Figures 1 and 2 (Mermaid 03 and 02 as colored TikZ).
- `sections/q1-competence.tex` ... `q8-workflow.tex` - the eight confidence
  questions, each opening with the clinical concern, anchoring it in cited
  evidence, defining terms on first use, carrying one colored TikZ figure
  (Figures 3 to 10) and one body-width table (`tab:competence` to `tab:workflow`),
  and closing on the concrete mechanism that answers the question.
- `sections/appendix-figures.tex` - Figures 11 to 20, the remaining Mermaid figures
  reproduced as colored TikZ, so the manuscript carries 20 figures in all.
- `sections/back_matter.tex` - Acknowledgments, Ethical Disclosures, Rights and
  Permissions, Cite This Framework, and Data Availability.
- `frameworkstyle.sty` and `references.bib` - carried from the draft stage
  unchanged (the full stage keeps `\flushbottom`; the final stage switches to
  `\raggedbottom`).

### How the named sources were used

The eight sections are grounded in the author's lineage in
`review/references/author_works.bib` (the surgical humanoid, the VVUQ verification
automation, the 24/7 adverse-event response team, the site documentation package,
the CFR and ICH adaptions, the patient journey, and the national platform), in the
Bill (`Kawchak2026HR9510Bill`, DOI 10.5281/zenodo.20619762), and in the
clinician-confidence literature in `adoption/references/framework_refs.bib`
(calibrated trust, automation bias, algorithm aversion, medical error, algorithmic
bias, the convergence of human and machine performance, the FDA action plan, and
ASME V&V 40). The ADOPTION ACTIONS and KEY TERMS are woven into the sections where
each is most relevant.

### Commit log for this stage

One commit each for `frameworkstyle.sty`, `main.tex`, `references.bib`, the twelve
`sections/*.tex` files, `prompt-full-framework.md`, and this
`output-full-framework.md`; a second-to-last commit that fixes all errors across
the stage; and a last commit for the directory `README.md` and the
`full-framework-LaTeX.zip` Overleaf bundle, with the pull request refreshed.
