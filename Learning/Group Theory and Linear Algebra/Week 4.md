---
date created: Monday, August 15th 2022, 8:53:50 am
date modified: Wednesday, August 31st 2022, 4:52:35 pm
---

# Week 4

## Minimal Polynomial of a Linear Transformation

Let $f: V \to V$, $p(x) = a_k x^k + a_{k - 1} k^{k - 1} + \dots + a_1 x + a_0$.

We define a new linear transformation $p(f): V \to V$, $p(f) = a_k f^k + a_{k - 1} f^{k - 1} + \dots + a_1 f + a_0 \text{id}_V$.

Let the characteristic polynomial of $f$ or $A$ is $c(x) = \det (xI - A)$, its minimal polynomial $m(x)$ divides $c(x)$.

## Jordan Normal Form

Given $\lambda \in K$ and $k \in \mathbb N$, define the *Jordan block*:

$$

J_k(\lambda) = \begin{bmatrix}

\lambda & 1 & 0 & \cdots & 0 \\

0 & \lambda & 1 & \ddots & \vdots \\

0 & 0 & \ddots & \ddots & 0 \\

\vdots & \vdots & \ddots & \lambda & 1 \\

0 & 0 & \cdots & 0 & \lambda \\

\end{bmatrix}

$$

$$

JNF(f) = \begin{bmatrix}

A_1 & & \\

& \ddots & \\

& & A_k

\end{bmatrix}

$$

> each $A_i$ is a Jordan Block

## Computing the Jordan Normal Form

Let $f∶ V \to V$ be a linear transformation and let $λ \in K$ be an eigenvalue of $f$. Write

- $m(x) = (x - \lambda)^{e_m}p(x)$ where $(x - \lambda)$ does not divide $p(x)$
- $c(x) = (x - \lambda)^{e_c}q(x)$ where $(x - \lambda)$ does not divide $q(x)$

Then $e_m$ is the size of the largest Jordan block in $JNF(f; \lambda)$ and $e_c$ is the size of $JNF(f; \lambda)$, that is the sum of the sizes of all the Jordan blocks of the form $J_?(\lambda)$ in $JNF(f)$.

---

Let $f∶ V \to V$ be a linear transformation on a finite-dimensional vector space
$V$ over an algebraically closed field $K$. Given any eigenvalue $\lambda$ of $f$, the number of Jordan blocks of the form $J_?(\lambda)$ is equal to the dimension of the $\lambda$-eigenspace $V_\lambda$.