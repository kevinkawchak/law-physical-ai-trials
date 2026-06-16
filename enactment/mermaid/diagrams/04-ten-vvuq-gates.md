### 04. The Ten Gates Congress Is Enacting

The regulatory content of section 515D: ten verification gates, each bound to a
published external standard, with three hard catastrophe predicates (vascular
no-fly, shared-room collision, and fault or emergency stop) that must hold without
exception. A top-down flowchart is correct because it shows a fixed schedule
converging on the predicates that can stop everything. Reproduced in the compiled
LaTeX framework as a matching colored TikZ figure (palette: black, grayscales,
#4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':26,'rankSpacing':40,'htmlLabels':true}}}%%
flowchart TB
  subgraph SUITE["Ten-gate VVUQ suite (section 515D(c))"]
    direction LR
    G1["1 Hand-eye"]:::n1
    G2["2 Finger force"]:::n1
    G3["3 Balance"]:::n1
    G4["4 Plan"]:::n1
    G5["5 Grasp"]:::n1
    G7["7 Suturing"]:::n2
    G8["8 Perception"]:::n2
  end
  subgraph HARD["Hard catastrophe predicates (agreement 1.00)"]
    direction LR
    G6["6 Vascular<br/>no-fly"]:::act
    G9["9 Shared-room<br/>collision"]:::act
    G10["10 Fault and<br/>emergency stop"]:::act
  end
  SUITE --> DEC{"Verification<br/>fraction = 1.0?"}:::evid
  HARD --> DEC
  DEC -->|yes, all hold| PASS["Cleared to generate<br/>and execute"]:::evid
  DEC -->|no| STOP["BLOCK"]:::caut
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
