---
date created: Monday, March 21st 2022, 10:14:37 am
date modified: Friday, April 8th 2022, 1:45:39 pm
---

# Week 4

## Binomial Distribution

[[Probability/Week 3#Bernoulli Trials]]

The pmf for a binomial distribution is

$$f(x) = P(X = x) = \binom{n}{x} p^x (1 - p)^{n - x}$$

We call the function defined by $F(x) = P(X < x)$ the **cumulative distribution function** (or simply the **distribution function**) of $X$, abbreviated as cdf or df of X.

For a random variable $X$ having a binomial distribution $b(n, p)$, the cdf is:

$$F(x) = P(X < x) = \sum^x_{k = 0} \binom{n}{k} p^k (1 - p)^{n - k}$$

> In particular, $F(n) = 1$

The mean, variance and standard deviation for a binomial distribution $b(n, p)$:

- $\mu_X = E(X) = np$
- $\sigma_X^2 = Var(x) = np(1 - p)$

## The Moment-Generating Function

Let $X$ be a discrete random variable with pmf $f(x)$ and range (or space) $S$. If there is a positive number $h$ such that $$E(e^{tX}) = \sum_{x \in S}e^{tx}f(x)$$ is finite for $t = \pm h$ (and hence for $–h < t < h$), then the function of $t$ defined by $$M(t) = E(e^{tX})$$ is called the **moment-generating function** (mgf) of X (or of the distribution of X).

How the mgf and moments are related:

- $M(t) = \sum_{x \in S}e^{tx}f(x)$
- $M'(t) = \sum_{x \in S}xe^{tx}f(x)$, so $M'(0) = \sum_{x \in S} x \cdot e^{0 \cdot x}f(x) = E(X)$
- $M''(t) = \sum_{x \in S}x^2e^{tx}f(x)$, so $M''(0) = \sum_{x \in S} x^2 \cdot e^{0 \cdot x}f(x) = E(X^2)$
- In general, the r-th derivative of M is $M^{(r)}(t) = \sum_{x \in S}x^r e^{tx}f(x)$, so $M^{(r)}(0) = \sum_{x \in S} x^r \cdot e^{0 \cdot x}f(x) = E(X^r)$
- In particular, $\mu = M'(0)$ and $\sigma^2 = M''(0) - [M'(0)]^2$

The mgf of the **binomial distribution** is:

$$M(t) = \sum_{x \in S} e^{tx} \binom{n}{x} p^x (1 - p)^{n - x} = (pe^t + 1 - p)^n$$

> When $n = 1$, the above $M(t) = pe^t + 1 - p$ is the mgf of Bernoulli distribution.

## Negative Binomial Distribution

[[#Binomial Distribution]]

Let the r.v. $X$ be the number of trials needed to obtain $r$ successes,

- The pmf of $X$ is $$f(x) = \binom{x - 1}{r - 1}p^r(1 - p)^{x - r} = \binom{x - 1}{r - 1}p^rq^{x - r}, x = r, r + 1, r + 2, …$$
- We say that X has a **negative binomial distribution**, i.e. $X^d = NB(r, p)$
- The pmf is similar to each term in the Maclaurin’s series expansion of the binomial function $1 - w$ to the negative exponent $–r$, that is $h(w) = (1 - w)^{-r} = \sum^\infty_{k = 0}\frac{h^{(k)}(0)}{k!}w^k = \sum^\infty_{x = r}\binom{x - 1}{r - 1}w^{x - r}$
- Thus, $\sum^\infty_{x = r}f(x) = p^r\sum^\infty_{x = r}\binom{x - 1}{r - 1}q^{x - r} = p^r(1 - q)^{-r} = 1$
- mgf, $M(t) = (\frac{pe^t}{1 - (1 - p)e^t})^r$
- mean and variance,
    - $\mu = \frac{r}{p}$
    - $\frac{r(1 - p)}{p^2}$

## Geometric Distribution

[[#Negative Binomial Distribution]]

Consider a special case of negative binomial distribution where we are interested in the trial number $X$ at which the first success is observed.

- We know $X^d = NB(1, p)$, and say $X$ has a **geometric distribution**, $X^d = Geo(p)$
- The pmf is $$f(x) = p(1 - p)^{x - 1} = pq^{x - 1}, x = 1, 2, 3, …$$
- Note that for a geometric series, $\sum^\infty_{k = 1}as^{k - 1} = \frac{a}{1 - s}$, when $|s| < 1$
- The mgf is $$M(t) = E(e^{tX}) = \frac{pe^t}{1 - (1 - p)e^t} = \frac{pe^t}{1 - qe^t}$$
- $\mu = E(X) = \frac{1}{p}$ and,
- $\sigma^2 = Var(X) = \frac{1 - p}{p^2} = \frac{q}{p^2}$

- A special property of the geometric distribution is,
    - $P(X > k) = (1 - p)^k = q^k$
    - $P(X \le k) = 1 - P(X > k) = 1 - (1 - p)^k = 1 - q^k$
- **Loss of Memory**, for any integers $m, k \ge 0$, $P(X > m + k | X > m) = \frac{P(X > m + k)}{P(X > m)} = \frac{q^{m + k}}{q^m} = q^k = P(X > k)$

> If the Maclaurin’s series expansion for a mgf $M(t)$ exists, then $$\begin{align} M(t) &= M(0) + M'(0)\frac{t}{1!} + M''(0)\frac{t^2}{2!} + M'''(0)\frac{t^3}{3!} + …\\ &= 1 + E(X)\frac{t}{1!} + E(X^2)\frac{t^2}{2!} + E(X^3)\frac{t^3}{3!} + … \end{align}$$
