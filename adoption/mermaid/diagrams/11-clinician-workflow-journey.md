### 11. A Clinician's Day with the System

Workflow decides whether a safe tool is actually used: a clinician's day is scored
step by step, from reviewing overnight monitoring through accepting recommendations
under audit to countersigning records and flagging drift. A user journey is correct
because the content is an ordered lived experience with a satisfaction score per
step. Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryColor':'#EBCB8B','primaryBorderColor':'#000000','primaryTextColor':'#1A1505','lineColor':'#333333'}}}%%
journey
  title A Clinician's Day with a Verified Physical AI System
  section Before clinic
    Review overnight monitoring: 4: Clinician
    Confirm system validated on site: 5: Clinician
  section In clinic
    Receive recommendation with reasons: 5: System, Clinician
    Confirm consent and subgroup fit: 4: Clinician, Patient
    Accept under audit or escalate: 5: Clinician
  section After clinic
    Countersign audit records: 4: Clinician
    Flag drift or adverse event: 3: Clinician, Response team
```
