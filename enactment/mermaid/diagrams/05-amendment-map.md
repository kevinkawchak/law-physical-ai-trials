### 05. The Amendment Map

What the bill changes in the United States Code: a single new section 515D
(21 U.S.C. 360e-5) carries ten conforming amendments across Title 21, from the
device definition to State preemption, plus a clerical update to the table of
contents. A clustered flowchart is correct because one new section radiates targeted
edits into existing law. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111','clusterBkg':'#F2F2F2','clusterBorder':'#888888'},'flowchart':{'curve':'cardinal','nodeSpacing':22,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart TB
  CORE["New section 515D<br/>21 U.S.C. 360e-5"]:::act
  subgraph DEF["Scope and prohibition"]
    A1["321(h) device"]:::n1
    A2["331 prohibited act (jjj)"]:::n1
    A3["351 adulteration (k)"]:::n1
  end
  subgraph PATH["Premarket pathways"]
    A4["355g real-world evidence"]:::n2
    A5["360(k) 510(k)"]:::n2
    A6["360c classification (l)"]:::n2
    A7["360e PMA"]:::n2
    A8["360e-4 change control (d)"]:::n2
  end
  subgraph BOUND["Boundaries"]
    A9["360j(o) CDS exclusion"]:::n3
    A10["360k State savings (c)"]:::n3
  end
  CORE --> DEF
  CORE --> PATH
  CORE --> BOUND
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
