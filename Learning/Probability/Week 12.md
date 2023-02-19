---
date created: Monday, May 23rd 2022, 11:14:52 am
date modified: Friday, May 27th 2022, 11:47:26 am
---

# Week 12

## Normal Approximation for the Binomial Distribution

By CLT, $\frac{X - np}{\sqrt{np(1 - p)}}^d \approx N(0, 1)$, when $n$ is large enough.

Equivalently, $\frac{X}{n}^d \approx N(p, \frac{p(1 - p)}{n})$ and $X^d \approx N(np, np(1 - p))$.

In general, to approximate distribution:

- $P(X = k) = P(k - \frac 1 2 \le X \le k + \frac 1 2)$
- $P(a < k \le b) = P(a + \frac 1 2 \le X \le b + \frac 1 2)$
- $P(a \le k < b) = P(a - \frac 1 2 \le X \le b - \frac 1 2)$

## Normal Approximation for the Poisson Distribution

$\frac{X - \lambda}{\sqrt \lambda}^d \approx N(0, 1)$ or $X^d \approx N(\lambda, \lambda)$

## Normal Approximation for the Negative-binomial Distribution

$\frac{pX - r}{\sqrt{rq}} \approx N(0, 1)$ or $X^d \approx N(\frac r p, \frac{rq}{p^2})$

## Bivariate Normal Distribution

If $(X, Y)^d = BN(\mu_X, \mu_Y, \sigma_X^2, \sigma_Y^2, \rho)$, then

1. $X^d = N(\mu_X, \sigma_X^2)$
2. $Y^d = N(\mu_Y, \sigma_Y^2)$
3. $\rho$ is the correlation coefficient of $X$ and $Y$
4. $(X|Y = y)^d = N(\mu_X + \rho \frac{\sigma_X}{\sigma_Y} (y - \mu_Y), \sigma_X^2(1 - \rho^2))$
5. $(Y|X = x)^d = N(\mu_Y + \rho \frac{\sigma_Y}{\sigma_X} (x - \mu_X), \sigma_Y^2(1 - \rho^2))$

## Stochastic Process

A (discrete time) **stochastic processes** is a collection of r.v.’s $X_t \in T$.

E.g. $X_t$ could be

- the number of patients visiting a hospital on day $t$
- the ASX All Ords index value at time $t$
- the amount of rainfall in month $t$

**Markov Chain**: In a stochastic process $\{X_n\}^\infty_{n = 0}$, if for all $n \ge 0$ and $j_0, j_1, j_2, \dots, j_n, j_{n + 1} \in S$, $$P(X_{n + 1} = j_{n + 1} | X_0 = j_0, X_1 = j_1, \dots, X_n = j_n) = P(X_{n + 1} = j_{n + 1} | X_n = j_n)$$

For a homogeneous Markov chain, we define:

1. The m-step transition probability $P_{ij}^{(m)} = P(X_{n + m} = j | X_n = i)$
2. The one-step transition probability $P_{ij} = P_{ij}^{(1)} = P(X_{n + 1} = j | X_n = i)$
3. The m-step transition matrix $P^{(m)}$
4. The one-step transition matrix $P = P^{(1)}$

Theorem: $P^{(m)} = P^m$
