# verification-report - Stage 4: table and figure audit (v0.3.0)

This report is the deliverable of the verification stage, which is new to the v0.3.0
build and sits between the full and final source files. It double-verifies every
table and every figure in the full-framework against the instructions, records a
verdict for each test, and certifies the corrected source files in this directory.
Figures are audited twice, as required: a first pass reasons about the geometry and
fixes any defect, and a second pass confirms the fix holds.

## Method

The full-framework sources were copied into this directory unchanged in prose. Each
table was checked for body-measure width, ragged-right fixed columns, column widths
matched to the text each column carries, a `\needspace` guard, and an `\autoref`
reference. Each figure was checked for the three required properties: (a) no text box
and arrow overlaps, (b) an explicit looseness on every curved arrow, and (c) even box
spacing, plus the uniform `\vspace{-0.75cm}` figure-to-caption gap (built into
`\psgcaption`) and the palette (black, grayscales, `#4B0082`, `#000080`, `#C0C0C0`).

## Caption-gap and palette checks (whole document)

| Check | Method | Verdict |
|:--|:--|:--|
| Uniform `\vspace{-0.75cm}` between every figure and caption | `\psgcaption` begins with `\vspace{-0.75cm}`; no ad hoc spacing is used anywhere | PASS (centralized, so uniform by construction) |
| Palette restricted to black, grays, `#4B0082`, `#000080`, `#C0C0C0` | Only `accentcol`, `navyblue`, `silvergray`, and `pg1`/`pg2`/`pg3` are defined and used; no other color macro exists | PASS |
| Curved arrows carry explicit looseness | Counted every `to[...]`: 20 curved edges, 20 with an explicit `looseness=` | PASS (0 missing) |

## Table audit

| Table | Width | Columns ragged-right `p{}` | Widths optimized to text | `\needspace` guard | `\autoref` | Verdict |
|:--|:--|:--|:--|:--|:--|:--|
| `tab:terms` (Introduction) | `\textwidth` | yes (`L`, `Y`) | term column widened 3.2 to 3.6 cm so multi-word terms no longer wrap awkwardly | 12 lines | yes | FIX applied |
| `tab:mandate` (Mandate) | `\textwidth` | yes | 3.4 cm label, flexible `Y` | 10 lines | yes | PASS |
| `tab:authority` (Authority) | `\textwidth` | yes | 4.2 cm clause, flexible `Y` | 9 lines | yes | PASS |
| `tab:gates` (Safety) | `\textwidth` | yes | gate column 3.5 to 3.75 cm, agreement and CV columns trimmed to 1.35 and 0.95 cm so numbers sit on one line and the standards column gains room | 16 lines | yes | FIX applied |
| `tab:fiscal` (Fiscal) | `\textwidth` | yes | 2.6 cm year, 3.0 cm amount, flexible `Y` | 12 lines | yes | PASS |
| `tab:constituents` (Constituents) | `\textwidth` | yes | 3.0 cm label, flexible `Y` | 10 lines | yes | PASS |

All six tables match the body measure exactly; the two marked FIX had their column
widths re-balanced to the amount of text each column carries.

## Figure audit (each figure verified twice)

For each figure: pass 1 reasons about the geometry and applies any fix; pass 2
re-reads the corrected figure to confirm. The columns (a), (b), (c) are the three
required checks.

| Figure | (a) No overlap | (b) Looseness | (c) Box spacing | Pass 1 finding and fix | Pass 2 |
|:--|:--|:--|:--|:--|:--|
| Fig 1 path (Intro) | FIX | n/a then PASS | PASS | The wrap edge from box 4 to box 5 swept diagonally across the whole figure and could clip the bottom-row boxes 6 to 8; relaid the bottom row in reverse so box 5 sits under box 4, replaced the long curve with a short straight vertical link, making a clean serpentine | confirmed: no edge crosses a box |
| Fig 2 three gaps (Mandate) | PASS | PASS (0.7, 0.7) | PASS | converging curves enter distinct corner anchors of the target | confirmed |
| Fig 3 federalism (Authority) | PASS | PASS (straight) | PASS | straight edges only, even pitch 4.0 | confirmed |
| Fig 4 verification (Safety) | PASS | PASS (0.5) | PASS | three outcomes on distinct anchors; dashed return bows clear of the BLOCK box | confirmed |
| Fig 5 cost asymmetry (Fiscal) | PASS | PASS (straight) | PASS | the 19 to 1 label sits in empty space right of the vertical edge | confirmed |
| Fig 6 rollout (Constituents) | PASS | PASS (0.7) | PASS | the return curve enters the east anchor, clear of box 2 | confirmed |
| Fig 7 convergence (Bipartisan) | PASS | PASS (0.7, 0.7) | PASS | symmetric curves to the north-west and south-west anchors | confirmed |
| Fig 8 coalition (Coalition) | PASS | PASS (0.6, 0.6) | PASS | radial curves to three stacked nodes, vertical pitch 1.6 | confirmed |
| Fig 9 capstone (Passage) | PASS | PASS (0.7) | PASS | the down-curve enters the east anchor of the implement box | confirmed |
| Fig 10 decision (Appendix) | PASS | PASS (0.5) | PASS | three outcomes on distinct anchors, dashed return clear | confirmed |
| Fig 11 ten gates (Appendix) | PASS | PASS (0.7, 0.7) | PASS | two inputs converge on the diamond from distinct anchors | confirmed |
| Fig 12 amendment map (Appendix) | PASS | PASS (0.6, 0.6) | PASS | radial, vertical pitch 1.4 | confirmed |
| Fig 13 journey (Appendix) | PASS | PASS (straight) | PASS | even pitch 3.6 | confirmed |
| Fig 14 standards (Appendix) | PASS | PASS (0.6, 0.6) | PASS | three inputs to distinct anchors of the examination box | confirmed |
| Fig 15 platform proof (Appendix) | PASS | PASS (straight) | PASS | even pitch 4.2 | confirmed |
| Fig 16 two-chamber (Appendix) | PASS | PASS (0.5) | FIX | node pitch was uneven (3.8, 3.8, 3.4); evened to 3.7 across so spacing is uniform | confirmed: pitch 3.7 throughout |
| Fig 17 markup (Appendix) | PASS | PASS (0.6, 0.6) | PASS | the straight merge edge runs at y=0 while the committee branch dips to y=-1.0, so they do not overlap | confirmed |
| Fig 18 thresholds (Appendix) | PASS | PASS (straight) | PASS | even pitch 4.0 | confirmed |
| Fig 19 objections (Appendix) | PASS | PASS (straight) | FIX | four two-line boxes at vertical pitch 1.0 nearly touched; widened pitch to 1.4 and pushed the column to x=4.6 so the boxes are clearly separated and the fan-out arrows do not crowd | confirmed: gaps even |
| Fig 20 scoring (Appendix) | PASS | PASS (straight) | PASS | even pitch 3.6 | confirmed |

## Summary of corrections carried into the source files

1. Introduction Figure 1: rerouted as a serpentine; the wrap is now a short straight
   vertical link, so no edge crosses a box.
2. Appendix Figure 16: node pitch evened to 3.7 throughout.
3. Appendix Figure 19: vertical box pitch widened from 1.0 to 1.4 and the column
   moved to x=4.6 so the two-line boxes no longer touch.
4. Table `tab:terms`: term column widened to 3.6 cm.
5. Table `tab:gates`: gate column widened to 3.75 cm and the numeric columns trimmed,
   so numbers sit on one line and the standards column gains room.

Every other table and figure passed both checks unchanged. The corrected sources in
this directory compile in Overleaf and are the input to the final stage, which adds
the synthesis table and applies prose and pagination polish without altering the
certified geometry.
