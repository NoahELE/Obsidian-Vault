# Transactions

## SQL Keywords

```SQL
BEGIN; (or START TRANSACTIONS;)
some sql statement
some sql statement
COMMIT; (or ROLLBACK;)
```

## Possible Problems

- lost updates
- uncommitted data
- inconsistent retrievals

True Serializations: no concurrency (**seldom used**)

## Concurrency Control

- Locking - main
- Time Stamping - alternative
- Optimistic Concurrency control - alternative

### Lock

- Guarantees exclusive use of a data item to a current transaction
  - T1 acquires a lock prior to data access, the lock is released when the transaction is done
  - T2 does not have access to data item currently being used by T1
  - T2 has to wait until T1 release the lock
- Lock Manager
  - responsible for assigning and policing the locks used by the transactions

#### Lock Options

- database-level lock
- table-level lock
- page-level lock
- row-level lock
- field-level lock

#### Types of Locks

- Binary Locks
  - has only two states, 'locked' or 'unlocked'
  - eliminates lost updates problem
  - too restrictive --- even locked for two concurrent READs
- Exclusive Locks
  - Access is reserved for the transaction which locks the object
  - **Must** be used when WRITE
  - Granted *if and only* if there is no other locks on the object
  - In MySQL, `SELECT ... FOR UPDATE`
- Shared Locks
  - Other transactions are also granted `READ` access
  - Issued when a transaction wants to `READ` the object and there is no exclusive lock on the object
  - In MySQL, `SELECT ... FOR SHARE`

#### Dead Lock

- occurs when two transactions both waits for each other to unlock data
  - T1 locks X and wants Y; T2 locks Y and wants X;
  - could wait forever
- only happens with exclusive lock
- dealt with by:
  - Prevention
  - Detection
