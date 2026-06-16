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
