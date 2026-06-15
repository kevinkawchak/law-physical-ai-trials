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
