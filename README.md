Here are some of the **most common database-related interview questions** that you might encounter:

### 1. **What is the difference between `DELETE`, `TRUNCATE`, and `DROP` in SQL?**
   - **DELETE**: Removes specific rows from a table (can use `WHERE` clause), row deletions are logged, and it can be rolled back. It does not reset identity columns.
   - **TRUNCATE**: Removes all rows from a table but does not log individual row deletions. It resets identity columns, and it is faster than `DELETE` for large datasets.
   - **DROP**: Completely removes the table from the database, along with its structure and data.

### 2. **What are the different types of joins in SQL?**
   - **INNER JOIN**: Returns records with matching values in both tables.
   - **LEFT JOIN (or LEFT OUTER JOIN)**: Returns all records from the left table and matching records from the right table; if there is no match, NULL values are returned for the right table.
   - **RIGHT JOIN (or RIGHT OUTER JOIN)**: Returns all records from the right table and matching records from the left table; if there is no match, NULL values are returned for the left table.
   - **FULL JOIN (or FULL OUTER JOIN)**: Returns all records when there is a match in either left or right table; returns NULLs for non-matching rows.

### 3. **What is normalization? Explain its types.**
   - **Normalization** is the process of organizing data in a database to reduce redundancy and improve data integrity. 
   - **Types**:
     1. **1NF (First Normal Form)**: Eliminate duplicate columns and ensure atomicity (one value per cell).
     2. **2NF (Second Normal Form)**: Meet all the requirements of 1NF and ensure all non-key attributes are fully dependent on the primary key.
     3. **3NF (Third Normal Form)**: Meet all requirements of 2NF and ensure there are no transitive dependencies (non-key attributes should not depend on other non-key attributes).
     4. **BCNF (Boyce-Codd Normal Form)**: A stronger version of 3NF where every determinant must be a candidate key.

### 4. **What is a primary key? What is a foreign key?**
   - **Primary Key**: A column (or combination of columns) that uniquely identifies each row in a table. It does not allow NULL values.
   - **Foreign Key**: A column in one table that is a primary key in another table, used to enforce a relationship between the two tables.

### 5. **What are indexes in SQL?**
   - An **index** is a database object that improves the speed of data retrieval operations on a table. It works like an index in a book, allowing quick lookups of data.
   - **Types of indexes**:
     - **Clustered Index**: Sorts and stores the rows of the table based on the key values. A table can have only one clustered index.
     - **Non-clustered Index**: Stores a pointer to the actual data, allowing multiple non-clustered indexes on a table.

### 6. **What is ACID in the context of a database?**
   - **ACID** stands for **Atomicity**, **Consistency**, **Isolation**, and **Durability**:
     - **Atomicity**: Transactions are all-or-nothing; either all operations succeed or none do.
     - **Consistency**: Transactions bring the database from one valid state to another, maintaining data integrity.
     - **Isolation**: Transactions are executed independently, without interference from other transactions.
     - **Durability**: Once a transaction is committed, the changes are permanent, even in the event of a system crash.

### 7. **What is the difference between SQL and NoSQL databases?**
   - **SQL (Structured Query Language)** databases are relational databases that use structured data and a predefined schema. Examples include MySQL, PostgreSQL, and SQL Server.
   - **NoSQL (Not Only SQL)** databases are non-relational databases that work with unstructured or semi-structured data and flexible schemas. Examples include MongoDB, Cassandra, and Redis.

### 8. **What is a view in SQL?**
   - A **view** is a virtual table based on the result of a SQL query. It does not store data itself but presents data from one or more tables in a specific format. Views can be used to simplify complex queries, enhance security by restricting access to specific data, and provide abstraction.

### 9. **What is the difference between `HAVING` and `WHERE`?**
   - **WHERE**: Filters rows before the aggregation of data and can be used with any condition.
   - **HAVING**: Filters data after aggregation and is used with aggregate functions like `COUNT()`, `SUM()`, etc.

### 10. **What is a transaction? What is a commit and rollback?**
   - A **transaction** is a sequence of operations performed as a single logical unit of work. Transactions ensure that the database remains in a consistent state.
   - **COMMIT**: Saves all changes made by the transaction to the database.
   - **ROLLBACK**: Reverts all changes made by the transaction to the last committed state, undoing any modifications.

### 11. **What is a deadlock in a database? How can it be avoided?**
   - A **deadlock** occurs when two or more transactions are waiting for each other to release locks on resources, causing them to remain blocked indefinitely.
   - Deadlock can be avoided by:
     - Ensuring that transactions lock resources in the same order.
     - Implementing timeouts or deadlock detection mechanisms.
     - Keeping transactions short and minimizing the locking of resources.

### 12. **Explain the difference between INNER JOIN and OUTER JOIN.**
   - **INNER JOIN**: Returns only the rows that have matching values in both tables.
   - **OUTER JOIN**: Returns all rows from one or both tables, and fills in NULLs for missing matches:
     - **LEFT OUTER JOIN**: Returns all rows from the left table and the matched rows from the right table.
     - **RIGHT OUTER JOIN**: Returns all rows from the right table and the matched rows from the left table.
     - **FULL OUTER JOIN**: Returns all rows when there is a match in either the left or right table.

### 13. **What is the difference between `CHAR` and `VARCHAR`?**
   - **`CHAR(n)`**: A fixed-length string where the length is always the specified `n`. If the actual data is shorter, it will be padded with spaces.
   - **`VARCHAR(n)`**: A variable-length string where the length is up to `n`. It only uses the space necessary for the data and does not pad with spaces.

### 14. **What are stored procedures?**
   - A **stored procedure** is a set of precompiled SQL statements stored in the database that can be executed as a single unit. Stored procedures allow for code reusability, improved performance (as they are precompiled), and reduced client-server traffic.

### 15. **What is denormalization?**
   - **Denormalization** is the process of introducing redundancy into a database to improve read performance by reducing the need for complex joins. It is the opposite of normalization and is often used in data warehousing or reporting environments to optimize queries.

These questions are frequently asked to assess a candidate's understanding of database fundamentals, SQL, and their ability to optimize and manage database operations effectively.