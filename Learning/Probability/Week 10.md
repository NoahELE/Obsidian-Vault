---
date created: Monday, May 9th 2022, 11:06:07 am
date modified: Friday, May 13th 2022, 11:56:09 am
---

# Week 10

## Several Independent Random Variables

## Distributions of Sums of Independent Random Variables

- sample mean, $\bar X = \frac{1}{n}(X_1 + X_2 + \dots + X_n)$
- sample variance, $S^2 = \frac{1}{n - 1} \sum^n_{i = 1}(X_i - \bar X)^2$
- order statistics

## Chebyshev’s Inequality

If the random variable $X$ has a mean $\mu$ and a variance $\sigma^2$, then for every $k \ge 1$, $$P(|X - \mu| \ge k\sigma) \le \frac{1}{k^2}$$

## The Normal Distribution

$$f(x) = \frac{1}{\sigma \sqrt{2 \pi}} exp(-\frac{(x - \mu)^2}{2 \sigma^2}), -\infty < x < \infty$$

Random variable with pdf like above is said to have normal distribution.

For a normal distribution $N(\mu, \sigma^2)$:

- $E(X) = \mu$
- $Var(X) = \sigma^2$
- mgf: $M(t) = e^{\mu t + \frac 1 2 \sigma^2 t^2}$

If a random variable $Z$ has normal distribution $N(0, 1)$, we say $Z$ is a **standard normal random variable**, and $N(0, 1)$ is the **standard normal distribution**.

- standard normal pdf: $\phi(z) = \frac{1}{\sqrt{2\pi}} e^{-\frac{z^2}{2}}$
- standard normal cdf: $\Phi(z) = P(Z \le z) = \int_{-\infty}^z \frac{1}{\sqrt{2\pi}} e^{-\frac{w^2}{2}} dw$
- standard normal mgf: $M(t) = e^{\frac{t^2}{2}}$
- $E(Z) = 0$
- $Var(Z) = 1$
