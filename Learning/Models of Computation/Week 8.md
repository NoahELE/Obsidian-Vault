---
date created: Monday, September 12th 2022, 4:38:46 pm
date modified: Tuesday, September 13th 2022, 9:38:08 pm
---

# Week 8

## Regular Expressions

Theorem: $L$ is *regular* iff $L$ can be described by a regular expression.

## The Pumping Lemma

If $A$ is regular then there is a number $p$ such that for any string $s \in A$ with $|s| \ge p$, $s$ can be written as $s = xyz$, satisfying

- $xy^iz \in A$ for all $i \ge 0$
- $y \ne \epsilon$
- $|xy| \le p$

## Context-Free Grammars

A *grammar* is a set of substitution rules, or productions.

> [!EXAMPLE]
> $R \to 0 | 1 |eps | empty | R \cup R | R \ R | R^*$

$R$ is called a *variable*. Other symbols (here 0 and 1) are *terminals*. We refer to a valid string of terminals (such as 00100100) as a *sentence*. The intermediate strings that mix variables and terminals are *sentential forms*.

---

A context-free grammar (CFG) $G$ is a 4-tuple $(V, \Sigma, R, S)$, where

- $V$ is a finite set of variables,
- $\Sigma$ is a finite set of terminals,
- $R$ is a finite set of rules, each consisting of a variable (the left-hand side) and a string in $(V \cup \Sigma)^*$ (the right-hand side),
- $S$ is the start state.
