### 04. Compounding Human Error Versus the Verified Path

The legacy trial and peer-review system passes work through many manual handoffs,
and each handoff is an independent opportunity for error that compounds downstream.
The verified path inserts an automated gate at each step so a defect is caught
where it occurs. Two parallel flows make the contrast legible. Reproduced in the
compiled LaTeX narrative as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'cardinal','nodeSpacing':30,'rankSpacing':46,'htmlLabels':true}}}%%
flowchart LR
  subgraph LEG["Legacy path: error compounds"]
    direction LR
    L1["Manual entry"]:::risk
    L2["Manual review"]:::risk
    L3["Manual handoff"]:::risk
    L4["Outcome at risk"]:::risk
    L1 --> L2 --> L3 --> L4
  end
  subgraph VER["Verified path: error contained"]
    direction LR
    V1["Generate"]:::n2
    G1{"gate"}:::act
    V2["Review"]:::n2
    G2{"gate"}:::act
    V3["Execute under audit"]:::hope
    V1 --> G1 --> V2 --> G2 --> V3
  end
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
```
