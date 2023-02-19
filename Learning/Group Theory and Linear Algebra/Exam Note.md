---
date created: Friday, November 4th 2022, 11:25:00 am
date modified: Friday, November 4th 2022, 5:32:39 pm
---
# Exam Note

- Euclidean algorithm: if $a > b$, $\gcd(a,b) = \gcd(b, a \% b) = \cdots$
- Let $a, b \in \mathbb Z$ and $d = \gcd(a, b)$, $\exists x, y \in \mathbb Z \ ax + by = d$ (calculate by unwinding the Euclidean algorithm)
- If $c \mid ab$ and $\gcd(a, c) = 1$, $c \mid b$
- The element $[a]_m$ is invertible in $\mathbb Z/m\mathbb Z$ if and only if $\gcd(a, m)$ = 1
- A set $A$ is a field if and only if:
    - $(a + b) + c = a + (b + c); a + b = b + a; 0 \in A; -a \in A$
    - $a(bc) = (ab)c; 1 \in A; a(b + c) = ab+ ac$
    - $ab = ba$
    - $a\ne 0, a^{-1} \in A$
- A subset A is a subfield if:
    - $0, 1 \in A$
    - if $x, y \in A$, $x + y \in A$ and $xy \in A$
    - if $x \in A$, $-x \in A$ and $x^{-1} \in A$

- $W_2$ is the complement of $W_1$ in $V$, $V$ is the direct sum of $W_1, W_2$, $V = W_1 \oplus W_2$:
    - $W_1 \cap W_2 = \{0\}$
    - $W_1 + W_2 = V$, where $W_1 + W_2 = \{w_1 + w_2 \mid w_1 \in W_1, w_2 \in W_2\}$
- $W$ is $f$-invariant if $\forall w \in W, f(w) \in W$
