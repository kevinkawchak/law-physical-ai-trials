## output-draft-passage

This file records the markdown narrative of Stage 2, the draft-framework scaffold.
It is not the source files; those are `main.tex`, `passagestyle.sty`,
`references.bib`, and the twelve `sections/*.tex`.

### What the draft stage produced

The draft lays out the full manuscript on the recolored template (the `#4B0082`
indigo accent, the title rule, the abstract box, the `L`/`C`/`Y` table columns) and,
in every body section, leaves bracketed `[DRAFTING INSTRUCTIONS: ...]` that name the
exact repository files the later stages must process. It is a scaffold, not finished
prose: it establishes the skeleton, the figure and table slots, and the citation
plan, so the full stage has an unambiguous brief.

### Structure laid down

- Front matter: title page on the indigo theme, abstract, disclaimer, keywords.
- Introduction: the lay-term glossary to be written, the three recurring passage
  questions, and the framework-in-miniature figure.
- Eight body sections, one file each, mapped to the passage questions: mandate,
  authority, safety, fiscal, constituents, bipartisanship, coalition, passage path.
- Appendix A figure compendium and the back matter (acknowledgments, ethical
  disclosures, rights and permissions, cite this article, data availability).

### Self-learning carried forward

The draft encodes the formatting lessons from the prior publication: the
`>{\raggedright\arraybackslash}p{<width>}` table columns sized to the text each
column carries, the `\needspace` guard before every table, maximal widow and club
penalties, single hyphens only, and the colored TikZ figure primitive (`psgfig`)
with a uniform `\vspace{-0.75cm}` figure-to-caption gap built into `\psgcaption`.
Each body section names which Mermaid figure slot and which table it will carry in
the full stage, and every bracket names exact source files in the bill publication,
the platform paper, and the two reference bibliographies.

### Next stage

The full stage (`../full-framework/`) replaces every bracket with finished prose
drawn from the named sources, renders the colored TikZ figures from the catalog, and
completes every table.
