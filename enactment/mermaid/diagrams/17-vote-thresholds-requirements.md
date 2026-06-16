### 17. The Vote Thresholds

What "passage" concretely requires: a simple majority in the House, sixty votes to
invoke cloture in the Senate, and a simple majority to pass the Senate, each
satisfied by a recorded action. A requirement diagram is correct because it states
the thresholds as formal requirements and links the action that verifies each.
Reproduced in the compiled LaTeX framework as a matching colored TikZ figure
(palette: black, grayscales, #4B0082, #000080, #C0C0C0).

```mermaid
%%{init: {'theme':'base','themeVariables':{'fontFamily':'Helvetica, Arial, sans-serif','primaryTextColor':'#111111'}}}%%
requirementDiagram
  requirement HousePassage {
    id: 1
    text: Simple majority of the House, 218 of 435.
    risk: medium
    verifymethod: test
  }
  requirement SenateCloture {
    id: 2
    text: Sixty votes to end debate.
    risk: high
    verifymethod: test
  }
  requirement SenatePassage {
    id: 3
    text: Simple majority of the Senate, 51 of 100.
    risk: medium
    verifymethod: test
  }
  element HouseRollCall {
    type: recorded_vote
  }
  element ClotureMotion {
    type: recorded_vote
  }
  element SenateRollCall {
    type: recorded_vote
  }
  HouseRollCall - satisfies -> HousePassage
  ClotureMotion - satisfies -> SenateCloture
  SenateRollCall - satisfies -> SenatePassage
  SenateCloture - derives -> SenatePassage
```
