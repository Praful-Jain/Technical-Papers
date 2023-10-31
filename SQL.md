# SQL
- It is a programming language specifically designed to create, update and share databases.

## SQL Data-types
1) Numeric - INT, DECIMAL(p, s), NUMERIC(p, s), FLOAT, REAL
2) Character/String - CHAR(n), VARCHAR(n), TEXT
3) Date and Time Data Types -DATE, TIME, DATETIME, TIMESTAMP
4) Boolean Data Type- BOOL or BOOLEAN
5) Miscllaneous - JSON, XML

## SQL Constraints
1) PRIMARY KEY Constraint: Ensures that each row in a table is uniquely identified. It enforces the uniqueness and non-null property for a specific column or set of columns.
2) UNIQUE Constraint: Ensures that all values in a column (or a set of columns) are unique. Unlike the primary key, a table can have multiple unique constraints.
3) NOT NULL Constraint: Ensures that a column cannot contain any NULL values.
4) CHECK Constraint: Restricts the values that can be inserted into a column based on a logical expression. It allows for custom-defined rules to be enforced on the data.
5) FOREIGN KEY Constraint: Establishes a relationship between data in two tables. It ensures referential integrity, meaning values in one table must exist in another table.
6) DEFAULT Constraint: Sets a default value for a column when no value is specified during an insert operation.

## SQL Command Groups
1) DDL (Data Definition Language):
   - DDL is used to define the structure of a database and database objects.
   - It includes commands such as CREATE, ALTER, and DROP, which are used to create and modify database objects like tables, views, indexes, and schemas.
   - CREATE: Used to create new databases, tables, views, indexes, or other database objects.
   - ALTER: Used to modify the structure of existing database objects.
   - DROP: Used to delete or remove database objects, such as tables or indexes.

2) DML (Data Manipulation Language):
   - DML is used for managing data within the database.
   - It includes commands such as SELECT, INSERT, UPDATE, and DELETE, which are used to retrieve, insert, modify, and delete data from a database table.
   - SELECT: Used to retrieve data from one or more database tables.
   - INSERT: Used to add new rows of data into a table.
   - UPDATE: Used to modify existing data within a table.
   - DELETE: Used to remove rows of data from a table.
   - MERGE: Used to perform insert, update, or delete operations on a target table based on the results of a join with a source table.

3) DCL (Data Control Language): 
   - DCL is used to control access to data within the database.
   - It includes commands such as GRANT and REVOKE, which are used to grant or revoke privileges and permissions to users or roles in a database.
   - GRANT: Used to provide specific privileges to a user or role, allowing them to perform specific actions on the database objects.
   - REVOKE: Used to revoke previously granted privileges from a user or role, restricting their access to specific database objects.

## SQL Operations
1. Joins:
   - INNER JOIN: Retrieves records that have matching values in both tables.
   - LEFT JOIN and RIGHT JOIN: Retrieve records from one table even if there are no matches in the other table.
   - FULL JOIN: Retrieves all records when there is a match in either the left or right table.
2. Aggregation:
   - COUNT: Counts the number of rows that meet a specific condition.
   - SUM, AVG, MIN, MAX: Calculates the sum, average, minimum, and maximum values of a specific column.

3. Sorting:
   - ORDER BY: Sorts the result set by one or more columns in ascending or descending order.

4. Grouping:
   - GROUP BY: Groups the result set by one or more columns.
   - HAVING: Filters the result set based on the groups created by the GROUP BY clause.

5. Subqueries:
   - Nested SELECT statements: Perform queries within queries.

6. Constraints:
   - WHERE: Filters data based on specific conditions.
   - LIKE: Performs pattern matching for character strings.
   - BETWEEN: Filters data within a range.
