## output-mermaid

# Colored Mermaid Catalog for the H. R. 9510 Narrative Review

Twenty-one professional, colored Mermaid figures that illustrate the eight
emotional-pillar sections and the legislative argument of the narrative review.
They are produced by sub-prompt 1 (`../sub-prompts/prompt-1-mermaid.md`) and are
adapted from the curated Mermaid families in
`Clinical-AI-Demos/tree/main/ai-outputs/output-01`, re-themed to this project.

Every figure uses the strict palette only: black, grayscales, and the three theme
colors `#EBCB8B` (gold, hope), `#D08770` (clay, risk), and `#8B2E3F` (burgundy,
the Act). The `#8B2E3F` paper template theme is preserved. Each figure is
reproduced in the compiled LaTeX narrative as a matching colored TikZ figure in
the same palette, and the figures are refined across the draft, full, and final
stages.

### Palette

| Role | Fill | Text | Meaning |
|:--|:--|:--|:--|
| `act` | `#8B2E3F` | white | the Act, verification, human protection |
| `hope` | `#EBCB8B` | black | hope, benefit, accepted outcome |
| `risk` | `#D08770` | black | harm, risk, the legacy path |
| `n1` | `#F2F2F2` | black | inputs, light structure |
| `n2` | `#D9D9D9` | black | process steps |
| `n3` | `#BFBFBF` | black | gates, emphasis structure |

### Index

1. Verification Before Generation Workflow
2. The Eight Emotional Pillars
3. The Bill-to-Law Process
4. Compounding Human Error Versus the Verified Path
5. The Coalition Map
6. Evidence-to-Law Lineage
7. The Ten VVUQ Gates
8. The Annual Reporting Sequence
9. The Verification Decision State Machine
10. Trust Scaffolding
11. The Patient Journey Through a Regulated Trial
12. The Evidence-and-Legislation Timeline
13. Legislative Actions by Effort and Impact
14. Reconciliation of Two Chambers
15. Safeguards for Vulnerable Populations
16. The Widening Capability-Regulation Gap
17. System Context
18. Composite Oversight State Machine
19. Markup and Testimony
20. Patient Throughput: Legacy Versus Verified
21. The National Platform Capstone

---

### 01. Verification Before Generation Workflow

The core idea of H. R. 9510 in one figure: human investigators write the
specification, Claude Code generates candidate code, Codex performs independent
peer review, and a ten-gate VVUQ check decides ACCEPT, ESCALATE, or BLOCK before
anything executes on a patient. A flowchart is correct here because the content is
a directed control flow with a decision node. Reproduced in the compiled LaTeX
narrative as a matching colored TikZ figure (palette: black, grayscales, #EBCB8B,
#D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':55,'htmlLabels':true}}}%%
flowchart TB
  SPEC["Clinical specification<br/>human investigators"]:::n1
  GEN["Claude Code<br/>generates candidate code"]:::n2
  REV["Codex<br/>independent peer review"]:::n2
  VVUQ{"VVUQ verification<br/>ten gates"}:::act
  ACC["ACCEPT<br/>execute under audit"]:::hope
  ESC["ESCALATE<br/>return to a qualified human"]:::n3
  BLK["BLOCK<br/>stop before execution"]:::risk
  SPEC --> GEN
  GEN --> REV
  REV --> VVUQ
  VVUQ -->|all gates pass| ACC
  VVUQ -->|uncertain| ESC
  VVUQ -->|catastrophe predicate| BLK
  ESC -.->|human revises| GEN
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
### 02. The Eight Emotional Pillars

The reader's path through the narrative, from the most common appeal (compassion)
to the closing appeal (urgency), each pillar leading to the single action of
enacting H. R. 9510. A left-to-right flowchart is correct because it shows an
ordered argument that accumulates toward one decision. Reproduced in the compiled
LaTeX narrative as a matching colored TikZ figure (palette: black, grayscales,
#EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':26,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart LR
  P1["1 Compassion"]:::n1
  P2["2 Fear of harm"]:::risk
  P3["3 Moral outrage"]:::risk
  P4["4 Hope"]:::hope
  P5["5 Responsibility"]:::n2
  P6["6 Protection"]:::n2
  P7["7 Trust"]:::hope
  P8["8 Urgency"]:::risk
  ACT["Enact<br/>H. R. 9510"]:::act
  P1 --> P2 --> P3 --> P4 --> P5 --> P6 --> P7 --> P8 --> ACT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
```
### 03. The Bill-to-Law Process

How H. R. 9510 becomes law: introduction, committee referral and markup, hearings
with expert and patient testimony, floor passage in each chamber, reconciliation
of any differences, and enactment. A top-down flowchart is correct because the
legislative path is a staged process with a feedback loop at markup. Reproduced in
the compiled LaTeX narrative as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'monotoneY','nodeSpacing':34,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart TB
  INTRO["Introduction<br/>H. R. 9510"]:::n1
  REFER["Committee referral"]:::n2
  HEAR["Hearings<br/>expert and patient testimony"]:::n2
  MARK{"Markup<br/>debate and amend"}:::act
  FLOOR["Floor passage<br/>House and Senate"]:::n3
  RECON["Reconciliation<br/>one final text"]:::n3
  LAW["Enacted Federal law"]:::hope
  INTRO --> REFER --> HEAR --> MARK
  MARK -->|reported| FLOOR --> RECON --> LAW
  MARK -.->|revise| HEAR
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
### 04. Compounding Human Error Versus the Verified Path

The legacy trial and peer-review system passes work through many manual handoffs,
and each handoff is an independent opportunity for error that compounds downstream.
The verified path inserts an automated gate at each step so a defect is caught
where it occurs. Two parallel flows make the contrast legible. Reproduced in the
compiled LaTeX narrative as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  subgraph LEG["Legacy path: error compounds"]
    direction LR
    L1["Manual entry"]:::risk
    L2["Manual review"]:::risk
    L3["Manual handoff"]:::risk
    L4["Outcome at risk"]:::risk
    L1 --> L2 --> L3 --> L4
  end
  subgraph VER["Verified path: error contained"]
    direction LR
    V1["Generate"]:::n2
    G1{"gate"}:::act
    V2["Review"]:::n2
    G2{"gate"}:::act
    V3["Execute under audit"]:::hope
    V1 --> G1 --> V2 --> G2 --> V3
  end
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
```
### 05. The Coalition Map

Coalition building shows lawmakers that the bill has wide-ranging support.
Patient-advocacy groups, hospital networks, technology developers, and medical
boards each bring distinct evidence to the same committee. A clustered flowchart
with one subgraph per constituency is correct because it groups independent actors
that converge on a single legislative target. Reproduced in the compiled LaTeX
narrative as a matching colored TikZ figure (palette: black, grayscales, #EBCB8B,
#D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':50,'htmlLabels':true}}}%%
flowchart TB
  subgraph PAT["Patients and families"]
    A1["Advocacy groups"]:::n1
  end
  subgraph HOSP["Hospital networks"]
    A2["Investigators and sites"]:::n2
  end
  subgraph TECH["Technology developers"]
    A3["Physical AI and assurance"]:::n2
  end
  subgraph BOARD["Medical boards"]
    A4["Standards and ethics"]:::n3
  end
  CONG["Congressional committee"]:::act
  PASS["Enact H. R. 9510"]:::hope
  A1 --> CONG
  A2 --> CONG
  A3 --> CONG
  A4 --> CONG
  CONG --> PASS
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
### 06. Evidence-to-Law Lineage

H. R. 9510 did not arrive from nowhere. It rests on a documented lineage of prior
work, from early conversational-AI cancer studies, through the National Physical
AI Oncology Trial Platform and the verification pipeline, to the five successive
bill versions. A left-to-right flowchart is correct because it traces a single
evidentiary thread over time. Reproduced in the compiled LaTeX narrative as a
matching colored TikZ figure (palette: black, grayscales, #EBCB8B, #D08770,
#8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':28,'rankSpacing':44,'htmlLabels':true}}}%%
flowchart LR
  E1["Conversational AI<br/>cancer studies"]:::n1
  E2["VVUQ pipeline<br/>51-test method"]:::n2
  E3["Surgical humanoid<br/>172 tests, 10 gates"]:::n2
  E4["National platform<br/>and CFR adaptions"]:::n3
  E5["Bill v1.0 to v4.0"]:::n3
  E6["H. R. 9510 v5.0"]:::act
  LAW["Federal AI law"]:::hope
  E1 --> E2 --> E3 --> E4 --> E5 --> E6 --> LAW
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
### 07. The Ten VVUQ Gates

Every candidate robotic action descends through ten verification, validation, and
uncertainty-quantification gates before it may execute, ending with a catastrophe
predicate that can hard-block. A vertical flowchart funnel is correct because the
content is a strict sequence of pass conditions that narrows to a single accept.
Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'monotoneY','nodeSpacing':22,'rankSpacing':24,'htmlLabels':true}}}%%
flowchart TB
  IN["Candidate robotic action"]:::n1
  G1["Gate 1 verification fraction 1.0"]:::n2
  G2["Gate 2 validation agreement"]:::n2
  G3["Gate 3 relative error bound"]:::n2
  G4["Gate 4 coefficient of variation"]:::n2
  G5["Gates 5 to 9 standards binding"]:::n3
  G10["Gate 10 catastrophe predicate"]:::act
  OUT["ACCEPT and execute under audit"]:::hope
  IN --> G1 --> G2 --> G3 --> G4 --> G5 --> G10 --> OUT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
### 08. The Annual Reporting Sequence

Accountability under the Act flows on a fixed schedule: the trial sponsor files a
verified record, the Secretary reviews and certifies it, and a public report
reaches Congress. A sequence diagram is correct because the content is an ordered
exchange of messages between named parties over time, with a review loop.
Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant S as Trial sponsor
  participant H as Secretary (HHS / FDA)
  participant C as Congress and the public
  S->>H: File verified annual record
  activate H
  loop Certification cycle
    H-->>S: Findings and corrections
    S->>H: Revised record
  end
  H->>C: Certified public report
  deactivate H
  Note over C: Transparent record of safety and cost
```
### 09. The Verification Decision State Machine

At runtime the system is always in one of a few states: it detects an event,
verifies against the gates, and resolves to ACCEPT, ESCALATE to a qualified human,
or BLOCK before execution. A state diagram is correct because the content is a set
of discrete states with guarded transitions and a choice. Reproduced in the
compiled LaTeX narrative as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  direction LR
  [*] --> Detect
  Detect --> Verify: event flagged
  Verify --> Decision
  state Decision <<choice>>
  Decision --> Accept: all gates pass
  Decision --> Escalate: uncertain
  Decision --> Block: catastrophe predicate
  Escalate --> Verify: human revises
  Accept --> [*]
  Block --> [*]
  classDef act fill:#8B2E3F,stroke:#000000,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,color:#1A0A04
  class Verify act
  class Accept hope
  class Block risk
```
### 10. Trust Scaffolding

Public trust in medical AI is not asserted; it is built from named supports:
physician endorsement, academic review, safety-testing requirements, transparency
provisions, pilot results, and an immutable audit trail. A mindmap is correct
because the content is one central concept with parallel, non-sequential
supports. Reproduced in the compiled LaTeX narrative as a matching colored TikZ
figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryColor':'#EBCB8B','primaryBorderColor':'#000000','primaryTextColor':'#1A1505','lineColor':'#333333'}}}%%
mindmap
  root(("Trust in<br/>medical AI"))
    Physician endorsement
      Investigators
      Specialty boards
    Academic review
      Independent experts
    Safety testing
      Ten VVUQ gates
      172 of 172 tests
    Transparency
      Public record
      Open standards
    Pilot results
      Site rotation
    Audit trail
      Hash-chained records
```
### 11. The Patient Journey Through a Regulated Trial

A patient's experience scored step by step, from referral and consent through a
verified procedure to follow-up, showing where confidence is highest and where
friction remains. A user journey is correct because the content is an ordered
lived experience with a satisfaction score per step. Reproduced in the compiled
LaTeX narrative as a matching colored TikZ figure (palette: black, grayscales,
#EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryColor':'#EBCB8B','primaryBorderColor':'#000000','primaryTextColor':'#1A1505','lineColor':'#333333'}}}%%
journey
  title A Patient's Journey Through a Verified Physical AI Oncology Trial
  section Enrollment
    Referral and eligibility: 3: Patient, Investigator
    Informed consent: 4: Patient
  section Verified care
    Plan verified by ten gates: 5: Claude Code, Codex
    Procedure under audit: 5: Surgical humanoid
  section Follow-up
    Adverse-event monitoring: 4: Response team
    Transparent outcome record: 5: Patient, Secretary
```
### 12. The Evidence-and-Legislation Timeline

The work that supports H. R. 9510 unfolded over a clear sequence of phases:
foundational AI research, the verification pipeline, the bill versions, and the
present push to enactment. A timeline is correct because the content is ordered by
date and grouped into phases. Reproduced in the compiled LaTeX narrative as a
matching colored TikZ figure (palette: black, grayscales, #EBCB8B, #D08770,
#8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','cScale0':'#8B2E3F','cScale1':'#BFBFBF','cScale2':'#D08770','cScale3':'#EBCB8B','cScaleLabel0':'#ffffff','cScaleLabel1':'#111111','cScaleLabel2':'#1A0A04','cScaleLabel3':'#1A1505'}}}%%
timeline
  title From Research to Enactment
  section Foundations
    2024 to 2025 : Conversational AI for cancer : VVUQ method and pipeline
  section Physical AI
    2025 to 2026 : Surgical humanoid, 172 tests : National platform and CFR adaptions
  section Legislation
    2026 H1 : Bill v1.0 through v4.0 : H. R. 9510 v5.0
  section Enactment
    Present : Hearings and markup : Transition to Federal law
```
### 13. Legislative Actions by Effort and Impact

The MAIN ACTIONS plotted by the effort they require against the impact they have
on passage, so a coalition can decide where to invest. A quadrant chart is correct
because the content is a set of options compared on two continuous axes.
Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','quadrant1Fill':'#EBCB8B','quadrant2Fill':'#F2F2F2','quadrant3Fill':'#E5E5E5','quadrant4Fill':'#D9D9D9','quadrant1TextFill':'#1A1505','quadrant2TextFill':'#111111','quadrant3TextFill':'#111111','quadrant4TextFill':'#111111','quadrantPointFill':'#8B2E3F','quadrantPointTextFill':'#111111','quadrantTitleFill':'#111111','quadrantXAxisTextFill':'#333333','quadrantYAxisTextFill':'#333333','quadrantInternalBorderStrokeFill':'#888888','quadrantExternalBorderStrokeFill':'#333333'}}}%%
quadrantChart
  title Legislative Actions by Effort and Impact
  x-axis Low Effort --> High Effort
  y-axis Low Impact --> High Impact
  quadrant-1 Invest
  quadrant-2 Protect
  quadrant-3 Delegate
  quadrant-4 Maintain
  Patient testimony: [0.30, 0.88]
  Coalition building: [0.70, 0.85]
  Policy entrepreneurship: [0.55, 0.78]
  Committee markup: [0.65, 0.72]
  Reconciliation: [0.60, 0.62]
  Foundation grants: [0.35, 0.55]
```
### 14. Reconciliation of Two Chambers

When the House and the Senate pass different versions of the bill, a conference
reconciles them into one final text that both chambers vote on. A version-control
graph is the most literal rendering of two branches merging back into a single
line. Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','git0':'#8B2E3F','git1':'#D08770','git2':'#BFBFBF','gitBranchLabel0':'#ffffff','gitBranchLabel1':'#1A0A04','gitBranchLabel2':'#111111','commitLabelColor':'#111111','commitLabelBackground':'#F2F2F2','tagLabelColor':'#1A1505','tagLabelBackground':'#EBCB8B','tagLabelBorder':'#000000'}}}%%
gitGraph
  commit id: "introduced"
  commit id: "committee-markup"
  branch senate
  commit id: "senate-amendments"
  checkout main
  branch house
  commit id: "house-amendments"
  checkout main
  merge house
  merge senate id: "reconciled"
  commit id: "enrolled" tag: "enacted"
```
### 15. Safeguards for Vulnerable Populations

Protection is built in, not bolted on: every enrolled subgroup passes a bias
surveillance check, an informed-consent gate, and a subgroup-outcome audit before
results are accepted. A flowchart with explicit gates is correct because the
content is a set of mandatory checks guarding a single accept. Reproduced in the
compiled LaTeX narrative as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart TB
  SUB["Subgroup data<br/>children, elderly, disabled, veterans, rural"]:::n1
  BIAS{"Bias surveillance<br/>subgroup parity"}:::act
  CONS{"Informed consent<br/>verified and logged"}:::act
  AUD{"Subgroup outcome audit"}:::act
  OK["Accept with subgroup report"]:::hope
  HOLD["Hold and review by humans"]:::risk
  SUB --> BIAS
  BIAS -->|parity met| CONS
  CONS -->|consent valid| AUD
  AUD -->|no disparity| OK
  BIAS -.->|disparity| HOLD
  CONS -.->|gap| HOLD
  AUD -.->|disparity| HOLD
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
```
### 16. The Widening Capability-Regulation Gap

Technology capability is advancing faster than the rules that govern it, and the
distance between the two is where preventable harm accumulates. The Act is the
bridge that closes the gap. A two-track flowchart is correct because it contrasts
two trajectories over time and the single instrument that joins them. Reproduced
in the compiled LaTeX narrative as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':28,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  subgraph CAP["Capability (rising fast)"]
    direction LR
    C1["Physical AI"]:::n2 --> C2["Surgical humanoids"]:::n2 --> C3["Autonomous pipelines"]:::n2
  end
  subgraph REG["Regulation (lagging)"]
    direction LR
    R1["Legacy CFR"]:::n1 --> R2["Guidance only"]:::n1 --> R3["Gap"]:::risk
  end
  ACT["H. R. 9510<br/>closes the gap"]:::act
  GOAL["Patients protected now"]:::hope
  C3 --> ACT
  R3 --> ACT
  ACT --> GOAL
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
```
### 17. System Context

The whole arrangement seen from a distance: the people (patient, legislator,
sponsor, independent reviewer) and the systems (the verified platform and the
public registry) and how they relate. Distinct node shapes carry the system
context lens without leaving the strict palette. Reproduced in the compiled LaTeX
narrative as a matching colored TikZ figure (palette: black, grayscales, #EBCB8B,
#D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'cardinal','nodeSpacing':34,'rankSpacing':52,'htmlLabels':true}}}%%
flowchart LR
  PAT([Patient]):::n1
  LEG([Legislator]):::n1
  REV([Independent reviewer]):::n2
  subgraph PLAT["Verified Physical AI platform"]
    SPON["Sponsor operations"]:::n2
    GATE{"VVUQ gates"}:::act
    REG[("Public registry")]:::hope
  end
  PAT -->|enrolls, consents| SPON
  SPON -->|submits for checks| GATE
  GATE -->|certified record| REG
  REV -.->|peer review| GATE
  REG -->|transparent report| LEG
  LEG -->|enacts and funds| PLAT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
```
### 18. Composite Oversight State Machine

The same workflow nested into three super-states, Authoring, Verification, and
Oversight, to show that the model scales to institutional complexity without
clutter. A composite state diagram is correct because the content is nested states
with internal transitions and a clean exit. Reproduced in the compiled LaTeX
narrative as a matching colored TikZ figure (palette: black, grayscales, #EBCB8B,
#D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  direction LR
  [*] --> Authoring
  state Authoring {
    [*] --> Specify
    Specify --> Generate
    Generate --> [*]
  }
  Authoring --> Verification
  state Verification {
    direction TB
    [*] --> Gates
    Gates --> Review: pass
    Review --> [*]: peer reviewed
  }
  Verification --> Oversight
  state Oversight {
    [*] --> Report
    Report --> Certify
    Certify --> [*]
  }
  Oversight --> [*]: public record
  classDef act fill:#8B2E3F,stroke:#000000,color:#ffffff
  class Verification act
```
### 19. Markup and Testimony

The committee markup is where the bill is debated, amended, and rewritten on the
strength of testimony from AI experts, physicians, and patients, building the
official public record. A sequence diagram is correct because the content is a
structured exchange between the committee and its witnesses with an amendment
loop. Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant W as Witnesses (experts, doctors, patients)
  participant K as Committee
  participant B as Bill text
  W->>K: Testimony and evidence on record
  loop Markup
    K->>B: Propose amendment
    B-->>K: Revised clause
    W-->>K: Clarifying testimony
  end
  K->>B: Order reported
  Note over B: Strengthened, on the public record
```
### 20. Patient Throughput: Legacy Versus Verified

How a cohort of patients flows to outcomes under the legacy path and under the
verified path, with the edge labels carrying the volume at each split. A weighted
flowchart is correct because it shows how work divides and converges while keeping
every color under the strict palette. Reproduced in the compiled LaTeX narrative
as a matching colored TikZ figure (palette: black, grayscales, #EBCB8B, #D08770,
#8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':30,'rankSpacing':52,'htmlLabels':true}}}%%
flowchart LR
  COH["Patient cohort"]:::n1
  LEG["Legacy path"]:::risk
  VER["Verified path"]:::act
  HARM["Preventable harm"]:::risk
  GOOD["Protected outcome"]:::hope
  COH -->|"share A"| LEG
  COH -->|"share B"| VER
  LEG -->|"higher error"| HARM
  LEG -->|"residual"| GOOD
  VER -->|"contained at gates"| GOOD
  VER -->|"rare, escalated"| HARM
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
```
### 21. The National Platform Capstone

The capstone shows how the six-step verification baseline extends to a national
Physical AI oncology trial platform, grouped into four phases, define, build,
verify, and govern, with the Act binding the whole. A phase-grouped flowchart is
correct because it scales the model to many connected components while keeping the
flow fluent. Reproduced in the compiled LaTeX narrative as a matching colored TikZ
figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'basis','nodeSpacing':28,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  subgraph PH1["Define"]
    direction TB
    REQ["Clinical specification"]:::n1
  end
  subgraph PH2["Build"]
    direction TB
    GEN["Claude Code generation"]:::n2
    REV["Codex peer review"]:::n2
  end
  subgraph PH3["Verify"]
    direction TB
    GATE{"Ten VVUQ gates"}:::act
    SAFE{"Subgroup safeguards"}:::act
  end
  subgraph PH4["Govern"]
    direction TB
    AUD[("Audit trail")]:::n3
    REP["Public report"]:::hope
    FUND["Authorized funding"]:::hope
  end
  ACT["H. R. 9510"]:::act
  REQ --> GEN --> REV --> GATE
  GATE --> SAFE --> AUD --> REP
  REP --> FUND
  ACT -.->|binds| GATE
  ACT -.->|binds| SAFE
  ACT -.->|requires| REP
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```

---

## Notes

- All 21 figures keep the same strict palette so the set reads as one coherent,
  professional family: black, grayscales, and `#EBCB8B`, `#D08770`, `#8B2E3F`.
- Diagram types are varied so no two figures repeat the same pattern
  unnecessarily: flowchart, sequence, state, composite state, mindmap, journey,
  timeline, quadrant, and gitGraph.
- Boxes use a small 2 to 4 pixel corner radius and connectors use smooth splines
  (`basis`, `natural`, `cardinal`, `monotoneY`) so the figures read as formal
  exhibits for a legislative briefing, not cartoon cards.
- No raster image is used anywhere; each Markdown figure renders natively on
  GitHub and is reproduced as a colored TikZ figure in the compiled LaTeX.
- Single dashes only; black text on white backgrounds; no dark mode.
