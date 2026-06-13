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
