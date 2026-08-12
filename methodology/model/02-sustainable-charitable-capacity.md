# 2. Sustainable Charitable Capacity

Suppose individual $i$ owns $n_i$ assets. Define sustainable charitable capacity as

$$C_i = C_i^{\text{cash}} + \sum_{j=1}^{n_i} \int_0^{q_{ij}^{*}} P_{ij}(q)\, L_{ij}(q)\, K_{ij}(q)\, dq$$

where

- $C_i^{\text{cash}}$ = cash and immediately disposable liquid assets
- $P_{ij}(q)$ = realizable marginal price of asset $j$ — [§3](03-public-market-liquidity.md)
- $L_{ij}(q)$ = liquidity and marketability adjustment — [§5](05-private-company-wealth.md)
- $K_{ij}(q)$ = control and founder-dependence adjustment — [§4](04-control-and-ownership.md), [§6](06-founder-dependence-and-sentiment.md)
- $q_{ij}^{*}$ = maximum quantity of asset $j$ that can be economically relinquished

This formulation distinguishes between the quoted value of an asset and the amount of economic value that can actually be transferred.

## 2.1 Why an integral

The three adjustment terms are all functions of $q$, not constants. Selling the first 1% of a position is not economically equivalent to selling the fortieth percent:

- $P_{ij}(q)$ declines as cumulative disposal grows, because each additional unit is absorbed by a thinner bid.
- $K_{ij}(q)$ can drop discontinuously at the point where remaining ownership crosses a control threshold.
- $L_{ij}(q)$ tightens as the residual block becomes a larger share of realistic private-market demand.

Multiplying a headline position value by a single blended discount would discard this structure. Integrating over $q$ preserves it.

## 2.2 The upper limit $q^{*}$

$q_{ij}^{*}$ is a modeling choice, not an observable. It is the point beyond which further disposal is not economically meaningful — because the marginal realizable price has collapsed, because control constraints bind absolutely, or because the individual's remaining position is legally restricted from transfer.

Where $q_{ij}^{*}$ is genuinely uncertain, it belongs in the parameter vector $\boldsymbol{\theta}$ and is drawn per simulation ([§9](09-monte-carlo-estimation.md)) rather than fixed.

## 2.3 Interpretation of the components

| Component | Answers |
|---|---|
| $C_i^{\text{cash}}$ | What could be given away today with no market consequence? |
| $P_{ij}(q)$ | What price would the market actually pay for each successive unit? |
| $L_{ij}(q)$ | Is there a market for this unit at all, and on what timeline? |
| $K_{ij}(q)$ | Does disposing of this unit destroy value in the units retained? |
