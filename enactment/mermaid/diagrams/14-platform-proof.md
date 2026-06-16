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
