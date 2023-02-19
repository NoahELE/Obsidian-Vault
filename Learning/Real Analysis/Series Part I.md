---
date created: Wednesday, May 18th 2022, 9:00:16 am
date modified: Tuesday, May 24th 2022, 2:14:35 pm
---

# Series Part I

Definition: Let $(a_n)$ be a sequence and let $(A_n)$ be the sequence such that $A_n = \sum^n_{k = 0} a_k$. We say $(A_n)$ is a **series**. We refer to terms of $(A_n)$ as **partial sums**.

**Divergence Test**: If $\sum^\infty_{n = 1} a_n$ converges, then $a_n \to 0$.

**p-series Test**: The series $\sum^\infty_{n = 1} \frac{1}{n^p}$:
- converges when $p > 1$;
- diverges when $0 < p \le 1$.

Geometric Series: $a, ar, ar^2, ar^3, \dots$ converges if and only if $|r| < 1$.

**Geometric Series Test**: The geometric series $a + ar + ar^2 + ar^3 + ar^4 + \dots$ converges if and only if $|r| < 1$.

**Limit Ratio Test**: Let $(a_n)$ be a sequence, and $\frac{a_{n + 1}}{a_n} \to r$.

1. If $|r| < 1$, then the series converges.
2. If $|r| > 1$, then the series diverges.
3. If $|r| = 1$, the test is not conclusive.

**Alternating Series Test**: Let $(b_n)$ be a monotone decreasing sequence so that $b_n \to 0$. The alternating series $b_0 - b_1 + b_2 - b_3 + b_4 - b_5 + \dotsb$ converges.
