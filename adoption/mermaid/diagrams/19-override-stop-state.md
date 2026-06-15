### 19. Override and the Stop Authority

Control means the clinician can always intervene: a running action can be paused
for review and resumed, or overridden to a full stop, and the catastrophe predicate
can stop it without any human in the path. A state diagram is correct because the
content is a small set of states with guarded transitions, including an
unconditional stop. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'}}}%%
stateDiagram-v2
  direction LR
  [*] --> Running
  Running --> Hold: clinician pause
  Hold --> Running: resume after review
  Hold --> Stopped: clinician override
  Running --> Stopped: catastrophe predicate
  Stopped --> [*]
  classDef act fill:#8B2E3F,stroke:#000000,color:#ffffff
  classDef risk fill:#D08770,stroke:#000000,color:#1A0A04
  class Hold act
  class Stopped risk
```
