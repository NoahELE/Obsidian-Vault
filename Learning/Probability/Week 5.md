---
date created: Monday, March 28th 2022, 10:08:19 am
date modified: Friday, April 8th 2022, 4:10:33 pm
---

# Week 5

## The Poisson Distribution

Definition: Let the number of changes that occur in a given _continuous interval_ be counted. We have a Poisson process with parameter $\lambda > 0$ if the following are satisfied,

- The numbers of changes occurring in non-overlapping intervals are independent.
- The probability of exactly one change in a short interval of length $h$ is approximately $\lambda h$
- The probability of two or more changes in a short interval of length $h$ is much smaller than $h$.

Let $\lambda$ denote the number of changes in unit interval:

- $$P(X = x) \approx \binom{n}{x} (\frac{\lambda}{n})^x (1 - \frac{\lambda}{n})^{n - x}$$
- If n increases without bound, we have $$P(X = x) = \lim_{n \rightarrow \infty} \frac{n!}{x!(n - x)!} (\frac{\lambda}{n})^x (1 - \frac{\lambda}{n})^{n - x} = \frac{\lambda^x e^{-\lambda}}{x!}$$

---

We say X has a **Poisson distribution** $Poi(\lambda)$, if $X$ has the pmf $f(x) = \frac{\lambda^x e^{-\lambda}}{x!}$

The mgf of $X$ can be found to be $M(t) = E(e^{tX}) = \sum^\infty_{x = 0} e^{tx} \frac{\lambda^x e^{-\lambda}}{x!} = e^{-\lambda} \sum^\infty_{x = 0} \frac{(\lambda e^t)^x}{x!} = e^{-\lambda}e^{\lambda e^t} = e^{\lambda(e^t - 1)}$

- $\mu = E(X) = M'(0) = \lambda$
- $\sigma^2 = Var(X) = E(X^2) - E(X)^2 = \lambda$

Calculate Poisson Probability Recursively:

$$P(X = 0) = e^{-\lambda}$$
$$P(X = x) = \frac{\lambda}{x} P(X = x - 1)$$

The binomial probability from $b(n, p)$ can be approximated by the respective Poisson probability from $Poi(np)$

## Continuous Random Variables

The probability density function (pdf) of a continuous r.v. $X$ with space $S$ (or support $S$) is an integrable function $f(x)$ satisfying,

1. $f(x) > 0$ for $x \in S$
2. $\int_S f(x) dx = 1$

The distribution function (df) (or cumulative distribution function (cdf)) of a continuous r.v. $X$ is a continuous function $F(x)$ given by:$$F(X) = P(X \le x) = \int_{-\infty}^x f(t) dt$$
