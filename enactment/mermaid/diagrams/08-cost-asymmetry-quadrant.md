### 08. The Cost Asymmetry

The argument that disarms the fiscal objection: the verification gate is priced in
compute, storage, and bounded human review (small, fixed, measurable), while the
embodied failure it prevents is priced in lives and litigation (large, unbounded). A
quadrant chart is correct because it places each item on the two axes that matter to
a scorekeeper, cost magnitude and predictability. Reproduced in the compiled LaTeX
framework as a matching colored TikZ figure (palette: black, grayscales, #4B0082,
#000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111','quadrant1Fill':'#F2F2F2','quadrant2Fill':'#D9D9D9','quadrant3Fill':'#D9D9D9','quadrant4Fill':'#F2F2F2','quadrantPointFill':'#4B0082','quadrantPointTextFill':'#ffffff'}}}%%
quadrantChart
  title Cost magnitude against predictability
  x-axis Low cost --> High cost
  y-axis Unpredictable --> Predictable
  quadrant-1 Affordable and bounded
  quadrant-2 Bounded but heavier
  quadrant-3 Cheap but uncertain
  quadrant-4 The risk being removed
  Verification gate suite: [0.22, 0.86]
  Records and storage: [0.16, 0.80]
  ESCALATE human review: [0.34, 0.70]
  Embodied failure: [0.88, 0.18]
  Litigation exposure: [0.80, 0.12]
```
