### 04. The Ten VVUQ Gates from the Clinician's Seat

Before any candidate action executes it descends through ten verification,
validation, and uncertainty-quantification gates, ending with a catastrophe
predicate that can hard-block. The clinician does not run the gates by hand, but
relies on the fact that all ten must pass. A vertical flowchart funnel is correct
because the content is a strict sequence of pass conditions that narrows to a
single accept. Reproduced in the compiled LaTeX framework as a matching colored
TikZ figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'monotoneY','nodeSpacing':22,'rankSpacing':24,'htmlLabels':true}}}%%
flowchart TB
  IN["Candidate action"]:::n1
  G1["Gate 1 verification fraction 1.0"]:::n2
  G2["Gate 2 validation agreement"]:::n2
  G3["Gate 3 relative error bound"]:::n2
  G4["Gate 4 coefficient of variation"]:::n2
  G5["Gates 5 to 9 standards binding"]:::n3
  G10["Gate 10 catastrophe predicate"]:::act
  OUT["ACCEPT and act under audit"]:::hope
  IN --> G1 --> G2 --> G3 --> G4 --> G5 --> G10 --> OUT
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
