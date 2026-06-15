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
