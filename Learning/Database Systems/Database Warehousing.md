# Database Warehousing

To solve:

- Duplicated data
- Inaccessible data
- Inconsistent data

A **informational database** rather than a transactional database

A single repository of organisational data

## Supported Analytical Queries

numerical aggregation and dimensions

## Characteristics

- subject oriented
  - organised around certain subjects
- validated and integrated data
  - validated and convert to certain format before storing
- time variant
  - historical data
  - snapshot regularly
- non-volatile _(read only)_
  - all updated done automatically and periodically

## Dimensional Modeling

consists of:
- fact table
- several dimensional tables
- (sometimes) hierarchies in the dimensions

a simple and restricted type of ER Model

Star Schema