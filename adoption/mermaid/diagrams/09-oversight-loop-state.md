### 09. The Human-in-the-Loop Oversight Loop

Oversight is a loop the clinician never leaves: the system monitors, recommends,
and presents a decision the clinician accepts, escalates, or overrides, after
which control returns to monitoring. A state diagram is correct because the content
is a set of discrete states with guarded transitions and a choice. Reproduced in
the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  direction LR
  [*] --> Monitor
  Monitor --> Recommend: action proposed
  Recommend --> Decision
  state Decision <<choice>>
  Decision --> Execute: clinician accepts
  Decision --> Escalate: clinician unsure
  Decision --> Override: clinician rejects
  Execute --> Monitor
  Escalate --> Recommend: senior review
  Override --> Monitor: action withheld
  classDef act fill:#8B2E3F,stroke:#000000,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,color:#1A0A04
  class Recommend act
  class Execute hope
  class Override risk
```
