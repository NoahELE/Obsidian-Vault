---
date created: Tuesday, April 12th 2022, 8:12:42 am
date modified: Wednesday, April 13th 2022, 10:39:12 am
---

# Limits and Continuity Part I

Definition: Let $f: \mathbb R \to \mathbb R$, we say $f$ is continuous when for every $a \in \mathbb R$ we have $\lim_{x \to a} f(x) = f(a)$.

## Limits of Real Functions

Definition: Let $E \subseteq \mathbb R$ and $a \in \mathbb R$, we say $a$ is a **limit point** of $E$ when for all $\delta > 0$ there exists $x \in E$ so that $0 < |x - a| < \delta$.

Definition: Let $E \subseteq \mathbb R$, let $a$ be a limit point of $E$, let $f: E \to \mathbb R$ and let $L \in \mathbb R$, we say the limit of $f(x)$ as $x$ approaches $a$ is $L$ when for every $\epsilon > 0$ there exists $\delta > 0$ so that $|f(x) - L| < \epsilon$ whenever $0 < |x - a| < \delta$. We write $\lim_{x \to a} f(x) = L$ and we say $f(x)$ converges to $L$ as $x$ approaches $a$.

### Divergence

Definition: Let $E \subseteq \mathbb R$, let $a$ be a limit point of $E$, let $f: E \to \mathbb R$, we say $f(x)$ diverges as $x$ approaches $a$ when the state $\lim_{x \to a} f(x) = L$ is false for all $L \in \mathbb R$.

Theorem: $\lim_{x \to a} f(x) = L$ if and only if $\lim_{x \to a^+} f(x) = L$ and $\lim_{x \to a^-} f(x) = L$.

Corollary: If $\lim_{x \to a^+} f(x) \ne \lim_{x \to a^-} f(x)$, then $f(x)$ diverges as $x$ approaches $a$.

Definition: Let $E \subseteq \mathbb R$, let $a$ be a limit point of $E$, let $f: E \to \mathbb R$, we say $f(x)$ diverges to $\infty$ as $x$ approaches to $a$ when for every $r \in \mathbb R$ there exists $\delta > 0$ so that $f(x) > r$ whenever $0 < |x - a| < \delta$. We write $\lim_{x \to a} f(x) = \infty$.

### Limits to Infinity

Definition: Let $E \subseteq \mathbb R$ so that $E$ is not bounded above, let $f: E \to \mathbb R$ and let $L \in \mathbb R$, we say the limit of $f(x)$ as $x$ goes to $\infty$ is $L$ when for every $\epsilon > 0$ there exists $M \in \mathbb R$ so that $|f(x) - L| < \epsilon$ whenever $x > M$. We write $\lim_{x \to \infty} f(x) = L$ and we say $f(x)$ converges to $L$ as $x$ goes to $\infty$.
