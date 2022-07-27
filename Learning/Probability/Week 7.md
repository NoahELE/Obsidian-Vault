---
date created: Monday, April 11th 2022, 11:07:13 am
date modified: Tuesday, May 10th 2022, 3:52:52 pm
---

# Week 7

## Chi-Square Distribution

[[Probability/Week 6#Gamma Distribution]]

a special Gamma distribution.

When $\theta = 2$ and $\alpha = \frac r 2$, the associated random variable $X$ has pdf $$f(x) = \frac{1}{\Gamma(\frac r 2) 2^{\frac r 2}} x^{\frac r 2 - 1} e^{-\frac x 2}$$

$X$ has a **chi-square distribution**, denoted by $X^d = \chi^2(r)$. $r$ is called the degrees of freedom.

- $\mu = E(X) = \alpha \theta = r$
- $\sigma^2 = Var(X) = \alpha \theta^2 = 2r$
- mgf: $M(t) = (1 - 2t)^{-\frac r 2}$

## Distributions of Functions of a Continuous Random Variable

- distribution function technique
    1. first finding the support of the new random variable $Y$,
    2. second finding the cdf, i.e. $G(Y) = P(Y \le y)$,
    3. and possibly third finding the derivative of the cdf to get the pdf.
- change-of-variable technique
    1. In general, if $Y = u(X)$ is a continuous monotonic function of $X$, we have $X = v(Y)$, then the pdf of $Y$ is $g(y) = f(v(y)) \cdot |v'(y)|$.

## Multivariate Distribution

### Joint Discrete Random Variables

joint pmf: $$f(x, y) = P(X = x, Y = y)$$

1. $0 \le f(x, y) \le 1$
2. $\mathop{\sum\sum}_{(x, y) \in S} f(x, y) = 1$
3. $P((X, Y) \in A) = \mathop{\sum\sum}_{(x, y) \in A} f(x, y)$, for any $a \subseteq S$

 joint cdf: $$F(x, y) = P(X \le x, Y \le y) = \mathop{\sum\sum}_{x \le x, t \le y} f(s, t)$$

pmf of $X$ alone is called marginal pmf of $X$; similarly pmf of $Y$ alone is called marginal pmf of $Y$.

$X, Y$ are said to be independent if and only if $P(X = x, Y = y) = P(X = x)P(Y = y)$. Otherwise, they are dependent.
