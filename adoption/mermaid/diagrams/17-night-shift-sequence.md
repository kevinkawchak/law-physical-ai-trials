### 17. The Night-Shift Scenario

The hardest test of reliability is the one no one is watching: an event at 03:00 is
submitted to the same ten gates with the same thresholds as at noon, and the night
clinician receives the same reasoned recommendation. A sequence diagram is correct
because the content is an ordered, time-stamped exchange between parties.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant P as Patient at 03:00
  participant Y as System
  participant G as VVUQ gates
  participant N as Night clinician
  P->>Y: Event detected
  Y->>G: Submit candidate action
  G-->>Y: Same ten gates, same thresholds
  Y->>N: Recommendation with reasons
  N->>P: Act under audit or escalate
  Note over G,N: 03:00 is treated exactly like noon
```
