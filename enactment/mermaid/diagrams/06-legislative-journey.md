### 06. The Legislative Journey

The path the bill must travel: introduction and referral, subcommittee and full
committee markup, House floor passage, the same sequence in the Senate, conference
or amendment exchange, and finally enrollment and signature. A journey diagram is
correct because it scores each stage as a sentiment the sponsor must manage, not
just a box to clear. Reproduced in the compiled LaTeX framework as a matching
colored TikZ figure (palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
journey
  title H. R. 9510 from introduction to enactment
  section House
    Introduction and referral: 4: Sponsor
    Subcommittee markup: 3: Sponsor, Committee
    Full committee reported: 4: Committee
    House floor passage: 5: House
  section Senate
    Companion referred: 3: Senate sponsor
    Committee reported: 4: Committee
    Senate floor passage: 5: Senate
  section To law
    Amendments reconciled: 4: Both chambers
    Enrolled and signed: 5: President
```
