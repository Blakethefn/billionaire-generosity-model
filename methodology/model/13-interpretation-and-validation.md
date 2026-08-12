# 13. Interpretation and Empirical Validation

## 13.1 What the model does not measure

The final ranking should not be described as an objective ranking of the "most generous" and "least generous" human beings.

Generosity is a psychological and moral characteristic that cannot be directly observed from financial data.

## 13.2 What the model does measure

$$\text{Adjusted Giving Rate} = \frac{\text{Documented Economic Value Relinquished to Charity}}{\text{Estimated Sustainable Economic Capacity to Give}}$$

The correct interpretation is:

> The Adjusted Giving Rate measures documented charitable giving relative to a probabilistic estimate of the economic wealth an individual could relinquish after accounting for liquidity, market impact, ownership concentration, control, founder dependence, private-market discounts, investor sentiment, and uncertainty.

Two further limits follow from the word *documented*. The model measures what is on the record; undisclosed giving is invisible to it, and disclosure practices differ systematically by jurisdiction and by individual. And it measures value relinquished, not good accomplished — a dollar to an effective program and a dollar to an ineffective one enter identically.

## 13.3 Parameter standard

To make the resulting ranking difficult to reject on methodological grounds, every uncertain parameter should satisfy at least one of the following conditions:

1. **Directly observable**, or
2. **Empirically estimated**, or
3. **Represented by a probability distribution and subjected to sensitivity analysis.**

**No important parameter should depend solely upon an arbitrary point estimate.**

This is the test to apply to each new parameter before it enters the model. A parameter that fails all three conditions should either be removed or elevated to a distribution wide enough to reflect genuine ignorance.

## 13.4 Form of the strongest conclusion

The strongest conclusion is not

> "Individual $i$ is the 93rd most generous billionaire."

Instead, it is a probabilistic statement such as

$$P(R_i \geq 90) = 0.96$$

This means that under 96% of reasonable simulated economic conditions and parameter combinations, individual $i$ remains within the bottom ten members of the sample according to the Adjusted Giving Rate.

Such a result distinguishes uncertainty in wealth valuation from uncertainty in the ultimate conclusion, and provides a substantially more defensible basis for comparing charitable giving among the world's wealthiest individuals.

## 13.5 Validation checklist

Before publishing any result:

- [ ] Every parameter meets one of the three conditions in §13.3
- [ ] Both nominal and opportunity-cost-adjusted rates reported ([§8](08-giving-numerator.md))
- [ ] Both $G^{\text{legal}}$ and $G^{\text{distributed}}$ reported ([§8.2](08-giving-numerator.md))
- [ ] Common random numbers used across individuals ([§9.5](09-monte-carlo-estimation.md))
- [ ] Ratio percentiles computed per draw, not from expectations ([§10.3](10-adjusted-giving-rate.md))
- [ ] Rank intervals reported alongside median ranks ([§11.2](11-comparisons-and-rank-stability.md))
- [ ] Elasticities reported per individual ([§12.2](12-sensitivity-and-robustness.md))
- [ ] Headline claims survive adversarial parameter selection ([§12.4](12-sensitivity-and-robustness.md))
- [ ] No claim stated as an ordinal rank without a probability attached
