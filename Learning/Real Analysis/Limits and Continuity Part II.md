---
date created: Tuesday, April 26th 2022, 10:00:40 am
date modified: Saturday, April 30th 2022, 12:45:30 pm
---

# Limits and Continuity Part II

## Continuity

Definition: Let $E \subseteq \mathbb R$, let $f: E \to \mathbb R$ and let $a \in E$. We say $f$ is *continuous at* $a$ when for every $\epsilon > 0$ there exists $\delta > 0$ so that $|f(x) - f(a)| < \epsilon$ whenever $|x - a| < \delta$. We say $f$ is *continuous on* $E$ when $f$ is continuous at $a$ for all $a \in E$.

Theorem: Let $E \subseteq \mathbb R$, let $f: E \to \mathbb R$ and let $a \in E$ so that $a$ is a limit point of $E$. The function $f$ is continuous if and only if $\lim_{x \to a} f(x) = f(a)$.

Theorem: (Algebra of Continuous Functions Theorem) Let $E \subseteq \mathbb R$, let $f, g: E \to \mathbb R$ and let $a \in E$. If $f, g$ are both continuous at $a$, then

1. $k \cdot f(x)$ is continuous at $a$ for all $k \in \mathbb R$;
2. $f(x) + g(x)$ is continuous at $a$;
3. $f(x) \cdot g(x)$ is continuous at $a$;
4. $f(x) / g(x)$ is continuous at $a$ if $g(a) \ne 0$;

## Boundedness

Theorem: Let $f: [a, b] \to \mathbb R$, if $f$ is continuous on $[a, b]$, then $f$ is bounded on $[a, b]$.

## Extreme Theorem

Theorem: Let $f: [a, b] \to \mathbb R$, if $f$ is continuous on $[a, b]$, then there exists $c, d \in \mathbb R$, so that $f(c) \le f(x) \le f(d)$, for all $x \in [a, b]$.

## Intermediate Value Theorem

Theorem: Let $f$ be continuous on $[a, b]$ so that $f(a) < f(b)$ and let $y \in \mathbb R$. If $f(a) < y < f(b)$, there exists $c \in [a, b]$ so that $f(c) = y$.

## Sequences of Continuous Functions

Theorem: (Uniform Limit Theorem) Let $(f_n(x))$ be a sequence of functions with domain $D$, if $(f_1(x), f_2(x), \dots)$ converges uniformly to $f(x)$, then $f(x)$ is continuous.
