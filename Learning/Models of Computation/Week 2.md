---
date created: Monday, August 1st 2022, 2:37:49 pm
date modified: Tuesday, August 16th 2022, 2:43:10 pm
---

# Week 2

## Validity and Satisfiability

A propositional formula is **valid** if no truth assignment makes it false. Otherwise it is **non-valid** (also referred to as **invalid** and as **falsifiable**).

It is **unsatisfiable** if no truth assignment makes it true. Otherwise it is **satisfiable**.

A valid propositional formula is a **tautology**.

An unsatisfiable propositional formula is a **contradiction**.

> [!TIP]
> A formula is unsatisfiable iff its negation is valid.

## Models, Logical Consequence, and Equivalence

Let $\theta$ be a truth assignment and $F$ be a propositional formula. If $\theta$ makes $F$ true then $\theta$ is a **model** of $F$.

$G$ is a **logical consequence** of $F$ if and only if every model of $F$ is a model of $G$ as well.

In this case, we write $F \models G$.

If $F \models G$ and $G \models F$ both hold, that is, $F$ and $G$ have exactly the same models, then $F$ and $G$ are logically **equivalent**.

In this case, we write $F \equiv G$.

Theorem: $F \models G$ if and only if $F \land \neg G$ is unsatisfiable.

## Some Equivalence

- Absorption:
    - $P \land P \equiv P$
    - $P \lor P \equiv P$
- Commutativity:
    - $P \land Q \equiv Q \land P$
    - $P \lor Q \equiv Q \lor P$
- Associativity:
    - $P \land (Q \land R) \equiv (P \land Q) \land R$
    - $P \lor (Q \lor R) \equiv (P \lor Q) \lor R$
- Distributivity:
    - $P \land (Q \lor R) \equiv (P \land Q) \lor (P \land R)$
    - $P \lor (Q \land R) \equiv (P \lor Q) \land (P \lor R)$
- Double negation:
    - $P \equiv \neg \neg P$
- De Morgan:
    - $\neg (P \land Q) \equiv \neg P \lor \neg Q$
    - $\neg (P \lor Q) \equiv \neg P \land \neg Q$
- Implication:
    - $P \implies Q \equiv \neg P \lor Q$
- Contraposition:
    - $\neg P \implies \neg Q \equiv Q \implies P$
    - $P \implies \neg Q \equiv Q \implies \neg P$
    - $\neg P \implies Q \equiv \neg Q \implies P$
- Biimplication:
    - $P \iff Q \equiv (P \land Q) \lor (\neg P \land \neg Q)$
