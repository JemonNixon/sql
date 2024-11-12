### Table: `employees`

| id | name    | age | department | salary |
|----|---------|-----|------------|--------|
| 1  | Alice   | 25  | HR         | 50000  |
| 2  | Bob     | 32  | IT         | 60000  |
| 3  | Charlie | 29  | IT         | 55000  |

---

### COUNT: Count the number of records

```sql
SELECT COUNT(*) FROM employees;
```

**Output:**

| COUNT(*) |
|----------|
| 3        |

---

### SUM: Add values

```sql
SELECT SUM(salary) FROM employees;
```

**Output:**

| SUM(salary) |
|-------------|
| 165000      |

---

### AVG: Calculate average

```sql
SELECT AVG(salary) FROM employees;
```

**Output:**

| AVG(salary) |
|-------------|
| 55000       |

---

### MIN/MAX: Find minimum and maximum values

```sql
SELECT MIN(salary), MAX(salary) FROM employees;
```

**Output:**

| MIN(salary) | MAX(salary) |
|-------------|-------------|
| 50000       | 60000       |

---

### GROUP BY: Group results by one or more columns

```sql
SELECT department, COUNT(*) FROM employees GROUP BY department;
```

**Output:**

| department | COUNT(*) |
|------------|----------|
| HR         | 1        |
| IT         | 2        |
