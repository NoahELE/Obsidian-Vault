---
date created: Monday, March 7th 2022, 2:27:53 pm
date modified: Friday, April 8th 2022, 1:43:40 pm
---

# Mathematical Proofs

Definition: _A **mathematical proof**, is a sequence of statements where each statement is_

- a declaration of notation,
- a premise, or
- a true statement that follows from
    - a definition,
    - algebra, or
    - previous true statements

Definition: a **formal mathematical proof** is a finite sequence of statements $A_1, A_2, \dots, A_n$, such that each $A_i$ is either

- known or assumed true or
- can be inferred from a known or assumed true statement $A_j$, with $j < i$ (i.e. a previous statement).

## Direct Proof

One assumes the hypothesis is true and deduces the conclusion is true.

## Indirect Methods

**Contrapositive**: Instead of proving $p(x) \implies q(x)$ is true for every x in the domain, we prove that $\neg q(x) \implies \neg p(x)$ is true for every x in the domain.

**Proof by Contradiction**: one assumes that the hypothesis is true and the conclusion is false. From these two premises, one then attempts to deduce a false statement.

## Quantified Statements

Proving Existentially Quantified Statements: We can use examples to prove an existential statement and disprove universal statements.

_counter examples_

Proving Universally Quantified Statements:

One common tool for proving universally quantified statements over the natural numbers is _mathematical induction_.

**Proof by Induction**

$$(\forall n \in \mathbb N)\ p(n)$$

1. $p(0)$ is true; and
2. for every $k \in N$, if $p(k)$ is true, then $p(k + 1)$ is true.

Surjective: let $f: x \to y$, $f$ is surjective if and only if $\forall y \in Y$, $\exists x \in X$, such that $f(x) = y$
