### 05. The Coalition Map

Coalition building shows lawmakers that the bill has wide-ranging support.
Patient-advocacy groups, hospital networks, technology developers, and medical
boards each bring distinct evidence to the same committee. A clustered flowchart
with one subgraph per constituency is correct because it groups independent actors
that converge on a single legislative target. Reproduced in the compiled LaTeX
narrative as a matching colored TikZ figure (palette: black, grayscales, #EBCB8B,
#D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':50,'htmlLabels':true}}}%%
flowchart TB
  subgraph PAT["Patients and families"]
    A1["Advocacy groups"]:::n1
  end
  subgraph HOSP["Hospital networks"]
    A2["Investigators and sites"]:::n2
  end
  subgraph TECH["Technology developers"]
    A3["Physical AI and assurance"]:::n2
  end
  subgraph BOARD["Medical boards"]
    A4["Standards and ethics"]:::n3
  end
  CONG["Congressional committee"]:::act
  PASS["Enact H. R. 9510"]:::hope
  A1 --> CONG
  A2 --> CONG
  A3 --> CONG
  A4 --> CONG
  CONG --> PASS
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
