## prompt-narrative

Your goal is to generate a comprehensive narrative story that helps transition Physical AI Trial Bill H. R. 9510 v5.0 into a new Federal AI law. Deposit all files into kevinkawchak/law-physical-ai-trials/tree/main/review. The story needs to be valid, compelling, and fluid to those in medical AI legislation who do not have either robotics experience or Claude Code/Codex AI application experience. This new work needs to gain in technical substance as the story evolves; setting up definitions and providing explanations where necessary.

There are 8 body sections in the narrative (besides other toc/back matter, etc. sections). The SECTION GOALS below describe the objectives that each section must meet in order to appeal to the emotions of legislators who will be taking action converting the Bill to Law. The sentiment throughout should politely align with questions like "How did we ever utilize humans alone for this challenging task?", "Why did we ever fully trust the prior human clinical trial system if there were so many opportunities for compounding human error?", and "Why would the human peer-review process continue to be utilized for increasingly complex and voluminous AI outputs?" The BACKGROUND information below provides additional methods that supports the SECTION GOALS. MAIN ACTIONS below represent the types of movements that need to occur in order for the Bill to pass. KEY TERMS should be utilized in different parts of the paper to add reputability to the narrative story.

This will be accomplished by first A) generating unique and comprehensive sub-prompts inspired by single-prompt-bill/tree/main/auto-bill-02 and single-prompt-bill/tree/main/auto-bill-02/sub-prompts. B) Run each sub-prompt sequentially as the project continues to grow from draft-narrative to full-narrative to final-narrative. You will have to adapt to a self-learning process inspired by prior user works, while ensuring each narrative paper stage is appropriate, high quality, and comprehensive throughout. There is no sub-prompt need for the narrative template, as law-physical-ai-trials/tree/main/review/template is the template.

Create an auto-commit / auto-PR process in real-time that allows for the user to monitor branch progress without any user intervention. This is an extensive process. A single last update by you provides changelog, versioning, and other updates provided below.

"SUB-PROMPT SCHEDULE"
1. 20+ Mermaid figures must be high quality, comprehensive, professional and professionally colored (adapt most relevant diagrams using only black, grayscales, and #EBCB8B, #D08770, #8B2E3F throughout the paper inspires by Clinical-AI-Demos/tree/main/ai-outputs/output-01) (20+ commits) (diagrams will be changed and improved throughout the draft, full, final process below). Keep the existing #8B2E3F paper template color theme
2. draft-narrative: (the new paper's first paper that provides sets of bracketed instructions that also identify exact repository files and directories for subsequent papers to process) (10+ commits) Adapt a table of contents, back matter and other paper supporting information from: cancer-automated/tree/main/papers/VVUQ-02/final-paper
3. full-narrative: (the new second iteration paper needs to utilize the files and directories identified in draft-narrative effectively to generate a full version) (10+ commits)
4. final-narrative: (your context and formatting quality should be publication quality) (learn from and implement corrections you identify from full-narrative) (10+ commits)
"SUB-PROMPT SCHEDULE"

"RULES"
1. Only commit to the "kevinkawchak/law-physical-ai-trials" repository with a comprehensive README. All subdirectories need to have detailed READMEs. Do not commit to other repositories
2. The law-physical-ai-trials/tree/main/review/template paper template visual appearance needs to remain, but contents and 8 sections based on SECTION GOALS need to be adapted with this project
3. Only Claude Code Opus 4.8 (1M Context) Max can be used throughout all of this single prompt and sub-prompts. Do not stall, ask questions, or go into plan mode
4. No png images are allowed
5. Use tables where relevant, make sure each table is the width of the body text - based on prior user code formatting preferences from the Bill v5.0.
6. Each README.md for each directory must be comprehensive and state which files from other directories were used and where
7. For each sub-prompt: 1 commit is required for each of the following (main.tex, .sty, .bib, and README); and 1 commit is required for each of the narrative's .tex sections (1 .tex file per section) that each correspond to main.tex
8. For each sub-prompt: the 2nd to last commit, fix all of your errors for all files. For the last commit, perform the remaining repository updates defined below
9. All commits and PRs must be submitted to GitHub in real-time the moment they are generated for user viewing. Do not hold commits and PRs from GitHub as they are completed
10. There must be a single last v0.1.0 update that provides the main directory CHANGELOG.md, releases.md, repository updates, (as inspired by kevinkawchak/cancer-automated, but with 3x as many relevant main readme badges)
11. You have permission to commit, commit to main, merge, and create PRs in GitHub
12. Do not take shortcuts from sub-prompt to sub-prompt: every stage must be fully developed. All files generated from prompts must be present and working. Each set of LaTeX files must compile properly in Overleaf by the author
13. Don't stop until all tasks are completed. The user will continue the session by using the phrase "Continue" if tokens are exhausted. This is a lengthy process
14. Leave DOI in the format: 10.5281/zenodo.xxxxxxxx (with Hyperlink: https://doi.org/10.5281/zenodo.xxxxxxxx).
15. Learn and implement the author's /clearpage, table formatting column widths, and other types of /vspace and /hspace formatting methods. Learn from and implement the author's other corrections/proof reading techniques to create the polished final-narrative source files.
16. All draft-narrative, full-narrative, and final-narrative developments must have their own .tex outputs and tex zip file that run properly in Overleaf
17. Utilize prior author works where relevant in law-physical-ai-trials/blob/main/review/references/author_works.bib, in this prompt, and from accurate BibTeX sources you find online
18. You will be judged on how well you followed these rules and sub-prompt schedule after you finish by the author and other people
19. Don't take any shortcuts
"RULES"

In later commits, update law-physical-ai-trials/blob/main/README.md repository structures, badges, ASCII diagrams and toc, and other affected areas in the repository (this is the only repository that needs to be edited). Add a short 425 character (with spaces) summary for this update. Add 1 additional section towards the top of the README body that further details this version (followed by the toc, repository structure, badges, etc.) Include tables and colored mermaid diagrams from the final-narrative paper where relevant throughout the main/README.

For each narrative paper: avoid large white empty spaces without text. Where large spacing between words exist throughout the body of text.: modify \raggedright spacing to make positioning between words look equally and properly spaced. Make sure text doesn't run off the right side of the page anywhere. Include instructions to avoid lines with a single or two words. All tables need to use a similar format for each column width as in this example: The contents of every table cell must be properly left aligned using the example format:{>{\raggedright\arraybackslash}p{2cm}. Every width value must have a prepended \raggedright\arraybackslash to ensure no big gaps between words in tables. It is also important that tables match the exact width of the body of the text.

Avoid single lines separate from the main paragraph on the next page. Perform the final formatting steps that a senior author would take by correcting white space formatting and removing and/or adding relevant text to make each section and page look properly formatted and self standing by itself. (Don't overcrowd the page with text, some white space formatting is ok). Make sure to correct all incorrect symbols such as SS into "§" where relevant. Use single dashes, but no em dashes, double dashes, or triple dashes throughout the paper.

Inside law-physical-ai-trials/tree/main/review/prompts: Create a prompt-narrative.md that uses a "## prompt-narrative" heading followed by this entire prompt word-for-word. Make sure only a heading and this exact prompt text is included. Create a separate output-narrative.md that uses a "## output-narrative" heading followed by the entire output of this prompt (containing the Claude markdown output, not the code files). Be sure only the heading with the exact Claude Code output is included.

"SECTION GOALS"
Section 1
1. Compassion and Empathy
Probably the most common emotion.
Advocates highlight:
* Patients suffering from serious illness
* Families caring for loved ones
* Children with rare diseases
* People unable to access treatment
* Patient testimony often answers the question: "What happens if we do nothing?"
Examples:
* Rare disease legislation
* Cancer screening laws
* Expanded insurance coverage
* Right-to-try and compassionate-use initiatives.
* A lawmaker may hear statistics from experts all day, but a patient describing their experience can create a memorable emotional anchor.

Section 2
2. Fear of Preventable Harm
Another powerful motivator.
Legislation is often supported by stories involving:
* Missed diagnoses
* Medical errors
* Unsafe products
* Delayed treatment
* Deaths that might have been prevented
* The underlying emotional message is:
"Without this law, more people will suffer." This has historically been influential in areas such as:
* Drug safety regulation
* Medical device oversight
* Public health measures
* Electronic health record requirements
* AI safety and algorithmic accountability proposals
Section 3
3. Moral Outrage
Many healthcare laws gain momentum after a perceived injustice.
Common narratives:
* Insurance denials
* Unaffordable treatments
* Discrimination
* Corporate negligence
* Unequal access to care
* The emotional framing becomes:
"This is unfair and should not happen in America."
Outrage can be particularly effective because it motivates both public attention and media coverage.

Section 4
4. Hope
Not all successful healthcare legislation relies on fear.
Supporters often emphasize:
* New cures
* Scientific breakthroughs
* Better patient outcomes
* Faster diagnosis
* More efficient healthcare delivery
* For medical AI legislation, hope-based arguments frequently include:
* Earlier cancer detection
* Reduced physician burnout
* Improved rural healthcare access
* Faster drug discovery
The emotional appeal is:
"We have an opportunity to save lives if we act."

Section 5
5. Responsibility and Duty
This emotion is often directed specifically at legislators.
Advocates frame issues as:
"You have the power to prevent this."
or
"Future generations will judge what we do now."
This creates a sense of obligation rather than sympathy.

Section 6
6. Protection of Vulnerable People
Healthcare debates often focus on groups viewed as needing protection:
* Children
* Elderly individuals
* Disabled patients
* Veterans
* Rural communities
* The emotional appeal is protective rather than purely compassionate.
For AI legislation, this often appears as concerns about:
* Bias against minority populations
* Errors affecting vulnerable patients
* Lack of informed consent
Section 7
7. Trust and Reassurance
Particularly important in medical AI.
Many AI-related bills face public skepticism. Supporters often try to evoke confidence through:
* Physician endorsements
* Academic experts
* Safety testing requirements
* Transparency provisions
* Pilot program results
* The emotional objective is:
"This technology can be trusted."

Section 8
8. Urgency
Legislation often accelerates when advocates successfully create a sense that delay has consequences.
Messages include:
* Patients are waiting now.
* Lives are being lost now.
* Technology is advancing faster than regulation.
"SECTION GOALS"

"BACKGROUND"
In the landscape of U.S. health policy, the path to passing new medical or AI-related legislation is often paved not just with data, but with "emotional narratives" that make complex, abstract technical topics feel urgent and human-centered. Advocacy strategies frequently use specific emotional levers to bridge the gap between technical complexity and the priorities of legislators [1].
The Role of Emotional Narratives
Legislators are often influenced more by compelling, concise stories than by complex statistical data alone. Stories serve to humanize abstract policy concepts, making the stakes of a bill-whether it involves medical AI or new clinical standards-tangible [2].
* Humanizing the Abstract: When AI is the subject, the technology is often viewed as cold, black-box, or intangible [1]. Advocates use patient stories to provide "contextual depth," grounding the bill in a lived experience (e.g., a patient misdiagnosed by an algorithm or saved by a predictive tool) to give decision-makers a clear sense of the "real-world" impact [3].
* The Power of Testimonial: While few legislators report that testimony directly changes their vote, effective testimony-particularly that which is credible and knowledge-based-influences their awareness, informs floor debates, and can strengthen or clarify the language of a bill [2].
* Empathetic Witnessing: Techniques like narrative-based advocacy are used to create space for marginalized voices or those who have been harmed by systemic gaps, allowing them to share vulnerabilities that statistics often obscure [4].
Emotional Levers in Advocacy
Advocates often target specific emotional states to motivate action. The "right" emotion depends on the goal:
1. Urgency (Fear of Inaction): Appeals to fear are common, especially when demonstrating the "negative health consequences" of current practices. However, psychological research suggests that fear is only effective if the audience also feels a sense of self-efficacy-the belief that the proposed legislation can actually solve the problem [5]. If a problem is presented as catastrophic without a viable legislative solution, legislators may become defensive or paralyzed rather than motivated to act.
2. Empathy and Connection: By highlighting the "lived experiences of illness," advocates aim to foster a sense of mutual understanding between the patient community and the policymaker [3]. This "empathetic witnessing" transforms a bill from a technical requirement into a moral imperative to protect a specific group [4].
3. Sense-Making (Relabeling): When trying to pass complex reforms, advocates often engage in "sense-making," which involves reinterpreting current failures (like a medical error or an AI bias incident) as a "call to action" to modernize or improve the system.
The Balancing Act: Emotion vs. Evidence
Despite the reliance on storytelling, the most effective advocacy strategies for medical and AI legislation balance narrative with credible, unbiased data [2].
* Credibility: Legislators often weigh the "characteristics of the presenter"-their credibility and knowledge-more heavily than the emotional intensity of the story [2].
* Translating Evidence: Advocates are increasingly trained to act as "boundary spanners" who can mobilize both formal scientific evidence and lived experience simultaneously [4]. The goal is to provide a "bridge between evidence, ethics, and power," where the emotional story makes the data memorable, and the data makes the story actionable.
Summary of Strategic Tools
Tool	Function
Personalized Narratives [3]	Humanizes abstract technology (like AI) and clarifies the "human cost" of policy inaction.
Credible Testimony[2]	Provides the necessary data foundation to ensure the legislative language is technically sound.
Scenario-Based Risk Info [1]	Helps decision-makers visualize future losses or benefits, turning "what-if" scenarios into clear policy goals.
Advocacy Frameworks [4]	Connects lived experiences of marginalized groups to institutional decision-making to address health inequities.
References
Code snippet

@phdthesis{ingber2025regulating,
  title={Regulating Emotion AI in the United States: Insights from Empirical Inquiry},
  author={Ingber, A.},
  year={2025},
  school={Deep Blue Repositories},
  note={Working paper / Doctoral dissertation}
}

@article{moreland2015hearing,
  title={"Hearing from all sides": How legislative testimony influences state level policy-makers in the United States},
  author={Moreland-Russell, S. and Barbero, C. and Andersen, S. and Geary, N. and Dodson, E. A. and Brownson, R. C.},
  journal={International Journal of Health Policy and Management},
  volume={4},
  number={2},
  pages={91--98},
  year={2015},
  publisher={Kerman University of Medical Sciences},
  doi={10.15171/ijhpm.2015.13}
}

@article{novak2020patient,
  title={Patient stories can make a difference in patient-centered research design},
  author={Novak, L. L. and George, S. and Wallston, K. A. and Joosten, Y. A. and Israel, T. L. and Simpson, C. L. and Wilkins, C. H.},
  journal={Journal of Patient Experience},
  volume={7},
  number={6},
  pages={1438--1444},
  year={2020},
  publisher={SAGE Publications},
  doi={10.1177/2374373520958340}
}

@article{putturaj2025honouring,
  title={"Honouring the storyteller": The potential of Playback Theatre in health policy and systems research},
  author={Putturaj, M.},
  journal={Health Policy and Planning},
  volume={40},
  number={7},
  pages={809--817},
  year={2025},
  publisher={Oxford University Press},
  doi={10.1093/heapol/czad000}
}

@article{kok2013finding,
  title={Finding theory- and evidence-based alternatives to fear appeals: Intervention Mapping},
  author={Kok, G. and Bartholomew, L. K. and Parcel, G. S. and Gottlieb, N. H. and Fern{\'a}ndez, M. E.},
  journal={International Journal of Psychology},
  volume={49},
  number={2},
  pages={98--107},
  year={2013},
  publisher={Wiley Online Library},
  doi={10.1002/ijop.12001}
}
"BACKGROUND"

"MAIN ACTIONS"
Advocacy: Advocacy is any action that speaks in favor of, recommends, or defends a cause-in this case, safe or innovative medical AI.
Coalition Building: Forming an alliance of diverse groups (e.g., tech companies, hospital networks, patient advocacy groups, and medical boards) to show lawmakers that the bill has wide-ranging support.
Policy Entrepreneurship: When an individual or group actively identifies a problem (like algorithmic bias in healthcare) and champions a specific legislative solution (the bill) to fill that gap.
Reconciliation: If the House and the Senate pass two different versions of a medical AI bill, a committee must "reconcile" the differences into one final bill that both chambers can vote on.
"MAIN ACTIONS"

"KEY TERMS"
Lobbying
Fundraising / PAC Contributing
Campaign Finance / Political
Contributions
Soft Money vs. Hard Money
Grants / Foundation Funding
Markup: The process by which a congressional committee debates, amends, and rewrites the medical AI bill based on feedback from experts and lobbyists.
Testimony / Committee Hearings: Bringing in AI experts, doctors, and patients to testify before a committee to build an official public record of why the bill is needed.
"KEY TERMS"

Include GitHub v0.1.0 documentation headings and release notes. Be sure to fix and address errors that would cause failed checks for the single pull request (such as for lint and Python environment issues to avoid the following error during final checks): "3 failing checks
x Cl / lint-and-format (3.10) (pull...
x Cl / lint-and-format (3.11) (pull...
x Cl / lint-and-format (3.12) (pull... " Place the new release notes in releases.main under main using the format below. Update other relevant documentation such as project structures. Update the main Readme diagrams, repository structure, etc. where necessary. Update the CHANGELOG.md (v0.1.0).

"FORMAT"
Release title
v0.1.0 - [Fill in Title Here]

## Summary

## Features

## Contributors
@kevinkawchak
@claude
@google-gemini
@openai

## Notes
"FORMAT"
