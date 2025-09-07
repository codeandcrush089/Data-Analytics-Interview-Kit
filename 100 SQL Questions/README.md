
## Top 100 SQL Interview Questions (With Answers, Examples & Company Context)

---

### 1. **Difference Between WHERE and HAVING Clauses**

**Answer:**
`WHERE` filters rows before aggregation; `HAVING` filters groups after aggregation.
**Example:**

```sql
SELECT department, COUNT(*) AS cnt
FROM employee
WHERE salary > 3000
GROUP BY department
HAVING cnt > 5;
```

**Company/Year:** Common at FAANGs (e.g., Google, Amazon) in 2024–2025 .

---

### 2. **Group By vs Order By**

**Answer:**
`GROUP BY` groups rows for aggregation; `ORDER BY` sorts the result set.
**Example:**

```sql
SELECT department, AVG(salary)
FROM employee
GROUP BY department
ORDER BY AVG(salary) DESC;
```

**Context:** Frequently tested in data analyst interviews (2025) .

---

### 3. **Remove Duplicate Records**

**Answer:**
Use `DISTINCT` or use window functions with `ROW_NUMBER()` for complex cases.
**Example:**

```sql
SELECT DISTINCT department FROM employee;
```

**Context:** Asked in analyst and data engineer interviews (2025) .

---

### 4. **Primary Key vs Foreign Key**

**Answer:**

* **Primary Key**: Unique identifier for each row.
* **Foreign Key**: Links to a primary key in another table.
  **Example:**

```sql
CREATE TABLE Department (
  dept_id INT PRIMARY KEY,
  name VARCHAR(50)
);

CREATE TABLE Employee (
  emp_id INT,
  dept_id INT,
  FOREIGN KEY (dept_id) REFERENCES Department(dept_id)
);
```

**Context:** Core concept—used across major companies (2025) .

---

### 5. **Usage of LIKE Operator**

**Answer:**
Used for pattern matching with `%` and `_`.
**Example:**

```sql
SELECT * FROM employee WHERE name LIKE 'A%'; -- names starting with A
```

**Context:** Basic filtering in interviews for analysts (2025) .

---

### 6. **Types of SQL JOINs**

**Answer:**
Support INNER, LEFT, RIGHT, FULL, CROSS joins.
**Example:**

```sql
SELECT e.name, d.name AS dept
FROM employee e
LEFT JOIN department d ON e.dept_id = d.dept_id;
```

**Context:** Frequently used across data roles (2025) .

---

### 7. **DELETE vs TRUNCATE vs DROP**

**Answer:**

* `DELETE`: Row-by-row deletion, can filter with WHERE, logged.
* `TRUNCATE`: Quickly deletes all rows, not logged per row.
* `DROP`: Removes entire table schema and data.
  **Context:** Important for DB ops, asked in dev roles (2025) .

---

### 8. **Purpose of DISTINCT Keyword**

**Answer:**
Removes duplicate values from result set.
**Example:**

```sql
SELECT DISTINCT department FROM employee;
```

**Context:** Basic SQL concept for analysts (2025) .

---

### 9. **VARCHAR vs CHAR Data Types**

**Answer:**

* **CHAR(n)**: Fixed length, padded.
* **VARCHAR(n)**: Variable length, no padding.
  **Context:** Common knowledge tested in SQL dev roles (2025) .

---

### 10. **Aggregate Functions (COUNT, SUM, AVG…)**

**Answer:**
Used to calculate summary values.
**Example:**

```sql
SELECT department, COUNT(*) AS total_emp, AVG(salary) AS avg_sal
FROM employee
GROUP BY department;
```

**Context:** Core for reporting roles at Amazon, etc. (2025) .

---

### 11. **UNION vs UNION ALL**

**Answer:**

* `UNION`: Removes duplicates.
* `UNION ALL`: Keeps duplicates.
  **Context:** Common in interview prep materials (2025) .

---

### 12. **Purpose of NULL Value**

**Answer:**
Represents missing or unknown data; not equal to 0 or empty string.
**Context:** Fundamental concept used widely in interviews (2025) .

---

### 13. **SQL Views**

**Answer:**
Virtual tables saved as a query. Simplify complex logic, improve security.
**Example:**

```sql
CREATE VIEW v_emp_dept AS
SELECT e.name, d.name AS dept
FROM employee e
JOIN department d ON e.dept_id = d.dept_id;
```

**Context:** Asked in intermediate-level interviews (2025) .

---

### 14. **Indexes & Their Usage**

**Answer:**
Indexes improve read query performance at cost of extra storage and slower writes.
**Context:** Important for performance — Amazon may ask this (2025).

---

### 15. **Subquery**

**Answer:**
A query within another query, useful in WHERE etc.
**Example:**

```sql
SELECT * FROM employee
WHERE dept_id IN (SELECT dept_id FROM department WHERE name LIKE '%Sales%');
```

**Context:** Frequently tested in data roles (2025) .

---

### 16. **2nd Highest Salary Query**

**Answer:**
One way: use `DENSE_RANK()` or subquery.
**Example:**

```sql
SELECT MAX(salary) AS second_highest
FROM employee
WHERE salary < (SELECT MAX(salary) FROM employee);
```

**Company/Year:** Known from Ernst & Young interviews (2025) .

---

### 17. **Find 3rd Transaction per User (Example from Uber)**

**Answer:**
Use `ROW_NUMBER()` over partition by user.
**Example:**

```sql
SELECT user_id, spend, transaction_date
FROM (
  SELECT user_id, spend, transaction_date,
         ROW_NUMBER() OVER (PARTITION BY user_id ORDER BY transaction_date) AS rn
  FROM transactions
) t
WHERE rn = 3;
```

**Company/Year:** Uber (recent, as of 2025) .

---

### 18. **Explain SQL to a Non-technical Person**

**Answer:**
SQL is like asking questions to a huge spreadsheet: “Give me these rows quickly.”
**Company/Year:** Amazon, often as an icebreaker (2025) .

---

### 19. **Calculate 7-Day Rolling Average (Amazon)**

**Answer:**
Use window functions like `AVG() OVER (ORDER BY date ROWS BETWEEN 6 PRECEDING AND CURRENT ROW)`.
**Context:** Amazon applied SQL (2025) ([Interview Query][2]).

---

### 20. **Difference Between WHERE and HAVING** *(Reinforced)*

**Answer Recap:** Pre-aggregation vs post-aggregation filtering.
**Context:** Very common concept; emphasized in Amazon prep (2025) .

---

### 21. **Explain COUNT(DISTINCT user\_id) Unexpected Behavior**

**Answer:**
Might miscount when NULLs or duplicates exist unexpectedly.
**Context:** Conceptual Amazon-level question (2025) .

---

### 22. **Optimization: Avoid Full Table Scan on Partitioned Dataset**

**Answer:**
Use partition filters in WHERE clause to limit scan.
**Context:** Amazon senior roles (L5+), optimization focus (2025) .

---

### 23. **Window Functions (ROW\_NUMBER, RANK, LAG)**

**Answer:**
Used to rank or compare within partitions.
**Example:**

```sql
SELECT user_id, spend, RANK() OVER (PARTITION BY user_id ORDER BY spend DESC) AS rnk
FROM transactions;
```

**Context:** Common at FAANG data roles (2025) .

---

### 24. **CTEs (Common Table Expressions)**

**Answer:**
Temporary named result sets using `WITH`.
**Example:**

```sql
WITH dept_avg AS (
  SELECT dept_id, AVG(salary) AS avg_sal
  FROM employee
  GROUP BY dept_id
)
SELECT e.name, d.avg_sal
FROM employee e
JOIN dept_avg d ON e.dept_id = d.dept_id;
```

**Context:** Frequently seen in intermediate/advanced interviews (2025) .

---

### 25. **Conceptual: Handling NULLs in GROUP BY**

**Answer:**
NULL is grouped separately; e.g., `GROUP BY dept` will treat NULL as a separate group.
**Context:** Conceptual Amazon question (2025) .

---

### **26. What is SQL?**

**Answer:** SQL stands for *Structured Query Language*. It's the standard language for communicating with relational databases—used to read, write, update, and delete data.
**Example:**

```sql
SELECT * FROM customers;
```

**Context:** Fundamental question asked at almost every entry-level role—from freshers in tech companies to business analyst positions

---

### **27. What are DDL, DML, DCL, and TCL commands?**

**Answer:**

* **DDL (Data Definition Language):** CREATE, ALTER, DROP, TRUNCATE (modify schema).
* **DML (Data Manipulation Language):** SELECT, INSERT, UPDATE, DELETE (manipulate data).
* **DCL (Data Control Language):** GRANT, REVOKE (permissions).
* **TCL (Transaction Control Language):** COMMIT, ROLLBACK, SAVEPOINT (transaction handling).
  
**Context:** Core concept asked in many interviews, including MAANG companies 

---

### **28. Difference between SQL, MySQL, and SQL Server?**

**Answer:**

* **SQL:** Language.
* **MySQL:** An open-source relational database management system (RDBMS).
* **SQL Server:** Microsoft's proprietary RDBMS.
**Context:** Frequently asked for clarity at both fresher and experience levels .

---

### **29. What is normalization and denormalization?**

**Answer:**

* **Normalization:** Organizing tables to reduce redundancy (e.g., 1NF, 2NF, 3NF).
* **Denormalization:** Introducing redundancy to improve read performance.
**Context:** Common in data analyst and DB designer interviews .

---

### **30. What is a relational database?**

**Answer:** A database where data is organized in tables (relations) with rows and columns, and relationships can be established between them using keys.
**Context:** Basic database concept across interviews .

---

### **31. Table vs Field (Row vs Column)?**

**Answer:**

* **Table:** Organized set of rows and columns.
* **Field (Column):** Attribute describing each row.
* **Row:** A single record.

**Context:** Freshers are often evaluated on such fundamentals ).

---

### **32. What are SQL operators?**

**Answer:**

* **Arithmetic:** `+`, `-`, `*`, `/`.
* **Comparison:** `=`, `!=`, `<`, `<=`, `>`, `>=`.
* **Logical:** `AND`, `OR`, `NOT`.
* **Set:** `UNION`, `INTERSECT`, `EXCEPT`.
* **Special:** `IN`, `BETWEEN`, `LIKE`, `IS NULL`.

**Context:** Intermediate questions across interviews .

---

### **33. What is a query in SQL?**

**Answer:** A command to request data manipulation or retrieval, most commonly using `SELECT`.
**Example:**

```sql
SELECT id, name FROM users WHERE active = 1;
```

**Context:** Fundamental knowledge for any SQL-based role .

---

### **34. What are constraints in SQL? (NOT NULL, UNIQUE, etc.)**

**Answer:** Rules to enforce data integrity—like `NOT NULL`, `UNIQUE`, `PRIMARY KEY`, `FOREIGN KEY`, `CHECK`, `DEFAULT`.

**Context:** Core concept for data integrity and design .

---

### **35. What is a cursor (in SQL)?**

**Answer:** A database object used to retrieve query results row by row—handy for procedural logic.

**Context:** More technical; often in backend developer or PL/SQL interviews .

---

### **36. What is a trigger?**

**Answer:** An automatic reaction to specific table events (e.g., `INSERT`, `UPDATE`, `DELETE`).
**Example (simplified):**

```sql
CREATE TRIGGER trg_after_insert
AFTER INSERT ON orders
BEGIN
  -- logic here
END;
```

**Context:** Asked in roles involving automation or DB maintenance ).

---

### **37. What is a stored procedure?**

**Answer:** A set of precompiled SQL statements stored and executed in the database, with optional parameters.

**Context:** Important for optimization and enterprise setups .

---

### **38. What is pattern matching in SQL?**

**Answer:** Using `LIKE` with wildcards `%` (any number of chars) or `_` (single char).
**Example:**

```sql
WHERE name LIKE 'Jo_n%'  -- Josn, John, Jonnny, etc.
```

**Context:** Common for filtering tasks in interviews .

---

### **39. Create an empty table like another table:**

**Answer:**

```sql
CREATE TABLE new_table LIKE existing_table;
```

**Context:** Quick schema duplication, often seen in DB admin scenarios .

---

### **40. What is COALESCE?**

**Answer:** Returns the first non-NULL value from a list.
**Example:**

```sql
SELECT COALESCE(NULL, salary, 0) AS effective_salary;
```

**Context:** Useful for data cleanup and default handling .

---

### **41. Difference between COUNT() and SUM()?**

**Answer:**

* `COUNT()`: Counts rows or non-null values.
* `SUM()`: Adds up numeric values.
**Context:** Essential for basic aggregate understanding .

---

### **42. NVL vs NVL2 (Oracle-specific functions)?**

**Answer:**

* `NVL(expr1, expr2)`: If `expr1` is NULL, returns `expr2`.
* `NVL2(expr1, expr2, expr3)`: Returns `expr2` if `expr1` is not NULL, otherwise `expr3`.
  **Context:** Important in Oracle SQL interviews .

---

### **43. Difference between ROW\_NUMBER() and RANK()?**

**Answer:**

* `ROW_NUMBER()`: Assigns unique sequential numbers.
* `RANK()`: Gives the same rank to ties, skipping subsequent ranks.
  **Example:**

```sql
RANK() OVER (ORDER BY score DESC)
```

**Context:** Used in leaderboard or ranking queries in FAANG interviews .

---

### **44. Window Functions – What are they?**

**Answer:** Functions like `ROW_NUMBER()`, `RANK()`, `SUM() OVER(...)`, that perform calculations across rows without collapsing the result set.
**Example:**

```sql
SUM(amount) OVER (ORDER BY date ROWS BETWEEN 6 PRECEDING AND CURRENT ROW) AS rolling_sum
```

**Context:** Frequently seen in analytics/data roles ).

---

### **45. Clustered vs Non-clustered Index?**

**Answer:**

* **Clustered Index:** Physically orders table rows.
* **Non-clustered Index:** Separate structure that points to table rows.
**Context:** Critical for performance tuning in DB roles .

---

### **46. What is a sequence in SQL?**

**Answer:** Object that generates sequential numeric values—often used for unique IDs.
**Example:**

```sql
CREATE SEQUENCE seq_emp START WITH 1 INCREMENT BY 1;
SELECT NEXT VALUE FOR seq_emp;
```

**Context:** Used in schema design especially in Oracle or PostgreSQL .

---

### **47. Horizontal vs Vertical Partitioning?**

**Answer:**

* **Horizontal Partitioning:** Splitting data rows across partitions.
* **Vertical Partitioning:** Splitting columns into multiple tables.
**Context:** Advanced performance and scaling technique .

---

### **48. Strategies for optimizing slow SQL queries (e.g., Amazon)?**

**Answer:**

* Use indexes
* Rewrite queries efficiently
* Partition large tables
* Use caching or sharding
* Optimize schema and data types
  
**Context:** Known to appear in Amazon interview questions .

---

### **49. SQL query: Calculate monthly average review rating (Amazon)?**

**Answer & Example:**

```sql
SELECT product_id,
       EXTRACT(YEAR FROM review_date) AS year,
       EXTRACT(MONTH FROM review_date) AS month,
       AVG(rating) AS avg_rating
FROM Reviews
GROUP BY product_id, year, month
ORDER BY product_id, year, month;
```

**Context:** Directly from Amazon’s SQL interview materials.

---

### **50. How is data integrity maintained in SQL?**

**Answer:**
Through constraints (`PRIMARY KEY`, `FOREIGN KEY`, `NOT NULL`, `UNIQUE`), transactions (ACID), triggers, and normalization.

**Context:** Standard advanced/optimization question .

