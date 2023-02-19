---
date created: Monday, September 5th 2022, 9:50:26 am
date modified: Monday, September 12th 2022, 11:16:12 am
---

# Week 7

## Checking for Isomorphism

1. Check the cardinality.
2. Look at orders of elements.
3. Use other algebraic or counting properties (e.g. count solutions to certain equations).
4. Exhibit an isomorphism.

## Direct Product

Let $G, H$ be groups. Consider the set $G \times H = \{(g, h) \mid g \in G, h \in H\}$.

Define an operation on $G \times H$ by $(g_1, h_1)(g_2, h_2) = (g_1g_2, h_1h_2)$.

$G \times H$ is a group. (We call it the *(direct) product* of $G$ and $H$)

## Cosets and Quotients of Groups

Let $H$ be a subgroup of a group $G$.

- A *left coset* of $H$ in $G$ is a set of the form $gH = \{gh \mid h \in H\}$ for a fixed $g \in G$.
- A *right coset* of $H$ in $G$ is a set of the form $Hg = \{hg \mid h \in H\}$ for a fixed $g \in G$.

We write $a \sim_H b$ if $aH = bH$.

We have $a \sim_H b$ if and only if $a^{-1}b \in H$.

> The relation $\sim_H$ is an equivalence relation on G.

We denote the set of cosets $G/H = \{aH \mid a \in G\}$, called the quotient of $G$ by $H$.

> In general, $G/H$ is just a set.

The cardinality $\#(G/H)$ is called the index of $H$ in $G$ and often denoted $[G:H]$

## Quotients as Groups

Define an operation,

$$
\begin{align}
& G/H \times G/H \to G/H \\
& (aH, bH) \mapsto (aH)(bH) := abH
\end{align}
$$

The operation on $G/H$ is well-defined if and only if $Hb = bH$ for all $b \in G$.

We say that $H$ is *normal* if $Hg = gH$ for all $g \in G$.

---

If $H$ is a normal subgroup of $G$, then $G/H$ is a group with,

- operation $(aH)(bH) = abH$
- identity element $e_{G/H} = H$
- inverse of $gH$ given by $g^{−1}H$

---

Let $f: G_1 \to G_2$ be a group homomorphism. We define the *kernel* of $f$ by $ker(f) = \{x \in G_1 \mid f(x) = e_{G_2}\}$, and the *image* of $f$ by $im(f) = \{y \in G_2 \mid y = f(x), x \in G_1\}$

- $ker(f)$ is a normal subgroup of $G_1$
- $im(f)$ is a subgroup of $G_2$
- $f$ is injective if and only if $ker(f) = \{e_{G_1}\}$

---

Let $H$ be a normal subgroup of a group $G$. There is another bit of structure to the quotient group $G/H$: it comes with a natural group homomorphism,

$$
\begin{align}
\pi: & G \to G/H \\
& g \mapsto gH
\end{align}
$$

The map $\pi$ is surjective with $ker(\pi) = H$.

---

If $f: G_1 \to G_2$ is a group homomorphism, then $G_1/ker(f) \cong im(f)$.

In particular, if $f$ is surjective then $G_1/ker(f) \cong G_2$
