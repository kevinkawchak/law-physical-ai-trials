### 10. The Subgroup Equity Map

Equity is measured, not assumed: each clinically relevant subgroup is plotted by
its representation in validation against its performance relative to the overall
model, so disparities and under-sampled groups become surveillance priorities. A
quadrant chart is correct because the content compares subgroups on two continuous
axes. Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','quadrant1Fill':'#EBCB8B','quadrant2Fill':'#F2F2F2','quadrant3Fill':'#D08770','quadrant4Fill':'#D9D9D9','quadrant1TextFill':'#1A1505','quadrant2TextFill':'#111111','quadrant3TextFill':'#1A0A04','quadrant4TextFill':'#111111','quadrantPointFill':'#8B2E3F','quadrantPointTextFill':'#111111','quadrantTitleFill':'#111111','quadrantXAxisTextFill':'#333333','quadrantYAxisTextFill':'#333333','quadrantInternalBorderStrokeFill':'#888888','quadrantExternalBorderStrokeFill':'#333333'}}}%%
quadrantChart
  title Subgroup Representation and Performance
  x-axis Under-represented --> Well-represented
  y-axis Below overall --> At or above overall
  quadrant-1 Equitable and evidenced
  quadrant-2 Good but under-sampled
  quadrant-3 Surveillance priority
  quadrant-4 Disparity flagged
  Older adults: [0.78, 0.80]
  Pediatric rare cancer: [0.24, 0.72]
  Underserved ancestry: [0.30, 0.34]
  Rural access cohort: [0.66, 0.40]
```
