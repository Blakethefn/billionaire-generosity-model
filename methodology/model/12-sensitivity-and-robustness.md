# 12. Sensitivity and Robustness

## 12.1 Sensitivity analysis

The robustness of the ranking should be evaluated through sensitivity analysis. For an Adjusted Giving Rate

$$G = G\!\left(\lambda,\ D_M,\ F,\ r,\ \eta,\ \delta_c,\ \ldots\right)$$

calculate partial derivatives such as

$$\frac{\partial G}{\partial \lambda}, \qquad \frac{\partial G}{\partial D_M}, \qquad \frac{\partial G}{\partial F}, \qquad \frac{\partial G}{\partial r}, \qquad \frac{\partial G}{\partial \eta}, \qquad \frac{\partial G}{\partial \delta_c}$$

## 12.2 Elasticity

A normalized elasticity is more useful than a raw derivative:

$$\varepsilon_{G,x} = \frac{\partial G}{\partial x} \cdot \frac{x}{G}$$

This measures the percentage change in the generosity score resulting from a 1% change in parameter $x$. Because it is unitless, elasticities are comparable across parameters measured in different units, which raw partials are not.

Elasticities should be reported per individual, not only in aggregate. A parameter that barely moves the median individual may dominate the result for a founder-dependent case.

## 12.3 Robustness criterion

Suppose individual $i$ ranks near the bottom of the sample. A strong conclusion requires the ranking to remain relatively stable across reasonable parameter assumptions.

Define

$$P(R_i \geq r^{*})$$

as the probability that individual $i$ remains below some ranking threshold $r^{*}$.

For a sample of the 100 wealthiest individuals,

$$P(R_i \geq 90) = 0.96$$

would mean that the individual appears among the bottom ten Adjusted Giving Rates in 96% of simulations.

That is considerably stronger evidence than simply assigning the individual rank 97 using one set of assumptions.

## 12.4 Adversarial parameter selection

Sensitivity analysis over a stipulated distribution answers "what if the parameters are drawn as I assumed?" A stronger test asks whether a *hostile* analyst could overturn the conclusion by choosing parameters within a defensible range.

For each headline claim, search for the parameter combination most favorable to the individual — the smallest $\lambda$, the smallest $\delta_c$, the largest $\alpha, \beta, \gamma$, the most generous $r$ convention, each held within its empirically supportable interval — and check whether the conclusion survives.

A conclusion that survives adversarial selection is far harder to dismiss than one that merely holds on average. A conclusion that does not survive should be reported as conditional on the parameter assumptions that produce it, with those assumptions named explicitly.
