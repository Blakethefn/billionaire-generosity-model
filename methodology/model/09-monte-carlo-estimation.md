# 9. Monte Carlo Estimation

Many of the model's parameters cannot be known precisely.

## 9.1 Parameter vector

Instead of producing a single deterministic charitable-capacity estimate, define a parameter vector

$$\boldsymbol{\theta} = \{g,\ m,\ M,\ \lambda,\ L,\ F,\ \delta_c,\ \eta,\ \sigma,\ \ldots\}$$

representing uncertain quantities:

| Symbol | Quantity |
|---|---|
| $g$ | Future growth |
| $m$ | Future margins |
| $M$ | Future valuation multiple |
| $\lambda$ | Market impact |
| $L$ | Liquidity |
| $F$ | Founder dependence |
| $\delta_c$ | Control-loss penalty |
| $\eta$ | Investor-sentiment sensitivity |
| $\sigma$ | Volatility |

## 9.2 Simulation

For simulation $k$,

$$\boldsymbol{\theta}^{(k)} \sim p(\boldsymbol{\theta})$$

and charitable capacity becomes

$$C_i^{(k)} = f_i\!\left(\boldsymbol{\theta}^{(k)}\right)$$

For $N$ simulations,

$$\hat{E}[C_i] = \frac{1}{N}\sum_{k=1}^{N} C_i^{(k)}$$

For example, $N = 100{,}000$.

## 9.3 Reported output

The model should report

$$C_i^{5\%}, \qquad C_i^{50\%}, \qquad C_i^{95\%}$$

Thus, rather than claiming that an individual possesses exactly $X billion of charitable capacity, the result is reported as

$$C_i^{50\%} = \$X\text{ billion}$$

with a 90% simulation interval

$$C_i \in [\$A, \$B] \quad \text{with probability approximately } 0.90$$

## 9.4 Correlation structure

$p(\boldsymbol{\theta})$ is a joint distribution, not a product of marginals. Drawing the parameters independently would understate the true dispersion in some places and overstate it in others. At minimum:

- $\lambda$ and $\eta$ are not separately identified from disposal data ([§6.5](06-founder-dependence-and-sentiment.md)) and should be drawn jointly.
- $\sigma$, $M$, and $\lambda$ move together — the same conditions that raise volatility and multiples also thin the book.
- $F$ and $\delta_c$ share a common cause in founder-centric governance.
- Across individuals, market-wide draws (broad returns, multiple compression) must be **common** to all $i$ within simulation $k$. Independent per-individual draws would destroy the comparisons in [§11](11-comparisons-and-rank-stability.md), which depend on all individuals being evaluated under the same simulated state of the world.

## 9.5 Common random numbers

The same draw index $k$ must index a coherent state of the world across every individual in the sample. This is what makes $P(G_i > G_j)$ meaningful: the comparison holds market conditions fixed and varies only what actually differs between the two people. Using independent simulation streams per individual would answer a different and much less interesting question.
