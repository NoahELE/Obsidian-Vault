---
date created: Monday, September 5th 2022, 6:40:09 pm
date modified: Tuesday, September 13th 2022, 4:11:08 pm
---

# Week 7

## Functions

- Mathematically: A function $f$ is a relation with the property that $(x, y) \in f \land (x, z) \in f \implies y = z$.
- Computationally: A prescription (an algorithm) for how to calculate output values from input values.

---

We say that the function $f$ is from $X$ to $Y$ , or $f: X \to Y$ if $dom(f ) = X$ and $ran(f ) \subseteq Y$ . We call $Y$ the *co-domain* of $f$ .

---

Let $A \subseteq X, B \subseteq Y$ , and consider $f: X \to Y$.

$f[A] = \{f(x) \mid x \in A\}$ is the *image* of $A$ under $f$.

$f^{-1}[B] = \{x \in X \mid f(x) \in B\}$ is the *co-image* of $B$ under $f$.

---

A function $f: X \to Y$ is

- *surjective* iff $f[X] = Y$
- *injective* iff $f(x) = f(y) \implies x = y$
- *bijective* iff it is both surjective and injective

## Finite Automata

A **finite automaton** is a 5-tuple $(Q, \Sigma, \delta, q_0, F)$, where

- $Q$ is a finite set of *states*;
- $\Sigma$ is a finite set of *alphabet*;
- $\delta: Q \times \Sigma \to Q$ is the *transition function*;
- $q_0 \in Q$ is the *start state*;
- $F \subseteq Q$ is the *accept states*;

Here $\delta$ is a total function, that is, $\delta$ must be defined for all possible inputs.

### Strings and Language

An alphabet $\Sigma$ can be any non-empty finite set.

The elements of $\Sigma$ are the symbols of the alphabet. Usually we choose symbols such as $a, b, c, 1, 2, 3 \dots$

A string over $\Sigma$ is a finite sequence of symbols from $\Sigma$.

We write the *concatenation* of a string $y$ to a string $x$ as $xy$.

The *empty string* is denoted by $\epsilon$.

A *language* (over alphabet $\Sigma$) is a (finite or infinite) set of finite strings over $\Sigma$.

$\Sigma^*$ denotes the set of all finite strings over $\Sigma$.

### Acceptance and Recognition, Formally

Let $M = (Q, \Sigma, \delta, q_0, F)$ and let $w = v_1v_2 \dots v_n$ be a string from $\Sigma^*$.

$M$ accepts $w$ iff there is a sequence of states $r_0, r_1, \dots, r_n$ with each $r_i \in Q$ such that

1. $r_0 = q_0$
2. $\delta(r_i, r_{i + 1}) = r_{i + 1}$ for $i = 0, \dots, n - 1$
3. $r_n \in F$

$M$ recognises language $A$ iff $A = \{w \mid M \ accepts \ w\}$.

### Regular Languages

A language is *regular* iff there is a finite automaton that recognises it.

Let $A$ and $B$ be languages. The regular operations are:

1. Union: $A \cup B$
2. Concatenation: $A \circ B = \{xy \mid x \in A, y \in B\}$
3. Kleene star: $A^* = \{x_1x_2 \dots x_k \mid k \ge 0, each \ x_i \in A\}$

> [!NOTE]
> The empty string $\epsilon$ is always in $A^*$

## Non-Deterministic Finite Automata

NFA allows 1 or more possible transitions from when we meet a input.

NFA may also be allowed to move from one state to another without consuming input. Such a transition is an $\epsilon$ transition.

NFA is also allowed to have multiple start states.

---

A **NFA** is a 5-tuple $(Q, \Sigma, \delta, I, F)$, where

- $Q$ is a finite set of *states*;
- $\Sigma$ is a finite set of *alphabet*;
- $\delta: Q \times \Sigma_\epsilon \to \mathcal P(Q)$ is the *transition function*;
- $I \subseteq Q$ is the *start state*;
- $F \subseteq Q$ is the *accept states*;

## DFAs Vs NFAs

Theorem: Every NFA has an equivalent DFA.

## Equivalence of DFAs

We can always find a *minimal* DFA for a given regular language (by minimal we mean having the smallest possible number of states).

The following algorithm takes an NFA and produces an equivalent minimal DFA.

1. Reverse the NFA (start state as final state and final state as start state)
2. Determinize the result (subset construction)
3. Reverse again
4. Determinize again
