# Normalization

## Anomalies

- Insertion Anomaly
- Deletion Anomaly
- Update Anomaly

## Definitions

**Normalization**: A technique used to remove undesired redundancy from databases (Break one large table into several smaller tables).

### Functional Dependency

A functional dependency concerns values of

attributes in a relation

A set of attributes X determines another set of

attributes Y if each value of X is associated with only

one value of Y

- Written $X \rightarrow Y$
    - X determines Y (If I know X then I also know Y)

**Determinants** ($X, Y \rightarrow Z$): the attribute(s) on the left hand side of the arrow

**Key and Non-Key attributes**: each attribute is either part of the primary key or it is not

**Partial functional dependency** ($Y \rightarrow Z$): a functional dependency of one or more non-key attributes upon part (but not all) of the primary key

**Transitive dependency** ($Z \rightarrow D$): a functional dependency between 2 (or more) non-key attributes

## Armstrong’s Axioms

$A = (X_1,\ X_2,\ ...,\ X_n)$ and $B = (Y_1,\ Y_2,\ ...,\ Y_n)$

1. Reflexivity: $B \subseteq A \Rightarrow A \rightarrow B$
2. Augmentation: $A \rightarrow B \Rightarrow AC \rightarrow BC$
3. Transitivity: $A \rightarrow B\ and\ B \rightarrow C \Rightarrow A \rightarrow C$

## Steps of Normalization

A relation is normalized if all determinants are candidate keys

- First Normal Form(1NF): Keep atomic data/Remove repeating groups
- Second Normal Form(2NF): Remove partial dependencies
- Third Normal Form(3NF): Remove transitive dependencies

## Normalization vs Denormalization

Normalization:

- Normalized relations contains a minimum amount of redundancy and allow users to insert, modify, and delete rows in tables without errors or inconsistencies (anomalies)

Denormalization:

- The pay-off: query speed.
- The price: extra work on updates to keep redundant data consistent.
- Denormalization may be used to improve performance of time-critical operations.

