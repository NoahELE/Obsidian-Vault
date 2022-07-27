---
date created: Tuesday, April 5th 2022, 7:55:39 am
date modified: Wednesday, April 6th 2022, 3:12:43 pm
---

# Functions and Sequences Part II

Definition: Let $(f_n)$ be a sequence. We say $(f_n)$ is **monotone increasing** when we have $f_n \le f_{n + 1}$ for all $n \in \mathbb N^+$. We say $(f_n)$ is **monotone decreasing** when we have $f_n \ge f_{n + 1}$ for all $n \in \mathbb N^+$. We say $(f_n)$ is **monotone** when it is either monotone increasing or monotone decreasing.

Theorem: Let $(f_n)$ be a monotone sequence. The sequence converges if and only if $(f_n)$ is bounded.

Definition: Let $(f_n)$ be a sequence. We say $(f_n)$ is **Cauchy** or $(f_n)$ is a **Cauchy sequence** when for each $\epsilon > 0$ there exists $M \in \mathbb N^+$ so that $|f_j - f_k| < \epsilon$ whenever $j, k > M$.

Theorem: Let $(f_n)$ be a sequence. The sequence $(f_n)$ converges if and only if $(f_n)$ is Cauchy. (Cauchy convergent Criterion)

## Sequences of Functions

Definition: Let $D \subseteq \mathbb R$. Let $(f_n(x))$ be a sequence of functions $f_n: D \to \mathbb R$ and let $f: D \to \mathbb R$ be a function. We say $(f_n(x))$ **converges pointwise** to $f(x)$ when for every $x \in D$ we have $f_n(x) \to f(x)$.

Definition: Let $D \subseteq \mathbb R$. Let $(f_n(x))$ be a sequence of functions $f_n: D \to \mathbb R$ and let $f: D \to \mathbb R$ be a function. We say $(f_n(x))$ **converges uniformly** to $f(x)$ when for every $\epsilon > 0$ there exists $M \in \mathbb N^+$ such that for all $x \in D$ we have $|f_n(x) - f(x)| < \epsilon$ whenever $n > M$.
