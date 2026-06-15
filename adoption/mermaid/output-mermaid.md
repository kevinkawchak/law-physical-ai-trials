## output-mermaid

# Colored Mermaid Catalog for the Clinician Confidence Framework

Twenty professional, colored Mermaid figures that illustrate the eight
confidence-question sections and the bedside adoption argument of the framework.
They are produced by sub-prompt 1 (`../sub-prompts/prompt-1-mermaid.md`) and are
adapted from the curated Mermaid families in the prior build (`../../review/mermaid/`),
re-themed to this clinician-facing project. This is a new paper topic and does not
rewrite the prior review.

Every figure uses the strict palette only: black, grayscales, and the three theme
colors `#EBCB8B` (gold, confidence and benefit), `#D08770` (clay, harm and risk),
and `#8B2E3F` (burgundy, verification, the gate, and clinician authority). The
`#8B2E3F` paper template theme is preserved. Each figure is reproduced in the
compiled LaTeX framework as a matching colored TikZ figure in the same palette, and
the figures are refined across the draft, full, and final stages.

### Palette

| Role | Fill | Text | Meaning |
|:--|:--|:--|:--|
| `act` | `#8B2E3F` | white | verification, the gate, clinician authority |
| `hope` | `#EBCB8B` | black | confidence, benefit, accepted outcome |
| `risk` | `#D08770` | black | harm, risk, the withheld or blocked action |
| `n1` | `#F2F2F2` | black | inputs, light structure |
| `n2` | `#D9D9D9` | black | process steps |
| `n3` | `#BFBFBF` | black | gates, emphasis structure |

### Index

| # | Title | Type | Confidence slot |
|:--|:--|:--|:--|
| 01 | The Bedside Trust Decision | flowchart | Framework |
| 02 | The Eight Confidence Questions | flowchart | Introduction |
| 03 | Verification Before Generation, the Clinician's View | flowchart | Framework |
| 04 | The Ten VVUQ Gates from the Clinician's Seat | flowchart | 2 Safety |
| 05 | The Calibrated-Trust Band | quadrant | Introduction |
| 06 | The Competence Evidence Stack | flowchart | 1 Competence |
| 07 | Safety Containment | flowchart | 2 Safety |
| 08 | The Audit Trail a Clinician Can Show | sequence | 3 Transparency |
| 09 | The Human-in-the-Loop Oversight Loop | state | 4 Oversight |
| 10 | The Subgroup Equity Map | quadrant | 5 Equity |
| 11 | A Clinician's Day with the System | journey | 8 Workflow |
| 12 | The Adoption Maturity Ladder | timeline | Framework |
| 13 | Where Accountability Sits | flowchart | 7 Accountability |
| 14 | The Escalation Pathway | sequence | 4 Oversight |
| 15 | The Uncertainty Gate | flowchart | 6 Reliability |
| 16 | Model Revalidation Under Version Control | gitGraph | 6 Reliability |
| 17 | The Night-Shift Scenario | sequence | 6 Reliability |
| 18 | Defensible at Tumor Board | mindmap | 3 Transparency |
| 19 | Override and the Stop Authority | state | 4 Oversight |
| 20 | From Bedside Confidence to Trial-Wide Trust | flowchart | Appendix capstone |

---

### 01. The Bedside Trust Decision

The core idea of the framework in one figure: when an autonomous system proposes
an action at the bedside, the clinician runs the eight confidence questions and
then relies on it under audit, escalates it to a qualified human, or withholds it
and documents why. A flowchart is correct because the content is a directed
control flow that ends in a single decision with three guarded outcomes.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':52,'htmlLabels':true}}}%%
flowchart TB
  REC["Autonomous recommendation<br/>at the bedside"]:::n1
  Q{"Eight confidence<br/>questions satisfied?"}:::act
  RELY["Rely and act<br/>under audit"]:::hope
  ESC["Escalate to a<br/>qualified human"]:::n3
  WITH["Withhold and<br/>document the reason"]:::risk
  REC --> Q
  Q -->|all satisfied| RELY
  Q -->|some unmet| ESC
  Q -->|safety in doubt| WITH
  ESC -.->|resolved by review| Q
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 02. The Eight Confidence Questions

The framework's reading path: a clinician moves from the first question any tool
must answer, competence, through safety, transparency, oversight, equity,
reliability, and accountability, to the question that decides daily use, workflow,
and the answers together yield calibrated trust. A left-to-right flowchart is
correct because the content is an ordered reasoning path that converges on one
outcome. Reproduced in the compiled LaTeX framework as a matching colored TikZ
figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':24,'rankSpacing':38,'htmlLabels':true}}}%%
flowchart LR
  Q1["1 Competence"]:::n1
  Q2["2 Safety"]:::risk
  Q3["3 Transparency"]:::n2
  Q4["4 Oversight"]:::n2
  Q5["5 Equity"]:::risk
  Q6["6 Reliability"]:::n3
  Q7["7 Accountability"]:::n2
  Q8["8 Workflow"]:::hope
  CT["Calibrated<br/>trust"]:::act
  Q1 --> Q2 --> Q3 --> Q4 --> Q5 --> Q6 --> Q7 --> Q8 --> CT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 03. Verification Before Generation, the Clinician's View

The mechanism the framework rests on, seen from the clinician's seat: a clinical
question is posed, Claude Code proposes a candidate action, Codex reviews it
independently, and a ten-gate VVUQ check resolves to ACCEPT, ESCALATE to the
clinician, or BLOCK before anything reaches the patient. A flowchart is correct
because the content is a directed control flow with a decision node. Reproduced in
the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':55,'htmlLabels':true}}}%%
flowchart TB
  SPEC["Clinical question<br/>investigator and clinician"]:::n1
  GEN["Claude Code<br/>proposes an action"]:::n2
  REV["Codex<br/>independent review"]:::n2
  VVUQ{"Ten VVUQ gates"}:::act
  ACC["ACCEPT<br/>act under audit"]:::hope
  ESC["ESCALATE<br/>to the clinician"]:::n3
  BLK["BLOCK<br/>before the patient"]:::risk
  SPEC --> GEN
  GEN --> REV
  REV --> VVUQ
  VVUQ -->|all gates pass| ACC
  VVUQ -->|uncertain| ESC
  VVUQ -->|catastrophe predicate| BLK
  ESC -.->|clinician revises| GEN
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 04. The Ten VVUQ Gates from the Clinician's Seat

Before any candidate action executes it descends through ten verification,
validation, and uncertainty-quantification gates, ending with a catastrophe
predicate that can hard-block. The clinician does not run the gates by hand, but
relies on the fact that all ten must pass. A vertical flowchart funnel is correct
because the content is a strict sequence of pass conditions that narrows to a
single accept. Reproduced in the compiled LaTeX framework as a matching colored
TikZ figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'monotoneY','nodeSpacing':22,'rankSpacing':24,'htmlLabels':true}}}%%
flowchart TB
  IN["Candidate action"]:::n1
  G1["Gate 1 verification fraction 1.0"]:::n2
  G2["Gate 2 validation agreement"]:::n2
  G3["Gate 3 relative error bound"]:::n2
  G4["Gate 4 coefficient of variation"]:::n2
  G5["Gates 5 to 9 standards binding"]:::n3
  G10["Gate 10 catastrophe predicate"]:::act
  OUT["ACCEPT and act under audit"]:::hope
  IN --> G1 --> G2 --> G3 --> G4 --> G5 --> G10 --> OUT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 05. The Calibrated-Trust Band

The framework's organizing concept: a clinician should rely on a system exactly as
much as its demonstrated capability warrants. Plotting demonstrated capability
against clinician reliance separates calibrated trust from its two failure modes,
automation bias (over-trust) and algorithm aversion (under-trust). A quadrant chart
is correct because the content compares states on two continuous axes. Reproduced
in the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','quadrant1Fill':'#EBCB8B','quadrant2Fill':'#D08770','quadrant3Fill':'#F2F2F2','quadrant4Fill':'#D9D9D9','quadrant1TextFill':'#1A1505','quadrant2TextFill':'#1A0A04','quadrant3TextFill':'#111111','quadrant4TextFill':'#111111','quadrantPointFill':'#8B2E3F','quadrantPointTextFill':'#111111','quadrantTitleFill':'#111111','quadrantXAxisTextFill':'#333333','quadrantYAxisTextFill':'#333333','quadrantInternalBorderStrokeFill':'#888888','quadrantExternalBorderStrokeFill':'#333333'}}}%%
quadrantChart
  title Calibrated Trust and Its Failure Modes
  x-axis Low Capability --> High Capability
  y-axis Low Reliance --> High Reliance
  quadrant-1 Calibrated trust
  quadrant-2 Automation bias
  quadrant-3 Appropriate caution
  quadrant-4 Algorithm aversion
  Verified action under audit: [0.85, 0.83]
  Unvalidated tool over-used: [0.22, 0.74]
  Proven tool ignored: [0.82, 0.24]
  Experimental and watched: [0.27, 0.27]
```


### 06. The Competence Evidence Stack

Competence is not one number but a stack of evidence built in order: bench
accuracy, a retrospective cohort, prospective validation on the site's own
patients, and the assurance run that passed every automated gate test. A
phase-grouped flowchart is correct because it shows independent evidence stages
that build to a single conclusion. Reproduced in the compiled LaTeX framework as a
matching colored TikZ figure (palette: black, grayscales, #EBCB8B, #D08770,
#8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'basis','nodeSpacing':28,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  subgraph BENCH["Bench"]
    B1["Benchmark accuracy"]:::n1
  end
  subgraph RETRO["Retrospective"]
    R1["Historical cohort agreement"]:::n2
  end
  subgraph PROSP["Prospective"]
    P1["Validation on site population"]:::n2
  end
  subgraph ASSURE["Assurance"]
    A1["172 of 172 gate tests"]:::act
  end
  CONF["Competence established"]:::hope
  B1 --> R1 --> P1 --> A1 --> CONF
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 07. Safety Containment

The safety case in motion: a candidate action or a detected adverse event is
classified, checked against the catastrophe-predicate gate, and then either
contained under audit, blocked before harm, or escalated to the response team. A
flowchart is correct because the content is a directed control flow with a guarded
decision. Reproduced in the compiled LaTeX framework as a matching colored TikZ
figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':34,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart TB
  EV["Candidate action or<br/>adverse event"]:::n1
  DET["Detect and classify"]:::n2
  GATE{"Catastrophe<br/>predicate gate"}:::act
  CONT["Contain under audit"]:::hope
  BLK["BLOCK before harm"]:::risk
  ESC["Escalate to<br/>response team"]:::n3
  EV --> DET --> GATE
  GATE -->|safe| CONT
  GATE -->|predicate true| BLK
  GATE -->|uncertain| ESC
  ESC -.->|reassess| DET
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 08. The Audit Trail a Clinician Can Show

Transparency is operational, not rhetorical: every action appends a hash-chained
record, the clinician countersigns the decision, and an auditor can later
reconstruct exactly what happened and why. A sequence diagram is correct because
the content is an ordered exchange of messages between named parties over time.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant Y as System
  participant D as Clinician
  participant L as Audit log
  participant U as Auditor
  loop Every action
    Y->>L: Append record (previous hash + action)
    D->>L: Countersign the decision
  end
  U->>L: Request reconstruction
  L-->>U: Tamper-evident timeline
  Note over U: Exactly what happened, and why
```


### 09. The Human-in-the-Loop Oversight Loop

Oversight is a loop the clinician never leaves: the system monitors, recommends,
and presents a decision the clinician accepts, escalates, or overrides, after
which control returns to monitoring. A state diagram is correct because the content
is a set of discrete states with guarded transitions and a choice. Reproduced in
the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  direction LR
  [*] --> Monitor
  Monitor --> Recommend: action proposed
  Recommend --> Decision
  state Decision <<choice>>
  Decision --> Execute: clinician accepts
  Decision --> Escalate: clinician unsure
  Decision --> Override: clinician rejects
  Execute --> Monitor
  Escalate --> Recommend: senior review
  Override --> Monitor: action withheld
  classDef act fill:#8B2E3F,stroke:#000000,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,color:#1A0A04
  class Recommend act
  class Execute hope
  class Override risk
```


### 10. The Subgroup Equity Map

Equity is measured, not assumed: each clinically relevant subgroup is plotted by
its representation in validation against its performance relative to the overall
model, so disparities and under-sampled groups become surveillance priorities. A
quadrant chart is correct because the content compares subgroups on two continuous
axes. Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','quadrant1Fill':'#EBCB8B','quadrant2Fill':'#F2F2F2','quadrant3Fill':'#D08770','quadrant4Fill':'#D9D9D9','quadrant1TextFill':'#1A1505','quadrant2TextFill':'#111111','quadrant3TextFill':'#1A0A04','quadrant4TextFill':'#111111','quadrantPointFill':'#8B2E3F','quadrantPointTextFill':'#111111','quadrantTitleFill':'#111111','quadrantXAxisTextFill':'#333333','quadrantYAxisTextFill':'#333333','quadrantInternalBorderStrokeFill':'#888888','quadrantExternalBorderStrokeFill':'#333333'}}}%%
quadrantChart
  title Subgroup Representation and Performance
  x-axis Under-represented --> Well-represented
  y-axis Below overall --> At or above overall
  quadrant-1 Equitable and evidenced
  quadrant-2 Good but under-sampled
  quadrant-3 Surveillance priority
  quadrant-4 Disparity flagged
  Older adults: [0.78, 0.80]
  Pediatric rare cancer: [0.24, 0.72]
  Underserved ancestry: [0.30, 0.34]
  Rural access cohort: [0.66, 0.40]
```


### 11. A Clinician's Day with the System

Workflow decides whether a safe tool is actually used: a clinician's day is scored
step by step, from reviewing overnight monitoring through accepting recommendations
under audit to countersigning records and flagging drift. A user journey is correct
because the content is an ordered lived experience with a satisfaction score per
step. Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryColor':'#EBCB8B','primaryBorderColor':'#000000','primaryTextColor':'#1A1505','lineColor':'#333333'}}}%%
journey
  title A Clinician's Day with a Verified Physical AI System
  section Before clinic
    Review overnight monitoring: 4: Clinician
    Confirm system validated on site: 5: Clinician
  section In clinic
    Receive recommendation with reasons: 5: System, Clinician
    Confirm consent and subgroup fit: 4: Clinician, Patient
    Accept under audit or escalate: 5: Clinician
  section After clinic
    Countersign audit records: 4: Clinician
    Flag drift or adverse event: 3: Clinician, Response team
```


### 12. The Adoption Maturity Ladder

Adoption is a sequence of phases, not a switch: a site evaluates the system with
local validation and training, integrates it under supervision, operates it with
continuous monitoring, and sustains it with periodic revalidation. A timeline is
correct because the content is ordered into phases that advance over time.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','cScale0':'#8B2E3F','cScale1':'#BFBFBF','cScale2':'#D08770','cScale3':'#EBCB8B','cScaleLabel0':'#ffffff','cScaleLabel1':'#111111','cScaleLabel2':'#1A0A04','cScaleLabel3':'#1A1505'}}}%%
timeline
  title Adoption Maturity, from Pilot to Standard Work
  section Evaluate
    Pilot : Local validation on site data : Credentialing and training
  section Integrate
    Supervised use : Human in the loop : Every action audited
  section Operate
    Routine use : Continuous monitoring : Drift surveillance
  section Sustain
    Standard work : Periodic revalidation : Subgroup audit
```


### 13. Where Accountability Sits

Accountability is unambiguous only when it is drawn: the clinician is accountable
for the patient, the sponsor for operation, the developer for the model, and the
IRB is consulted on consent, all converging on a signed standard operating
procedure that the auditor can read. A clustered flowchart is correct because it
groups distinct responsible parties that converge on one record. Reproduced in the
compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':50,'htmlLabels':true}}}%%
flowchart TB
  subgraph CARE["At the bedside"]
    CLIN["Clinician<br/>accountable for the patient"]:::act
  end
  subgraph PLAT["Platform"]
    SPON["Sponsor<br/>accountable for operation"]:::n2
    VEND["Developer<br/>responsible for the model"]:::n2
  end
  subgraph GOV["Governance"]
    IRB["IRB<br/>consulted on consent"]:::n3
    AUD["Auditor<br/>informed by the record"]:::n1
  end
  SOP["Signed SOP and<br/>documentation chain"]:::hope
  CLIN --> SOP
  SPON --> SOP
  VEND --> SOP
  IRB --> SOP
  SOP --> AUD
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 14. The Escalation Pathway

When a gate is uncertain the system does not guess: it escalates to the on-call
clinician, who resolves it at the bedside or escalates further to the attending,
and every step writes to the record. A sequence diagram with an alternative path is
correct because the content is an ordered exchange with a branch. Reproduced in the
compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant Y as System
  participant O as On-call clinician
  participant A as Attending
  participant R as Record
  Y->>O: ESCALATE (uncertain gate)
  O->>O: Review reasons and audit trail
  alt Resolved at the bedside
    O->>R: Document decision and act under audit
  else Needs senior judgment
    O->>A: Escalate with full context
    A->>R: Decide, document, and act
  end
  Note over R: Escalation never bypasses the record
```


### 15. The Uncertainty Gate

Reliability includes honesty about doubt: every estimate carries a quantified
confidence interval, and an action proceeds only when that interval falls within
clinical tolerance, otherwise it is escalated or flagged. A flowchart is correct
because the content is a directed control flow with a guarded decision. Reproduced
in the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':34,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart TB
  EST["Model estimate<br/>with uncertainty"]:::n1
  UQ["Quantify confidence interval"]:::n2
  CHK{"Within clinical<br/>tolerance?"}:::act
  ACC["Report with confidence band"]:::hope
  ESC["Escalate for human judgment"]:::n3
  WIDE["Flag wide uncertainty"]:::risk
  EST --> UQ --> CHK
  CHK -->|narrow band| ACC
  CHK -->|borderline| ESC
  CHK -->|wide band| WIDE
  WIDE -.->|return for review| ESC
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


### 16. Model Revalidation Under Version Control

Reliability over time is managed like code: a validated model is deployed, drift is
detected, a branch retrains and revalidates against the gates, and only a passing
revalidation merges back and is redeployed in service. A version-control graph is
the most literal rendering of a branch that retrains and merges back into a single
line. Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','git0':'#8B2E3F','git1':'#D08770','git2':'#BFBFBF','gitBranchLabel0':'#ffffff','gitBranchLabel1':'#1A0A04','gitBranchLabel2':'#111111','commitLabelColor':'#111111','commitLabelBackground':'#F2F2F2','tagLabelColor':'#1A1505','tagLabelBackground':'#EBCB8B','tagLabelBorder':'#000000'}}}%%
gitGraph
  commit id: "validated"
  commit id: "deployed"
  commit id: "drift-detected"
  branch retrain
  commit id: "retrain-on-new-data"
  commit id: "revalidate-gates"
  checkout main
  merge retrain id: "revalidated"
  commit id: "redeployed" tag: "in-service"
```


### 17. The Night-Shift Scenario

The hardest test of reliability is the one no one is watching: an event at 03:00 is
submitted to the same ten gates with the same thresholds as at noon, and the night
clinician receives the same reasoned recommendation. A sequence diagram is correct
because the content is an ordered, time-stamped exchange between parties.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant P as Patient at 03:00
  participant Y as System
  participant G as VVUQ gates
  participant N as Night clinician
  P->>Y: Event detected
  Y->>G: Submit candidate action
  G-->>Y: Same ten gates, same thresholds
  Y->>N: Recommendation with reasons
  N->>P: Act under audit or escalate
  Note over G,N: 03:00 is treated exactly like noon
```


### 18. Defensible at Tumor Board

The framework's practical test is whether a clinician can defend a decision to
peers: the figure gathers what the clinician brings, validation, the safety block,
the reasons and record, subgroup performance, and the signed roles. A mindmap is
correct because the content is one central claim with parallel, non-sequential
supports. Reproduced in the compiled LaTeX framework as a matching colored TikZ
figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryColor':'#EBCB8B','primaryBorderColor':'#000000','primaryTextColor':'#1A1505','lineColor':'#333333'}}}%%
mindmap
  root(("Defensible at<br/>tumor board"))
    Competence
      Validation on site data
      172 of 172 gate tests
    Safety
      Catastrophe-predicate block
    Transparency
      Reasons for the action
      Hash-chained record
    Equity
      Subgroup performance
    Accountability
      Signed SOP
      Named roles
```


### 19. Override and the Stop Authority

Control means the clinician can always intervene: a running action can be paused
for review and resumed, or overridden to a full stop, and the catastrophe predicate
can stop it without any human in the path. A state diagram is correct because the
content is a small set of states with guarded transitions, including an
unconditional stop. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  direction LR
  [*] --> Running
  Running --> Hold: clinician pause
  Hold --> Running: resume after review
  Hold --> Stopped: clinician override
  Running --> Stopped: catastrophe predicate
  Stopped --> [*]
  classDef act fill:#8B2E3F,stroke:#000000,color:#ffffff
  classDef risk fill:#D08770,stroke:#000000,color:#1A0A04
  class Hold act
  class Stopped risk
```


### 20. From Bedside Confidence to Trial-Wide Trust

The capstone shows how one verified decision at the bedside scales: local
validation and a credentialed team make a site trustworthy, continuous monitoring
and subgroup audit make a trial trustworthy, and shared standards and a public
registry make the national platform trustworthy. A phase-grouped flowchart is
correct because it scales the model across connected levels while keeping the flow
fluent. Reproduced in the compiled LaTeX framework as a matching colored TikZ
figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'basis','nodeSpacing':26,'rankSpacing':44,'htmlLabels':true}}}%%
flowchart LR
  subgraph BED["Bedside"]
    direction TB
    D1["One verified decision"]:::n1
  end
  subgraph SITE["Site"]
    direction TB
    S1["Local validation"]:::n2
    S2["Credentialed team"]:::n2
  end
  subgraph TRIAL["Trial"]
    direction TB
    T1["Continuous monitoring"]:::act
    T2["Subgroup audit"]:::act
  end
  subgraph PLAT["National platform"]
    direction TB
    N1["Shared standards"]:::n3
    N2["Public registry"]:::hope
  end
  CT["Trial-wide<br/>calibrated trust"]:::act
  D1 --> S1 --> S2 --> T1 --> T2 --> N1 --> N2 --> CT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```

