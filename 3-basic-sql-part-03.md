
### Tables: employees and departments

**employees Table**

| id | name    | age | department_id |
|----|---------|-----|---------------|
| 1  | Alice   | 30  | 1             |
| 2  | Bob     | 32  | 2             |
| 3  | Charlie | 28  | NULL          |

**departments Table**

| id | department_name |
|----|------------------|
| 1  | HR              |
| 2  | IT              |
| 3  | Marketing       |

---

### INNER JOIN: Return matching records from both tables
```sql
SELECT employees.name, departments.department_name 
FROM employees 
INNER JOIN departments ON employees.department_id = departments.id;
```

**Output:**

| name  | department_name |
|-------|------------------|
| Alice | HR              |
| Bob   | IT              |

---

### LEFT JOIN: Return all records from the left table, with matching records from the right
```sql
SELECT employees.name, departments.department_name 
FROM employees 
LEFT JOIN departments ON employees.department_id = departments.id;
```

**Output:**

| name    | department_name |
|---------|------------------|
| Alice   | HR              |
| Bob     | IT              |
| Charlie | NULL            |

---

### RIGHT JOIN: Return all records from the right table, with matching records from the left
```sql
SELECT employees.name, departments.department_name 
FROM employees 
RIGHT JOIN departments ON employees.department_id = departments.id;
```

**Output:**

| name    | department_name |
|---------|------------------|
| Alice   | HR              |
| Bob     | IT              |
| NULL    | Marketing       |

---

### FULL JOIN: Combine all records from both tables
```sql
SELECT employees.name, departments.department_name 
FROM employees 
FULL OUTER JOIN departments ON employees.department_id = departments.id;
```

**Output:**

| name    | department_name |
|---------|------------------|
| Alice   | HR              |
| Bob     | IT              |
| Charlie | NULL            |
| NULL    | Marketing       |

---

### Data Manipulation

#### INSERT INTO: Add new records to a table
```sql
INSERT INTO employees (id, name, age) VALUES (4, 'Dave', 26);
```

**employees Table After Insert:**

| id | name    | age | department_id |
|----|---------|-----|---------------|
| 1  | Alice   | 30  | 1             |
| 2  | Bob     | 32  | 2             |
| 3  | Charlie | 28  | NULL          |
| 4  | Dave    | 26  | NULL          |

---

#### UPDATE: Modify existing records
```sql
UPDATE employees SET age = 31 WHERE id = 1;
```

**employees Table After Update:**

| id | name    | age | department_id |
|----|---------|-----|---------------|
| 1  | Alice   | 31  | 1             |
| 2  | Bob     | 32  | 2             |
| 3  | Charlie | 28  | NULL          |

---

#### DELETE: Remove records
```sql
DELETE FROM employees WHERE age < 25;
```

**employees Table After Delete:**

| id | name    | age | department_id |
|----|---------|-----|---------------|
| 1  | Alice   | 31  | 1             |
| 2  | Bob     | 32  | 2             |
| 3  | Charlie | 28  | NULL          |

---

### Advanced Clauses

#### HAVING: Filter groups after aggregation
```sql
SELECT department_id, COUNT(*) 
FROM employees 
GROUP BY department_id 
HAVING COUNT(*) > 1;
```

**Output:**

| department_id | COUNT(*) |
|---------------|----------|
| 2             | 1        |

---

#### UNION/UNION ALL: Combine results from multiple queries
```sql
SELECT name FROM employees 
UNION 
SELECT name FROM managers;
```

**Output:**

| name    |
|---------|
| Alice   |
| Bob     |
| Charlie |

---

#### SUBQUERIES: Nest queries within queries
```sql
SELECT name FROM employees 
WHERE age > (SELECT AVG(age) FROM employees);
```

**Output:**

| name |
|------|
| Bob  |

---

#### CASE: Conditional logic within queries
```sql
SELECT name, 
  CASE 
    WHEN age < 30 THEN 'Young' 
    ELSE 'Experienced' 
  END AS experience_level 
FROM employees;
```

**Output:**

| name    | experience_level |
|---------|-------------------|
| Alice   | Experienced      |
| Bob     | Experienced      |
| Charlie | Young            |

 
