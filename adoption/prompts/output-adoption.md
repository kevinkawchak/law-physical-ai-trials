## output-adoption

This is the markdown narration of the v0.2.0 run. It records what the agent did,
not the code files themselves (those live under `adoption/`). The objective was to
create and execute comprehensive mermaid, draft, full, and final sub-prompts to
generate a new paper topic, with analogous files and structures auto-committed and
auto-PRed, without rewriting the prior version and without shortcuts.

### Process A: the four sub-prompts

From the single submitted prompt (`prompt-adoption.md`), Process A generated four
unique sub-prompts in `../sub-prompts/`, adapted from the prior build's
`review/sub-prompts/` and re-targeted to the `adoption/` tree and the eight
CONFIDENCE GOALS: `prompt-1-mermaid.md`, `prompt-2-draft-framework.md`,
`prompt-3-full-framework.md`, and `prompt-4-final-framework.md`.

### Process B: four stages, committed one file at a time

- **Stage 1, mermaid.** 20 professional colored Mermaid figures across eight
  distinct diagram types (flowchart, quadrant, sequence, state, journey, timeline,
  gitGraph, mindmap), one commit each, plus the `output-mermaid.md` catalog and a
  README. Strict palette black, grayscales, `#EBCB8B`, `#D08770`, `#8B2E3F`.
- **Stage 2, draft-framework.** The scaffold: `frameworkstyle.sty` (built on
  `review/template/tmpl20style.sty`, adding the colored TikZ `cfwfig` primitive),
  `main.tex`, `references.bib` (57 entries), and ten section files in which every
  body section leaves a bracketed `[DRAFTING INSTRUCTIONS]` naming exact sources.
  Overleaf zip committed.
- **Stage 3, full-framework.** Every bracket replaced with finished, cited prose;
  20 colored TikZ figures (two introduction, eight body, ten appendix); eight
  body-width tables referenced with `\autoref`; the ADOPTION ACTIONS and KEY TERMS
  woven in. Overleaf zip committed.
- **Stage 4, final-framework.** Publication quality: `\raggedbottom` page
  balancing, a ninth synthesis table mapping each question to the mechanism that
  answers it, refined figure routing, and a clean symbol and dash sweep. Overleaf
  zip committed.

Each stage followed the rules: one commit each for `main.tex`, the `.sty`, the
`.bib`, and the `README`; one commit per section; a second-to-last commit that
fixed all errors; and a last commit for the README and the Overleaf bundle. All
commits were pushed to GitHub in real time inside a single pull request.

### Verification

With no local LaTeX toolchain available, every stage was checked with a static
validator (environment begin and end balance, `\input` targets, every `\cite` key
present in `references.bib`, no en or em dashes, no literal "SS", ASCII only) and
by confirming figure numbering (1 to 20), table labels (nine in the final stage),
table widths at `\textwidth`, and that the carried files matched byte for byte. The
`frameworkstyle.sty` and `main.tex` are faithful adaptations of the prior build's
working Overleaf files, so each stage compiles in Overleaf with pdfLaTeX as
committed.

### The single v0.2.0 update

After the four stages, one update added the root `CHANGELOG.md` (v0.2.0),
`releases.md` (v0.2.0 notes above the v0.1.0 notes), and the main `README.md` (a
v0.2.0 version section near the top with a short summary, new badges, a colored
Mermaid diagram, and the synthesis table, plus the `adoption/` tree in the
repository structure). The prior v0.1.0 `review/` content was not rewritten, and
only `kevinkawchak/law-physical-ai-trials` was edited.
