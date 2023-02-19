---
date created: Monday, March 7th 2022, 10:19:34 am
date modified: Monday, August 15th 2022, 9:53:22 am
---

# Week 2

## Conditional Probability

Definition: The **conditional probability** of event A, given that event B has occurred, is $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$, provided that P(B) is larger than 0.

Conditional probability also satisfy the three probability axioms:

- $P(A | B) > 0$
- $P(B | B) = 1$
- If $A_1, A_2, \dots, A_n$ are mutually exclusive events:
    1. $P(A_1 \cup A_2 \cup \dots \cup A_n | B) = P(A_1 | B) + P(A_2 | B) + \dots + P(A_n | B)$
    2. $P(\cup^\infty_1 A_i | B) = \sum^\infty_1 P(A_i | B)$

Multiplication Rule:

$P(A \cap B) = P(A)P(B | A)\ or\ P(A \cap B) = P(B)P(A | B)$

## Independent Events

Definition: Events A and B are **independent** if and only if $P(A \cap B) = P(A)P(B)$, otherwise A and B are called **dependent** events

If A and B independent, then the following are true:

- A and B' are independent.
- A' and B are independent.
- A' and B' are independent.

Definition: Events A, B, and C are mutually independent if and only if the following conditions hold:

- They are pair-wisely independent; $P(A \cap B) = P(A)P(B), P(A \cap C) = P(A)P(C), P(B \cap C) = P(B)P(C)$
- Also $P(A \cap B \cap C) = P(A)P(B)P(C)$

Definition: $A_1, A_2, \dots, A_k$ are said to be mutually independent if for every $j = 2, 3, \dots, k$ and every subset of distinct indices $i_1, i_2, \dots, i_j$, $P(A_{i_1} \cap A_{i_2} \cap \dots \cap A_{i_j}) = P(A_{i_1})P(A_{i_2}) \dotsm P(A_{i_j})$

**Law of total probability**: If $B_1, B_2, B_3, \dots, B_k$ are mutually exclusive and exhaustive events, namely, $B_i \cap B_j = \varnothing$ for $1 \leq i \ne j \leq k$ and $S = B_1 + B_2 + \dots + B_k = \cup ^k _{i = 1} B_i$:

1. $A = (A \cap B_1) \cup (A \cap B_2) \cup \dots \cup (A \cap B_k) = \cup ^k _{i = 1} A \cap B_i$ for any event $A$
2. $P(A) = P(A \cap B_1) + P(A \cap B_2) + \dots + P(A \cap B_k) = \sum ^k _{i = 1} P(A \cap B_i)$

**Bayes’s Theorem**: If $B_1, B_2, B_3, \dots, B_k$ are mutually exclusive and exhaustive events, namely, $B_i \cap B_j = \varnothing$ for $1 \leq i \ne j \leq k$ and $S = B_1 + B_2 + \dots + B_k = \cup ^k _{i = 1} B_i$: (such $B_1, B_2, B_3, \dots, B_k$ may also be said to constitute a **partition** of the sample space.)

Then for each $j = 1, 2, \dots, k$, we have $$P(A | B_j) = \frac{P(B_j)P(A | B_j)}{\sum ^k _{i = 1} P(B_i)P(A | B_i)}$$
