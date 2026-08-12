# 6. Founder Dependence and Investor Sentiment

## 6.1 Founder dependence

Some companies may derive part of their valuation from investor expectations surrounding a particular founder. Define

$$F_i = P\!\left(\text{material company impairment} \mid \text{founder relinquishes control}\right)$$

Expected company value conditional on founder ownership can then be modeled as

$$E[V \mid s] = P(S \mid s)\,V_S + P(F \mid s)\,V_F$$

where

- $S$ = successful continuation state
- $F$ = founder-disruption state
- $V_S$ = company value under successful continuation
- $V_F$ = company value under founder disruption

## 6.2 Endogeneity of company value

For example,

$$P(S \mid s = 51\%) = 0.90$$

may differ materially from

$$P(S \mid s = 20\%) = 0.65$$

The expected value of the company consequently becomes endogenous to the founder's remaining ownership:

$$E[V \mid s] = p(s)V_S + [1 - p(s)]V_F$$

This is the key structural point: for a founder-dependent company, the act of giving away shares changes the value of the shares given away. The denominator of the generosity ratio cannot be computed independently of the disposal path.

## 6.3 Smooth specification

A smooth specification could use a logistic function:

$$p(s) = \frac{1}{1 + \exp[-(a + bs)]}$$

The parameters $a$ and $b$ determine how strongly expected company performance depends on continued founder ownership. A company with $b \approx 0$ is founder-independent; large $b$ concentrates the transition in a narrow band of ownership.

Note that this smooth form and the step function $K(q)$ of [§4](04-control-and-ownership.md) capture different mechanisms — a legal-control discontinuity versus a gradual erosion of investor confidence — and are intended to coexist rather than substitute for one another.

## 6.4 Investor-sentiment effects

A founder selling or relinquishing a large ownership position may itself transmit information to investors. Define the sentiment effect as

$$S(q) = \exp(-\eta q)$$

where $\eta$ is investor-sentiment sensitivity.

A more complete marginal-price equation becomes

$$P(q) = P_0 \exp\!\left(-\lambda \frac{q}{ADV}\right) \exp(-\eta q)\, K(q)$$

and the realizable value becomes

$$V(Q) = \int_0^Q P(q)\, dq$$

## 6.5 Estimating $\eta$

The parameter $\eta$ can potentially be estimated using

- historical founder-sale announcements
- insider transactions
- ownership reductions
- executive departures
- event-study abnormal returns

The identification problem is real: $\lambda$ and $\eta$ both depress price with cumulative quantity and are not separately identified from disposal data alone. Event studies around *announced* sales that have not yet executed isolate the sentiment channel, since the mechanical impact channel has not yet operated. Where separation is not achievable, the two should be treated as jointly distributed in $\boldsymbol{\theta}$ rather than independently drawn.
