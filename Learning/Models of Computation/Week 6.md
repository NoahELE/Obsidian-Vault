---
date created: Thursday, September 1st 2022, 6:21:18 pm
date modified: Friday, September 2nd 2022, 6:05:30 pm
---

# Week 6

## Set Theory

Definition: (Georg Cantor) A set is a collection into a whole of definite, distinct objects of our intuition or of our thought. The objects are called the elements (members) of the set.

### Algebra of Sets

Let $A$ and $B$ be sets. Then

- $A \cap B = \{x \mid x \in A \land x \in B\}$ is the **intersection** of $A$ and $B$
- $A \cup B = \{x \mid x \in A \lor x \in B\}$ is the **union** of $A$ and $B$
- $A \setminus B = \{x \mid x \in A \land x \notin B\}$ is the **difference** of $A$ and $B$
- $A \oplus B = (A \setminus B) \cup (B \setminus A)$ is the **symmetric difference** of $A$ and $B$
- $A^c = X \setminus A$ is the **complement** of $A$

---

- Absorption:
    - $A \cap A = A$
    - $A \cup A = A$
- Commutativity:
    - $A \cap B = B \cap B$
    - $A \cup B = B \cup B$
- Associativity:
    - $A \cap (B \cap C) = (A \cap B) \cap C$
    - $A \cup (B \cup C) = (A \cup B) \cup C$
- Distributivity:
    - $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
    - $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$
- Double complement:
    - $A = (A^c)^c$
- De Morgan:
    - $(A \cap B)^c = A^c \cup B^c$
    - $(A \cup B)^c = A^c \cap B^c$
- Duality:
    - $X^c = \emptyset$
    - $\emptyset^c = X$
- Identity:
    - $A \cup \emptyset = A$
    - $A \cap X = A$
- Dominance:
    - $A \cap \emptyset = \emptyset$
    - $A \cup X = X$
- Complementation:
    - $A \cap A^c = \emptyset$
    - $A \cup A^c = X$

### Ordered Pairs

Define ordered pair as $(a, b) = \{a, \{a, b\}\}$

### Cartesian Product and Tuples

The *Cartesian product* of $A$ and $B$ is defined $A \times B = \{(a, b) \mid a \in A \land b \in B\}$

We define the set $A^n$ of n-tuples over $A$ as follows:

- $A^0 = \{\emptyset\}$
- $A^{n + 1} = A \times A^n$

- $(A \times B) \cap (C \times D) = (A \times D) \cap (C \times B)$
- $(A \cap B) \times C = (A \times C) \cap (B \times C)$
- $(A \cup B) \times C = (A \times C) \cup (B \times C)$
- $(A \cap B) \times (C \cap D) = (A \times C) \cap (B \times D)$
- $(A \cup B) \times (C \cup D) = (A \times C) \cup (A \times D) \cup (B \times C) \cup (B \times D)$

## Binary Relations

A **binary relation** is a set of pairs, or 2-tuples.

We can express membership of a relation in many ways:

- $(x, y) \in R$
- $R(x, y)$
- $x \ R \ y$

### Domain and Range of a Relation

The *domain* of R is $dom(R) = \{x \mid \exists y \ R(x, y)\}$.

The *range* of R is $ran(R) = \{y \mid \exists x \ R(x, y)\}$.

We say that $R$ is a relation from A to B if $dom(R) \subseteq A$ and $ran(R) \subseteq B$. Or, $R$ is a relation between $A$ and $B$.

A relation from $A$ to $A$ is a relation on $A$.

### Identity and Inverse

$A \times B$ is a relation—the *full* relation from $A$ to $B$.

$\emptyset$ is a relation.

$\Delta_A = \{(x, x) \mid x \in A\}$ is a relation on A - the *identity* relation.

If $R$ is a relation from $A$ to $B$ then $R^{−1} = \{(b, a) \mid (a, b) \in R\}$ is a relation from B to A, called the *inverse* of R.

> $(R^{-1})^{-1} = R$

> Since relations are sets, all the set operations, such as $\cap$ and $\cup$, are applicable to relations.

### Properties of Relations

Let A be a non-empty set and let R be a relation on A.

- $R$ is *reflexive* iff $R(x, x)$ for all $x \in A$.
- $R$ is *irreflexive* iff $R(x, x)$ holds for no $x \in A$.
- $R$ is *symmetric* iff $R(x, y) \implies R(y, x)$ for all $x, y \in A$.
- $R$ is *asymmetric* iff $R(x, y) \implies \neg R(y, x)$ for all $x, y \in A$.
- $R$ is *antisymmetric* iff $R(x, y) \land R(y, x) \implies x = y$ for all $x, y \in A$.
- $R$ is *transitive* iff $R(x, y) \land R(y, z) \implies R(x, z)$ for all $x, y, z \in A$.

### Reflexive, Symmetric, Transitive Closures

For any binary relation $R$, there is a *unique smallest* transitive relation $R^+$ which includes $R$.

We call $R^+$ the **transitive closure** of $R$.

Similarly we have the *(unique)* **reflexive** closure and the *(unique)* **symmetric** closure of R.

### Composing Relations

Let $R_1$ and $R_2$ be relations on $A$. The **composition** $R_1 \circ R_2$ is the relation on $A$ defined by $(x, z) \in (R_1 \circ R_2) \iff \exists y \ (R_1(x, y) \land R_2(y, z))$

The n-fold composition $R^n$ is defined by $R^1 = R$ and $R^{n + 1} = R^n \circ R$.

### Equivalence Relations

A binary relation which is *reflexive, symmetric and transitive* is an **equivalence** relation.

The identity relation $\Delta_A$ is the *smallest* equivalence relation on a set $A$. The full relation $A^2$ is the *largest* equivalence relation on $A$.

### Partial Orders

- $R$ is a *pre-order* iff $R$ is transitive and reflexive.
- $R$ is a *strict partial order* iff $R$ is transitive and irreflexive.
- $R$ is a *partial order* iff $R$ is an antisymmetric pre-order.
- $R$ is *linear* iff $R(x, y) \lor R(y, x) \lor x = y$ for all $x, y \in A$.
- A linear partial order is also called a *total order*.
- In a total order, every two elements from A are *comparable*.
