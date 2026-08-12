# 8. The Charitable-Giving Numerator

Reported charitable giving also requires adjustment.

## 8.1 Weighted giving

Define

$$D_i^{*} = D_i^{\text{external}} + \alpha D_i^{\text{foundation}} + \beta D_i^{\text{DAF}} + \gamma D_i^{\text{controlled}}$$

where

- $D_i^{\text{external}}$ = direct transfers to independent charities
- $D_i^{\text{foundation}}$ = qualifying distributions from private foundations
- $D_i^{\text{DAF}}$ = donor-advised-fund transfers
- $D_i^{\text{controlled}}$ = transfers to charitable entities substantially controlled by the donor

The weights satisfy

$$0 \leq \alpha, \beta, \gamma \leq 1$$

## 8.2 Two reported measures instead of one

Rather than imposing a single subjective definition, two separate measures can be reported.

**Legal Charitable Transfer Rate**

$$G_i^{\text{legal}} = \frac{D_i^{\text{irrevocably transferred}}}{C_i}$$

**Independent Distribution Rate**

$$G_i^{\text{distributed}} = \frac{D_i^{\text{independently deployed}}}{C_i}$$

This prevents disagreements about donor-controlled foundations from determining the entire ranking. The two measures bracket the honest range: an individual who has irrevocably transferred large sums into a foundation that distributes little will score high on the first and low on the second, and that gap is itself the finding.

## 8.3 Opportunity cost of historical donations

A dollar donated decades ago represents more economic wealth relinquished than the same nominal dollar donated today, because the earlier donation surrendered future investment returns.

Suppose donation $D_t$ occurred at time $t$. Its opportunity-cost-adjusted value at terminal time $T$ is

$$D_t^{OC} = D_t \prod_{k=t}^{T}(1 + r_k)$$

Under a constant return assumption,

$$D_t^{OC} = D_t(1 + r)^{T-t}$$

Total opportunity-cost-adjusted giving becomes

$$D_i^{OC} = \sum_{t=1}^{T} D_{it}\, w_{it}\, (1 + r)^{T-t}$$

where $w_{it}$ is the charitable independence/deployment weight associated with donation $t$.

## 8.4 Choice of $r$

$r$ is a modeling choice with large leverage over the result, since it compounds over decades. Three defensible conventions:

| Convention | Interpretation |
|---|---|
| Broad market return | What the donor would have earned in a diversified alternative |
| Own-asset return | What the donor actually forwent, given their concentrated holdings |
| Risk-free rate | A conservative floor on opportunity cost |

The own-asset convention is the most faithful to the model's logic but is also the most volatile — a founder whose company compounded at extreme rates would see early donations inflated enormously. Because the choice is consequential, $r$ belongs in the sensitivity analysis ([§12](12-sensitivity-and-robustness.md)) rather than being fixed by fiat.

**Both nominal and opportunity-cost-adjusted results should be reported.**
