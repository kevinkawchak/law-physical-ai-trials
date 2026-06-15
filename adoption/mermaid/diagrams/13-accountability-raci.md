### 13. Where Accountability Sits

Accountability is unambiguous only when it is drawn: the clinician is accountable
for the patient, the sponsor for operation, the developer for the model, and the
IRB is consulted on consent, all converging on a signed standard operating
procedure that the auditor can read. A clustered flowchart is correct because it
groups distinct responsible parties that converge on one record. Reproduced in the
compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':50,'htmlLabels':true}}}%%
flowchart TB
  subgraph CARE["At the bedside"]
    CLIN["Clinician<br/>accountable for the patient"]:::act
  end
  subgraph PLAT["Platform"]
    SPON["Sponsor<br/>accountable for operation"]:::n2
    VEND["Developer<br/>responsible for the model"]:::n2
  end
  subgraph GOV["Governance"]
    IRB["IRB<br/>consulted on consent"]:::n3
    AUD["Auditor<br/>informed by the record"]:::n1
  end
  SOP["Signed SOP and<br/>documentation chain"]:::hope
  CLIN --> SOP
  SPON --> SOP
  VEND --> SOP
  IRB --> SOP
  SOP --> AUD
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
