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
