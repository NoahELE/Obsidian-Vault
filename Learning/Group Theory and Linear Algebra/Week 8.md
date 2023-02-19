---
date created: Monday, September 12th 2022, 9:15:46 am
date modified: Monday, September 19th 2022, 9:20:00 am
---

# Week 8

## Conditions on Orders of Elements and Subgroups

Theorem (Lagrange): Let $G$ be a finite group,

1. if $H$ is a subgroup of $G$, then $\#H | \#G$
2. if $g \in G$, then $o(g) | \#G$

> $[G:H] = \frac{\#G}{\#H}$

Theorem (Fermat’s little theorem): Let $p$ be a prime, if $a \in \mathbb Z$ is not divisible by $p$, then $a^{p - 1} \equiv 1 \pmod p$.

Theorem: Let $p$ be prime. Every group of order $p$ is cyclic, hence isomorphic to $\mathbb Z / p \mathbb Z$.

Theorem (Euler): Let $m = pq$, where $p \ne q$ are prime. If $N \equiv 1 \pmod{(p - 1)(q - 1)}$, then $a^N \equiv a \pmod m$ for all $a \in \mathbb Z$.

## Inner Products

From now on, $K$ will denote either $\mathbb R$ or $\mathbb C$. These fields are endowed with

- the absolute value function $|\cdot|: K \to \mathbb R_{\ge 0}, a \mapsto |a|$;
- the conjugate function $\overline \cdot :K \to K, a \mapsto \overline a$. (the conjugate is just the identity function when $K = \mathbb R$.)

An inner product on a $K$-vector space $V$ is a function,

$$
\begin{align}
(\cdot, \cdot): & V \times V \to K \\
& v, w \mapsto (v, w)
\end{align}
$$

such that,

- $(v, w) = \overline{(w, v)}$ for all $v, w \in V$;
- $(au + bv, w) = a(u, w) + b(v, w)$;
- $(v, v) \in R_{\ge 0}$ for all $v \in V$ and $(v, v) = 0$ if and only if $v = 0$.

---

Let $V$ be a inner product space, we define:

- $||v|| = \sqrt{(v, v)}$ be the *length* of $v \in V$;
- $v \bot w$ ($v$ and $w$ are *orthogonal*) if $(v, w) = 0$;
- if $W$ is a subspace of $V$, the *orthogonal complement* of $W$ in $V$ is $W^\bot = \{v \in V \mid (v, w) = 0\}$;
- a subset $S \subset V$ is *orthonormal* if for all $v, w \in S$, we have $(v, w) = 0$ if $v \ne w$ and $(v, w) = 1$ if $v = w$;
- a *distance* function $\delta(v, w) = ||v - w||$;
- if $V$ is a real inner product space and $v, w \in V \setminus \{0\}$, the *angle* $\theta$ between $v$ and $w$ is defined by $cos \theta = \frac{(v, w)}{||v|| ||w||}$.
