### 18. Handling the Standard Objections

How each predictable objection is answered rather than avoided: a stated objection
(cost, federal overreach, innovation chill, or redundancy) is met with the specific
cited provision that resolves it, and only a genuinely new concern is routed to an
amendment. A flowchart is correct because objection handling is a routed decision
that mostly terminates in a citation. Reproduced in the compiled LaTeX framework as a
matching colored TikZ figure (palette: black, grayscales, #4B0082, #000080,
#C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':28,'rankSpacing':42,'htmlLabels':true}}}%%
flowchart TB
  OBJ{"Stated<br/>objection?"}:::act
  COST["Cost: zero net mandatory,<br/>PAYGO clause, 19 to 1 saving"]:::evid
  FED["Overreach: savings clause<br/>preserves State human-over-AI"]:::evid
  CHILL["Innovation chill: 510(k) and<br/>change-control carve-outs"]:::evid
  REDUN["Redundant: closest analogues<br/>are voluntary, not automated"]:::evid
  NEWC["Genuinely new concern"]:::n3
  AMEND["Route to a<br/>committee amendment"]:::caut
  OBJ -->|cost| COST
  OBJ -->|federalism| FED
  OBJ -->|innovation| CHILL
  OBJ -->|redundancy| REDUN
  OBJ -->|other| NEWC --> AMEND
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
