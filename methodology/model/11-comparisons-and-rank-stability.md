# 11. Pairwise Comparison and Rank Stability

## 11.1 Probability that one individual is more generous than another

The Monte Carlo simulations can estimate the probability that individual $i$ has a greater Adjusted Giving Rate than individual $j$:

$$P(G_i > G_j) \approx \frac{1}{N}\sum_{k=1}^{N} \mathbf{1}\!\left(G_i^{(k)} > G_j^{(k)}\right)$$

where $\mathbf{1}(\cdot)$ is the indicator function.

If

$$P(G_i > G_j) = 0.97$$

there is strong model-based evidence that $i$'s adjusted giving rate exceeds $j$'s.

If

$$P(G_i > G_j) = 0.53$$

the available evidence does not justify confidently ranking the two individuals.

This comparison is only valid under the common-random-numbers requirement of [§9.5](09-monte-carlo-estimation.md): $G_i^{(k)}$ and $G_j^{(k)}$ must be evaluated under the same simulated state of the world.

## 11.2 Rank stability

For each Monte Carlo simulation, rank all $N_B$ individuals:

$$R_i^{(k)} = \operatorname{rank}\!\left(G_i^{(k)}\right)$$

Then estimate the expected rank:

$$E[R_i] = \frac{1}{N}\sum_{k=1}^{N} R_i^{(k)}$$

A rank interval can also be reported:

$$R_i^{5\%}, \qquad R_i^{50\%}, \qquad R_i^{95\%}$$

An individual might therefore be reported as

$$R_i^{50\%} = 63$$

with

$$R_i \in [57, 69]$$

in 90% of simulations.

This is more informative than reporting a single ordinal ranking.

## 11.3 Why rank intervals matter more than ranks

In the dense middle of the distribution, adjacent individuals will have heavily overlapping $G$ distributions and their rank intervals will be correspondingly wide — an individual whose median rank is 63 may plausibly occupy anything from 45 to 80. Reporting the point rank alone would imply a precision the data cannot support.

At the extremes the opposite holds: individuals at the top and bottom tend to have tight rank intervals, because their $G$ distributions barely overlap with anyone's. **The model's defensible claims live at the tails.** This is the basis of the robustness criterion in [§12](12-sensitivity-and-robustness.md).
