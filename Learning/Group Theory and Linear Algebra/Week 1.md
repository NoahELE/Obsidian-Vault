---
date created: Monday, July 25th 2022, 9:10:17 am
date modified: Friday, November 4th 2022, 11:27:16 am
---

# Week 1

## Division Algorithm

If $a \in \mathbb Z$ and $d \in \mathbb N$, there exists unique integers $q$ and $r$ such that $a = qd + r$ and $0 \le r < d$

When $r = 0$, so $a = qd$, we say that $d$ *divides* $a$, and write $d \mid a$.

1. If $a \mid b$ and $b \mid c$ then $a \mid c$
2. If $a \mid b$ and $a \mid c$ then $a \mid xb + yc$ for all $x, y \in \mathbb Z$

The **greatest common divisor** (*gcd*) of $a, b \in\mathbb Z$ is the integer $d \ge 0$ such that

1. $d \mid a$ and $d \mid b$
2. if $e \mid a$ and $e \mid b$ then $e \mid d$

Denoted by $\gcd(a, b) = d$

We say $a, b \in \mathbb Z$ are *relatively prime* (or *coprime*) if $\gcd(a, b) = 1$.

## Euclidean Algorithm

1. $\gcd(a, b) = \gcd(b, a) = \gcd(-a, b)$
2. $\gcd(a, 0) = |a|$
3. If $a = qb + r$ with $q, r \in \mathbb Z$, then $\gcd(a, b) = \gcd(b, r)$.

Bezout’s Lemma: Let $a, b \in \mathbb Z$ and $d = \gcd(a, b)$. There exists $x, y \in \mathbb Z$ such that $ax + by = d$.

**Fundamental Theorem of Arithmetic**: Every integer $n \ge 2$ can be expressed uniquely as a product $n = p_1^{e_1}p_2^{e_2} \dots p_r^{e_r}$, where $p_1 < p_2 < \dots < p_r$ are prime numbers and $e_1, e_2, \dots, e_r \in \mathbb N$.

## Modular Congruences

Fix $m \in \mathbb Z$ and $a, b \in \mathbb Z$, we say that $a, b$ are *congruent modulo* $m$ if $m$ divides $a - b$. We write $a \equiv b \pmod m$.

1. reflexivity: $a \equiv a \pmod m$ for all $a \in \mathbb Z$
2. symmetry: if $a \equiv b \pmod m$ then $b \equiv a \pmod m$
3. transitivity: if $a \equiv b \pmod m$ and $b \equiv c \pmod m$ then $a \equiv c \pmod m$

Suppose $a \equiv c \pmod m$ and $b \equiv d \pmod m$. Then,

1. $a + b \equiv c + d \pmod m$
2. $a - b \equiv c - d \pmod m$
3. $ab \equiv cd \pmod m$
4. $a^n \equiv c^n \pmod m$ for all $n \in \mathbb N$
