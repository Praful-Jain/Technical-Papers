# Lock Based Protocol
- To achieve consistency, isolation is the most important idea. Locking is the simplest idea to achieve isolation ie., first obtain a lock
  on a data item then perform a desired operation and then unlock it.
- To provide better concurrency along with isolation we use different modes of locks.

## Shared mode:
- It is denoted by lock-S(Q).
- The transaction can perform READ operation, any other transaction can also obtain same lock on same data item at same time.

## Exclusive mode:
- It is denoted by lock-X(Q).
- The transaction can perform both READ/WRITE operations, any other transaction can not obtain either Shared/Exclusive lock.

## Properties of Lock Based Protocol:
### 1. Concurrency Control:
- Lock-based protocols are designed to manage the concurrent execution of transactions, allowing multiple transactions to access the database simultaneously while maintaining data consistency.

### 2. Isolation:
- Locks help in isolating transactions from each other, ensuring that the operations of one transaction do not interfere with the operations of another. This helps maintain the integrity of the database.

### 3. Atomicity:
- Locks contribute to the atomicity of transactions. Transactions are treated as indivisible units of work, and locks help ensure that either the entire transaction is completed or none of its operations are performed.

### 4. Consistency:
- Locks play a crucial role in maintaining the consistency of the database. They prevent concurrent transactions from interfering with each other in a way that could lead to inconsistent or incorrect data.

### 5. Deadlock Prevention and Detection:
- Lock-based protocols include mechanisms for preventing and detecting deadlocks. Deadlocks occur when two or more transactions are waiting for each other to release resources, leading to a cycle of waiting. Techniques such as timeout mechanisms and deadlock detection algorithms help in managing deadlocks.
