## output-final-framework

This is the narrative output of Stage 4. The final-framework carries the
full-framework to publication quality by implementing the corrections identified
from the full stage. It is the submission-ready manuscript a senior author would
sign, and it does not rewrite the prior review under `review/`.

### Corrections identified from the full stage and applied here

- **Vertical white bands.** `frameworkstyle.sty` switches from `\flushbottom` to
  `\raggedbottom` and lowers `\tolerance` to 1800, so the page bottom is natural
  rather than stretched and interword spacing stays even with no right-margin
  overflow.
- **Synthesis.** A ninth body-width table (`tab:synthesis`) is added to the close
  of the workflow section, mapping each of the eight questions to the specific
  mechanism, a gate, a record, a role, or a control, that answers it. It is
  referenced with `\autoref` and is the bridge a clinician can carry into a
  credentialing committee or a tumor board.
- **Stranded tables.** Every table keeps a `\needspace` guard so none is split or
  stranded; the synthesis table uses `\needspace{12\baselineskip}`.
- **Figure routing.** The widest appendix figure (Figure 17, model revalidation)
  is pulled inward so it sits comfortably within the body measure; all figures
  remain strictly in the palette black, grayscales, `#EBCB8B`, `#D08770`,
  `#8B2E3F`.
- **Symbols and dashes.** Section references use `\S` (never "SS"); single hyphens
  only, with no en, em, double, or triple dashes; the only `--` are the required
  TikZ edge operators inside figures.

### What this stage contains

- `main.tex` - the publication cover, abstract, disclaimer, keywords,
  Introduction, a clickable table of contents, the eight body sections, the
  appendix figure compendium (Figures 11 to 20), References (`ieeetr`,
  `\nocite{*}`), and the back matter.
- `sections/` - twelve files: `abstract`, `introduction`, `q1-competence` through
  `q8-workflow`, `appendix-figures`, and `back_matter`. Twenty colored TikZ
  figures and nine body-width tables in all.
- `frameworkstyle.sty` - the final style (raggedbottom) preserving the template
  visual theme exactly.
- `references.bib` - the 57 entries cited cleanly so every DOI prints its
  clickable resolver URL.

### Commit log for this stage

One commit each for `frameworkstyle.sty`, `main.tex`, `references.bib`, the twelve
`sections/*.tex` files, `prompt-final-framework.md`, and this
`output-final-framework.md`; a second-to-last commit that fixes all errors across
the stage; and a last commit for the directory `README.md` and the
`final-framework-LaTeX.zip` Overleaf bundle, with the pull request refreshed. After
this stage, the single v0.2.0 release update follows (root `CHANGELOG.md`,
`releases.md`, and the main `README.md`), without rewriting the prior v0.1.0
content.
