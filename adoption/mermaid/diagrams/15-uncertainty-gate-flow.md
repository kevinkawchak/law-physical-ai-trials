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
