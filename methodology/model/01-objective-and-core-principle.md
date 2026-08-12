# 1. Objective and Core Principle

## 1.1 The naive measure

A conventional measure of billionaire generosity might be written as

$$G_i^{\text{naive}} = \frac{D_i}{W_i}$$

where

- $D_i$ = documented charitable giving of individual $i$
- $W_i$ = estimated headline net worth of individual $i$

This measure has a major weakness. Headline net worth does not necessarily represent wealth that can realistically be transferred, sold, or donated without materially changing the value of the underlying assets.

For an individual whose wealth consists primarily of liquid and diversified securities, headline net worth may approximate economically disposable wealth reasonably well. For a founder whose wealth consists primarily of controlling stakes in highly valued public or private companies, the difference can be substantial.

## 1.2 The objective

The purpose of this model is to estimate

$$G_i = \frac{\text{Economic Value Relinquished to Charity}_i}{\text{Sustainable Charitable Capacity}_i}$$

rather than simply dividing donations by headline net worth.

The resulting quantity is referred to as the individual's **Adjusted Giving Rate**.

## 1.3 Core principle

The fundamental distinction underlying the model is

$$\text{Headline Net Worth} \neq \text{Liquid Wealth} \neq \text{Realizable Wealth} \neq \text{Control-Safe Wealth} \neq \text{Sustainable Charitable Capacity}$$

Therefore

$$\frac{\text{Donations}}{\text{Headline Net Worth}}$$

should not automatically be interpreted as an economically comparable measure of generosity across individuals whose wealth structures differ substantially.

The proposed framework instead estimates the economic sacrifice represented by charitable giving relative to the amount of wealth that could realistically be relinquished.

## 1.4 Structure of the argument

Each of the five quantities in the core-principle chain is separated by an adjustment developed in a later section:

| From | To | Adjustment | Section |
|---|---|---|---|
| Headline net worth | Liquid wealth | Asset decomposition | [§2](02-sustainable-charitable-capacity.md) |
| Liquid wealth | Realizable wealth | Market impact, private-market discounts | [§3](03-public-market-liquidity.md), [§5](05-private-company-wealth.md) |
| Realizable wealth | Control-safe wealth | Control threshold, control-loss penalty | [§4](04-control-and-ownership.md) |
| Control-safe wealth | Sustainable capacity | Founder dependence, investor sentiment, valuation risk | [§6](06-founder-dependence-and-sentiment.md), [§7](07-valuation-risk.md) |
