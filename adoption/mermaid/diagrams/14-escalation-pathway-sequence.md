### 14. The Escalation Pathway

When a gate is uncertain the system does not guess: it escalates to the on-call
clinician, who resolves it at the bedside or escalates further to the attending,
and every step writes to the record. A sequence diagram with an alternative path is
correct because the content is an ordered exchange with a branch. Reproduced in the
compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','actorBkg':'#D9D9D9','actorBorder':'#000000','actorTextColor':'#111111','actorLineColor':'#888888','signalColor':'#333333','signalTextColor':'#111111','noteBkgColor':'#EBCB8B','noteBorderColor':'#000000','noteTextColor':'#1A1505','labelBoxBkgColor':'#8B2E3F','labelBoxBorderColor':'#000000','labelTextColor':'#ffffff','sequenceNumberColor':'#ffffff','loopTextColor':'#111111'}}}%%
sequenceDiagram
  autonumber
  participant Y as System
  participant O as On-call clinician
  participant A as Attending
  participant R as Record
  Y->>O: ESCALATE (uncertain gate)
  O->>O: Review reasons and audit trail
  alt Resolved at the bedside
    O->>R: Document decision and act under audit
  else Needs senior judgment
    O->>A: Escalate with full context
    A->>R: Decide, document, and act
  end
  Note over R: Escalation never bypasses the record
```
