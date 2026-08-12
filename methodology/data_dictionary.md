# Proposed Dataset

For each individual $i$, construct approximately 40–60 variables across the following categories.

## Wealth

| Variable | Description |
|---|---|
| $W_i^{\text{headline}}$ | Estimated headline net worth |
| $C_i^{\text{cash}}$ | Cash and immediately disposable liquid assets |
| $W_i^{\text{public equity}}$ | Public equity holdings |
| $W_i^{\text{private equity}}$ | Private company holdings |
| $W_i^{\text{real estate}}$ | Real estate |
| $W_i^{\text{other}}$ | Residual |

## Public equity

Per public position $j$:

| Variable | Description |
|---|---|
| $P_0$ | Current market price |
| $Q$ | Shares owned |
| $ADV$ | Average daily trading volume |
| $\sigma$ | Equity volatility |
| $P/E$ | Price-to-earnings |
| $P/S$ | Price-to-sales |
| $EV/EBITDA$ | Enterprise value to EBITDA |
| $FCF_Y$ | Free-cash-flow yield |
| $SI$ | Short interest |

## Ownership and control

| Variable | Description |
|---|---|
| $s_i$ | Ownership percentage |
| $s_i^{\min}$ | Minimum ownership preserving effective control |
| Voting percentage | May diverge sharply from economic ownership |
| Board influence | Seats held, appointment rights |
| Dual-class voting rights | Structure and ratio |
| Shareholder restrictions | Lockups, transfer restrictions, standstills |

## Private equity

| Variable | Description |
|---|---|
| $V_{\text{last round}}$ | Most recent funding-round valuation |
| $D_M$ | Discount for lack of marketability |
| $D_B$ | Large-block discount |
| $D_I$ | Information and transaction uncertainty discount |
| Secondary transaction prices | Observed secondary sales |
| Tender-offer prices | Company or investor tender prices |

## Founder dependence

| Variable | Description |
|---|---|
| $F_i$ | Founder dependence probability |
| $\eta_i$ | Investor-sentiment sensitivity |
| $\delta_{c,i}$ | Control-loss penalty |

## Charitable giving

| Variable | Description |
|---|---|
| $D_i^{\text{external}}$ | Direct transfers to independent charities |
| $D_i^{\text{foundation}}$ | Qualifying distributions from private foundations |
| $D_i^{\text{DAF}}$ | Donor-advised-fund transfers |
| $D_i^{\text{controlled}}$ | Transfers to donor-controlled entities |
| $D_i^{\text{distributed}}$ | Independently deployed |

## Time series

For every major donation, the triple

$$\{D_t,\ t,\ w_t\}$$

— amount, date, and independence/deployment weight. This is what makes the opportunity-cost adjustment of [§8.3](../docs/08-giving-numerator.md) possible, and it is the most labor-intensive part of the dataset: a single aggregate lifetime-giving figure cannot be compounded.

## Recording provenance

Every value should carry a source and a confidence indicator. The parameter standard in [§13.3](../docs/13-interpretation-and-validation.md) requires each variable to be observable, estimated, or distributed — and which of the three it is must be recorded per variable per individual, not assumed uniformly across the sample. The same variable may be directly observable for one individual (an SEC-filed ownership stake) and a distributional guess for another (a private holding with no transaction history).
