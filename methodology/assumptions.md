# Open Questions

Unresolved problems standing between the specification and a runnable model. Roughly ordered by how much they affect the result.

## Identification

**$\lambda$ vs. $\eta$.** Both depress price with cumulative quantity and are not separately identified from disposal data alone ([§6.5](../docs/06-founder-dependence-and-sentiment.md)). Announced-but-unexecuted sales isolate the sentiment channel in principle; whether enough such events exist per individual is an empirical question. Fallback: treat as jointly distributed with an assumed correlation, and report sensitivity to that correlation.

**$s^{\min}$ is almost never observable.** Effective control is a function of voting structure, board composition, shareholder agreements, and the realistic behavior of other blockholders. For most individuals this will be a distribution informed by governance documents rather than an estimate.

**$q^{*}$ has no natural definition.** The point at which further disposal stops being economically meaningful is a modeling choice, and the capacity estimate is directly proportional to how generously it is set.

## Estimation

**$\lambda$ for positions that have never been traded at scale.** The market-impact literature is built on institutional trades orders of magnitude smaller than a founder's stake. Extrapolating a square-root or exponential impact law that far beyond its calibration range is the single least defensible step in the model.

**$\delta_c$ from control premiums.** Acquisition premiums bundle control value with synergy value and with the acquirer's overpayment. Isolating the control component requires assumptions about the other two.

**Private-company discounts for companies with no secondary market.** Where §5.2's evidence sources are all absent, $D_M$, $D_B$, and $D_I$ collapse to judgment. These cases should be flagged rather than silently filled in.

## Specification

**Choice of $r$.** ([§8.4](../docs/08-giving-numerator.md)) Compounding over four decades means the choice between a market return and an own-asset return can change early donations by an order of magnitude. Probably needs to be reported under multiple conventions rather than resolved.

**Weights $\alpha, \beta, \gamma$.** The two-measure approach ([§8.2](../docs/08-giving-numerator.md)) defers this rather than settling it. If both $G^{\text{legal}}$ and $G^{\text{distributed}}$ are reported, are the weighted $D^*$ and its parameters needed at all, or is $D^*$ redundant?

**Interaction of $K(q)$ and $p(s)$.** [§6.3](../docs/06-founder-dependence-and-sentiment.md) asserts these capture different mechanisms and should coexist. That is defensible but risks double-counting the same economic effect. Needs an explicit statement of what each includes and excludes.

**Real estate and "other" wealth** are in the dataset but have no treatment in the model. Either they need liquidity and marketability adjustments of their own, or they should be documented as entering at face value with the resulting bias acknowledged.

## Data

**Donation dating.** The opportunity-cost adjustment requires a dated series. Pledges, multi-year commitments, and in-kind stock gifts all complicate the date and the amount. Is the relevant date the pledge, the transfer, or the distribution?

**Disclosure asymmetry.** ([§13.2](../docs/13-interpretation-and-validation.md)) Individuals in jurisdictions with mandatory foundation reporting will appear more thoroughly documented than those without. Since the model measures *documented* giving, this is a systematic bias in favor of the less transparent — and it runs in the opposite direction from what most readers would assume.

**Sample definition.** Top 100 by headline net worth is the obvious frame, but headline net worth is precisely the measure the model rejects. Selecting the sample on it introduces a dependence worth thinking through.
