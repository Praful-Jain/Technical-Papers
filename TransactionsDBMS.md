# Transaction

- It is a set of operations used to perform a logical unit of work.
- A transaction generally represent change in database
- Operations in a transaction
  - READ : Database access.
  - WRITE : Make changes in database
 

## ACID Properties
### 1) Atomicity:
- It states that all operations of the transaction take place at once; if not, the transaction is aborted.
- There is no midway, i.e., the transaction cannot occur partially. Each transaction is treated as one unit and either runs to execution or is not executed at all.
- The transaction management component ensures atomicity in a DBMS.
  
### 2) Consistency
- This property states that the database should remain consistent after every transaction, i.e., the transaction is used to transform the database from one consistent state to another consistent state.
  
### 3) Isolation
- It means that if data is being used in the execution of a particular transaction, it cannot be used by a second transaction at the same time. It has to wait until the first transaction is completed.
- The concurrency control component ensures isolation in the DBMS.
  
### 4) Durability
- It states that the changes made by a transaction in a database remain there permanently. They cannot be lost by faulty transactions or system failures.
- When a transaction is completed, then the database reaches a state known as the consistent state. That consistent state cannot be lost, even in the event of a system's failure.
- The recovery management component ensures durability in DBMS.
