---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, April 8th 2022, 1:53:06 pm
---

# Database Development Process

Three Design Process:

- Conceptual
- Logical
- Physical

## Conceptual Design

- Construction of a model of the data used in the database – independent of all physical considerations
- Data Models, like ER model

## Logical Design

- Construction of a (relational) model of the data based on the conceptual design
- Independent of a specific database and other physical considerations
  - e.g. adding foreign keys in the model

## Physical Design

- A description of the implementation of the logical design – for a specific DBMS.
- Describes:
    - Basic Relations (Data Types)
    - File Organization
    - Indices

## Implementation

- The physical realization of the database
- Implementing the design made
