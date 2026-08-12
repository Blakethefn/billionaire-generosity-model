# 5. Private-Company Wealth

Private-company ownership requires additional adjustments because no continuously traded public market necessarily exists for the shares.

## 5.1 Basic private-market model

$$V_{\text{private}}^{*} = V_{\text{headline}}\,(1 - D_M)(1 - D_B)(1 - D_I)$$

where

- $D_M$ = discount for lack of marketability
- $D_B$ = large-block discount
- $D_I$ = information and transaction uncertainty discount

The three discounts compound multiplicatively rather than adding, so that no combination of individually plausible discounts can drive the adjusted value below zero.

## 5.2 Sources for the discounts

These parameters should be estimated from observable transactions whenever possible, including

- secondary-market transactions
- tender offers
- funding rounds
- employee share sales
- comparable private-company transactions

Employee share sales and company-run tender offers are particularly informative because they reveal a price at which the company itself, or its existing investors, were willing to transact — as opposed to a headline valuation set by a small marginal investment with liquidation preferences attached.

## 5.3 The last-round problem

A private company's most recent funding-round valuation should not automatically imply that a controlling shareholder could sell their entire position at the same valuation.

A headline round price is set by a marginal buyer purchasing preferred stock with downside protection. A founder's common shares lack those protections, and the block on offer is orders of magnitude larger than the round. The headline number is therefore an upper bound on per-share realizable value, not an estimate of it.

## 5.4 Relationship to $L(q)$

$L_{ij}(q)$ in the capacity integral ([§2](02-sustainable-charitable-capacity.md)) is the quantity-dependent generalization of the discounts above. Where transaction evidence is thin, a defensible reduction is to hold $L$ constant over $q$ at $(1-D_M)(1-D_B)(1-D_I)$ and let the uncertainty live in the distributions of the three discounts rather than in an assumed shape for $L(q)$.
