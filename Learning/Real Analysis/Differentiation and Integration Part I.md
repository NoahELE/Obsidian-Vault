---
date created: Monday, May 2nd 2022, 9:19:19 am
date modified: Tuesday, May 3rd 2022, 8:03:39 am
---

# Differentiation and Integration Part I

Theorem: If $f: [a, b] \to \mathbb R$ is integrable and let $F: [a, b] \to \mathbb R$ satisfies $F'(x) = f(x)$. Then, $$\int^a_b f(x) = F(a) - F(b)$$

## Differentiation

Definition: Let $f: I \to \mathbb R$, $c \in I$. We say $f$ is differentiable at $c$ when there exists $L \in \mathbb R$, so that $$\lim_{x \to c} \frac{f(x) - f(c)}{x - c} = L$$

We call $L$ the derivative of $f$ at $c$. When $f$ is differentiable at $c$ for all $c \in I$ we say $f$ is differentiable on  $I$.

## The Mean Value Theorem

Theorem: Let $f: [a, b] \to \mathbb R$ be continuous on $[a, b]$ and differentiable on $(a, b)$. There exists $c \in (a, b)$ so that $f'(c) = \frac{f(b) - f(a)}{b - a}$ .
