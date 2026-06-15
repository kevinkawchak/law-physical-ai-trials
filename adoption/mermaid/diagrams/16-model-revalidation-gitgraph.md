### 16. Model Revalidation Under Version Control

Reliability over time is managed like code: a validated model is deployed, drift is
detected, a branch retrains and revalidates against the gates, and only a passing
revalidation merges back and is redeployed in service. A version-control graph is
the most literal rendering of a branch that retrains and merges back into a single
line. Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','git0':'#8B2E3F','git1':'#D08770','git2':'#BFBFBF','gitBranchLabel0':'#ffffff','gitBranchLabel1':'#1A0A04','gitBranchLabel2':'#111111','commitLabelColor':'#111111','commitLabelBackground':'#F2F2F2','tagLabelColor':'#1A1505','tagLabelBackground':'#EBCB8B','tagLabelBorder':'#000000'}}}%%
gitGraph
  commit id: "validated"
  commit id: "deployed"
  commit id: "drift-detected"
  branch retrain
  commit id: "retrain-on-new-data"
  commit id: "revalidate-gates"
  checkout main
  merge retrain id: "revalidated"
  commit id: "redeployed" tag: "in-service"
```
