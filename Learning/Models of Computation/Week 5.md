---
date created: Wednesday, August 24th 2022, 8:44:17 am
date modified: Thursday, September 1st 2022, 6:11:47 pm
---

# Week 5

## Notation for Variables and Constants

We use letters from the start of the alphabet *(a, b, c, . . . )* for constants, and letters from the end of the alphabet *(u, v, x, y . . . )* for variables.

We also usually use lower case letters such as *f , g, h, . . .* as function symbols, and, of course, upper case letters for predicate symbols.

## Substitutions

A **substitution** is a finite set of replacements of variables by terms, that is, a set $\theta$ of the form $\{x_1 \mapsto t_1, x_2 \mapsto t_2, \dots , x_n \mapsto t_n\}$, where the $x_i$ are variables and the $t_i$ are terms.

## Most General Unifiers

A **unifier** of two terms $s$ and $t$ is a substitution $\theta$ such that $\theta(s) = \theta(t)$.

The terms $s$ and $t$ are *unifiable* if and only if there exists a unifier for $s$ and $t$.

## Resolvents

For predicate logic we have:

- Two literals $L$ and $\neg L'$ are complementary if $\{L, L'\}$ is unifiable.
- Let $C_1$ and $C_2$ be clauses, renamed apart. Let $\theta$ be an mgu of complementary literals $\{L, \neg L'\}$ with $L$ a literal in $C_1$ and $\neg L'$ a literal in $C_2$. Then the resolvent of $C_1$ and $C_2$ is the union $\theta(C_1 \setminus \{L\}) \cup \theta(C_2 \setminus \{\neg L'\})$.