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
