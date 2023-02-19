---
date created: Monday, August 8th 2022, 9:10:09 am
date modified: Monday, August 29th 2022, 11:01:17 am
---

# Week 3

## Transformation-Invariant Subspaces

Let $f: V \to V$, be a linear transformation, and let $W$ be a subspace of $V$. We say that $W$ is *$f$-invariant* if $f(w) \in W$ for all $w \in W$. In this case, $f$ can be restricted to $W$.

Given an eigenvalue $\lambda$ of $f$, the *generalised eigenspace* for $\lambda$ is $G_\lambda = \{v \in V \mid (f - \lambda \text{id}_V)^n (v) = 0 \text{ for some } n \in \mathbb N^+\}$

## Jordan Normal Form for Nilpotent Transformations

We say that a linear transformation $n: V \to V$ is *nilpotent* if there exists $e \in \mathbb N$ such that $n^e = 0$, in other words the linear transformation $n^e: V \to V$ satisfies $n^e(v) = 0$ for all $v \in V$.

---

We say that the vector space $V$ is *$f$-indecomposable* if

- $V \ne \{0\}$, and
- for any direct sum decomposition $V = W_1 \oplus W_2$, where both $W_1$ and $W_2$ are $f$-invariant, we must have $W_1 = 0$ or $W_2 = 0$.

---

If $n: V \to V$ is a *nilpotent* transformation on a k-dimensional vector space $V$ and $V$ is n-indecomposable, then there exists $v \in V$ such that $n^k(v) = 0$ and $B ∶= \{n^{k − 1}(v),n^{k − 2}(v), \dots,n(v),v\}$ is a basis of $V$ . (In particular, $n^k = 0$ and $n^k−1 \ne 0$.)
