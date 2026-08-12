# 4. Control-Safe Wealth and Discontinuous Control Loss

Ownership can possess economic value beyond the proportional value of the shares themselves.

## 4.1 Control-safe ownership

Let

- $s_i$ = current ownership percentage
- $s_i^{\min}$ = minimum ownership necessary to preserve effective control

The maximum control-safe ownership percentage that can be relinquished is

$$s_i^{\text{safe}} = \max\left(0,\ s_i - s_i^{\min}\right)$$

For a company with equity value $V$, an elementary control-safe wealth estimate is therefore

$$W_i^{\text{control-safe}} = V \max\left(0,\ s_i - s_i^{\min}\right)$$

## 4.2 Worked example

Suppose an individual owns $s_i = 51\%$ of a company worth $V = \$1$ trillion, while effective control requires $s_i^{\min} = 40\%$.

Headline wealth associated with the position is

$$0.51 \times \$1\text{T} = \$510\text{B}$$

Control-safe ownership is only

$$51\% - 40\% = 11\%$$

Therefore

$$W_i^{\text{control-safe}} = 0.11 \times \$1\text{T} = \$110\text{B}$$

This does not imply that the remaining $400 billion is fictitious. It distinguishes between **ownership wealth** and **freely disposable wealth that can be relinquished without crossing the assumed control threshold**.

## 4.3 Discontinuous control loss

Crossing a control threshold may create a discontinuous change in value. Define

$$K(q) = \begin{cases} 1, & s(q) > s_{\text{control}} \\[6pt] 1 - \delta_c, & s(q) \leq s_{\text{control}} \end{cases}$$

where $s(q)$ is remaining ownership after relinquishing $q$, and $\delta_c$ is the estimated economic penalty associated with loss of control.

Because $K(q)$ is a step function, the capacity integral of [§2](02-sustainable-charitable-capacity.md) is naturally evaluated piecewise: once over $q$ values that leave control intact, once over those that do not.

## 4.4 Estimating $\delta_c$

The parameter $\delta_c$ should not be arbitrarily selected. It should be estimated using observable evidence such as

$$\delta_c = f\!\left(\text{voting rights},\ \text{shareholder agreements},\ \text{board structure},\ \text{control premiums},\ \text{comparable transactions},\ \text{historical event studies}\right)$$

Control premiums observed in acquisitions provide the most direct evidence: the premium paid to acquire control is an upper-bound estimate of the value that evaporates when control is surrendered without compensation.

## 4.5 Relationship between $s^{\min}$ and $s_{\text{control}}$

$s_i^{\min}$ (§4.1) and $s_{\text{control}}$ (§4.3) describe the same threshold from two directions. §4.1 treats it as a hard stop — nothing below it is disposable. §4.3 treats it as a priced discontinuity — disposal below it is possible but the retained position is worth $(1-\delta_c)$ of its prior value.

The second formulation is the general one; the first is its special case at $\delta_c \to 1$. Dual-class share structures matter here: an individual may hold well under half the economic shares while retaining unambiguous voting control, in which case $s^{\min}$ measured against economic ownership is low and $\delta_c$ binds only at the voting threshold.
