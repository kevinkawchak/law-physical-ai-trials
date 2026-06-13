### 08. The Annual Reporting Sequence

Accountability under the Act flows on a fixed schedule: the trial sponsor files a
verified record, the Secretary reviews and certifies it, and a public report
reaches Congress. A sequence diagram is correct because the content is an ordered
exchange of messages between named parties over time, with a review loop.
Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant S as Trial sponsor
  participant H as Secretary (HHS / FDA)
  participant C as Congress and the public
  S->>H: File verified annual record
  activate H
  loop Certification cycle
    H-->>S: Findings and corrections
    S->>H: Revised record
  end
  H->>C: Certified public report
  deactivate H
  Note over C: Transparent record of safety and cost
```
