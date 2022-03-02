# Week 1

- Experiment: a process of obtaining an observed result .
- Trial: performing an experiment.
- Outcome: an observed result of an experiment.
- Random experiment: an experiment in which the outcome cannot be predicted with certainty.

**Definition 1**: **Sample space**, or **Outcome space**, denoted by $S$, is the set of all possible outcomes of an experiment. Each outcome in S is called a **sample point**, which is often generically denoted as $\omega$.

- $S$ is called a discrete sample space if $S$ is either finite or countably infinite.

**Definition 2**: **Event**. $A$ is called an event if $A$ is a subset of the outcomes in the sample space $S$, i.e. $A \subset S$. We say event $A$ has occurred if we perform a random experiment and the outcome of the experiment is in $A$.

- An event is called an elementary event if it contains exactly one outcome of the experiment.
- There are two special events: The empty set $\varnothing$ is called the null (or impossible) event. It cannot happen at any time. The sample space $S$ itself is called the certain event which always happens.

*Operations of events are the same as those of sets.*

1. sub-event: $A \subset B$
   - if $A \subset B$ and $B \supset A$, $A = B$
2. intersection: $A \cap B$
3. union: $A \cup B$
4. complement: $A'$

**Definition 3**:

1. Events $A$ and $B$ are **mutually exclusive** if $A \cap B = \varnothing$
2. Events $A_1, A_2, A_3, …, A_k$ are **mutually exclusive** if they are pair-wise mutually exclusive, i.e. $A_i \cap A_j = \varnothing$ for any $i \ne j$
3. Events $A_1, A_2, A_3, …, A_k$ are **collectively exhaustive** if $A_1 \cap A_2 \cap … \cap A_k = S$
4. Events $A_1, A_2, A_3, …, A_k$ are **mutually exclusive and exhaustive** if $A_1 \cap A_2 \cap … \cap A_k = S$ and $A_i \cap A_j = \varnothing$ for any $i \ne j$

*Priority of the operations*:

1. complement
2. intersection
3. union or difference

*Properties of the event operations*:

- Commutative laws. $A \cap B = B \cap A$, $A \cup B = B \cup A$
- Associative laws. $(A \cap B) \cap C = A \cap (B \cap C)$, $(A \cup B) \cup C = A \cup (B \cup C)$
- Distributive laws. $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$, $A \cup (B \cap C) = (A \cup B) \cap (B \cup C)$
- De Morgan's laws. $(A \cap B)' = A' \cup B'$, $(A \cup B)' = A' \cap B'$

**Definition 4**: **Probability** is a real-valued set function $P$ that assigns to each event $A$ in the sample space $S$ a number $P(A)$, called the probability of the event $A$, such that the following axioms are satisfied:

1. (Non-negative) $P(A) \geq 0$
2. (Regular) $P(S) = 1$
3. (Countably additive) $P(\cup ^k _{i = 1} A_i) = \sum ^k _{i = 1} P(A_i)$ for each integer $k$, and further, $P(\cup ^\infty _{i = 1} A_i) = \sum ^\infty _{i = 1} P(A_i)$, for countable infinities
