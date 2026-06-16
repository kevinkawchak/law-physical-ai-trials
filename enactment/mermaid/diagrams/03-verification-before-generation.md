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
