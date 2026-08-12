# 3. Public-Market Liquidity and Price Impact

## 3.1 The mark-to-market assumption

The conventional mark-to-market value of a public equity position is

$$V^{\text{MTM}} = QP_0$$

where $Q$ is the number of shares owned and $P_0$ is the current market price.

This assumes that every share could be disposed of at $P_0$, which is generally unrealistic for extremely large positions.

## 3.2 Marginal liquidation price

Define the marginal liquidation price as

$$P(q) = P_0 \exp\!\left(-\lambda \frac{q}{ADV}\right)$$

where $ADV$ is average daily trading volume and $\lambda$ is the estimated market-impact coefficient.

## 3.3 Realizable value

The realizable value of liquidating $Q$ shares is

$$V_{\text{realizable}}(Q) = \int_0^Q P_0 \exp\!\left(-\lambda \frac{q}{ADV}\right) dq$$

which evaluates to

$$V_{\text{realizable}}(Q) = \frac{P_0 \cdot ADV}{\lambda}\left[1 - \exp\!\left(-\lambda \frac{Q}{ADV}\right)\right]$$

Consequently

$$V_{\text{realizable}}(Q) \leq QP_0$$

and the difference

$$QP_0 - V_{\text{realizable}}(Q)$$

represents estimated value lost through market impact.

Two limiting cases are worth noting. As $\lambda \to 0$ the expression converges to $QP_0$ — a frictionless market recovers the mark-to-market value. As $Q/ADV \to \infty$ the expression converges to the ceiling $P_0 \cdot ADV / \lambda$, so realizable value is bounded no matter how many shares are held.

## 3.4 A dynamic market-impact coefficient

The coefficient $\lambda$ should not be identical for every company. Define

$$\lambda = f\!\left(M,\ \sigma,\ ADV,\ SI,\ F,\ OC\right)$$

where

- $M$ = valuation multiple
- $\sigma$ = equity volatility
- $ADV$ = average daily trading volume
- $SI$ = short interest
- $F$ = founder dependence
- $OC$ = ownership concentration

A highly liquid mature corporation with stable cash flows and diversified ownership should generally have a smaller $\lambda$. A highly valued, volatile, founder-dependent corporation with concentrated ownership may have a larger $\lambda$.

## 3.5 Why valuation multiples enter here rather than as a discount

This provides a more defensible treatment of valuation ratios than directly applying an arbitrary discount to companies with high price-to-earnings ratios.

For example, a company trading at

$$P/E = 300$$

should not automatically have its value divided by some constant. Instead, the high valuation multiple contributes to the uncertainty and market-impact parameters — it widens the distribution of outcomes rather than deterministically shrinking the central estimate. See [§7](07-valuation-risk.md).

## 3.6 Complete marginal-price equation

Sections [§4](04-control-and-ownership.md) and [§6](06-founder-dependence-and-sentiment.md) add two further factors to $P(q)$, producing

$$P(q) = P_0 \exp\!\left(-\lambda \frac{q}{ADV}\right) \exp(-\eta q)\, K(q)$$

with realizable value $V(Q) = \int_0^Q P(q)\, dq$. Unlike §3.3, this integral generally has no closed form — $K(q)$ is a step function — and is evaluated numerically.
