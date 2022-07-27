---
date created: Monday, April 11th 2022, 6:45:15 pm
date modified: Sunday, June 5th 2022, 10:59:03 am
---

# Week 7

## Supervised Learning

- classification (discrete variable)
- regression (continuous variable)

## Regression

Simple Linear Regression Model: $$Y_i=\underbrace{\beta_0 + \beta_1 X_i}_{linear\ component} + \underbrace{\epsilon_i}_{error\ component}$$

- SST: $\sum (Y_i - \bar Y)^2$
- SSE: $\sum (Y_i- \hat Y_i)^2$
- SSR: $\sum (\hat Y_i - \bar Y)^2$

Coefficient of Determination: $r^2 = \frac{SSR}{SST}$

> $0 < r^2 < 1$

Residual of an observation $e_i$ is $e_i = Y_i - \hat Y$

## Decision Tree

Stop splitting when:

1. all records are in the same classification
2. there are no records

- Advantages
    - Easy to interpret
    - Relatively efficient to construct
    - Fast for deciding about a test instance
- Disadvantages
    - A simple greedy construction strategy, producing a set of if-then rules. Sometimes this is too simple for data with complex structure:
        - Everything should be as simple as possible, but not simpler
    - For complex datasets, the tree might grow very big and difficult to understand

## K-Nearest Neighbors

- Compute distance between 2 data points:
    - Euclidean Distance
    - Pearson Correlation
- Determine the nearest neighbor

If k is too small, it is sensible to noise points.

If k is too large, the neighborhood may include points from other class.
