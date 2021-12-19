# Relational Model & Translating ER diagrams

Data Model allows us to translate real world things into structures that a computer can store.

Many models: Relational, ER, O-O, Network, Hierarchical, etc.

Relational Model:

- Rows & Columns (Tuples/records and Attributes/fields)
- Keys & Foreign Keys to link Relations

## Relational database

**Relational database**: a set of relations.

**Relation**: made up of 2 parts:

- **Schema** : specifies name of relation, plus name and type of each column (attribute).
- **Instance** : a table, with rows and columns.
    - rows = cardinality
    - fields = degree (or arity)

### Logical Design: ER to Relational Model

In logical design **entity set** becomes a **relation**.

Attributes become attributes of the relation.

### ER to Logical to Physical

In physical design we choose data types

### Creating Relations in SQL

Example: Creating the Students relation.

```sql
CREATE TABLE Students
    (sid CHAR(20),
    name CHAR(20),
    login CHAR(10),
    age INTEGER,
    gpa FLOAT)
```

## Keys & Integrity Constraints

- Keys are a way to associate tuples in different relations
- Keys are one form of integrity constraint (IC)
- Example: Only students can be enrolled in subjects.

### Primary Keys and Candidate Keys

- A set of fields is a **superkey** if no two distinct tuples can have same values in all key fields
- A set of fields is a **key** for a relation if it is a superkey and no subset of the fields is a superkey (**minimal subset**)
- Out of all keys one is chosen to be the **primary key** of the relation. Other keys are called **candidate keys**
- Each relation has a primary key
- There are possibly many candidate keys (specified using UNIQUE), one of which is chosen as the primary key. Keys must be chosen carefully.

### Foreign Keys & Referential Integrity

- **Foreign key** : A set of fields in one relation that is used to ‘refer’ to a tuple in another relation. Foreign key must correspond to the primary key of the other relation.
- If all foreign key constraints are enforced in a DBMS, we say **referential integrity** is achieved.

### Integrity Constraints (IC)

- IC: condition that must be true for any instance of the database; e.g., domain constraints.
    - ICs are specified when schema is defined.
    - ICs are checked when relations are modified.
- A legal instance of a relation is one that satisfies all specified ICs.
    - DBMS should not allow illegal instances.

## Translating ER to Logical and Physical Model

Multi-valued attributes need to be unpacked (flattened) when converting to logical design. _There is an alternative of creating a lookup table._

Composite attributes need to be unpacked (flattened) when converting to logical design.

In translating a many-to-many relationship set to a relation, attributes of a new relation must include:

1. Keys for each participating entity set (as foreign keys). This set of attributes forms a superkey of the relation.
2. All descriptive attributes.
