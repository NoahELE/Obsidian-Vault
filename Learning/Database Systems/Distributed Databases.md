# Distributed Databases

Distributed Database:

- a single logical database physically spread across multiple computers in multiple locations that are connected by a data communications link
- appears to users as though it is one database

Decentralized Database:

- a collection of independent databases which are not networked together as one logical database
- appears to users as though many databases

## Advantages of distributed DBMS

- Good fit for geographically distributed organizations / users
- Data located near site with greatest demand
- Faster data access (to local data)
- Faster data processing
- Allows modular growth
- Increased reliability and availability
- Supports database recovery

## Disadvantages of distributed DBMS

- Complexity of management and control
- Data integrity
- Security
- Lack of standards
- Increased training & maintenance costs
- Increased storage requirements

## Objectives of distributed DBMS

- Location transparency: a user does not need to know where particular data are stored
- Local autonomy: a node can continue to function for local users if connectivity to the network is lost

## Distribution options

Data replication is a process of duplicating data to different nodes.

Data partitioning is the process of partitioning data into subsets that are shipped to different nodes.

### Replication

#### Advantages

- High reliability due to redundant copies of data
- Fast access to data at the location where it is most accessed
- May avoid complicated distributed integrity routines
- Decoupled nodes don’t affect data availability
- Reduced network traffic at prime time
- This is currently popular as a way of achieving high availability for global systems

#### disadvantages

- Need more storage space
- Data Integrity
- Takes time for update operations
- Network communication capabilities

### Partitioning

- Horizontal partitioning

    - Table rows distributed across nodes (sides)
- Vertical partitioning

    - Table columns distributed across nodes (sides)


## Trade-offs

- Availability vs Consistency
- Synchronous vs Asynchronous updates

### Synchronous updates

- Data is continuously kept up to date
- If any copy of a data item is updated anywhere on the network, the same update is immediately applied to all other copies or it is aborted
- Ensures data integrity and minimizes the complexity of knowing where the most recent copy of data is located
- Can result in slow response time and high network usage


### Asynchronous updates

- Some delay in propagating data updates to remote databases
- Acceptable response time
- May be more complex to plan and design
- Suits some information systems more than others
