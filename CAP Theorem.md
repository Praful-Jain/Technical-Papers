# CAP Theorem in Databases

- CAP theorem is used to design efficient distributed storages.
- In CAP theorem:
  - C (Consistency) : In distributed storages the data should be exactly same across all the nodes. There should be no dissimilarity.
  - A (Availability) : The system should remain operational all the time. Even if some nodes fail.
  - P (Partition Tolerance) : When a distributed system encounters a partition, it means that there’s a break in communication between nodes. The system should be capable enough to tolerant that partition, the system does not fail.

- CAP theorem states that a distributed system can only provide two of these three properties simultaneously.
- Means when there is a partition in a distributed system, then the system can fulfil only one of the remaining two
  properties either the system can be consistent or remain available.

## CAP THeorem NoSQL Databases
1. CA database -
   - CA databases enable consistency and availability across all nodes.
   - But not practically possible beacuse in any distributed system, partitions are bound to happen.
2. CP Databases -
   - CP databases enable consistency and partition tolerance, but not availability.
   - When any partition occurs, the system has to turn off inconsistent nodes until the partition can be fixed.
   - MongoDB is an example of a CP database :
     - It’s a NoSQL database management system(DBMS) that uses documents for data storage.
     - It’s considered schema-less, which means that it doesn’t require a defined database schema.
     - It’s commonly used in big data and applications running in different locations.
   - The CP system is structured so that there’s only one primary node that receives all of the write
     requests in a given replica set. Secondary nodes replicate the data in the primary nodes, so if the
     primary node fails, a secondary node can stand-in.
   - In banking system Availability is not as important as consistency, so we can opt it(MongoDB).
  
    
3. AP Databases -
   - AP databases enable availability and partition tolerance, but not consistency.
   - Apache Cassandra is an example of an AP database :
     - It’s a NoSQL database with no primary node, meaning that all of the nodes remain available.
     -  Cassandra allows for eventual consistency because users can re-sync their data right after a partition is resolved.
   - For apps like Facebook, we value availability more than consistency, we’d opt for AP Databases like Cassandra or Amazon DynamoDB.
