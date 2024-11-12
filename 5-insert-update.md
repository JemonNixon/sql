
### 1. **INSERT** - Adding a new customer to the `Customers` table.

**Input Table: `Customers` (before insert):**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 1          | John Doe     | USA     |
| 2          | Jane Smith   | Canada  |

```sql
INSERT INTO Customers (CustomerID, CustomerName, Country)
VALUES (3, 'Alice Brown', 'UK');
```

**Output Table: `Customers` (after insert):**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 1          | John Doe     | USA     |
| 2          | Jane Smith   | Canada  |
| 3          | Alice Brown  | UK      |

---

### 2. **UPDATE** - Updating an existing customer’s country.

**Input Table: `Customers` (before update):**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 3          | Alice Brown  | UK      |

```sql
UPDATE Customers
SET Country = 'Australia'
WHERE CustomerID = 3;
```

**Output Table: `Customers` (after update):**

| CustomerID | CustomerName | Country    |
|------------|--------------|------------|
| 3          | Alice Brown  | Australia  |

---

### 3. **DELETE** - Removing a customer from the `Customers` table.

**Input Table: `Customers` (before delete):**

| CustomerID | CustomerName | Country    |
|------------|--------------|------------|
| 3          | Alice Brown  | Australia  |

```sql
DELETE FROM Customers
WHERE CustomerID = 3;
```

**Output Table: `Customers` (after delete):**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 1          | John Doe     | USA     |
| 2          | Jane Smith   | Canada  |

---

### 4. **VIEW** - Creating a view to show all customers from the USA.

```sql
CREATE VIEW US_Customers AS
SELECT * FROM Customers
WHERE Country = 'USA';
```

**Output (view result from `US_Customers`):**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 1          | John Doe     | USA     |

---

### 5. **UNION** - Combining `Customers` and `Orders` data for customers in Canada.

**Input Table: `Customers`:**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 2          | Jane Smith   | Canada  |

**Input Table: `Orders`:**

| OrderID | CustomerID | OrderAmount |
|---------|------------|-------------|
| 101     | 2          | 200         |

```sql
SELECT CustomerID, CustomerName, Country 
FROM Customers 
WHERE Country = 'Canada'
UNION
SELECT CustomerID, NULL AS CustomerName, NULL AS Country 
FROM Orders 
WHERE CustomerID = 2;
```

**Output:**

| CustomerID | CustomerName | Country |
|------------|--------------|---------|
| 2          | Jane Smith   | Canada  |
| 2          | NULL         | NULL    |

---

### 6. **HAVING** - Finding customers with total order amounts over 300.

**Input Table: `Orders`:**

| OrderID | CustomerID | OrderAmount |
|---------|------------|-------------|
| 101     | 1          | 200         |
| 102     | 1          | 150         |
| 103     | 2          | 50          |

```sql
SELECT CustomerID, SUM(OrderAmount) AS TotalAmount
FROM Orders
GROUP BY CustomerID
HAVING SUM(OrderAmount) > 300;
```

**Output:**

| CustomerID | TotalAmount |
|------------|-------------|
| 1          | 350         |

---
