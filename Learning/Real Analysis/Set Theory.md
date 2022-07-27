---
date created: Monday, March 14th 2022, 9:56:15 am
date modified: Tuesday, April 12th 2022, 1:52:07 pm
---

# Set Theory

Definition: A **set** is a collection of unique objects. Objects contained in a set are called **elements**. When $A$ is a set and $x$ is an element of $A$ we write $x \in A$.

By definition sets are unordered.

Russell’s Paradox: Let P be the set of sets that are not elements of themselves.

- If $P \in P$, P is a set that is element of itself, thus $P \notin P$
- If $P \notin P$, P is a set that is not element of itself, thus $P \in P$

## Preliminaries

Axiom of Specification: if $U$ is a set and $p(x)$ is a condition on $U$, then the collection of all elements of $U$ for which $p(x)$ is true forms a set. We denote such a set as follows: $\{x \in U | p(x)\}$

## Ordering and Bounded Sets

Definition: Let $S$ be a set. An **order** on $S$ is a relation, denoted $<$, so that the following two statements are true:

- (O1) for all $x, y \in S$, exactly one of the following is true:
    - $x < y$
    - $y < x$
    - $x = y$
- (O2) for all $x, y, z \in S$, if $x < y$ and $y < z$, then $x < z$

Definition: Let $S$ be an ordered set and let $A$ be a subset of $S$. We say $A$ _is bounded below in_ $S$ when there exists $\beta \in S$ so that the following statement is true:$(\forall x \in A)\ \beta \leq x$, $\beta$ is a **lower bound** for A in S.

Definition: Let $S$ be an ordered set and let $A$ be a subset of $S$. We say $A$ _is bounded above in_ $S$ when there exists $\beta \in S$ so that the following statement is true:$(\forall x \in A)\ \beta \geq x$, $\beta$ is a **upper bound** for A in S.

Definition: Let $S$ be an ordered set, let $A$ be a subset of $S$, let $U_A$ be the set of upper bounds of $A$ in $S$, and let $\alpha \in U_A$. We say $\alpha$ is a least upper bound of $A$ in $S$ when for all upper bounds $\beta \in U_A$ we have $\alpha \leq \beta$. In other words, $\alpha$ is a **least upper bound** of $A$ in $S$ when the following statement is true: $(\forall \beta \in U_A)\ \alpha \leq \beta$

When $\alpha$ is the least upper bound of $A$ in $S$ we say $\alpha$ is the **supremum** of $A$ in $S$ and we write $sup\ A = \alpha$.

Definition: Let $S$ be an ordered set, let $A$ be a subset of $S$, let $L_A$ be the set of lower bounds of $A$ in $S$, and let $\alpha \in L_A$. We say $\alpha$ is a greatest lower bound of $A$ in $S$ when for all upper bounds $\beta \in L_A$ we have $\alpha \geq \beta$. In other words, $\alpha$ is a **greatest lower bound** of $A$ in $S$ when the following statement is true: $(\forall \beta \in L_A)\ \alpha \geq \beta$

When $\alpha$ is the least upper bound of $A$ in $S$ we say $\alpha$ is the **infimum** of $A$ in $S$ and we write $inf\ A = \alpha$.

## Sets and Operations

Definition: Let $F$ be a set equipped with two operations, addition ($+$) and multiplication ($\times$). We say F is a field when the following statements are true for $F$:

1. $(\forall x, y \in F)\ x + y \in F$
2. $(\forall x, y \in F)\ x + y = y + x$
3. $(\forall x, y, z \in F)\ (x + y) + z = x + (y + z)$
4. $[\exists 0 \in F]((\forall x \in F)\ x + 0 = x)$
5. $[\forall x \in F]((\exists y \in F)\ x + y = 0)$
6. $(\forall x, y \in F)\ xy \in F$
7. $(\forall x, y \in F)\ xy = yx$
8. $(\forall x, y, z \in F)\ (xy)z = x(yz)$
9. $[\exists 1 \in F \setminus \{0\}]((\forall x \in F)\ 1x = x)$
10. $[\forall x \in F \setminus \{0\}]((\exists y \in F \setminus \{0\})\ xy = 1)$
11. $(\forall x, y, z \in F)\ x(y + z) = xy + xz$

Definition: Let $F$ be a field and let $x, y \in F$ We say $0$ is the **additive identity**. When $x + y = 0$ we say $y$ is the **additive inverse** of $x$. When y is the additive inverse of $x$ we denote $y$ as $-x$.

Definition: Let $F$ be a field and let $x, y \in F$ We say $1$ is the **multiplicative identity**. When $xy = 1$ we say $y$ is the **multiplicative inverse** of $x$. When y is the additive inverse of $x$ we denote $y$ as $x^{-1}$.
