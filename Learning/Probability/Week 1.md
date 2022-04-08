---
date created: Wednesday, March 2nd 2022, 10:09:31 am
date modified: Friday, April 8th 2022, 6:20:41 pm
---

# Week 1

- Experiment: a process of obtaining an observed result .
- Trial: performing an experiment.
- Outcome: an observed result of an experiment.
- Random experiment: an experiment in which the outcome cannot be predicted with certainty.

Definition: **Sample space**, or **Outcome space**, denoted by $S$, is the set of all possible outcomes of an experiment. Each outcome in S is called a **sample point**, which is often generically denoted as $\omega$.

- $S$ is called a discrete sample space if $S$ is either finite or countably infinite.

Definition: **Event**. $A$ is called an event if $A$ is a subset of the outcomes in the sample space $S$, i.e. $A \subset S$. We say event $A$ has occurred if we perform a random experiment and the outcome of the experiment is in $A$.

- An event is called an elementary event if it contains exactly one outcome of the experiment.
- There are two special events: The empty set $\varnothing$ is called the null (or impossible) event. It cannot happen at any time. The sample space $S$ itself is called the certain event which always happens.

_Operations of events are the same as those of sets._

1. sub-event: $A \subseteq B$
    - if $A \subseteq B$ and $B \supseteq A$, $A = B$
2. intersection: $A \cap B$
3. union: $A \cup B$
4. complement: $A'$

Definition:

1. Events $A$ and $B$ are **mutually exclusive** if $A \cap B = \varnothing$
2. Events $A_1, A_2, A_3, …, A_k$ are **mutually exclusive** if they are pair-wise mutually exclusive, i.e. $A_i \cap A_j = \varnothing$ for any $i \ne j$
3. Events $A_1, A_2, A_3, …, A_k$ are **collectively exhaustive** if $A_1 \cup A_2 \cup … \cup A_k = S$
4. Events $A_1, A_2, A_3, …, A_k$ are **mutually exclusive and exhaustive** if $A_1 \cup A_2 \cup … \cup A_k = S$ and $A_i \cap A_j = \varnothing$ for any $i \ne j$

_Priority of the operations_:

1. complement
2. intersection
3. union or difference

_Properties of the event operations_:

- Commutative laws. $A \cap B = B \cap A$, $A \cup B = B \cup A$
- Associative laws. $(A \cap B) \cap C = A \cap (B \cap C)$, $(A \cup B) \cup C = A \cup (B \cup C)$
- Distributive laws. $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$, $A \cup (B \cap C) = (A \cup B) \cap (B \cup C)$
- De Morgan's laws. $(A \cap B)' = A' \cup B'$, $(A \cup B)' = A' \cap B'$

Definition: **Probability** is a real-valued set function $P$ that assigns to each event $A$ in the sample space $S$ a number $P(A)$, called the probability of the event $A$, such that the following axioms are satisfied:

1. (Non-negative) $P(A) \geq 0$
2. (Regular) $P(S) = 1$
3. (Countably additive) $P(\cup^k_{i = 1} A_i) = \sum^k_{i = 1} P(A_i)$ for each integer $k$, and further, $P(\cup^\infty_{i = 1} A_i) = \sum^\infty_{i = 1} P(A_i)$, for countable infinities

In the case of a _discrete sample space_, probability can be equivalently defined as a set function satisfying:

- $P(\{\omega\}) \ge 0$ for any sample $\omega \in S$
- $\sum _{\omega \in S} P(\{\omega\}) = 1$
- for any sample point sequence, $P(\cup^\infty_{i = 1} \{\omega_i\}) = \sum^\infty_{i = 1} P(\{\omega_i\})$

**Properties of probability**:

- For each event A, $P(A) = 1 − P(A')$
- For the null event, $P(\varnothing) = 0$
- If events A and B are such that $A \subset B$, then $P(A) \le P(B)$
- For each event A, $P(A) < 1$
- If A and B are any two events, then $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
- If A, B and C are any three events, then $P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(A \cap B) - P(B \cap C) - P(A \cap C) + P(A \cap B \cap C)$

**The classic probability model**:

- A special type of experiment:
    - number of possible outcomes are finite, i.e. S is finite
    - all possible outcomes are equally likely, i.e. $P(\{\omega _1\}) = P(\{\omega_2\}) = … = P(\{\omega_n\}) = \frac{1}{n}$
- Probability of any event A is $P(A) = \frac{n(A)}{n}$

All counting techniques derived from 2 basic counting rules

- Multiplication Principle. If $A_1$ can be performed in $n_1$ ways and $A_2$ can be performed in $n_2$ ways, then there is $n_1 \times n_2$ ways to perform $A_1$ and $A_2$.
- Addition Principle. If $A_1$ can be performed in $n_1$ ways and $A_2$ can be performed in $n_2$ ways, then there is $n_1 + n_2$ ways to perform $A_1$ or $A_2$ (but not both).

**Some useful counting formulas**:

- Permutations: The number of permutations of n distinct objects taken r at a time is $$P^n_r = _nP_r = P_{n, r} = \frac{n!}{(n - r)!} = n(n - 1)(n - 2)…(n - r + 1)$$
- Combinations: The number of combinations of n distinct objects chosen r at a time is $$C^n_r = _nC_r = C_{n, r} = {n \choose r} = \frac{n!}{r!(n - r)!}$$
