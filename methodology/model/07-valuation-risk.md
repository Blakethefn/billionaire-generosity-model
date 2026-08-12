# 7. Valuation Risk

High valuation multiples should affect uncertainty rather than produce arbitrary deterministic discounts.

## 7.1 Valuation-risk measure

Let

$$R_V = f\!\left(P/E,\ P/S,\ EV/EBITDA,\ FCF_Y,\ \sigma_g,\ \sigma_m\right)$$

where

- $FCF_Y$ = free-cash-flow yield
- $\sigma_g$ = uncertainty in future growth
- $\sigma_m$ = uncertainty in future margins

## 7.2 Company value as a random variable

Future company value can be represented as

$$V_{t+1} = V_t(1 + R)$$

where

$$R \sim \mathcal{D}(\mu, \sigma, \text{skew}, \text{kurtosis})$$

A highly speculative valuation would generally produce a wider distribution of potential future values than a mature company with stable cash flows.

## 7.3 Why this is the right place for multiples

A deterministic haircut on high-multiple companies makes an unfalsifiable claim — that the market is wrong by a specific amount, in a specific direction. Routing multiples into the *dispersion* of $R$ instead makes a much weaker and more defensible claim: that the market's estimate is less reliable, without asserting which way it errs.

The consequences differ. A deterministic discount shifts a single point estimate and can be dismissed as an arbitrary choice. Wider dispersion propagates into the capacity distribution ([§9](09-monte-carlo-estimation.md)) and shows up honestly as a wider credible interval on the final rate and a less stable rank ([§11](11-comparisons-and-rank-stability.md)) — which is the accurate representation of not knowing.

$\mathcal{D}$ should admit skew and excess kurtosis rather than defaulting to normality; the distribution of outcomes for a speculatively valued company is neither symmetric nor thin-tailed.
