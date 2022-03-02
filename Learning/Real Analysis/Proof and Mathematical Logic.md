# Proof and Mathematical Logic

A primary activity in mathematics is _proving_ theorems

## Propositional Logic

Definition (statement): A statement is a sentence or expression that is either true or false.

Connectives:

- not (negation): $\lnot p$
- and: $p \land q$
- or: $p \lor q$

Definition (tautology): Let A be a compound a statement, A is a tautology when A is true regardless of the truth values of its smaller statements.

Connectives:

- then (implication): $p \implies q$
- if and only if: $p \iff q$
- logically equivalent: $p \equiv q$

$$
(p \implies q) \land (\lnot p \implies \lnot q) \equiv p \iff q
$$

## First Order Logic

Mathematical statements whose truth depends on variables are called conditions.

Definition (existential qualifier, universal qualifier): Let $p(x)$ be a condition over a domain $D$,

- The statement "$p(x)$ is true for every $x$ in the domain" is denoted as $(\forall x \in D)p(x)$; $\forall$ is called the universal qualifier and the statement is a universal qualified statement.
- The statement "$p(x)$ is true for at least one $x$ in the domain" is denoted as $(\exists x \in D)p(x)$; $\exists$ is called the existential qualifier and the statement is a existential qualified statement.

$$
\lnot[(\forall x \in D) p(x)] \equiv (\exists x \in D) \lnot p(x)
$$
