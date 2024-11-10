
1. **SQL Create DB**  
   - **Definition**: Creates a new database.
   - **SQL Code**:
     ```sql
     CREATE DATABASE my_database;
     ```
   - **Output**: A new empty database named `my_database` is created. No visual output for the table yet.

---

2. **SQL Drop DB**  
   - **Definition**: Deletes an existing database.
   - **SQL Code**:
     ```sql
     DROP DATABASE my_database;
     ```
   - **Output**: The database `my_database` is deleted. No table output here.

---

3. **SQL Backup DB**  
   - **Definition**: Backups the database to save a copy (usually no direct table output).
   - **SQL Code**:
     ```sql
     BACKUP DATABASE my_database TO DISK = 'backup_path';
     ```
   - **Output**: Database `my_database` is saved to the specified path. No visual output here.

---

4. **SQL Create Table**  
   - **Definition**: Creates a new table called `employees` with columns `id`, `name`, and `age`.
   - **SQL Code**:
     ```sql
     CREATE TABLE employees (
       id INT PRIMARY KEY,
       name VARCHAR(50),
       age INT
     );
     ```
   - **Output**: An empty `employees` table is created.

     | id | name | age |
     |----|------|-----|
     |    |      |     |

---

5. **SQL Drop Table**  
   - **Definition**: Deletes a table and all its data.
   - **SQL Code**:
     ```sql
     DROP TABLE employees;
     ```
   - **Output**: The `employees` table is deleted. No table to show here.

---

6. **SQL Alter Table**  
   - **Definition**: Adds a new column `email` to the existing `employees` table.
   - **SQL Code**:
     ```sql
     ALTER TABLE employees
     ADD email VARCHAR(50);
     ```
   - **Output**: The `employees` table now has an additional `email` column.

     | id | name | age | email |
     |----|------|-----|-------|
     |    |      |     |       |

---

7. **SQL Constraints**  
   - **Definition**: Adds a NOT NULL constraint to ensure a column cannot have a NULL value.
   - **SQL Code**:
     ```sql
     CREATE TABLE students (
       id INT PRIMARY KEY,
       name VARCHAR(50) NOT NULL
     );
     ```
   - **Output**: A `students` table is created where the `name` column must have a value.

     | id | name |
     |----|------|
     |    |      |

---

8. **SQL Not Null**  
   - **Definition**: Ensures a column (e.g., `name` in `products` table) cannot be NULL.
   - **SQL Code**:
     ```sql
     CREATE TABLE products (
       product_id INT PRIMARY KEY,
       name VARCHAR(50) NOT NULL
     );
     ```
   - **Output**: A `products` table is created with a `name` column that cannot be empty.

     | product_id | name |
     |------------|------|
     |            |      |

---

9. **SQL Unique**  
   - **Definition**: Ensures all values in the `email` column of the `customers` table are unique.
   - **SQL Code**:
     ```sql
     CREATE TABLE customers (
       customer_id INT PRIMARY KEY,
       email VARCHAR(50) UNIQUE
     );
     ```
   - **Output**: A `customers` table with a unique `email` column.

     | customer_id | email |
     |-------------|-------|
     |             |       |

---

10. **SQL Primary Key**  
    - **Definition**: Defines a unique identifier for each record in the `orders` table.
    - **SQL Code**:
      ```sql
      CREATE TABLE orders (
        order_id INT PRIMARY KEY,
        order_date DATE
      );
      ```
    - **Output**: An `orders` table where each `order_id` is unique.

      | order_id | order_date |
      |----------|------------|
      |          |            |

---

11. **SQL Foreign Key**  
    - **Definition**: Links a column in one table to the primary key of another, creating a relationship.
    - **SQL Code**:
      ```sql
      CREATE TABLE order_details (
        order_id INT,
        product_id INT,
        FOREIGN KEY (order_id) REFERENCES orders(order_id)
      );
      ```
    - **Output**: An `order_details` table, where `order_id` references `orders.order_id`.

      | order_id | product_id |
      |----------|------------|
      |          |            |
