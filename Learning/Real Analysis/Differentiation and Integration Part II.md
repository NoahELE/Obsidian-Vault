---
date created: Tuesday, May 10th 2022, 7:15:45 am
date modified: Tuesday, May 10th 2022, 8:44:09 am
---

# Differentiation and Integration Part II

Let $f: [a, b] \to \mathbb R$ be bounded on $\mathbb R$, and let $P = \{x_0, x_1, x_2, …, x_n\}$ of $[a,b]$. The lower Riemann sum of $f$ with respect to $P$ is given by $$L(f, P) = \sum^n_{k = 1} m_k(x_k - x_{k - 1})$$

The upper Riemann sum of $f$ with respect to $P$ is given by $$U(f, P) = \sum^n_{k = 1} M_k(x_k - x_{k - 1})$$

## Fundamental Theorem of Calculus:

If $f: [a, b] \to \mathbb R$ is integrable and $F: [a, b] \to \mathbb R$ satisfies $F'(x) = f(x)$ for all $x \in [a, b]$, then $$\int_a^b f(x) dx = F(a) - F(b)$$

Let $g: [a,b] \to \mathbb R$ and $G: [a,b] \to \mathbb R$ so that $$G(x) = \int^x_a g(u) du$$

1. The function $G$ is continuous on$[a, b]$
2. If $g$ is continuous at $c \in [a, b]$, then $G$ is continuous at $c$ and $G'(c) = g(c)$
