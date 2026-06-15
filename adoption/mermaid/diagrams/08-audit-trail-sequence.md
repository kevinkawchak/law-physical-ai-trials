### 08. The Audit Trail a Clinician Can Show

Transparency is operational, not rhetorical: every action appends a hash-chained
record, the clinician countersigns the decision, and an auditor can later
reconstruct exactly what happened and why. A sequence diagram is correct because
the content is an ordered exchange of messages between named parties over time.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant Y as System
  participant D as Clinician
  participant L as Audit log
  participant U as Auditor
  loop Every action
    Y->>L: Append record (previous hash + action)
    D->>L: Countersign the decision
  end
  U->>L: Request reconstruction
  L-->>U: Tamper-evident timeline
  Note over U: Exactly what happened, and why
```
