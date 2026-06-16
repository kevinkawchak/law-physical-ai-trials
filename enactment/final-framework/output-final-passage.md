## output-final-passage

This file records the markdown narrative of Stage 5, the final-framework. It is not
the source files; those are `main.tex`, `passagestyle.sty`, `references.bib`, the
twelve `sections/*.tex`, and the `publication/` mirror.

### What the final stage produced

The verify-stage sources, with their certified figure geometry and optimized table
columns, were carried to publication quality. The senior-author finishing applied
here is:

- `\raggedbottom` replaces `\flushbottom` so page bottoms are natural rather than
  stretched, removing large vertical white bands, and `\tolerance` is lowered to
  1800 for tighter, even interword spacing with no right-margin overflow.
- A ninth synthesis table (`tab:synthesis`) closes the manuscript by mapping each of
  the eight questions to the provision, score line, or evidence that answers it, the
  one page a member can carry into a markup.
- Citations are rendered cleanly with the `ieeetr` style and `\nocite{*}` so every
  entry prints and each DOI or URL resolves.
- The certified figures are carried unchanged in geometry; captions explain rather
  than narrate; section references use the section symbol and single hyphens only.

### The deposit mirror

The `publication/` subdirectory holds the identical source bundled for deposit, with
its own README and `LaTeX Source Files.zip`.

### What did not change

The prose is the full-stage prose, refined only at the margins; the twenty figures
keep the geometry the verify stage certified; the palette is unchanged. The prior
`review/` (v0.1.0) and `adoption/` (v0.2.0) content was not touched.

### Next

The single closing v0.3.0 update follows: the root `CHANGELOG.md`, `releases.md`, and
a new README section, with badges, a synthesis table, and a colored Mermaid diagram,
without rewriting the prior versions.
