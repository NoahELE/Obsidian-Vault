---
date created: Monday, March 14th 2022, 11:04:38 am
date modified: Friday, April 8th 2022, 11:59:36 am
---

# Week 3

Definition: Given a random experiment with an outcome space $S$, a function X that assigns to each element $s$ in $S$ a real number $X(s) = x$ is called a **random variable** (abbr. r.v.). The range (or space) of X is the set of real numbers$\{x: X(s) = x, s \in S\}$

The range of X is often denoted as $X(S)$ or $S_X$

$$1 = P_X(S_X) = P_X(X(S))$$

We often write $f(x) = P_X({x}) = P(X=x)$ for any $x \in S_X$; and call $f(x)$ the pmf (probability mass function) of $X$.

Definition: The pmf $f(x)$ of a discrete random variable $X$ is a function that satisfies the following properties:

1. $f(x) > 0$ for any $x \in S_X$
2. $\sum _{x \in S_X} f(x) = 1$
3. $P_X(A) = P(X \in A) = \sum _{x \in A} f(x)$ for any $A \subset S_X$

- $P(X = x) = 0$ if $x \notin S_X$, therefore we define $f(x) = 0$ if $x \notin S_X$
- If pmf is constant over $S_X$, we say that $X$ has **uniform distribution**, or $f(x)$ is a **uniform pmf**.
- The pmf can be expressed in different ways, such as a mathematics formula, or a table, or a bar graph or a probability histogram.

Definition: Suppose $f(x)$ is the pmf of a discrete random variable $X$ with range $S_X$, and $u(x)$ is also a function on $X$, $\sum _{x \in S_X} u(x)f(x)$ is called the **mathematical expectation** of function $u(x)$, denoted by $E(u(X))$.

When it exists, the mathematical expectation E satisfies the following properties:

- if $c$ is a constant, $E(c) = c$
- if $c$ is a constant and $u$ is a function, $E(cu(X)) = cE(u(X))$
- if $c_1$ and $c_2$ are constants and $u_1$ and $u_2$ are functions, then $E(c_1 u_1(X) + c_2 u_2(X)) = c_1 E(u_1(X)) + c_2 E(u_2(X))$
- Generalising: $E(\sum _{i = 1} ^k c_i u_i(X)) = \sum_{i = 1} ^k c_i E(u_i(X))$

- we also call $E(X)$ the **mean** of the random variable X; and also denote $E(X)$ by a Greek letter $\mu$.
- a third name for $E(X)$ is the **first moment** of $X$
- we call $E(X^2)$ the **second moment** of X; $E(X^k)$ the k-th moment of $X$
- $E((X - \mu)^k)$ is called the **k-th moment of X about the mean**
- we call $E((X - \mu)^2)$ the **variance** of X, denoted as $\sigma^2$ or $Var(X)$
- $\sigma = \sqrt{E((X - \mu)^2)}$ is the **standard deviation** of X
- $\sigma^2 = Var(X) = E((X - \mu)^2) = E(X^2) - \mu^2 = E(X^2) - (E(X))^2$

## Hypergeometric Distribution

Hypergeometric distribution $Hyper(N_1, N_2, n)$, pmf:

$$f(x) = P(X = x) = \frac{\binom{N_1}{x} \binom{N_2}{n - x}}{\binom{N}{n}} = \frac{\binom{N_1}{x} \binom{N_2}{n - x}}{\binom{N_1 + N_2}{n}}$$

- $\mu = E(X) = n(\frac{N_1}{N})$
- $\sigma^2 = Var(X) = n(\frac{N_1}{N})(\frac{N_2}{N})(\frac{N - n}{N - 1})$

## Bernoulli Trials

Some random experiments having the following properties are called **Binomial experiment**

1. Each such experiment consists of n trials, with n being fixed in advance.
2. Each of the n trials has only two possible outcomes which are denoted by 'success' (S) and 'failure' (F). A trial of this type is called a **Bernoulli trial**.
3. The n trials are independent of each other. That is, outcome on one trial does not affect the probability of occurrence of the outcome of other trials.
4. The probability of ‘success’ (denoted by p) is the same for all the n trials.

Let $X_i$ be a random variable associated with the i-th Bernoulli trial, which is defined as $X_i(success) = 1, X_i(failure) = 0$. $X_i$ is called a **Bernoulli random variable**.

- pmf: $f(x_i) = p^{x_i}(1 - p)^{1x_i}$
- $\mu_i = E(X_i) = p$
- $\sigma^2_i = Var(X_i) = p(1 - p)$
