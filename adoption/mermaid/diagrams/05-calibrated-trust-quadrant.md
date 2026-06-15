### 05. The Calibrated-Trust Band

The framework's organizing concept: a clinician should rely on a system exactly as
much as its demonstrated capability warrants. Plotting demonstrated capability
against clinician reliance separates calibrated trust from its two failure modes,
automation bias (over-trust) and algorithm aversion (under-trust). A quadrant chart
is correct because the content compares states on two continuous axes. Reproduced
in the compiled LaTeX framework as a matching colored TikZ figure (palette: black,
grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','quadrant1Fill':'#EBCB8B','quadrant2Fill':'#D08770','quadrant3Fill':'#F2F2F2','quadrant4Fill':'#D9D9D9','quadrant1TextFill':'#1A1505','quadrant2TextFill':'#1A0A04','quadrant3TextFill':'#111111','quadrant4TextFill':'#111111','quadrantPointFill':'#8B2E3F','quadrantPointTextFill':'#111111','quadrantTitleFill':'#111111','quadrantXAxisTextFill':'#333333','quadrantYAxisTextFill':'#333333','quadrantInternalBorderStrokeFill':'#888888','quadrantExternalBorderStrokeFill':'#333333'}}}%%
quadrantChart
  title Calibrated Trust and Its Failure Modes
  x-axis Low Capability --> High Capability
  y-axis Low Reliance --> High Reliance
  quadrant-1 Calibrated trust
  quadrant-2 Automation bias
  quadrant-3 Appropriate caution
  quadrant-4 Algorithm aversion
  Verified action under audit: [0.85, 0.83]
  Unvalidated tool over-used: [0.22, 0.74]
  Proven tool ignored: [0.82, 0.24]
  Experimental and watched: [0.27, 0.27]
```
