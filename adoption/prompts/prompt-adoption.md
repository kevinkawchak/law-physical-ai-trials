## prompt-adoption

Your goal is to generate a comprehensive clinician adoption framework that helps practicing oncologists, trial investigators, nurses, and clinical research coordinators decide when to trust a verified Physical AI system at the bedside of an oncology clinical trial. This is a new paper topic that is analogous in structure to, but does not rewrite, the legislative narrative review in law-physical-ai-trials/tree/main/review. Deposit all files into kevinkawchak/law-physical-ai-trials/tree/main/adoption. The framework needs to be valid, compelling, and fluid to clinicians who do not have robotics experience or Claude Code/Codex AI application experience. This new work needs to gain in technical substance as the framework evolves; setting up definitions and providing explanations where necessary.

There are 8 body sections in the framework (besides other toc/back matter, etc. sections). The CONFIDENCE GOALS below describe the objectives that each section must meet in order to answer the questions a clinician asks at the bedside before trusting an autonomous recommendation or action. The sentiment throughout should politely align with questions like "Would I let this system near my own family member?", "Can I defend this decision at tumor board?", and "If an auditor asked me tomorrow, could I show exactly what happened and why?" The BACKGROUND information below provides additional methods that support the CONFIDENCE GOALS. ADOPTION ACTIONS below represent the types of movements that need to occur in order for a clinical team to adopt the system. KEY TERMS should be utilized in different parts of the paper to add reputability to the framework.

This will be accomplished by first A) generating unique and comprehensive sub-prompts inspired by the prior build in law-physical-ai-trials/tree/main/review/sub-prompts. B) Run each sub-prompt sequentially as the project continues to grow from draft-framework to full-framework to final-framework. You will have to adapt to a self-learning process inspired by prior user works, while ensuring each framework paper stage is appropriate, high quality, and comprehensive throughout. There is no sub-prompt need for the paper template, as law-physical-ai-trials/tree/main/review/template is the template.

Create an auto-commit / auto-PR process in real-time that allows for the user to monitor branch progress without any user intervention. This is an extensive process. A single last update by you provides changelog, versioning, and other updates provided below.

"SUB-PROMPT SCHEDULE"
1. 20+ Mermaid figures must be high quality, comprehensive, professional and professionally colored (adapt most relevant diagrams using only black, grayscales, and #EBCB8B, #D08770, #8B2E3F throughout the paper inspired by review/mermaid) (20+ commits) (diagrams will be changed and improved throughout the draft, full, final process below). Keep the existing #8B2E3F paper template color theme
2. draft-framework: (the new paper's first paper that provides sets of bracketed instructions that also identify exact repository files and directories for subsequent papers to process) (10+ commits) Adapt a table of contents, back matter and other paper supporting information from: review/final-narrative
3. full-framework: (the new second iteration paper needs to utilize the files and directories identified in draft-framework effectively to generate a full version) (10+ commits)
4. final-framework: (your context and formatting quality should be publication quality) (learn from and implement corrections you identify from full-framework) (10+ commits)
"SUB-PROMPT SCHEDULE"

"RULES"
1. Only commit to the "kevinkawchak/law-physical-ai-trials" repository with a comprehensive README. All subdirectories need to have detailed READMEs. Do not commit to other repositories
2. The law-physical-ai-trials/tree/main/review/template paper template visual appearance needs to remain, but contents and 8 sections based on CONFIDENCE GOALS need to be adapted with this project
3. Only Claude Code Opus 4.8 (1M Context) Max can be used throughout all of this single prompt and sub-prompts. Do not stall, ask questions, or go into plan mode
4. No png images are allowed
5. Use tables where relevant, make sure each table is the width of the body text - based on prior user code formatting preferences from the review.
6. Each README.md for each directory must be comprehensive and state which files from other directories were used and where
7. For each sub-prompt: 1 commit is required for each of the following (main.tex, .sty, .bib, and README); and 1 commit is required for each of the framework's .tex sections (1 .tex file per section) that each correspond to main.tex
8. For each sub-prompt: the 2nd to last commit, fix all of your errors for all files. For the last commit, perform the remaining repository updates defined below
9. All commits and PRs must be submitted to GitHub in real-time the moment they are generated for user viewing. Do not hold commits and PRs from GitHub as they are completed
10. There must be a single last v0.2.0 update that provides the main directory CHANGELOG.md, releases.md, repository updates, (as inspired by the prior v0.1.0 update, but without rewriting the prior version, and with relevant main readme badges)
11. You have permission to commit, commit to the working branch, and create PRs in GitHub
12. Do not take shortcuts from sub-prompt to sub-prompt: every stage must be fully developed. All files generated from prompts must be present and working. Each set of LaTeX files must compile properly in Overleaf by the author
13. Don't stop until all tasks are completed. The user will continue the session by using the phrase "Continue" if tokens are exhausted. This is a lengthy process
14. Leave DOI in the format: 10.5281/zenodo.xxxxxxxx (with Hyperlink: https://doi.org/10.5281/zenodo.xxxxxxxx).
15. Learn and implement the author's \clearpage, table formatting column widths, and other types of \vspace and \hspace formatting methods. Learn from and implement the author's other corrections/proof reading techniques to create the polished final-framework source files.
16. All draft-framework, full-framework, and final-framework developments must have their own .tex outputs and tex zip file that run properly in Overleaf
17. Utilize prior author works where relevant in law-physical-ai-trials/blob/main/review/references/author_works.bib, in this prompt, and from accurate BibTeX sources you find online
18. You will be judged on how well you followed these rules and sub-prompt schedule after you finish by the author and other people
19. Don't take any shortcuts. Do not rewrite or alter the prior version under review/
"RULES"

In later commits, update law-physical-ai-trials/blob/main/README.md repository structures, badges, ASCII diagrams and toc, and other affected areas in the repository (this is the only repository that needs to be edited). Add a short 425 character (with spaces) summary for this update. Add 1 additional section towards the top of the README body that further details this version (followed by the toc, repository structure, badges, etc.), without removing or rewriting the prior v0.1.0 section. Include tables and colored mermaid diagrams from the final-framework paper where relevant throughout the main/README.

For each framework paper: avoid large white empty spaces without text. Where large spacing between words exist throughout the body of text.: modify \raggedright spacing to make positioning between words look equally and properly spaced. Make sure text doesn't run off the right side of the page anywhere. Include instructions to avoid lines with a single or two words. All tables need to use a similar format for each column width as in this example: The contents of every table cell must be properly left aligned using the example format:{>{\raggedright\arraybackslash}p{2cm}. Every width value must have a prepended \raggedright\arraybackslash to ensure no big gaps between words in tables. It is also important that tables match the exact width of the body of the text.

Avoid single lines separate from the main paragraph on the next page. Perform the final formatting steps that a senior author would take by correcting white space formatting and removing and/or adding relevant text to make each section and page look properly formatted and self standing by itself. (Don't overcrowd the page with text, some white space formatting is ok). Make sure to correct all incorrect symbols such as SS into "§" where relevant. Use single dashes, but no em dashes, double dashes, or triple dashes throughout the paper.

Inside law-physical-ai-trials/tree/main/adoption/prompts: Create a prompt-adoption.md that uses a "## prompt-adoption" heading followed by this entire prompt word-for-word. Make sure only a heading and this exact prompt text is included. Create a separate output-adoption.md that uses a "## output-adoption" heading followed by the entire output of this prompt (containing the Claude markdown output, not the code files). Be sure only the heading with the exact Claude Code output is included.

"CONFIDENCE GOALS"
Section 1
1. Competence
The first question a clinician asks of any tool.
Clinicians need to know:
* Is the system actually good at this specific task, on patients like mine?
* What is the validation evidence, and how was it measured?
* How does performance compare to the current standard of care?
* What are the known failure modes?
The underlying question: "Is it actually good at this, or only good on paper?" This is answered with benchmark results, prospective validation, and the assurance run that passed every automated test.

Section 2
2. Safety
The clinician's duty of non-maleficence.
Clinicians need to know:
* What concretely stops the system from harming my patient?
* Is there a hard stop before any irreversible action?
* How are adverse events detected and contained?
The underlying question: "What stops it before it hurts someone?" This is answered by the ten verification gates and the catastrophe-predicate BLOCK that halts execution.

Section 3
3. Transparency
The clinician cannot endorse a black box.
Clinicians need to know:
* Can I see why the system did what it did?
* Is there a complete, tamper-evident record of every decision?
* Can I reconstruct events after the fact?
The underlying question: "Can I see why it did that?" This is answered by explainable outputs and a hash-chained audit trail.

Section 4
4. Oversight
The clinician must remain the responsible agent.
Clinicians need to know:
* Am I still in control, or is the machine deciding alone?
* How do I override, pause, or stop the system?
* When does it escalate to a qualified human?
The underlying question: "Am I still in control?" This is answered by human-in-the-loop design, the ESCALATE path, and an unconditional override.

Section 5
5. Equity
The clinician treats this patient, not the average patient.
Clinicians need to know:
* Does it work for this patient, not just the population mean?
* Is performance reported per subgroup?
* Is bias actively surveilled and corrected?
The underlying question: "Does it work for the patient in front of me?" This is answered by subgroup performance reporting and continuous bias surveillance.

Section 6
6. Reliability
The clinician needs the same answer tomorrow.
Clinicians need to know:
* Will it behave the same way at 3 a.m. as at noon?
* How is model drift detected and handled?
* How is uncertainty quantified and communicated?
The underlying question: "Will it be the same tomorrow?" This is answered by reproducibility controls, drift monitoring, and uncertainty quantification.

Section 7
7. Accountability
The clinician must know where responsibility sits.
Clinicians need to know:
* Who answers when something goes wrong?
* What is documented, and by whom?
* How is liability allocated across the human and the system?
The underlying question: "Who is responsible when it is wrong?" This is answered by explicit roles, a signed standard operating procedure, and a documentation chain.

Section 8
8. Workflow
The best safe tool fails if it does not fit.
Clinicians need to know:
* Does it fit how I actually work?
* Does it reduce burden or add to it?
* How does it change consent and the clinic day?
The underlying question: "Does it fit how I actually work?" This is answered by workflow integration, burden measurement, and a verified consent process.
"CONFIDENCE GOALS"

"BACKGROUND"
Trust in clinical artificial intelligence is earned, not declared. The literature on clinician adoption of decision support and autonomous systems is consistent: clinicians adopt a tool when it is demonstrably competent, when its safety case is explicit, when its reasoning is inspectable, when they retain meaningful control, when it is fair across the patients they actually see, when it is reliable over time, when accountability is unambiguous, and when it fits the clinical workflow rather than fighting it. Each of these is a precondition; a system that is brilliant but opaque, or safe but unusable, will not be adopted, and should not be.

The Calibration of Trust. The goal is not maximal trust but calibrated trust: a clinician should rely on the system exactly as much as its demonstrated performance warrants, no more and no less. Over-trust (automation bias) and under-trust (algorithm aversion) are both failure modes. A good confidence framework gives the clinician the evidence to calibrate.

Verification Before Generation. The mechanism at the center of this framework is the same one defined in the prior review: a software agent (Claude Code) proposes a clinical action, a second independent agent (Codex) reviews it, and a ten-gate verification, validation, and uncertainty quantification examination either ACCEPTs the action under audit, ESCALATEs it to a qualified human, or BLOCKs it before it can reach a patient. The eight confidence questions are the clinician-facing view of that mechanism.

The Balancing Act: Confidence vs. Evidence. Every confidence claim in this framework is paired with a credible, cited fact, so that a clinician can defend the decision at tumor board and to an auditor. The framework draws on the author's documented engineering lineage, including a surgical-humanoid assurance run, and on widely cited external evidence on medical error, algorithmic bias, and the convergence of human and machine performance.

References (carried into framework_refs.bib):
kohn2000toerr; makary2016medical; obermeyer2019dissecting; topol2019high; fda2021samd; asme2018vv40; the advocacy-science set ingber2025regulating, moreland2015hearing, novak2020patient, putturaj2025honouring, kok2013finding.
"BACKGROUND"

"ADOPTION ACTIONS"
Local Validation: Confirming the system performs on the site's own patient population before clinical use, not only on the vendor's benchmark.
Credentialing and Training: Qualifying the clinical team to supervise, interpret, override, and document the system, with a defined competency.
Workflow Integration: Embedding the system into the clinic day, the electronic record, and the consent process so it reduces rather than adds burden.
Continuous Monitoring: Surveilling performance, drift, subgroup equity, and adverse events after go-live, with a defined response.
"ADOPTION ACTIONS"

"KEY TERMS"
Calibrated Trust: reliance proportional to demonstrated performance.
Automation Bias / Algorithm Aversion: the two symmetric failure modes of miscalibrated trust.
Human-in-the-Loop / Human-on-the-Loop: supervision models defining where the clinician sits relative to the action.
Standard Operating Procedure (SOP): the signed document allocating roles and steps for routine and adverse events.
Audit Trail: the tamper-evident, hash-chained record of every decision and action.
Subgroup Performance: model accuracy reported per clinically relevant population, not only in aggregate.
"KEY TERMS"

Include GitHub v0.2.0 documentation headings and release notes. Be sure to fix and address errors that would cause failed checks for the single pull request (such as for lint and Python environment issues to avoid the following error during final checks): "3 failing checks
x CI / lint-and-format (3.10) (pull...
x CI / lint-and-format (3.11) (pull...
x CI / lint-and-format (3.12) (pull... " Place the new release notes in releases.md under main using the format below. Update other relevant documentation such as project structures. Update the main Readme diagrams, repository structure, etc. where necessary. Update the CHANGELOG.md (v0.2.0). Do not remove or rewrite the prior v0.1.0 entries.

"FORMAT"
Release title
v0.2.0 - [Fill in Title Here]

## Summary

## Features

## Contributors
@kevinkawchak
@claude
@google-gemini
@openai

## Notes
"FORMAT"
