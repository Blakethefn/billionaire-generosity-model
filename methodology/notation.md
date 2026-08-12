# Notation

Symbols are consistent across all sections. Subscript $i$ indexes individuals, $j$ indexes assets held by an individual, $t$ indexes time, and $k$ indexes Monte Carlo simulation draws.

## Wealth and capacity

| Symbol | Meaning |
|---|---|
| $W_i$ | Estimated headline net worth |
| $C_i$ | Sustainable charitable capacity |
| $C_i^{\text{cash}}$ | Cash and immediately disposable liquid assets |
| $W_i^{\text{control-safe}}$ | Wealth relinquishable without crossing the control threshold |
| $n_i$ | Number of distinct assets held |

## Public-market positions

| Symbol | Meaning |
|---|---|
| $P_0$ | Current market price |
| $Q$ | Shares owned |
| $q$ | Quantity relinquished (integration variable) |
| $q_{ij}^{*}$ | Maximum quantity of asset $j$ economically relinquishable |
| $P(q)$ | Realizable marginal price at cumulative quantity $q$ |
| $ADV$ | Average daily trading volume |
| $\lambda$ | Market-impact coefficient |
| $V^{\text{MTM}}$ | Mark-to-market value, $QP_0$ |
| $V_{\text{realizable}}(Q)$ | Value actually realizable from liquidating $Q$ |
| $\sigma$ | Equity volatility |
| $SI$ | Short interest |
| $OC$ | Ownership concentration |

## Ownership and control

| Symbol | Meaning |
|---|---|
| $s_i$ | Current ownership percentage |
| $s_i^{\min}$ | Minimum ownership preserving effective control |
| $s_i^{\text{safe}}$ | $\max(0,\ s_i - s_i^{\min})$ |
| $s(q)$ | Remaining ownership after relinquishing $q$ |
| $s_{\text{control}}$ | Control threshold |
| $K(q)$ | Control / founder-dependence adjustment |
| $\delta_c$ | Economic penalty on loss of control |
| $V$ | Company equity value |

## Private holdings

| Symbol | Meaning |
|---|---|
| $V_{\text{headline}}$ | Stated (e.g. last-round) valuation |
| $V_{\text{private}}^{*}$ | Adjusted private-position value |
| $D_M$ | Discount for lack of marketability |
| $D_B$ | Large-block discount |
| $D_I$ | Information and transaction uncertainty discount |
| $L(q)$ | Liquidity and marketability adjustment |

## Founder dependence and sentiment

| Symbol | Meaning |
|---|---|
| $F_i$ | Founder dependence: $P(\text{material impairment} \mid \text{founder relinquishes control})$ |
| $p(s)$ | Probability of successful continuation given remaining ownership $s$ |
| $a, b$ | Logistic parameters of $p(s)$ |
| $V_S$ | Company value under successful continuation |
| $V_F$ | Company value under founder disruption |
| $S(q)$ | Investor-sentiment effect |
| $\eta$ | Investor-sentiment sensitivity |

## Valuation risk

| Symbol | Meaning |
|---|---|
| $M$ | Valuation multiple |
| $R_V$ | Valuation-risk measure |
| $FCF_Y$ | Free-cash-flow yield |
| $\sigma_g$ | Uncertainty in future growth |
| $\sigma_m$ | Uncertainty in future margins |
| $g$ | Future growth |
| $m$ | Future margins |

## Giving

| Symbol | Meaning |
|---|---|
| $D_i$ | Documented charitable giving |
| $D_i^{*}$ | Weighted charitable giving |
| $D_i^{\text{external}}$ | Direct transfers to independent charities |
| $D_i^{\text{foundation}}$ | Qualifying distributions from private foundations |
| $D_i^{\text{DAF}}$ | Donor-advised-fund transfers |
| $D_i^{\text{controlled}}$ | Transfers to donor-controlled charitable entities |
| $\alpha, \beta, \gamma$ | Weights on foundation, DAF, and controlled transfers, each in $[0,1]$ |
| $w_{it}$ | Charitable independence / deployment weight on donation $t$ |
| $D_t^{OC}$ | Opportunity-cost-adjusted value of donation at time $t$ |
| $r_k$ | Relevant investment return in period $k$ |
| $T$ | Terminal time |

## Results

| Symbol | Meaning |
|---|---|
| $G_i$ | Adjusted Giving Rate |
| $\boldsymbol{\theta}$ | Parameter vector |
| $N$ | Number of Monte Carlo simulations |
| $N_B$ | Number of individuals in the sample |
| $R_i$ | Rank of individual $i$ |
| $r^{*}$ | Rank threshold |
| $\varepsilon_{G,x}$ | Elasticity of $G$ with respect to parameter $x$ |
| $\mathbf{1}(\cdot)$ | Indicator function |
| $X^{5\%}, X^{50\%}, X^{95\%}$ | Simulation percentiles of quantity $X$ |
