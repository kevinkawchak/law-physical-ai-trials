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
