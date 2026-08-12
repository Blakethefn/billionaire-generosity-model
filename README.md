# Billionaire Generosity Model

A liquidity- and control-adjusted measure of charitable generosity for ultra-high-net-worth individuals.

## The problem

The conventional measure is

$$G_i^{\text{naive}} = \frac{D_i}{W_i}$$

where $D_i$ is documented charitable giving and $W_i$ is estimated headline net worth.

Headline net worth does not represent wealth that can realistically be transferred, sold, or donated without materially changing the value of the underlying assets. For an individual holding liquid, diversified securities, $W_i$ is a decent proxy for disposable wealth. For a founder holding a controlling stake in a highly valued company, the gap is substantial — and the naive ratio therefore compares two incomparable denominators.

## What the model estimates instead

$$G_i = \frac{\text{Economic Value Relinquished to Charity}_i}{\text{Sustainable Charitable Capacity}_i}$$

This quantity is the **Adjusted Giving Rate**. Every uncertain input is a distribution rather than a point estimate; the uncertainty propagates through Monte Carlo simulation, and conclusions are stated as probabilities about ranks rather than as ordinal rankings.

## Core principle

$$\text{Headline Net Worth} \neq \text{Liquid Wealth} \neq \text{Realizable Wealth} \neq \text{Control-Safe Wealth} \neq \text{Sustainable Charitable Capacity}$$

## Structure

```
billionaire-generosity-model/
├── README.md
├── requirements.txt
├── methodology/          the model specification
│   ├── data_dictionary.md
│   ├── assumptions.md
│   ├── notation.md
│   └── model/            sections 01–13
├── data/
│   ├── raw/              as collected, unmodified
│   ├── cleaned/          model-ready inputs
│   └── sources/          provenance; parameters.template.yaml
├── src/
│   ├── capacity_model.py     C_i, the capacity integral
│   ├── liquidity.py          price impact, P(q), realizable value
│   ├── control.py            control thresholds, K(q), founder dependence
│   ├── charity_efficiency.py the numerator: weighting and opportunity cost
│   ├── monte_carlo.py        sampling over theta
│   └── ranking.py            rates, rank intervals, pairwise probabilities
├── notebooks/
│   ├── exploratory_analysis.ipynb
│   ├── sensitivity_analysis.ipynb
│   └── results.ipynb
├── tests/
│   └── test_models.py
└── results/
    ├── rankings.csv
    └── confidence_intervals.csv
```

`src/`, `tests/`, `notebooks/`, and `results/` are scaffolding — the files exist but are empty. The methodology is written; the implementation is not.

## Methodology

**Denominator — capacity to give**

1. [Objective and core principle](methodology/model/01-objective-and-core-principle.md)
2. [Sustainable charitable capacity](methodology/model/02-sustainable-charitable-capacity.md)
3. [Public-market liquidity and price impact](methodology/model/03-public-market-liquidity.md)
4. [Control-safe wealth and control loss](methodology/model/04-control-and-ownership.md)
5. [Private-company wealth](methodology/model/05-private-company-wealth.md)
6. [Founder dependence and investor sentiment](methodology/model/06-founder-dependence-and-sentiment.md)
7. [Valuation risk](methodology/model/07-valuation-risk.md)

**Numerator — value relinquished**

8. [The charitable-giving numerator](methodology/model/08-giving-numerator.md)

**Estimation and results**

9. [Monte Carlo estimation](methodology/model/09-monte-carlo-estimation.md)
10. [The Adjusted Giving Rate](methodology/model/10-adjusted-giving-rate.md)
11. [Pairwise comparison and rank stability](methodology/model/11-comparisons-and-rank-stability.md)
12. [Sensitivity and robustness](methodology/model/12-sensitivity-and-robustness.md)
13. [Interpretation and empirical validation](methodology/model/13-interpretation-and-validation.md)

**Supporting**

- [Notation](methodology/notation.md) — symbol glossary
- [Data dictionary](methodology/data_dictionary.md) — the ~40–60 variables per individual
- [Assumptions](methodology/assumptions.md) — unresolved parameter-estimation problems

## Interpretation

The output is not a ranking of the most and least generous human beings. Generosity is a psychological and moral characteristic that cannot be observed from financial data. The model measures documented charitable giving relative to a probabilistic estimate of the wealth an individual could actually relinquish. See [methodology/model/13](methodology/model/13-interpretation-and-validation.md).

## Status

Specification only. No implementation, no dataset, no fitted parameters. See [methodology/assumptions.md](methodology/assumptions.md) for what has to be resolved before the model can be run.
