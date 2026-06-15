# Changelog

All notable changes to this repository are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/).

## [Unreleased]

## [0.2.0] - 2026-06-15

### Added
- `adoption/`: a complete, new paper topic, the clinician confidence framework
  *Earning the Clinician's Trust: An Eight-Question Confidence Framework for
  Verified Physical AI in Oncology Trials*. It is analogous in structure to the
  v0.1.0 review under `review/` but does not rewrite it: where the review
  persuades legislators through eight emotional pillars, the framework equips the
  practicing clinician to decide, at the bedside, when to place calibrated trust in
  a verified system. Built by one Claude Code Opus 4.8 (1M context) agent across
  the same four stages, one file per commit pushed to GitHub in real time inside a
  single pull request, with a second-to-last error-fix commit and a final
  repository-updates commit per stage.
- `adoption/prompts/`: the submitted Master prompt verbatim (`prompt-adoption.md`)
  and the run output (`output-adoption.md`).
- `adoption/sub-prompts/`: Process A output, four unique sub-prompts adapted from
  `review/sub-prompts/` and re-targeted to the clinician confidence framework.
- `adoption/references/`: `author_works.bib` (reused lineage, 43 entries) and
  `framework_refs.bib` (14 entries adding the landmark calibrated-trust,
  automation-bias, and algorithm-aversion references).
- `adoption/mermaid/`: Stage 1, 20 professional colored Mermaid figures (one commit
  each, eight distinct diagram types) in the strict palette black, grayscales,
  `#EBCB8B`, `#D08770`, `#8B2E3F`, plus a catalog and README.
- `adoption/draft-framework/`: Stage 2, the scaffold with bracketed
  `[DRAFTING INSTRUCTIONS]` naming exact source files; eight body sections mapped
  to the CONFIDENCE GOALS, `frameworkstyle.sty` with a colored TikZ figure
  primitive, `references.bib`, and an Overleaf bundle.
- `adoption/full-framework/`: Stage 3, the rendered manuscript; every bracket
  replaced with finished cited prose, 20 colored TikZ figures, 8 body-width tables,
  the ADOPTION ACTIONS and KEY TERMS woven in, and an Overleaf bundle.
- `adoption/final-framework/`: Stage 4, the publication-quality manuscript;
  `\raggedbottom` page balancing, a question-to-mechanism synthesis table (9 tables
  total), refined figure routing, and an Overleaf bundle.

### Changed
- `README.md`: added a v0.2.0 version section, badges, and the `adoption/` tree in
  the repository structure, without rewriting the prior v0.1.0 section.
- `releases.md`: added the v0.2.0 release notes above the v0.1.0 notes.

### Notes
- No raster images anywhere; the visual media are tables, ASCII, and colored
  Mermaid (native in Markdown, colored TikZ in the compiled LaTeX). The prior
  v0.1.0 `review/` content is unchanged.

## [0.1.0] - 2026-06-13

### Added
- `review/`: a complete narrative review that supports the transition of Physical
  AI Trial Bill H. R. 9510 v5.0 into Federal law, written for legislators in
  medical AI without robotics or Claude Code and Codex experience. Built by one
  Claude Code Opus 4.8 (1M context) agent across four stages, one file per commit
  pushed to GitHub in real time inside a single pull request, with a
  second-to-last error-fix commit and a final repository-updates commit per stage.
- `review/prompts/`: the submitted Master prompt verbatim (`prompt-narrative.md`)
  and the run output (`output-narrative.md`).
- `review/sub-prompts/`: Process A output, four unique sub-prompts adapted from
  `single-prompt-bill/auto-bill-02` and re-targeted to this narrative build.
- `review/references/narrative_refs.bib`: the five advocacy-science references
  from the prompt BACKGROUND block plus accurate external evidence (To Err Is
  Human, Makary 2016, Obermeyer 2019, Topol 2019, the FDA AI/ML SaMD Action Plan,
  ASME V&V 40-2018, the Statutory PAYGO Act), with a directory README.
- `review/mermaid/`: Stage 1, 21 professional colored Mermaid figures (one commit
  each) in the strict palette black, grayscales, `#EBCB8B`, `#D08770`, `#8B2E3F`,
  plus a catalog and README. Adapted from `Clinical-AI-Demos/ai-outputs/output-01`.
- `review/draft-narrative/`: Stage 2, the scaffold with bracketed
  `[DRAFTING INSTRUCTIONS]` naming exact source files; eight body sections mapped
  to the SECTION GOALS, a clickable table of contents and back matter adapted from
  `cancer-automated/papers/VVUQ-02/final-paper`, `narrativestyle.sty` with a
  colored TikZ figure primitive, `references.bib`, and an Overleaf bundle.
- `review/full-narrative/`: Stage 3, the rendered manuscript; every bracket
  replaced with finished cited prose, 20 colored TikZ figures, 8 body-width
  tables, the MAIN ACTIONS and KEY TERMS woven in, and an Overleaf bundle.
- `review/final-narrative/`: Stage 4, the publication-quality manuscript;
  `\raggedbottom` and `\needspace` page balancing, a pillar-to-provision synthesis
  table (9 tables total), refined figure routing, and an Overleaf bundle.
- `.github/workflows/ci.yml`: a `lint-and-format` workflow (ruff, yamllint) on
  Python 3.10, 3.11, and 3.12 that passes cleanly on this LaTeX and Markdown
  repository.
- `releases.md` and this `CHANGELOG.md`: the v0.1.0 release notes and changelog.

### Changed
- `README.md`: rebuilt as a comprehensive landing page with 23 badges (three times
  the prior convention), a 425-character v0.1.0 summary, a new version section, a
  table of contents, the repository structure, the eight-pillar and
  pillar-to-provision tables, three colored Mermaid diagrams from the
  final-narrative, the build pipeline, and the sources used.
- @kevinkawchak added publication and claude code manuscript pdfs to law-physical-ai-trials/tree/main/review on 2026-06-14.

### Notes
- No raster images anywhere; the visual media are tables, ASCII, and colored
  Mermaid (native in Markdown, colored TikZ in the compiled LaTeX).
- Independent research draft, not enacted law and not legal advice. The DOI is
  left as `10.5281/zenodo.xxxxxxxx` pending deposit.
