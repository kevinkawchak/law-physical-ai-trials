# Releases

Release notes for the law-physical-ai-trials repository.

---

Earning the Clinician's Trust: An Eight-Question Confidence Framework (v0.2.0)
v0.2.0 - The Clinician Confidence Framework (Mermaid, Draft, Full, and Final)

## Summary

- Adds `adoption/`, a complete and new paper topic: the clinician confidence
  framework *Earning the Clinician's Trust: An Eight-Question Confidence Framework
  for Verified Physical AI in Oncology Trials*. It is analogous in structure to the
  v0.1.0 review under `review/` but does not rewrite it. Where the review persuades
  legislators through eight emotional pillars, this framework equips the practicing
  clinician, the oncologist, investigator, nurse, and research coordinator, to
  decide at the bedside when to place calibrated trust in a verified Physical AI
  system. Authored by Claude Code Opus 4.8 (1M context) Max running autonomously
  across sequential commits in a single pull request, one file per commit pushed in
  real time, with a second-to-last error-fix commit and a final repository-updates
  commit per stage. Only kevinkawchak/law-physical-ai-trials is edited.
- Builds from a single submitted prompt through two processes: Process A generated
  four unique sub-prompts under `adoption/sub-prompts/` (adapted from
  `review/sub-prompts/`), and Process B ran them in sequence to grow the manuscript
  through four stages, the 20 colored Mermaid figures, then draft-framework,
  full-framework, and final-framework.
- Organizes the decision to trust as eight confidence questions mapped to the
  CONFIDENCE GOALS: competence, safety, transparency, oversight, equity,
  reliability, accountability, and workflow. Each question pairs a clinical concern
  with a credible, cited fact and closes on the concrete mechanism, a gate, a
  record, a role, or a control, that answers it. The goal is calibrated trust:
  reliance proportioned to demonstrated capability, avoiding automation bias and
  algorithm aversion.
- Carries 20 professional colored Mermaid figures (eight distinct diagram types)
  and their 20 colored TikZ reproductions in the manuscript, in the strict palette
  black, grayscales, `#EBCB8B`, `#D08770`, and `#8B2E3F`, preserving the `#8B2E3F`
  template theme, with nine body-width tables and no raster image anywhere.
- Reuses the `review/template` visual appearance and the verification-before-
  generation mechanism (Claude Code proposes, Codex reviews, ten VVUQ gates, ACCEPT
  / ESCALATE / BLOCK), and grounds the eight questions in the author's engineering
  lineage and the literature of trust in automation, clinical decision support, and
  algorithmic bias.
- Keeps the pull request green: the additions are LaTeX, BibTeX, Markdown, and
  zips, all outside the ruff and yamllint surface, so the lint-and-format CI job
  passes across Python 3.10, 3.11, and 3.12.
- Updates the main README (a v0.2.0 version section, badges, the `adoption/`
  structure, a synthesis table, and a colored Mermaid diagram from the
  final-framework), the CHANGELOG (v0.2.0), and these release notes, without
  rewriting the prior v0.1.0 content.

## Features

- `adoption/prompts/`: `prompt-adoption.md` (the submitted Master prompt verbatim)
  and `output-adoption.md` (the full markdown output of the run).
- `adoption/sub-prompts/`: `prompt-1-mermaid.md`, `prompt-2-draft-framework.md`,
  `prompt-3-full-framework.md`, and `prompt-4-final-framework.md`, with a README.
- `adoption/mermaid/`: 20 colored Mermaid figures under `diagrams/`, the
  `output-mermaid.md` catalog, and a README; one commit per figure.
- `adoption/draft-framework/`, `adoption/full-framework/`,
  `adoption/final-framework/`: each with `main.tex`, `frameworkstyle.sty`,
  `references.bib`, eight body sections plus an introduction, an appendix figure
  compendium (full and final), back matter, a README, the generating prompt
  verbatim, a framework output, and an Overleaf-ready LaTeX zip.
- `adoption/references/`: `author_works.bib` (the author's prior works and every
  bill version) and `framework_refs.bib` (calibrated trust and external evidence).

## Contributors
@kevinkawchak
@claude
@google-gemini
@openai

## Notes

- This is an independent research draft, not enacted law and not legal or clinical
  advice; it is not endorsed by the FDA, HHS, or any Member of Congress. The
  illustrative number "H. R. 9510" is a placeholder; the generated text is released
  under CC BY 4.0. All supporting numbers are illustrative or simulation results
  unless tied to a cited source. The DOI is left as 10.5281/zenodo.xxxxxxxx
  (https://doi.org/10.5281/zenodo.xxxxxxxx) pending deposit.
- Built autonomously by Claude Code Opus 4.8 (1M context) Max across sequential
  commits in a single pull request, one file per commit pushed in real time, with
  per-stage error-fix and repository-updates commits. Only
  kevinkawchak/law-physical-ai-trials was edited; the prior v0.1.0 `review/`
  content was not rewritten.

---

H. R. 9510 Narrative Review: Eight Emotional Pillars for the Transition to Law (v0.1.0)
v0.1.0 - The H. R. 9510 Narrative Review (Draft, Full, and Final)

## Summary

- Adds `review/`, a complete narrative review that supports the transition of
  Physical AI Trial Bill H. R. 9510 v5.0 into a new Federal AI law, written for
  legislators in medical AI who have neither robotics nor Claude Code and Codex
  experience. Authored by Claude Code Opus 4.8 (1M context) Max running
  autonomously across sequential commits in a single pull request, one file per
  commit pushed to GitHub in real time, with a second-to-last error-fix commit and
  a final repository-updates commit per stage. Only kevinkawchak/law-physical-ai-trials
  is edited.
- Builds from a single submitted prompt through two processes: Process A generated
  four unique sub-prompts under `review/sub-prompts/` (adapted from
  `single-prompt-bill/auto-bill-02` and its `sub-prompts/`), and Process B ran them
  in sequence to grow the manuscript through four stages, the 21 colored Mermaid
  figures, then draft-narrative, full-narrative, and final-narrative.
- Argues the case through eight body sections mapped to the SECTION GOALS:
  compassion, fear of preventable harm, moral outrage, hope, responsibility and
  duty, protection of vulnerable people, trust and reassurance, and urgency. Each
  pillar pairs a human appeal with a credible, cited fact, weaves in the MAIN
  ACTIONS and KEY TERMS, and closes on the specific provision of H. R. 9510 that
  answers it.
- Carries 21 professional colored Mermaid figures (catalog) and 20 colored TikZ
  reproductions in the manuscript, in the strict palette black, grayscales,
  `#EBCB8B`, `#D08770`, and `#8B2E3F`, preserving the `#8B2E3F` paper template
  theme, with nine body-width tables and no raster image anywhere.
- Preserves the `review/template` visual appearance and adapts its eight sections
  to the project; adapts the table of contents and back matter from
  `cancer-automated/papers/VVUQ-02/final-paper`.
- Keeps the pull request green: the additions are LaTeX, BibTeX, Markdown, and
  zips, all outside the ruff and yamllint surface, so the lint-and-format CI job
  passes across Python 3.10, 3.11, and 3.12.
- Updates the main README (23 badges, a 425-character v0.1.0 summary, a new version
  section, table of contents, repository structure, tables, and colored Mermaid
  diagrams from the final-narrative), this releases file, and the CHANGELOG
  (v0.1.0).

## Features

- `review/prompts/`: `prompt-narrative.md` (the submitted Master prompt verbatim)
  and `output-narrative.md` (the full markdown output of the run).
- `review/sub-prompts/`: `prompt-1-mermaid.md`, `prompt-2-draft-narrative.md`,
  `prompt-3-full-narrative.md`, and `prompt-4-final-narrative.md`, with a README.
- `review/mermaid/`: 21 colored Mermaid figures under `diagrams/`, the
  `output-mermaid.md` catalog, and a README; one commit per figure.
- `review/draft-narrative/`, `review/full-narrative/`, `review/final-narrative/`:
  each with `main.tex`, `narrativestyle.sty`, `references.bib`, eight body
  sections plus an introduction, an appendix figure compendium, back matter, a
  README, the generating prompt verbatim, a narrative output, and an
  Overleaf-ready LaTeX zip.
- `review/references/`: `author_works.bib` (the author's prior works and every
  bill version) and `narrative_refs.bib` (advocacy science and external evidence).
- `.github/workflows/ci.yml`: the lint-and-format workflow that passes on Python
  3.10, 3.11, and 3.12.

## Contributors
@kevinkawchak
@claude
@google-gemini
@openai

## Notes

- This is an independent research draft, not enacted law and not legal advice; it
  is not endorsed by the FDA, HHS, or any Member of Congress. The illustrative
  number "H. R. 9510" is a placeholder; the reproduced statutory framing is in the
  public domain and the generated text is released under CC BY 4.0. All supporting
  numbers are illustrative or simulation results unless tied to a cited source. The
  DOI is left as 10.5281/zenodo.xxxxxxxx (https://doi.org/10.5281/zenodo.xxxxxxxx)
  pending deposit.
- Built autonomously by Claude Code Opus 4.8 (1M context) Max across sequential
  commits in a single pull request, one file per commit pushed in real time, with
  per-stage error-fix and repository-updates commits. Only
  kevinkawchak/law-physical-ai-trials was edited; nothing was committed to any
  other repository.
