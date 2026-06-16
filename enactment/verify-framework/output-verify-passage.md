## output-verify-passage

This file records the markdown narrative of Stage 4, the verify-framework, which is
new to the v0.3.0 build and sits between the full and final source files. The full
audit, table by table and figure by figure, is in
[`verification-report.md`](verification-report.md); this narrative summarizes it.

### What the verify stage does

It does not write new prose. It copies the full-framework sources, runs a complete
table-and-figure audit against the instructions, fixes every defect it finds, and
certifies the corrected source files that the final stage polishes. Figures are
audited twice: the first pass reasons about the geometry and applies a fix, and the
second pass confirms the fix holds.

### What it certified

- The uniform `\vspace{-0.75cm}` figure-to-caption gap is centralized in
  `\psgcaption`, so it is identical for all twenty figures by construction.
- All twenty curved arrows carry an explicit looseness; none was left at the default.
- The palette is restricted to black, grayscales, `#4B0082`, `#000080`, and
  `#C0C0C0`, with no stray hue.
- All six tables match the body measure at `\textwidth` with ragged-right columns.

### What it fixed

- Figure 1 (the eight-question path) was rerouted as a serpentine so the wrap edge no
  longer sweeps across the figure and cannot clip a box.
- Figure 16 (the two-chamber strategy) had its uneven node pitch evened to 3.7.
- Figure 19 (objection handling) had its four two-line boxes spread from a pitch of
  1.0 to 1.4 so they no longer touch.
- Two tables (`tab:terms`, `tab:gates`) had their column widths re-balanced to the
  amount of text each column carries.

### Next stage

The final stage (`../final-framework/`) takes these certified sources, adds the
ninth synthesis table mapping each question to the provision that answers it, applies
`\raggedbottom` and the prose and pagination polish, and mirrors the result into
`final-framework/publication/` for deposit.
