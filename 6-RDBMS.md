### Basic RDBMS (Relational Database Management Systems)

1. **Primary and Foreign Keys**:
   - **Primary Key**: A unique identifier for each record in a table. Primary keys ensure that each row in the table is distinct and prevent duplicate entries.
   - **Foreign Key**: A field in one table that uniquely identifies a row of another table. It’s used to establish and enforce a link between the data in the two tables.

2. **Indexes**:
   - **Index**: A database object that improves the speed of data retrieval operations on a database table at the cost of additional storage and slower writes. Indexes are typically created on columns that are frequently used in search conditions (`WHERE`, `JOIN`).
   - **Types of Indexes**: Common types include `Unique Index` (ensures all values are unique) and `Non-Unique Index`.

3. **Normalization**:
   - **Normalization**: The process of organizing a database to reduce redundancy and improve data integrity. It involves dividing a database into tables and defining relationships between the tables.
   - **Normal Forms**:
     - **1NF (First Normal Form)**: Eliminate duplicate columns in the table and create separate tables for each group of related data.
     - **2NF (Second Normal Form)**: Meet all requirements of 1NF and move data that is partially dependent on the primary key to other tables.
     - **3NF (Third Normal Form)**: Meet all requirements of 2NF and remove columns that are not directly dependent on the primary key.

4. **Transactions and ACID Properties**:
   - **Transaction**: A unit of work in a database that is executed as a single operation. Transactions ensure that the database remains in a consistent state.
   - **ACID Properties**:
     - **Atomicity**: Ensures that all operations within a transaction are completed successfully. If not, the transaction is aborted.
     - **Consistency**: Ensures that a transaction brings the database from one valid state to another valid state.
     - **Isolation**: Ensures that concurrent transactions do not interfere with each other.
     - **Durability**: Guarantees that once a transaction is committed, it remains so, even in the event of a system failure.

5. **Database Relationships**:
   - **One-to-One**: Each row in Table A is linked to only one row in Table B, and vice versa.
   - **One-to-Many**: Each row in Table A can be related to multiple rows in Table B, but each row in Table B is related to only one row in Table A.
   - **Many-to-Many**: Rows in Table A can relate to multiple rows in Table B and vice versa. This relationship often requires an intermediary table (a "junction" or "bridge" table).

6. **Data Integrity Constraints**:
   - **NOT NULL**: Ensures that a column cannot have a NULL value.
   - **UNIQUE**: Ensures all values in a column are unique.
   - **CHECK**: Enforces a condition on each row in the table, ensuring all values in a column meet specific criteria.
   - **DEFAULT**: Assigns a default value to a column if no value is specified.

7. **Stored Procedures and Triggers**:
   - **Stored Procedure**: A set of SQL statements that can be stored and executed on demand. Useful for complex queries and repetitive tasks.
   - **Trigger**: A set of actions that are automatically executed in response to certain events on a table, like `INSERT`, `UPDATE`, or `DELETE`.

8. **Views**:
   - **View**: A virtual table based on the result-set of an SQL query. Views simplify complex queries and can restrict access to specific data by providing a controlled perspective of a table.

---

RBDMS's quick summary of how each area contributes to a data analysis role:

- **Primary and Foreign Keys**: Essential for understanding relational database structures and ensuring data integrity when joining tables.
- **Indexes**: Helpful in optimizing queries, which is crucial when working with large datasets.
- **Normalization**: Aids in designing efficient databases, reducing redundancy, and improving query performance.
- **Transactions and ACID Properties**: Ensures data reliability and consistency, especially when dealing with multiple updates.
- **Database Relationships**: Key for structuring data, which allows you to model real-world relationships in data analysis projects.
- **Data Integrity Constraints**: Important for maintaining clean, valid data.
- **Stored Procedures and Triggers**: Useful for automating repetitive tasks and ensuring certain actions take place in response to data changes.
- **Views**: Great for simplifying complex queries, creating reusable query components, and restricting data access.
 
