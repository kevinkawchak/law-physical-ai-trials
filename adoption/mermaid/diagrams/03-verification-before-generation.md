### 03. Verification Before Generation, the Clinician's View

The mechanism the framework rests on, seen from the clinician's seat: a clinical
question is posed, Claude Code proposes a candidate action, Codex reviews it
independently, and a ten-gate VVUQ check resolves to ACCEPT, ESCALATE to the
clinician, or BLOCK before anything reaches the patient. A flowchart is correct
because the content is a directed control flow with a decision node. Reproduced in
the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','lineColor':'#333333','primaryTextColor':'#111111'},'flowchart':{'curve':'basis','nodeSpacing':40,'rankSpacing':55,'htmlLabels':true}}}%%
flowchart TB
  SPEC["Clinical question<br/>investigator and clinician"]:::n1
  GEN["Claude Code<br/>proposes an action"]:::n2
  REV["Codex<br/>independent review"]:::n2
  VVUQ{"Ten VVUQ gates"}:::act
  ACC["ACCEPT<br/>act under audit"]:::hope
  ESC["ESCALATE<br/>to the clinician"]:::n3
  BLK["BLOCK<br/>before the patient"]:::risk
  SPEC --> GEN
  GEN --> REV
  REV --> VVUQ
  VVUQ -->|all gates pass| ACC
  VVUQ -->|uncertain| ESC
  VVUQ -->|catastrophe predicate| BLK
  ESC -.->|clinician revises| GEN
  classDef act fill:#8B2E3F,stroke:#000000,stroke-width:1.4px,color:#ffffff
  classDef hope fill:#EBCB8B,stroke:#000000,stroke-width:1.2px,color:#1A1505
  classDef risk fill:#D08770,stroke:#000000,stroke-width:1.2px,color:#1A0A04
  classDef n1 fill:#F2F2F2,stroke:#333333,stroke-width:1.1px,color:#111111
  classDef n2 fill:#D9D9D9,stroke:#222222,stroke-width:1.1px,color:#111111
  classDef n3 fill:#BFBFBF,stroke:#000000,stroke-width:1.2px,color:#111111
```
