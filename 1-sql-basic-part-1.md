### Table: `employees`

| id | name    | age | department |
|----|---------|-----|------------|
| 1  | Alice   | 25  | HR         |
| 2  | Bob     | 32  | IT         |
| 3  | Charlie | 29  | IT         |

---

### SELECT: Select all data from a table

```sql
SELECT * FROM employees;
```

**Output:**

| id | name    | age | department |
|----|---------|-----|------------|
| 1  | Alice   | 25  | HR         |
| 2  | Bob     | 32  | IT         |
| 3  | Charlie | 29  | IT         |

---

### WHERE: Filter records based on conditions

```sql
SELECT * FROM employees WHERE age > 30;
```

**Output:**

| id | name | age | department |
|----|------|-----|------------|
| 2  | Bob  | 32  | IT         |

---

### ORDER BY: Sort query results

```sql
SELECT * FROM employees ORDER BY name ASC;
```

**Output:**

| id | name    | age | department |
|----|---------|-----|------------|
| 1  | Alice   | 25  | HR         |
| 2  | Bob     | 32  | IT         |
| 3  | Charlie | 29  | IT         |

---

### DISTINCT: Remove duplicate values

```sql
SELECT DISTINCT department FROM employees;
```

**Output:**

| department |
|------------|
| HR         |
| IT         |

---

### LIMIT: Restrict the number of rows returned

```sql
SELECT * FROM employees LIMIT 2;
```

**Output:**

| id | name  | age | department |
|----|-------|-----|------------|
| 1  | Alice | 25  | HR         |
| 2  | Bob   | 32  | IT         |

---
