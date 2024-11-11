 ### 1. **Primary Key**
   - **Definition**: A primary key uniquely identifies each record in a table. It cannot contain `NULL` values and must contain unique values.
   - **Example**:
     ```sql
     CREATE TABLE Employees (
         EmployeeID INT PRIMARY KEY,
         Name VARCHAR(50),
         Department VARCHAR(50)
     );
     ```
   - **Visual**:
     | EmployeeID | Name        | Department |
     |------------|-------------|------------|
     | 1          | John Doe    | HR         |
     | 2          | Jane Smith  | Finance    |

### 2. **Foreign Key**
   - **Definition**: A foreign key is a field (or collection of fields) in one table that uniquely identifies a row in another table. The foreign key links the two tables.
   - **Example**:
     ```sql
     CREATE TABLE Departments (
         DepartmentID INT PRIMARY KEY,
         DepartmentName VARCHAR(50)
     );

     CREATE TABLE Employees (
         EmployeeID INT PRIMARY KEY,
         Name VARCHAR(50),
         DepartmentID INT,
         FOREIGN KEY (DepartmentID) REFERENCES Departments(DepartmentID)
     );
     ```
   - **Visual**:
     - **Departments Table**:
       | DepartmentID | DepartmentName |
       |--------------|----------------|
       | 1            | HR             |
       | 2            | Finance        |
     - **Employees Table**:
       | EmployeeID | Name        | DepartmentID |
       |------------|-------------|--------------|
       | 1          | John Doe    | 1            |
       | 2          | Jane Smith  | 2            |

### 3. **Unique Key**
   - **Definition**: A unique key ensures all values in a column are unique. Unlike a primary key, it can contain a single `NULL` value.
   - **Example**:
     ```sql
     CREATE TABLE Employees (
         EmployeeID INT PRIMARY KEY,
         Email VARCHAR(50) UNIQUE,
         Name VARCHAR(50)
     );
     ```
   - **Visual**:
     | EmployeeID | Email               | Name        |
     |------------|---------------------|-------------|
     | 1          | john@example.com    | John Doe    |
     | 2          | jane@example.com    | Jane Smith  |

### 4. **Composite Key**
   - **Definition**: A composite key is a combination of two or more columns to uniquely identify a row in a table.
   - **Example**:
     ```sql
     CREATE TABLE Orders (
         OrderID INT,
         ProductID INT,
         Quantity INT,
         PRIMARY KEY (OrderID, ProductID)
     );
     ```
   - **Visual**:
     | OrderID | ProductID | Quantity |
     |---------|-----------|----------|
     | 1       | 101       | 5        |
     | 1       | 102       | 3        |

### 5. **Candidate Key**
   - **Definition**: A candidate key is a column, or set of columns, that can uniquely identify a record in a table. A table can have multiple candidate keys, one of which can be chosen as the primary key.
   - **Example**:
     ```sql
     CREATE TABLE Employees (
         EmployeeID INT,
         Email VARCHAR(50),
         PhoneNumber VARCHAR(15),
         UNIQUE (Email),
         UNIQUE (PhoneNumber)
     );
     ```
   - **Visual**:
     | EmployeeID | Email               | PhoneNumber   |
     |------------|---------------------|---------------|
     | 1          | john@example.com    | 123-456-7890  |
     | 2          | jane@example.com    | 098-765-4321  |

### 6. **Alternate Key**
   - **Definition**: An alternate key is any candidate key not chosen as the primary key.
   - **Example**: If `Email` and `PhoneNumber` are candidate keys in the `Employees` table, and `EmployeeID` is the primary key, `Email` and `PhoneNumber` are alternate keys.
 An **Alternate Key** is a candidate key that was not selected as the primary key. In other words, it's an additional column (or set of columns) that could uniquely identify a row in a table but isn't the primary key.

```sql
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    Email VARCHAR(50) UNIQUE,
    PhoneNumber VARCHAR(15),
    Name VARCHAR(50)
);
```

In this case:
- `EmployeeID` is the **Primary Key**.
- `Email` is the **Alternate Key** because it uniquely identifies each row but isn’t the primary key.

#### Input Table (Employees Table)

| EmployeeID | Email               | PhoneNumber | Name       |
|------------|----------------------|-------------|------------|
| 1          | john@example.com     | 123-456-789 | John Doe   |
| 2          | jane@example.com     | 987-654-321 | Jane Smith |
| 3          | alex@example.com     | 555-123-456 | Alex Brown |

 
