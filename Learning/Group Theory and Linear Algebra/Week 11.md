---
date created: Monday, October 10th 2022, 8:13:25 am
date modified: Saturday, October 15th 2022, 9:57:37 pm
---

# Week 11

## Actions of Groups on Sets

Let $G$ be a group, $X$ be a set. A $G$-action on $X$ is a function

$$
\begin{align}
G \times X & \to X \\
(g, x) & \mapsto g \cdot x
\end{align}
$$

such that

- $e \cdot x = x$ for all $x \in X$
- $(gh) \cdot x = g \cdot (h \cdot x)$ for all $g, h \in G$ and $x \in X$

In this situation, we say that $G$ acts on $X$ and write $G \circlearrowleft X$.

---

Suppose $G$ acts on $X$.

Given $x \in X$, the *orbit* of $x$ is $\mathcal O(x) = \{g \cdot x \mid g \in G\} \subset X$.

Given $x \in X$, the *stabiliser* of $x$ is $\text{Stab}(x) = \{g \in G \mid g \cdot x = x\} \subset G$.
