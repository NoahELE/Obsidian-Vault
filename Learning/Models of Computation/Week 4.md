---
date created: Monday, August 15th 2022, 4:23:13 pm
date modified: Monday, August 22nd 2022, 8:48:17 am
---

# Week 4

## The Meaning of a Predicate Logic Formula

$\exists x\ F \equiv \neg \forall x\ \neg F$

The order of different quantifiers is important.

- $\forall x \exists y$ is different from $\exists y \forall x$
- $\forall x \forall y$ is the same as $\forall y \forall x$, and so are $\exists x\exists y$ and $\exists y \exists x$

If $G$ is a formula with *no free occurrences* of $x$, then we also get:

- $\exists x \ G \equiv G$
- $\forall x \ G \equiv G$
- $\exists x \ (F \land G) \equiv (\exists x \ F) \land G$
- $\forall x \ (F \lor G) \equiv (\forall x \ F) \lor G$
- $\forall x \ (F \implies G) \equiv (\exists x \ F) \implies G$
- $\forall x \ (G \implies F) \equiv G \implies (\forall x \ F)$

## Resolution for Predicate Logic

**clausal form**: without any quantifiers

Existential quantifiers are eliminated in a process called **Skolemization**.

### Eliminating Existential Quantifiers

$F = \exists x \forall y \ P(x, y) \implies \forall y \ P(a, y)$

> $a$ is a Skolem constant

$G = \forall y \exists x \ P(x, y) \implies \forall y \ P(f(y), y)$

> $f$ is a Skolem function

## From Predicate Logic Formulas to Clausal Form

1. Replace occurrences of $\oplus$, $\implies$, $\iff$;
2. Drive negation $\neg$ in;
3. Standardise bound variables apart;
4. Eliminate existential quantifiers (Skolemize);
5. Eliminate universal quantifiers (just remove them);
6. Bring to CNF (using the distributive laws).

> [!NOTE]
> Skolemization of a formula does not produce a logically equivalent formula.
>
> However, Skolemization does produce an **equisatisfiable** formula—one that is satisfiable iff the original was
