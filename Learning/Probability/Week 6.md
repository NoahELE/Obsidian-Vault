---
date created: Monday, April 4th 2022, 11:17:44 am
date modified: Friday, April 8th 2022, 4:17:41 pm
---

# Week 6

For continuous random variables:

- $\mu  = E(X) = \int^\infty_{-\infty} xf(x)dx$
- $\sigma^2 = Var(X) = E((X - \mu)^2) = \int^\infty_{-\infty} (x - \mu)^2f(x)dx$
- $E(X^k) = \int^\infty_{-\infty} x^kf(x)dx$
- mgf: $M(t) = E(e^{tX}) = \int^\infty_{-\infty} e^{tx} f(x)dx$
- percentile: a number $\pi_p$ such that $p = \int^{\pi_p}_{-\infty} xf(x)dx = F(\pi_p)$

## Uniform Distribution

Let $X$ be the outcome of selecting a point at random from an interval $[a, b]$, where any point in $[a, b]$ is equally likely to be selected.

- cdf: $F(x) = P(X \le x) = \begin{cases} 0, &x < a;\\ \frac{x - a}{b - a}, &a \le x < b;\\ 1, &x \ge b. \end{cases}$
- pdf: $f(x) = \frac{1}{b - a}, a\le x \le b$
- Such $X$ is said to have the **uniform** (or **rectangular**) distribution on $[a, b]$, and in that case we write $X^d = U(a, b)$.

- $\mu = E(X) = \frac{a + b}{2}$
- $\sigma^2 = Var(X) = \frac{(b - a)^2}{12}$
- mgf: $M(t) = \begin{cases} \frac{e^{tb} - e^{ta}}{t(b - a)}, &t \ne 0;\\ 1, &t = 0. \end{cases}$

> A special uniform distribution is that when $a = 0$ and $b = 1$, namely $U(0, 1)$, the **standard uniform distribution**.

## Exponential Distribution

[[Probability/Week 5#The Poisson Distribution]]

Consider a Poisson process introduced before where the number of changes occurring in a unit-length interval follows a Poisson distribution with parameter $\lambda$.

We are now interested in the waiting time $W$ until the first change occurs in observing the Poisson process.

- cdf: $F(w) = P(W \le w) = 1 - P(W > w) = 1 - P(no\ change\ in\ [0, w]) = 1 - e^{-\lambda w}$
- pdf: $f(w) = \lambda e^{-\lambda w}, w \ge 0$; or
    - $f(w) = \frac 1 \theta e^{-\frac w \theta}$ if we write $\lambda$ as $\frac 1 \theta$.

---

A random variable $X$ with pdf $f(x) = \frac{1}{\theta} e^{-\frac{x}{\theta}}, x \ge 0$ is said to have a **exponential distribution**. Denoted as $Exp(\theta)$

- $\mu = E(X) = \theta$
- $\sigma^2 = Var(X) = \theta^2$
- mgf: $M(t) = \frac{1}{1 - \theta t}, t < \frac{1}{\theta}$
- cdf: $F(x) = P(X \le x) = 1 - P(X > x) = 1 - e^{-\frac{w}{\theta}}$

> The exponential distribution has a **no-memory** property:
> $$P(X > x + y | X > x) = \frac{P(X > x + y)}{P(X > x)} = P(X > y)$$
> It is also the **only** continuous distribution having the no-memory property.

## Gamma Distribution

[[Probability/Week 5#The Poisson Distribution]]

Consider again a Poisson process with $\lambda$ being the rate of occurrence per unit time. We are now interested in $W$, the waiting time until the $\alpha$-th change occurs.

---

The important **Gamma Function** defined by $\Gamma(t) = \int^\infty_0 y^{t - 1} e^{-y} dy, t > 0$

$\Gamma(n) = (n - 1)!$ when $n$ is a positive integer. For this reason gamma function can also be called the **generalised factorial**

> $\Gamma(\frac 1 2) = \sqrt \pi$

---

Formally, a random variable X is said to have a **gamma distribution** with shape parameter $\alpha > 0$ and scale parameter $\theta > 0$ ($\theta = \frac 1 \lambda$, same as in exponential distribution), if the pdf of $X$ is: $$f(x) = \frac 1 {\Gamma(\alpha) \theta^\alpha} x^{\alpha - 1} e^{-\frac x \theta}$$

> When $\alpha$ is a positive integer, the gamma distribution's cdf can be evaluated using its relationship with Poisson process, $$\begin{align} F(x) &= P(X <= x)\\ &= 1 - P(X > x)\\ &=1 - P(fewer\ than\ \alpha\ changes\ in\ [0, x])\\ &= 1 - \sum^{\alpha - 1}_{k = 0} \frac{(\frac x \theta)^k e^{-\frac x \theta}}{k!} \end{align}$$

- mgf: $M(t) = \frac 1 {(1 - \theta t)^\alpha}, t < \frac 1 \theta$
- $\mu = E(X) = \alpha \theta$
- $\sigma^2 = Var(X) = \alpha \theta^2$
