---
date created: Monday, May 16th 2022, 11:07:04 am
date modified: Friday, May 20th 2022, 11:27:33 am
---

# Week 11

## Standard Normal Distribution and Standard Normal Random Variable

Theorem:

1. If $X^d = N(\mu, \sigma^2)$ and $Z = (X - \mu) / \sigma$, then $Z^d = N(0, 1)$
2. If $Z^d = N(0, 1)$ and $X = \sigma Z + \mu$, then $X^d = N(\mu, \sigma^2)$.

Given a normal distribution $X^d = N(\mu, \sigma^2)$, $$\begin{align} P(a \le X \le b) = &P(\frac{a - \mu}{\sigma} \le \frac{X - \mu}{\sigma} \le \frac{b - \mu}{\sigma})\\ = &P(\frac{a - \mu}{\sigma} \le Z \le \frac{b - \mu}{\sigma})\\ = &\Phi(\frac{b - \mu}{\sigma}) - \Phi(\frac{a - \mu}{\sigma}) \end{align}$$

$\Phi$ is the cdf of standard normal distribution

Theorem: If $Z^d = N(0, 1)$ and $V = Z^2$, then $V^d = \chi^2(1)$.

## Random Functions Associated with Normal Distributions

Theorem (Distribution of normal sample mean): If $X_1, X_2, …, X_n$ is an i.i.d. random sample of size $n$ from the normal distribution $N(\mu, \sigma^2)$. Then the distribution of sample mean $\bar X = \frac 1 n \sum^n_{i = 1} X_i$ is $N(\mu, \frac{\sigma^2}{n})$.

## Central Limit Theorem

If $\bar X_n$ is the mean of a random sample $X_1, X_2, …, X_n$ of size $n$ from a distribution with a finite mean $\mu$ and a finite positive variance $\sigma^2$, then the distribution of $$W = \frac{\bar X_n - \mu}{\sigma / \sqrt n} = \frac{\sum^n_{i = 1}X_i - n\mu}{\sqrt n \sigma}$$ is $N(0, 1)$ in the limit as $n \to \infty$.
