---
date created: Wednesday, April 27th 2022, 11:05:54 am
date modified: Tuesday, May 3rd 2022, 3:30:38 pm
---

# Week 8

## Joint pdf/cdf of Two Continuous Random Variables

joint **probability density function** (pdf):

1. $f(x, y) \ge 0$
2. $\int^\infty_{-\infty} \int^\infty_{-\infty} f(x, y) dxdy = 1$
3. $P((X, Y) \in A) = \mathop{\int\int}_A f(x, y) dxdy$

joint **cumulative distribution function** (cdf):

$$F(x, y) = P(X \le x, Y \le y) = \int^y_{-\infty} \int^x_{-\infty} f(s, t) dtds$$

**marginal pdf**:

- $f_1(x) = f_X(x) = \int^\infty_{-\infty} f(x, y) dy, x \in S_1$
- $f_2(y) = f_Y(y) = \int^\infty_{-\infty} f(x, y) dx, y \in S_2$

$X, Y$ are **independent** $\iff$ $f(x, y) = f_1(x)f_2(y)$ $\iff$ $F(x, y) = F_1(x)F_2(y)$

For any function $u(X_1, X_2)$, the **mathematical expectation** is

$$E(u(X_1, X_2)) = \int^\infty_{-\infty} \int^\infty_{-\infty} u(x_1, x_2) f(x_1, x_2) dx_1dx_2$$

## Trinomial Distribution

- Each trial has 3 possible outcomes: perfect, ‘seconds’ and defective, with $p_1, p_2, p_3$ as probabilities, $p_3 = 1 - p_1 - p_2$
- trinomial pmf: $$f(x_1, x_2) = P(X_1 = x_1, X_2 = x_2) = \binom{n}{x_1} \binom{n - x_1}{x_2} p_1^{x_1} p_2^{x_2} (1 - p_1 - p_2)^{n - x_1 - x_2}$$
- if $(X_1, X_2)$ has a trinomial distribution $(n, p_1, p_2)$, then $X_1^d = b(n, p_1), X_2^d = b(n, p_2)$

## Correlation Coefficient

- Write $u(X_1, X_2) = (X_1 - \mu_1)(X_2 - \mu_2)$ where $\mu_1 = E(X_1), \mu_2 = E(X_2)$. Then $$E(u(X_1, X_2)) = E((X_1 - \mu_1)(X_2 - \mu_2)) = \sigma_{12} = Cov(X_1, X_2)$$ is called the **covariance** of $X_1, X_2$.
- If standard deviations $\sigma_1, \sigma_2$ are positive then, $$\rho = \frac{Cov(X_1, X_2)}{\sigma_1 \sigma_2} = \frac{\sigma_{12}}{\sigma_1 \sigma_2}$$ is called the **correlation coefficient** of $X_1, X_2$.
- $Cov(X_1, X_2) = E(X_1 X_2) - \mu_1 \mu_2$.

---

- $E(a \cdot u_1(X, Y) + b \cdot u_2(X, Y) + c) = a \cdot E(u_1(X, Y)) + b \cdot E(u_2(X, Y)) + c$
- $Cov(X, Y) = E(XY) - \mu_X \mu_Y = E(XY) - E(X)E(Y)$
- $Cov(X, a) = E((X - \mu_X)(a - \mu_a)) = 0$
- $Cov(aX, bY) = abCov(X, Y)$
- $Cov(X + a, Y + b) = Cov(X, Y)$
- $Cov(X, aX + b) = aVar(X)$
- $Var(aX + bY) = a^2 Var(X) + 2abCov(X, Y) + b^2 Var(Y)$
