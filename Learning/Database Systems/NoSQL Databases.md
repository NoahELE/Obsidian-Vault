---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, April 8th 2022, 1:51:19 pm
---

# NoSQL Databases

Traditional Relational Databases: Schema on Write

NoSQL: Schema on Read

## Features

- does not use relational model or SQL language
- runs well on distributed servers
- most are open-source
- built for the modern web
- schema-less (implicit schema)
- support schema on read
- no ACID compliant
- eventually consistent
- available all the time (suitable for company like Facebook, Twitter)

## Types

### Key-Value Stores

Key = primary key, Value = anything

Example: Redis

### Document Stores

document is json file

Example: MongoDB

### Columns Families

columns rather than rows stored on disk

related columns grouped together as families

Example: Cassandra

### Graph Databases

a node-and-arc network

graphs are difficult to program in relational database

Example: Neo4j

## ACID Vs BASE

ACID: Atomic, Consistent, Isolated, Durable

BASE: Basically Available, Soft state, Eventual consistency
