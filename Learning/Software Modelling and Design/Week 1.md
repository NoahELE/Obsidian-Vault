---
date created: Monday, July 25th 2022, 2:23:48 pm
date modified: Monday, July 25th 2022, 3:05:09 pm
---

# Week 1

## Definitions

- SuD: System-under-Discussion
- Actor: something with behaviour, such as a person, computer system or organisation (e.g. a cashier)
- Scenario (or use case instance): a specific sequence of actions and interactions between actors and the SuD
- Use case: a collection of related success and failure scenarios that describe an actor using the SuD to support a goal

## Three Kinds of Actors

- Primary actor has user goals fulfilled through using services of the SuD (e.g. the cashier)
    - User goals drive the use case
- Supporting actor provides a service (e.g. information) to the SuD to clarify external interfaces and protocols (e.g. an automated payment authorization service)
    - Usually be a computer system but could be an organization or person
- Offstage actor has an interest in the behaviour of the use case, but is not primary or supporting (e.g. a government tax agency)
    - Ensure all interests identified/satisfied

## Use-Case Model

- A model of the system’s functionality and environment
    - Primarily includes the set of all written use cases
    - Optionally includes a UML use case diagram

## UML Use-Case Diagram

- A UML use case diagrams gives a context diagram of a system and its environment
    - Showing the names of use cases, actors and their relationships

## Finding Useful Use Cases

- Boss Test
    - If your boss asks: “What have you been doing all day?” and you reply: “Logging in!”, will your boss be happy?
- Elementary Business Process (EBP) Test
    - A task performed by one person in one place at one time, in response to a business event, which adds measurable business value and leaves the data in a consistent state.
- Size Test
    - Is a task very seldom a single action/step; typically many steps; fully dressed often require 3–10 pages of text
