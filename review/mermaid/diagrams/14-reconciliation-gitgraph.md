### 14. Reconciliation of Two Chambers

When the House and the Senate pass different versions of the bill, a conference
reconciles them into one final text that both chambers vote on. A version-control
graph is the most literal rendering of two branches merging back into a single
line. Reproduced in the compiled LaTeX narrative as a matching colored TikZ figure
(palette: black, grayscales, #EBCB8B, #D08770, #8B2E3F).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','git0':'#8B2E3F','git1':'#D08770','git2':'#BFBFBF','gitBranchLabel0':'#ffffff','gitBranchLabel1':'#1A0A04','gitBranchLabel2':'#111111','commitLabelColor':'#111111','commitLabelBackground':'#F2F2F2','tagLabelColor':'#1A1505','tagLabelBackground':'#EBCB8B','tagLabelBorder':'#000000'}}}%%
gitGraph
  commit id: "introduced"
  commit id: "committee-markup"
  branch senate
  commit id: "senate-amendments"
  checkout main
  branch house
  commit id: "house-amendments"
  checkout main
  merge house
  merge senate id: "reconciled"
  commit id: "enrolled" tag: "enacted"
```
