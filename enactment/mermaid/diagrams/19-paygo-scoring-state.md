### 19. The Scoring Path

How the bill clears the budget points of order: once introduced it is scored, the
authorization is found to create no direct spending and no revenue effect, the PAYGO
scorecard reads zero, and the bill is CutGo compatible and cleared for the floor. A
state diagram is correct because scorekeeping is a sequence of states with one guard
that could send a bill back for an offset. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  [*] --> Introduced
  Introduced --> Scored: referred to CBO
  Scored --> DirectSpendingCheck
  DirectSpendingCheck --> NeedsOffset: direct spending found
  DirectSpendingCheck --> ZeroNet: discretionary only
  NeedsOffset --> ZeroNet: offset or pay-for added
  ZeroNet --> CutGoCompatible: no net mandatory increase
  CutGoCompatible --> ClearedForFloor
  ClearedForFloor --> [*]
```
