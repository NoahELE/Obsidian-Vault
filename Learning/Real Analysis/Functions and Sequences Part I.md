---
date created: Tuesday, March 29th 2022, 8:53:53 am
date modified: Friday, April 8th 2022, 4:10:43 pm
---

# Functions and Sequences Part I

## Functions and Relations

Definition: Let $A$, $B$ and $R$ are sets. We say $R$ is a **relation** on $A$ and $B$ when $R$ is a subset of $A \times B$

Definition: Let $A$, $B$ be sets and let $f$ be a relation on $A$ and $B$. We say $f$ is a function from $A$ to $B$ when each element of $A$ appears as the first entry of an ordered pair exactly once. When $f$ is a **function** from $A$ to $B$ we write $f: A \to B$. We say that $A$ is the **domain** of $f$ and that $B$ is the **codomain** of $f$.

For $(a, b) \in f$, we say $b$ is the **image** of $a$ and $a$ is a **pre-image** of $b$, denoted by $f(a) = b$

The range of $f$ is the set $range(f) = \{f(a) \in B | a \in A\}$

## Sequences and Convergence

Definition: Let $A$ and $B$ be sets and let $f$ be a function from $A$ to $B$. We say $f$ is a sequence when $A = \mathbb N^+, B = \mathbb R$.

We use the notation $(f_n)$ to refer to the sequence in its entirety.

Definition: Let $f_n$ be a sequence and let $L \in \mathbb R$. We say $(f_n)$ **converges** to $L$ when for every $\epsilon > 0$ there exists $M \in \mathbb N^+$ so that $|f_n - L| < \epsilon$ whenever $n > M$. When $(f_n)$ converges to $L$, we write $f_n \to L$ or $\lim _{n \to \infty} f_n = L$.

Definition: Let $f_n$ be a sequence. We say $f_n$ **diverges** when the statement $f_n$ converges to $L$ is false for every $L \in \mathbb R$.

Theorem: Let $(f_n)$ be a sequence, if $(f_n)$ converges, then $(f_n)$ is bounded.

Theorem: Let $(f_n)$ be a sequence, if $(f_n)$ is not bounded, then $(f_n)$ diverges.

Theorem: A sequence $(f_n)$ converges to $L$ if and only if every subsequence of $(f_n)$ converges to $L$.

Theorem: Let $(f_n)$ be a sequence. If any of the following are true, then $(f_n)$ diverges.

1. $(f_n)$ is unbounded.
2. $(f_n)$ has 2 subsequences which converge to different values.
3. $(f_n)$ has a subsequence that diverges.

Every **bounded** sequence has a **convergent subsequence**.
