---
date created: Monday, August 1st 2022, 9:09:20 am
date modified: Monday, August 29th 2022, 11:01:33 am
---

# Week 2

## Integers Modulo

The *congruence class* of $a$ modulo $m$ is $[a]_m = \{x \in \mathbb Z \mid x \equiv a \pmod m\}$

$[a]_m = [b]_m$ if and only if $a \equiv b \pmod m$.

$\mathbb Z / m \mathbb Z = \{[0]_m, [1]_m, [2]_m, \dots, [m - 1]_m\}$

- $[a]_m + [b]_m = [a + b]_m$
- $[a]_m[b]_m = [ab]_m$

The element $[a]_m$ is only *invertible* if and only if $\gcd(a, m) = 1$.

> [!NOTE]
> We say $[a]_m, [b]_m$ is invertible when $[a]_m[b]_m = [1]_m$

If $p$ is prime, then every non-zero element of $\mathbb Z/p \mathbb Z$ is invertible.

## Fields

A **ring** is a set $R$ with 2 operations (addition and multiplication) satisfying the following properties:

- $a + (b + c) = (a + b) + c$
- $a + b = b + a$
- $\exists 0 \in R$ such that $a + 0 = a$
- $\forall a \in R$, $\exists (-a) \in R$ such that $a + (-a) = 0$
- $a(bc) = (ab)c$
- $\exists 1 \in R$ such that $1 \cdot x = x \cdot 1 = x$
- $a(b + c) = ab + ac$

---

A **commutative ring** is a ring $R$ such that

- $ab = ba$

---

A **field** is a commutative ring $K$ such that

- $\forall a \in K \setminus \{0\}$, $\exists a^{-1} \in K$ such that $a \cdot a^{-1} = 1$

> $\mathbb F_p = \mathbb Z / p \mathbb Z = \{[0]_p, [1]_p, [2]_p, \dots, [p - 1]_p\}$ is a field for any prime $p$.

## Algebraic Closure

A field $K$ is *algebraically closed* if any nonconstant polynomial with coefficients in $K$ has a root in $K$.

**Fundamental Theorem of Algebra**. The field $\mathbb C$ is algebraically closed.

Any field $K$ lies inside an (essentially unique) algebraic closure $\bar K$.

## Eigen Things and Jordan Normal Form

We say that two $n \times n$ matrices $A$ and $B$ are similar (and we write $A \sim B$) if there exists a invertible $n \times n$ matrix $P$ such that $B = PAP^{-1}$

## Complement and Direct Sum

Let $W_1$ be a subspace of a vector space $V$ . A *complement* of $W_1$ is a subspace $W_2$ of $V$ such that

1. $W_1 \cap W_2 = \{0\}$
2. $W_1 + W_2 = V$, where $W_1 + W_2 = \{w_1 + w_2 \mid w_1 \in W_1, w_2 \in W_2\}$

In this case, we write $V = W_1 \oplus W_2$ and say $V$ is the *direct sum* of $W_1$ and $W_2$.
