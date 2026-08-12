# 10. The Adjusted Giving Rate

## 10.1 Full form

Combining the preceding components gives

$$G_i = \frac{\displaystyle \sum_{t=1}^{T} D_{it}\, w_{it}\, (1 + r)^{T-t}}{\displaystyle E\left[C_i^{\text{cash}} + \sum_{j=1}^{n_i} \int_0^{q_{ij}^{*}} P_{ij}(q)\, L_{ij}(q)\, K_{ij}(q)\, dq\right]}$$

More compactly,

$$G_i = \frac{D_i^{OC}}{E[C_i]}$$

This represents documented charitable giving relative to estimated economic capacity to give.

## 10.2 Uncertainty in the rate

The Adjusted Giving Rate should itself be treated as a random variable:

$$G_i^{(k)} = \frac{D_i^{(k)}}{C_i^{(k)}}$$

The reported result should therefore contain

$$G_i^{5\%}, \qquad G_i^{50\%}, \qquad G_i^{95\%}$$

For example,

$$G_i^{50\%} = 7.3\%$$

with

$$G_i \in [5.1\%, 10.8\%]$$

under the model's assumed probability distributions.

This allows uncertainty in the underlying valuations to propagate into uncertainty in the final ranking.

## 10.3 A note on ratio expectations

§10.1 writes $G_i$ with $E[C_i]$ in the denominator; §10.2 forms the ratio inside each simulation and takes percentiles of the result. These are not the same quantity — $E[D/C] \neq E[D]/E[C]$, and for a right-skewed capacity distribution the divergence is material.

**The §10.2 construction is the operative one.** Form $G_i^{(k)}$ per draw and report its percentiles. The §10.1 expression is best read as a compact statement of what the model measures, not as the estimator.

## 10.4 Reported quantities per individual

| Quantity | Basis |
|---|---|
| $G_i^{\text{legal}}$, nominal | Irrevocable transfers, unadjusted dollars |
| $G_i^{\text{legal}}$, opportunity-cost-adjusted | Irrevocable transfers, compounded |
| $G_i^{\text{distributed}}$, nominal | Independently deployed, unadjusted dollars |
| $G_i^{\text{distributed}}$, opportunity-cost-adjusted | Independently deployed, compounded |

Each as a median with a 90% interval. Four numbers with intervals, not one number.
