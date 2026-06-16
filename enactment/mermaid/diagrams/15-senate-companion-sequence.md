### 15. The Two-Chamber Strategy

How passage in one chamber is converted into law: a Senate companion is introduced
in parallel, each chamber reports and passes its version, and the differences are
reconciled by amendment exchange or conference before enrollment. A sequence diagram
is correct because the content is an ordered exchange of messages between two
chambers over time. Reproduced in the compiled LaTeX framework as a matching colored
TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111','actorBkg':'#4B0082','actorTextColor':'#ffffff','actorBorder':'#000000','signalColor':'#333333','signalTextColor':'#111111'}}}%%
sequenceDiagram
  participant H as House
  participant S as Senate
  participant P as President
  H->>H: Pass H. R. 9510
  H->>S: Message the bill to the Senate
  S->>S: Introduce companion, report, pass
  S-->>H: Return with amendments
  H->>H: Concur or request conference
  H->>P: Enroll the reconciled bill
  P-->>H: Sign into law
```
