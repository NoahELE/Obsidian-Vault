---
date created: Monday, May 2nd 2022, 11:09:05 am
date modified: Monday, May 9th 2022, 10:31:13 am
---

# Week 9

## Correlation and Independence

Two random variables X and Y are said to be uncorrelated if $\rho = Cov(X, Y) = 0$

## Conditional Distributions

Let $X, Y$ has a joint distribution on $S$. Let $f_1(x), f_2(y)$ be the marginal pmfs for $X, Y$. The conditional probability mass function (pmf) of $X$, given $Y = y$, is $$g(x | y) = \frac{f(x, y)}{f_2(y)}$$

If $X, Y$ are **independent**, then

- $g(x | y) = f_1(x)$ and $h(y | x) = f_2(y)$
- $E(u(X) | Y = y) = E(u(X))$ and $E(v(Y) | X = x) = E(v(Y))$

### Conditional Distributions for Continuous Random Variables

Let $X$ and $Y$ be 2 continuous random variables with joint pdf $f(x, y)$ and marginal pdf $f_1(x)$ and $f_2(y)$.

- $h(y|x) = \frac{f(x, y)}{f_1(x)}$, provided that $f_1(x) > 0$
- $H(y|x) = P(Y \le y | X = x) = \int^y_{-\infty} h(t|x) dt = \int^y_{-\infty} \frac{f(x, t)}{f_1(x)} dt$
- $\mu_{Y|x} = E(Y|x) = \int^\infty_{-\infty} y h(y|x) dy$
- $\sigma^2_{Y|x} = Var(Y|x) = \int^\infty_{-\infty} [y - E(Y|x)]^2 h(y|x) dy = E(Y^2|x) - E(Y|x)^2$

$E(X) = E(E(X|Y))$ and $E(Y) = E(E(Y|X))$

$Var(X) = Var(E(X|Y)) + E(Var(X|Y))$ and $Var(Y) = Var(E(Y|X)) + E(Var(Y|X))$

## Change-of-Variable Technique in Multivariate Transformation

Let $Y_1 = u_1(X_1, X_2), Y_2 = u_2(X_1, X_2)$, to find the joint pdf of $(Y_1, Y_2)$ from $(X_1, X_2)$

1. Find the inverse transformation: $x_1 = v_1(y_1, y_2), x_2 = v_2(y_1, y_2)$
2. Compute the Jacobian, which is the determinant, $$J = \begin{vmatrix} \frac{\partial x_1}{\partial y_1} & \frac{\partial x_1}{\partial y_2}\\ \frac{\partial x_2}{\partial y_1} & \frac{\partial x_2}{\partial y_2} \end{vmatrix} = \frac{\partial x_1}{\partial y_1} \cdot \frac{\partial x_2}{\partial y_2} - \frac{\partial x_1}{\partial y_2} \cdot \frac{\partial x_2}{\partial y_1}$$
3. Find the support of $(Y_1, Y_2)$ from $(X_1, X_2)$ under the transformation
4. The joint pdf is then $g(y_1, y_2) = |J| \cdot f(v_1(y_1, y_2), v_2(y_1, y_2)), (y_1, y_2) \in S$
