## output-enactment

This file records the markdown narrative of the run that produced the `enactment/`
paper topic (repository release v0.3.0). It captures the reasoning and the build
schedule, not the source files themselves; the source files live in the stage
directories and are reproduced verbatim there.

### Topic selection

The submitted prompt asked for a new paper topic, analogous in structure to the
`adoption/` clinician confidence framework (v0.2.0) and the `review/` narrative
review (v0.1.0), whose single objective is to make H. R. 9510 (2026) most likely
to pass in **both** the House and the Senate. After reading the most recent bill
version (the *Verification Before Generation in Physical AI Oncology Trials Act of
2026*, the Financial Data Amendment, H. R. 9510 v5.0, DOI 10.5281/zenodo.20619762)
and the scope of the National Platform for Physical AI Oncology Trials
(DOI 10.5281/zenodo.19244918), the selected topic is:

> **Earning the Congress's Vote: An Eight-Question Passage Framework for Enacting
> H. R. 9510 in the House and Senate.**

The framework is built for the staffer, the member, and the committee counsel who
must decide whether to mark up, cosponsor, and vote for the bill. Where the
`adoption/` paper answered the eight questions a clinician asks at the bedside,
this paper answers the eight questions a legislator asks before a yes vote. Each
question is paired with a credible, cited fact drawn from the bill text, the
platform evidence, and the public record, so that the answer is defensible on the
floor and in a markup.

### The eight passage questions (the body sections)

1. Mandate: is the problem real enough to need a Federal statute?
2. Authority: is this within Congress's power and consistent with existing law?
3. Safety: what in the bill actually protects patients?
4. Fiscal: what does it cost, and is it paid for?
5. Constituents: who does this help back home, in every State and district?
6. Bipartisanship: can one caucus support it without losing the other?
7. Coalition: who is behind it, and is the opposition manageable?
8. Passage path: can it move through both chambers and then be implemented?

### How the build runs

A single submitted prompt (`prompts/prompt-enactment.md`) drives two processes.
Process A generated the five sub-prompts in `sub-prompts/`, adapted from the four
`adoption/sub-prompts/` and extended with a new verification stage. Process B ran
them in sequence to grow the manuscript through five stages:

```
sub-prompts/ -> mermaid/ -> draft-framework/ -> full-framework/ -> verify-framework/ -> final-framework/
 (5 prompts)   (20 figs)    (scaffold + cues)   (rendered prose)    (table/figure audit)   (publication)
```

The new `verify-framework/` stage sits between the full and final source files. It
double-verifies every table and every figure against the instructions: a uniform
`\vspace{-0.75cm}` between each figure and its caption; column widths optimized for
the amount of text per column; and a twice-repeated figure audit confirming that no
text box overlaps an arrow, that every curved arrow carries an explicit looseness
value, and that boxes are spaced evenly. Only the corrections it certifies are
carried into `final-framework/`.

### Palette and template

Figures use only black, grayscales, and the three theme colors `#4B0082` (indigo,
authority and the bill), `#000080` (navy, evidence and support), and `#C0C0C0`
(silver, cost and caution). The paper template color is `#4B0082`. No raster image
is used; every Mermaid figure is reproduced as colored TikZ in the compiled LaTeX.

### References

The author reference set was trimmed to the works that bear on legislation,
regulation, and the platform, and the chemistry and spectrometry preprints that do
not bear on passage were removed. Topic references were added with working URLs to
professional sources: the Federal Food, Drug, and Cosmetic Act, the 21st Century
Cures Act, the Congressional Budget Office, the Statutory Pay-As-You-Go Act, the
Unfunded Mandates Reform Act, the Open Payments system, the consensus safety
standards (ASME V&V 40, ISO 14971, IEC 80601-2-77, ISO/TS 15066, UL 4600,
IEEE 7009), and the named precedent bills.

### Build discipline

Every file is committed in real time on the working branch, one file per commit at
the required granularity, with a second-to-last error-fix commit and a final
repository-updates commit per stage, all visible in a single pull request. Only
`kevinkawchak/law-physical-ai-trials` is edited; the prior v0.1.0 `review/` and
v0.2.0 `adoption/` content is not rewritten. The single closing v0.3.0 update adds
the root `CHANGELOG.md`, `releases.md`, and a new README section without altering
the prior versions.
