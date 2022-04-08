---
date created: Tuesday, April 5th 2022, 7:55:31 am
date modified: Friday, April 8th 2022, 3:43:17 pm
---

# Week 6

## Correlation

Correlation is used to detect pairs of variables that might have some relationship and how strong is the relationship.

## Pearson Correlation

Pearson Correlation $r_{xy} \in [-1, 1]$:

- 1 for perfect linear correlation;
- -1 for perfect negative correlation;
- 0 means no correlation;
- $|r_{xy}|$ stands for the strength of correlation.

Formula:

$$r_{xy} = \frac{\sum^n_{i = 1}(x_i - \bar x)(y_i - \bar y)}{\sqrt{(\sum^n_{i = 1}(x_i - \bar x)^2) \times (\sum^n_{i = 1}(y_i - \bar y)^2)}}$$

> It assumes the data has a normal distribution.

## Entropy

- more uncertain, less predictable &rarr; high entropy
- less uncertain, more predictable &rarr; low entropy

Entropy formula:

$$H(X) = -\sum^k_{i = 1} p_i log_2 p_i$$

> $p_i$ is the proportion of points in the i-th category.

Need Discretization:

- equal-width bins
- equal-frequency bins
- manual split bins

Conditional Entropy:

$$H(Y|X) = \sum_{x \in X} p(x)H(Y|X = x)$$

## Mutual Information

Mutual Information $MI(X, Y)$:

$$MI(X, Y) = H(Y) - H(Y|X) = H(X) - H(X|Y)$$

- large: high correlation
- small: low correlation

> $0 \le MI(X, Y) \le \infty$

Normalised Mutual Information $NMI(X, Y)$:

- $NMI(X, y) = \frac{MI(X, Y)}{min(H(X), H(Y))}$
- $NMI(X, y) = \frac{MI(X, Y)}{max(H(X), H(Y))}$
- $NMI(X, y) = \frac{MI(X, Y)}{mean(H(X), H(Y))}$

> - Advantage:
>     - can detect both linear and non-linear dependencies
>     - effective with discrete features (unlike Pearson correlation)
> - Disadvantage:
>     - If feature is continuous, it needs to be discretised. Involve the choice of bins.
>     - Difference bin choices will lead to different estimations of mutual information.
