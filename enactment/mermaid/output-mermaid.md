## output-mermaid

The curated colored Mermaid set for the H. R. 9510 passage framework: 20
professional figures in the strict palette black, grayscales, #4B0082 (indigo,
authority and the bill), #000080 (navy, evidence and support), and #C0C0C0 (silver,
cost and caution). Each figure below renders natively on GitHub and is reproduced in
the compiled LaTeX manuscript as a matching colored TikZ figure across the draft,
full, verify, and final stages. No raster image is used.

### Catalog

| # | Title | Type | Framework slot |
|:--|:--|:--|:--|
| 01 | The Passage Decision | flowchart | Introduction / framework |
| 02 | The Eight Passage Questions | flowchart | Framework spine |
| 03 | Verification Before Generation | flowchart | Q3 Safety |
| 04 | The Ten Gates Congress Is Enacting | flowchart | Q3 Safety |
| 05 | The Amendment Map | flowchart | Q2 Authority |
| 06 | The Legislative Journey | journey | Q8 Passage path |
| 07 | The Fiscal Picture | timeline | Q4 Fiscal |
| 08 | The Cost Asymmetry | quadrant | Q4 Fiscal |
| 09 | Authority and the State Savings Clause | flowchart | Q2 Authority |
| 10 | The Recognized Standards Basis | sankey | Q3 Safety / Q2 Authority |
| 11 | Constituent Reach | block | Q5 Constituents |
| 12 | Where the Two Caucuses Converge | flowchart | Q6 Bipartisanship |
| 13 | The Supporting Coalition | mindmap | Q7 Coalition |
| 14 | The Platform as Proof of Implementability | flowchart | Q1 Mandate / Q5 |
| 15 | The Two-Chamber Strategy | sequence | Q8 Passage path |
| 16 | The Markup Lifecycle | gitGraph | Q8 Passage path |
| 17 | The Vote Thresholds | requirement | Q8 Passage path |
| 18 | Handling the Standard Objections | flowchart | Q6 / Q7 |
| 19 | The Scoring Path | state | Q4 Fiscal |
| 20 | From One Yes to Enactment | flowchart | Capstone |

---

### 01. The Passage Decision

The core idea of the framework in one figure: when H. R. 9510 reaches a member's
desk, the member runs the eight passage questions and then cosponsors and votes
yes, offers an amendment first, or declines and states the reason. A flowchart is
correct because the content is a directed decision flow that ends in one choice
with three guarded outcomes. Reproduced in the compiled LaTeX framework as a
matching colored TikZ figure (palette: black, grayscales, #4B0082, #000080,
#C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':52,'htmlLabels':true}}}%%
flowchart TB
  BILL["H. R. 9510<br/>reaches the desk"]:::n1
  Q{"Eight passage<br/>questions answered?"}:::act
  YES["Cosponsor and<br/>vote yes"]:::evid
  AMEND["Offer an amendment,<br/>then support"]:::n3
  NO["Decline and<br/>state the reason"]:::caut
  BILL --> Q
  Q -->|all answered| YES
  Q -->|one open| AMEND
  Q -->|unconvinced| NO
  AMEND -.->|adopted at markup| Q
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 02. The Eight Passage Questions

The framework's spine: a legislator's reasoning path runs from the mandate for a
statute through authority, safety, fiscal score, constituents, bipartisanship, and
coalition to the passage path itself. A left-to-right flowchart is correct because
the eight questions are an ordered argument, each building on the answer before it.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'natural','nodeSpacing':26,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart LR
  Q1["1 Mandate"]:::n1 --> Q2["2 Authority"]:::n2
  Q2 --> Q3["3 Safety"]:::act
  Q3 --> Q4["4 Fiscal"]:::n3
  Q4 --> Q5["5 Constituents"]:::n2
  Q5 --> Q6["6 Bipartisanship"]:::evid
  Q6 --> Q7["7 Coalition"]:::n3
  Q7 --> Q8["8 Passage path"]:::act
  Q8 --> OUT["A yes vote in<br/>both chambers"]:::evid
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 03. Verification Before Generation, the Legislator's View

The mechanism the bill actually codifies: before any robot-patient interaction code
is generated or executed, a system proposes the action, an independent reviewer
checks it, and a ten-gate examination resolves it to ACCEPT under audit, ESCALATE to
a qualified human, or BLOCK before the patient. A left-to-right flowchart is correct
because this is a pipeline with one gated branch. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':34,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  PROP["System proposes<br/>an action"]:::n1
  REV["Independent<br/>review"]:::n2
  GATE{"Ten VVUQ<br/>gates"}:::act
  ACC["ACCEPT<br/>and act under audit"]:::evid
  ESC["ESCALATE<br/>to a qualified human"]:::n3
  BLK["BLOCK<br/>before the patient"]:::caut
  PROP --> REV --> GATE
  GATE -->|fraction 1.0| ACC
  GATE -->|ambiguity| ESC
  GATE -->|any gate fails| BLK
  ESC -.->|resolved| GATE
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 04. The Ten Gates Congress Is Enacting

The regulatory content of section 515D: ten verification gates, each bound to a
published external standard, with three hard catastrophe predicates (vascular
no-fly, shared-room collision, and fault or emergency stop) that must hold without
exception. A top-down flowchart is correct because it shows a fixed schedule
converging on the predicates that can stop everything. Reproduced in the compiled
LaTeX framework as a matching colored TikZ figure (palette: black, grayscales,
#4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':26,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart TB
  subgraph SUITE["Ten-gate VVUQ suite (section 515D(c))"]
    direction LR
    G1["1 Hand-eye"]:::n1
    G2["2 Finger force"]:::n1
    G3["3 Balance"]:::n1
    G4["4 Plan"]:::n1
    G5["5 Grasp"]:::n1
    G7["7 Suturing"]:::n2
    G8["8 Perception"]:::n2
  end
  subgraph HARD["Hard catastrophe predicates (agreement 1.00)"]
    direction LR
    G6["6 Vascular<br/>no-fly"]:::act
    G9["9 Shared-room<br/>collision"]:::act
    G10["10 Fault and<br/>emergency stop"]:::act
  end
  SUITE --> DEC{"Verification<br/>fraction = 1.0?"}:::evid
  HARD --> DEC
  DEC -->|yes, all hold| PASS["Cleared to generate<br/>and execute"]:::evid
  DEC -->|no| STOP["BLOCK"]:::caut
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 05. The Amendment Map

What the bill changes in the United States Code: a single new section 515D
(21 U.S.C. 360e-5) carries ten conforming amendments across Title 21, from the
device definition to State preemption, plus a clerical update to the table of
contents. A clustered flowchart is correct because one new section radiates targeted
edits into existing law. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'cardinal','nodeSpacing':22,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart TB
  CORE["New section 515D<br/>21 U.S.C. 360e-5"]:::act
  subgraph DEF["Scope and prohibition"]
    A1["321(h) device"]:::n1
    A2["331 prohibited act (jjj)"]:::n1
    A3["351 adulteration (k)"]:::n1
  end
  subgraph PATH["Premarket pathways"]
    A4["355g real-world evidence"]:::n2
    A5["360(k) 510(k)"]:::n2
    A6["360c classification (l)"]:::n2
    A7["360e PMA"]:::n2
    A8["360e-4 change control (d)"]:::n2
  end
  subgraph BOUND["Boundaries"]
    A9["360j(o) CDS exclusion"]:::n3
    A10["360k State savings (c)"]:::n3
  end
  CORE --> DEF
  CORE --> PATH
  CORE --> BOUND
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 06. The Legislative Journey

The path the bill must travel: introduction and referral, subcommittee and full
committee markup, House floor passage, the same sequence in the Senate, conference
or amendment exchange, and finally enrollment and signature. A journey diagram is
correct because it scores each stage as a sentiment the sponsor must manage, not
just a box to clear. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
journey
  title H. R. 9510 from introduction to enactment
  section House
    Introduction and referral: 4: Sponsor
    Subcommittee markup: 3: Sponsor, Committee
    Full committee reported: 4: Committee
    House floor passage: 5: House
  section Senate
    Companion referred: 3: Senate sponsor
    Committee reported: 4: Committee
    Senate floor passage: 5: Senate
  section To law
    Amendments reconciled: 4: Both chambers
    Enrolled and signed: 5: President
```


---

### 07. The Fiscal Picture

What the bill authorizes and when: a declining authorization from 18 million dollars
in FY 2027 to 9 million dollars in FY 2031, 58 million dollars in all, with outlays
of 53.5 million dollars inside the window and no new mandatory spending. A timeline
is correct because the fiscal story is a dated, multi-year schedule a scorekeeper
reads year by year. Reproduced in the compiled LaTeX framework as a matching colored
TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111','cScale0':'#4B0082','cScale1':'#000080','cScale2':'#BFBFBF'}}}%%
timeline
  title Authorization of appropriations, FY 2027 to FY 2031 (58 million dollars total)
  FY 2027 : 18 million : Rulemaking heavy
  FY 2028 : 12 million : Records system build peak
  FY 2029 : 10 million : Steady-state operations
  FY 2030 : 9 million : Steady-state operations
  FY 2031 : 9 million : Steady-state, then sunset to user fees
```


---

### 08. The Cost Asymmetry

The argument that disarms the fiscal objection: the verification gate is priced in
compute, storage, and bounded human review (small, fixed, measurable), while the
embodied failure it prevents is priced in lives and litigation (large, unbounded). A
quadrant chart is correct because it places each item on the two axes that matter to
a scorekeeper, cost magnitude and predictability. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111','quadrant1Fill':'#F2F2F2','quadrant2Fill':'#D9D9D9','quadrant3Fill':'#D9D9D9','quadrant4Fill':'#F2F2F2','quadrantPointFill':'#4B0082','quadrantPointTextFill':'#ffffff'}}}%%
quadrantChart
  title Cost magnitude against predictability
  x-axis Low cost --> High cost
  y-axis Unpredictable --> Predictable
  quadrant-1 Affordable and bounded
  quadrant-2 Bounded but heavier
  quadrant-3 Cheap but uncertain
  quadrant-4 The risk being removed
  Verification gate suite: [0.22, 0.86]
  Records and storage: [0.16, 0.80]
  ESCALATE human review: [0.34, 0.70]
  Embodied failure: [0.88, 0.18]
  Litigation exposure: [0.80, 0.12]
```


---

### 09. Authority and the State Savings Clause

Why the bill is within Congress's power and respectful of the States: it acts on
interstate commerce in medical devices through the Federal Food, Drug, and Cosmetic
Act, sets a Federal floor in section 515D, and preserves State laws that require a
licensed human to monitor or override the system through a savings clause in section
360k(c). A top-down flowchart is correct because authority flows from a source to a
floor and then carves out what it does not displace. Reproduced in the compiled
LaTeX framework as a matching colored TikZ figure (palette: black, grayscales,
#4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':30,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart TB
  CC["Commerce in<br/>medical devices"]:::n1
  FDC["FD&C Act<br/>21 U.S.C. 301 et seq."]:::evid
  FLOOR["Section 515D<br/>Federal verification floor"]:::act
  SAVE["360k(c) savings clause:<br/>State human-over-AI laws preserved"]:::n3
  ROC["Rule of construction:<br/>parts 50, 312, and 520(g) undisturbed"]:::n2
  CC --> FDC --> FLOOR
  FLOOR --> SAVE
  FLOOR --> ROC
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 10. The Recognized Standards Basis

The bill does not invent its rigor; each gate is bound to a published consensus
standard, so the verification floor rests on work the relevant professions already
trust. A sankey diagram is correct because it shows several recognized standards
flowing into the one ten-gate examination the statute requires. Reproduced in the
compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
sankey-beta

ASME V and V 40,Ten-gate VVUQ examination,3
ISO 14971 risk management,Ten-gate VVUQ examination,2
IEC 80601-2-77 surgical robots,Ten-gate VVUQ examination,3
ISO/TS 15066 collaborative robots,Ten-gate VVUQ examination,2
UL 4600 autonomous products,Ten-gate VVUQ examination,2
IEEE 7009 fail-safe design,Ten-gate VVUQ examination,2
Ten-gate VVUQ examination,ACCEPT under audit,8
Ten-gate VVUQ examination,ESCALATE to a human,3
Ten-gate VVUQ examination,BLOCK before the patient,3
```


---

### 11. Constituent Reach

Why a member in any State has a stake: the platform's rollout grows from a single
site to fifty through one hundred operational sites across all major regions, so the
bill that enables it touches rural and urban districts alike. A block diagram is
correct because the content is a staged grid of capacity that a member reads against
their own district. Reproduced in the compiled LaTeX framework as a matching colored
TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
block-beta
  columns 3
  P1["Phase 1<br/>1 site"] P2["Phase 2<br/>5 to 10 sites"] P3["Phase 3<br/>50 to 100 sites"]
  space:3
  R1["Faster enrollment"] R2["Rural and underserved reach"] R3["New trial-site jobs"]
  style P1 fill:#F2F2F2,stroke:#333333,color:#111111
  style P2 fill:#000080,stroke:#000000,color:#ffffff
  style P3 fill:#4B0082,stroke:#000000,color:#ffffff
  style R1 fill:#D9D9D9,stroke:#222222,color:#111111
  style R2 fill:#D9D9D9,stroke:#222222,color:#111111
  style R3 fill:#D9D9D9,stroke:#222222,color:#111111
```


---

### 12. Where the Two Caucuses Converge

The bipartisan case in one figure: an innovation-and-deregulation appeal and a
patient-safety-and-oversight appeal start from different premises but converge on the
same vote, because verification before generation both speeds credible deployment
and sets a hard safety floor. A converging flowchart is correct because it shows two
distinct motivations meeting at one outcome. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'cardinal','nodeSpacing':32,'rankSpacing':48,'htmlLabels':true}}}%%
flowchart TB
  INNO["Innovation and<br/>deregulation appeal"]:::evid
  SAFE["Patient safety and<br/>oversight appeal"]:::act
  M1["Credible, faster<br/>deployment"]:::n2
  M2["Hard safety floor,<br/>no entitlement"]:::n2
  YES["One yes vote:<br/>verification before generation"]:::act
  INNO --> M1 --> YES
  SAFE --> M2 --> YES
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 13. The Supporting Coalition

Who stands behind the bill and why no organized opponent is evident: medical
societies, patient advocates, industry and standards bodies, and the States each find
something to support, from a clear safety floor to predictable rules of the road. A
mindmap is correct because it radiates one center (support for H. R. 9510) into the
distinct stakeholder groups that compose a coalition. Reproduced in the compiled
LaTeX framework as a matching colored TikZ figure (palette: black, grayscales,
#4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
mindmap
  root((Support for<br/>H. R. 9510))
    Clinicians
      Oncology societies
      Patient-safety groups
    Patients
      Advocacy organizations
      Rural access coalitions
    Industry
      Device and robotics makers
      Standards bodies
    Government
      FDA implementation
      State human-over-AI laws preserved
```


---

### 14. The Platform as Proof of Implementability

The answer to "can this actually be done": the National Platform's validated
simulation treated 168 patients with 29 robots across 15 cancer types at 99.7
percent uptime with zero patient harm events, which turns the bill from an
aspiration into a codification of something already shown to work. A left-to-right
flowchart is correct because it traces evidence into a conclusion a member can cite.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':30,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  SIM["24-hour simulation<br/>168 patients, 29 robots"]:::n1
  UP["99.7 percent uptime<br/>zero patient harm events"]:::evid
  STD["PSL and USL site<br/>and robot readiness"]:::n2
  CONC["The bill codifies a<br/>demonstrated system"]:::act
  SIM --> UP --> CONC
  STD --> CONC
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 15. The Two-Chamber Strategy

How passage in one chamber is converted into law: a Senate companion is introduced
in parallel, each chamber reports and passes its version, and the differences are
reconciled by amendment exchange or conference before enrollment. A sequence diagram
is correct because the content is an ordered exchange of messages between two
chambers over time. Reproduced in the compiled LaTeX framework as a matching colored
TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111','actorBkg':'#4B0082','actorTextColor':'#ffffff','actorBorder':'#000000','signalColor':'#333333','signalTextColor':'#111111'}}}%%
sequenceDiagram
  participant H as House
  participant S as Senate
  participant P as President
  H->>H: Pass H. R. 9510
  H->>S: Message the bill to the Senate
  S->>S: Introduce companion, report, pass
  S-->>H: Return with amendments
  H->>H: Concur or request conference
  H->>P: Enroll the reconciled bill
  P-->>H: Sign into law
```


---

### 16. The Markup Lifecycle

How a bill is improved without being lost: it is introduced, a committee print and a
manager's amendment refine it on a working branch, and the refined text merges back
as the reported bill that goes to the floor. A gitGraph is correct because markup is
literally a branch-and-merge of legislative text. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111','git0':'#4B0082','git1':'#000080','gitBranchLabel0':'#ffffff','gitBranchLabel1':'#ffffff'}}}%%
gitGraph
  commit id: "Introduced"
  branch committee
  commit id: "Committee print"
  commit id: "Manager amendment"
  commit id: "CBO points addressed"
  checkout main
  merge committee id: "Reported"
  commit id: "Floor passage"
  commit id: "Engrossed to Senate"
```


---

### 17. The Vote Thresholds

What "passage" concretely requires: a simple majority in the House, sixty votes to
invoke cloture in the Senate, and a simple majority to pass the Senate, each
satisfied by a recorded action. A requirement diagram is correct because it states
the thresholds as formal requirements and links the action that verifies each.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
requirementDiagram
  requirement HousePassage {
    id: 1
    text: Simple majority of the House, 218 of 435.
    risk: medium
    verifymethod: test
  }
  requirement SenateCloture {
    id: 2
    text: Sixty votes to end debate.
    risk: high
    verifymethod: test
  }
  requirement SenatePassage {
    id: 3
    text: Simple majority of the Senate, 51 of 100.
    risk: medium
    verifymethod: test
  }
  element HouseRollCall {
    type: recorded_vote
  }
  element ClotureMotion {
    type: recorded_vote
  }
  element SenateRollCall {
    type: recorded_vote
  }
  HouseRollCall - satisfies -> HousePassage
  ClotureMotion - satisfies -> SenateCloture
  SenateRollCall - satisfies -> SenatePassage
  SenateCloture - derives -> SenatePassage
```


---

### 18. Handling the Standard Objections

How each predictable objection is answered rather than avoided: a stated objection
(cost, federal overreach, innovation chill, or redundancy) is met with the specific
cited provision that resolves it, and only a genuinely new concern is routed to an
amendment. A flowchart is correct because objection handling is a routed decision
that mostly terminates in a citation. Reproduced in the compiled LaTeX framework as a
matching colored TikZ figure (palette: black, grayscales, #4B0082, #000080,
#C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':28,'rankSpacing':42,'htmlLabels':true}}}%%
flowchart TB
  OBJ{"Stated<br/>objection?"}:::act
  COST["Cost: zero net mandatory,<br/>PAYGO clause, 19 to 1 saving"]:::evid
  FED["Overreach: savings clause<br/>preserves State human-over-AI"]:::evid
  CHILL["Innovation chill: 510(k) and<br/>change-control carve-outs"]:::evid
  REDUN["Redundant: closest analogues<br/>are voluntary, not automated"]:::evid
  NEWC["Genuinely new concern"]:::n3
  AMEND["Route to a<br/>committee amendment"]:::caut
  OBJ -->|cost| COST
  OBJ -->|federalism| FED
  OBJ -->|innovation| CHILL
  OBJ -->|redundancy| REDUN
  OBJ -->|other| NEWC --> AMEND
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

### 19. The Scoring Path

How the bill clears the budget points of order: once introduced it is scored, the
authorization is found to create no direct spending and no revenue effect, the PAYGO
scorecard reads zero, and the bill is CutGo compatible and cleared for the floor. A
state diagram is correct because scorekeeping is a sequence of states with one guard
that could send a bill back for an offset. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  [*] --> Introduced
  Introduced --> Scored: referred to CBO
  Scored --> DirectSpendingCheck
  DirectSpendingCheck --> NeedsOffset: direct spending found
  DirectSpendingCheck --> ZeroNet: discretionary only
  NeedsOffset --> ZeroNet: offset or pay-for added
  ZeroNet --> CutGoCompatible: no net mandatory increase
  CutGoCompatible --> ClearedForFloor
  ClearedForFloor --> [*]
```


---

### 20. From One Yes to Enactment

The capstone: the eight answered questions become one member's yes, that yes becomes
a committee report, the report becomes House and Senate passage, and the two
chambers become enacted law that the platform is ready to implement. A top-down
flowchart is correct because it closes the framework by tracing a single decision up
to the statute it produces. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':30,'rankSpacing':44,'htmlLabels':true}}}%%
flowchart TB
  EIGHT["Eight questions<br/>answered with evidence"]:::n1
  YES["One member's<br/>yes vote"]:::evid
  RPT["Committee report<br/>and markup"]:::n2
  PASS["House and Senate<br/>passage"]:::act
  LAW["Enacted law,<br/>section 515D"]:::act
  IMPL["Platform ready<br/>to implement"]:::evid
  EIGHT --> YES --> RPT --> PASS --> LAW --> IMPL
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```


---

