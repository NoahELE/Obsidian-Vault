---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, April 8th 2022, 1:56:51 pm
---

# UML

Unified Modeling Language (UML): a graphical modeling language that can be used to represent object oriented analysis, design and implementation.

- `+` Public
- `~` Package
- `#` Protected
- `-` Private

Four types of common relationships:

- Association
- Generalization (Inheritance)
- Realization (Interfaces)
- Dependency

## Association

- Represents a has-a (containment) relationship between objects.
- Allows objects to delegate tasks to other objects.
- Shown by a solid line between classes.

### Properties of Association

- Name
- Role labels
- Directional
    - Unidirectional (hierarchical, ownership)
    - Bidirectional (co-operation)
- Multiplicity
- Type
    - Plain association
    - Aggregation
    - Composition

#### Multiplicity

specifies the number of links that can exist between instances (objects) of the associated classes.

- Indicates how many objects of one class relate to one object of another class
- Can be a single number or a range of numbers
- We can add multiplicity on either end of class relationship by simply indicating it next to the class

One class can be related to another in the following ways:

- One-to-one
- One-to-many
- One-to-one or more
- One-to-zero or one
- One-to-a bounded interval (one-to-two through twenty)
- One-to-exactly n
- One-to-a set of choices (one-to-five or eight)

Multiplicity can be expressed as:

- Exactly one - 1
- Zero or one - 0..1
- Many - 0.._or_
- One or more - 1..\*
- Exact Number - e.g. 3..4 or 6
- Or a complex relationship – e.g. 0..1, 3..4, 6..\* would mean any number of objects other than 2 or 5

Multiple Associations: express the multiple relationships between **classes**.

### Association - Type (Aggregation)

Different form of association, where one class “has” another class, but

both exist independently.

### Association - Type (Composition)

Different form of association, indicating one class cannot exist without the other; in other words, existing on its own doesn’t make sense.

## Generalization - Inheritance

### Abstract Classes

_Italic_ methods or classes are abstract.

## Realization - Interfaces

## Dependency

Dependency represents a weak relationship between classes; dependency implies that a change to one class may impact the other class. It is represented by a dotted arrow.
