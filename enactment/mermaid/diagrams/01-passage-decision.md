### 01. The Passage Decision

The core idea of the framework in one figure: when H. R. 9510 reaches a member's
desk, the member runs the eight passage questions and then cosponsors and votes
yes, offers an amendment first, or declines and states the reason. A flowchart is
correct because the content is a directed decision flow that ends in one choice
with three guarded outcomes. Reproduced in the compiled LaTeX framework as a
matching colored TikZ figure (palette: black, grayscales, #4B0082, #000080,
#C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':52,'htmlLabels':true}}}%%
flowchart TB
  BILL["H. R. 9510<br/>reaches the desk"]:::n1
  Q{"Eight passage<br/>questions answered?"}:::act
  YES["Cosponsor and<br/>vote yes"]:::evid
  AMEND["Offer an amendment,<br/>then support"]:::n3
  NO["Decline and<br/>state the reason"]:::caut
  BILL --> Q
  Q -->|all answered| YES
  Q -->|one open| AMEND
  Q -->|unconvinced| NO
  AMEND -.->|adopted at markup| Q
  classDef act fill:#4B0082,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef evid fill:#000080,stroke:#000000,stroke-width:1.3px,color:#ffffff
  classDef caut fill:#C0C0C0,stroke:#000000,stroke-width:1.2px,color:#111111
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
