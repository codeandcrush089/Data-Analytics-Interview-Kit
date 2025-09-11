
<div align="center">

# 🗄️ Top 100 SQL Interview Q&A  
💡 With Real-World Examples + Company Context (FAANG & Startups)

</div>



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

**Answer:** Use window functions like `AVG() OVER (ORDER BY date ROWS BETWEEN 6 PRECEDING AND CURRENT ROW)`.

**Context:** Amazon applied SQL (2025) 

---

### 20. **Difference Between WHERE and HAVING** *(Reinforced)*

**Answer Recap:** Pre-aggregation vs post-aggregation filtering.

**Context:** Very common concept; emphasized in Amazon prep (2025) .

---

### 21. **Explain COUNT(DISTINCT user\_id) Unexpected Behavior**

**Answer:** Might miscount when NULLs or duplicates exist unexpectedly.

**Context:** Conceptual Amazon-level question (2025) .

---

### 22. **Optimization: Avoid Full Table Scan on Partitioned Dataset**

**Answer:** Use partition filters in WHERE clause to limit scan.

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
* 
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


---


### **51. What is a staging table in ETL?**
   **Answer:**
    A temporary table used in data pipelines to hold raw input before transformation and loading.
  * **Example:** Load daily CSV into `staging_sales`, clean data, then insert into `fact_sales`.
    
**Context:** Common in data engineering roles focused on ETL systems.

---
### **52. Difference between OLTP and OLAP systems?**
   **Answer:**

   * **OLTP:** Transactional systems, high-speed reads/writes (e.g., banking).
   * **OLAP:** Analytical systems with batch processing and large aggregations.
     
**Context:** Important in data warehousing interviews.

---
### **53. Explain covering index vs composite index.**
   **Answer:**

   * **Composite index:** Multiple columns for index key.
   * **Covering index:** Includes the columns needed by a query to avoid fetching the table.
     
**Context:** Performance tuning scenarios in interviews.

---
### **54. What is a surrogate key in data warehousing?**
   **Answer:** A synthetic primary key (e.g., `surrogate_id`) used for simplicity and stability in fact tables.
   
 **Context:** Data warehousing interviews ).
   
---
### **55. Star schema vs snowflake schema—differences?**
   **Answer:**

   * **Star schema:** Denormalized dimensions connected directly to facts.
   * **Snowflake:** Dimensions normalized into sub-tables.
     
**Context:** Schema design discussions in analytics roles .

---
### **56. Challenges in maintaining data quality in ETL?**
  **Answer:** Issues like missing data, duplicates, schema changes, and incorrect formats. Fixes include validation, logging, and monitoring.  
  
**Context:** ETL and data engineering roles .

---
### 57. Error handling strategies in ETL workflows?**
   **Answer:** Use transactional checkpoints, audit logs, retry logic, and rollback mechanisms.
   
**Context:** Data engineering / ETL interviews .
   
---
### **58. Explain PIVOT and UNPIVOT operations.**
   **Answer:**

   * **PIVOT:** Turn rows into columns (e.g., aggregate sales by month).
   * **UNPIVOT:** Reverse operation—convert columns back into rows.
     
**Context:** Advanced SQL interviews .

---
### **59. What are materialized views?**
   **Answer:** Stored query results, refreshed periodically—improves performance for frequently-run aggregations.
   
**Context:** Optimization-focused interviews .
   
---
### **60. User-defined functions (UDFs) in SQL?**
   **Answer:** Custom reusable functions (scalar or table-valued) to encapsulate logic.
   
**Context:** Commonly used in real-world SQL solutions .
   
---
### **61. What are recursive queries & when to use them?**
   **Answer:** Queries that call themselves (using CTEs) to handle hierarchical data like org charts.
   
**Context:** Data analyst and engineering interviews .
   
---
### **62. Temporary tables vs table variables—when to use which?**
   **Answer:** Temporary tables live for session and can be indexed; table variables are in-memory and faster for small sets.
   
**Context:** SQL Server / performance tuning scenarios.
   
---
### **63. Explain dynamic SQL.**
   **Answer:** Building SQL queries dynamically in code (e.g., assemble SQL as a string and execute).
   
**Context:** Developer-focused SQL roles ).
   
---
### **64. What are database isolation levels?**
   **Answer:** Determines how transactions are isolated: READ UNCOMMITTED, READ COMMITTED, REPEATABLE READ, SERIALIZABLE.
   
**Context:** Crucial for transactional systems and interviews .
   
---
### **65. Indexed views—what and when to use?**
   **Answer:** Views that store data and have indexes—improves query performance but consumes storage.
   
**Context:** Performance tuning in enterprise SQL environments ).
   
---
### **66. Describe hierarchical (recursive) queries use-cases.**
   **Answer:** Use cases like finding all child records of a parent in an org, or file system structure traversals.
   
**Context:** Advanced query topics in interviews .
   
---
### **67. What is SQL injection and how to prevent it?**
   **Answer:** Injecting malicious SQL via user inputs. Prevent with prepared statements, parameterized queries, and input sanitization.
   
**Context:** Common in dev & security-focused roles .
   
---
### **68. What's ACID in database systems?**
   **Answer:** Ensures reliable transactions:

   * **Atomicity**
   * **Consistency**
   * **Isolation**
   * **Durability**
     
 **Context:** Standard DB concept in interviews .
 
---
### **69. Explain recursive CTEs with an example.**
   **Answer:**

    ```sql
    WITH RECURSIVE employee_cte AS (
      SELECT emp_id, manager_id, name FROM employees WHERE manager_id IS NULL
      UNION ALL
      SELECT e.emp_id, e.manager_id, e.name
      FROM employees e
      JOIN employee_cte c ON e.manager_id = c.emp_id
    )
    SELECT * FROM employee_cte;
    ```

 **Context:** Analyze hierarchies—common in analytics/engineering roles ([Datainterview.com][1]).
   
---
### **70. What’s row-level security?**
   **Answer:** Restricts access to rows based on user roles—e.g., employees see only their data.
   
**Context:** Data governance and security discussions .
   
---
### **71. Explain CROSS APPLY / OUTER APPLY.**
   **Answer:** In SQL Server, APPLY runs a table-valued function per row of outer table. CROSS APPLY excludes non-matching rows; OUTER APPLY includes them with NULLs.
   
**Context:** Advanced SQL Server topics .
    
---
### **72. What are temporary tables vs table variables?**
  **Answer:**

* **Temporary Tables (`#Temp`)**: Stored in `tempdb`, can have indexes, constraints, and statistics. They behave much like regular tables but are scoped to the session or procedure. Good for handling large datasets and complex queries.
* **Table Variables (`@TableVar`)**: Stored in memory (though sometimes spill to `tempdb`), scoped to the batch, function, or procedure. They don’t maintain statistics, so the optimizer may assume only a single row. Best for small datasets and quick lookups.

**Context:** Common SQL Server interview question, often asked by companies like Microsoft, Accenture, and TCS (2019–2024).

---
### **73. How do you use MERGE statements?**
   **Answer:** Upserts—merge target with source: insert, update, or delete based on match conditions.
   **Example:**

    ```sql
    MERGE INTO target t
    USING source s
    ON t.id = s.id
    WHEN MATCHED THEN UPDATE SET t.val = s.val
    WHEN NOT MATCHED THEN INSERT (id,val) VALUES (s.id,s.val);
    ```
**Context:** Data sync tasks in data engineering .

---
### **74. Explain database partitioning strategies.**
   **Answer:**

   * **Horizontal partitioning:** Split rows (e.g., by date).
   * **Vertical partitioning:** Split columns into different tables.
      Improves query performance and maintainability.
     
**Context:** Scaling large datasets .

---
### **75. What are query execution plans and how do you analyze them?**
   **Answer:** Visual representation of how the DB engine runs a query; helps identify bottlenecks like scans or missing indexes.
   
**Context:** Performance tuning interviews .

---


### 76. **Write a query to get the second highest salary using `ROW_NUMBER()`**

**Answer:** Use `ROW_NUMBER()` over descending salary partitioned (or entire table) and filter where row number = 2.
**Example:**

```sql
SELECT salary
FROM (
  SELECT salary,
         ROW_NUMBER() OVER (ORDER BY salary DESC) AS rn
  FROM employee
) t
WHERE rn = 2;
```

**Context:** Common challenge-level question, seen in FAANG and data analyst rounds—2024–2025. ([Datainterview.com][1])

---

### 77. **How to delete duplicates while keeping one row?**

**Answer:** Use CTE with `ROW_NUMBER()` partitioned by duplicate columns and delete where row number > 1.
**Example:**

```sql
WITH cte AS (
  SELECT *,
         ROW_NUMBER() OVER (PARTITION BY col1, col2 ORDER BY id) AS rn
  FROM table_name
)
DELETE FROM cte WHERE rn > 1;
```

**Context:** Frequently used in cleaning data tasks across interviews. ([DataCamp][2], [Datainterview.com][1])

---

### 78. **Get cumulative sum per day**

**Answer:** Use window function with `SUM() OVER (ORDER BY date ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW)`.
**Example:**

```sql
SELECT date, sales,
       SUM(sales) OVER (ORDER BY date ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW) AS cum_sales
FROM daily_sales;
```

**Context:** Common in analytics interviews (e.g., FAANG data roles, 2025). ([Datainterview.com][1])

---

### 79. **Delete duplicate records**

*(Similar to Q77; referenced for reinforcement.)*
**Answer:** Same approach—use window functions or `DISTINCT`.

---

### 80. **Find nth highest salary (parameterized)**

**Answer:** Use `DENSE_RANK()` or `LIMIT/OFFSET`, depending on SQL dialect.
**Example (MySQL):**

```sql
SELECT DISTINCT salary FROM employee ORDER BY salary DESC LIMIT 1 OFFSET n-1;
```

---

### 81. **Extract top N payers per category (e.g., Amazon style)**

**Answer:** 
Use `ROW_NUMBER()` partitioned by category, filter `row_number <= N`.
**Example:** Identify top two products per category in 2022. 

---

### 82. **Find customers without orders**

**Answer:** Use `LEFT JOIN` and `WHERE tableB.id IS NULL` or `NOT EXISTS`.
**Example:**

```sql
SELECT c.id, c.name
FROM customers c
LEFT JOIN orders o ON c.id = o.customer_id
WHERE o.customer_id IS NULL;
```

**Context:** Very commonly asked in interviews. 

---

### 83. **Convert DATETIME to DATE**

**Answer:**

```sql
SELECT DATE(order_datetime) AS order_date FROM table;
```

---

### 84. **Calculate time-based changes**

**Answer:** Use CTEs, `CASE`, and window functions (`LAG`, `LEAD`).

**Context:** Asked for mid-level analytics roles. 

---

### 85. **Find users active for 4 consecutive days**

**Answer:** Use window functions and CTEs: calculate date differences and consecutive day counts.

**Context:** Came up in a real Sr. Data Analyst interview. 

---

### 86. **Identify duplicates across multiple tables**

**Answer:** 
Use `UNION` or `INTERSECT`, depending on the case. Filter rows with count > 1.

**Context:** A challenge from data analyst interviews. 

---

### 87. **Date manipulation (e.g., previous X months)**

**Answer:**
Use date functions like `DATE_SUB()`:

```sql
WHERE date_column >= DATE_SUB(CURDATE(), INTERVAL 6 MONTH);
```

---

### 88. **My favorite join? (Common witty question)**

**Answer:** Often answered humorously: “CROSS JOIN—because everything is a filtered cross join!”

**Context:** From Reddit—informal but highlights interviewer levity. 

---

### 89. **Emergency fallback query (MAX date)**

**Answer:**

```sql
SELECT product_name
FROM orders
WHERE order_date = (SELECT MAX(order_date) FROM orders);
```

But better to use `ROW_NUMBER()` and deterministic ORDER for single result. 

---

### 90. **Common Date Range reporting**

**Answer:**
Use `BETWEEN`:

```sql
WHERE order_date BETWEEN '2025-01-01' AND '2025-01-31';
```

---

### 91. **Use of INTERSECT**

**Answer:**
Return rows common to two queries:

```sql
SELECT column FROM A
INTERSECT
SELECT column FROM B;
```

---

### 92. **Set Operator Variations**

**Answer:**
`UNION`, `UNION ALL`, `INTERSECT`, `EXCEPT/MINUS`.

---

### 93. **Use of CASE in SQL**

**Answer:**

```sql
CASE
  WHEN sales > 1000 THEN 'High'
  WHEN sales > 500 THEN 'Medium'
  ELSE 'Low'
END AS sales_category;
```

**Context:** Frequently tested in beginner-to-intermediate interviews. 

---

### 94. **SQL comment types**

**Answer:**
Single-line: `-- comment`
Multi-line: `/* comment */` 

---

### 95. **SQL dialects—differences?**

**Answer:** SQL is a language; MySQL, PostgreSQL, SQL Server are dialects/RDBMS. 

---

### 96. **Schema vs database**

**Answer:**
A schema includes tables, views, procedures; depending on DBMS, schema is part of a database structure. 

---

### 97. **SQL vs PL/SQL**

**Answer:**
SQL is declarative query language; PL/SQL (Oracle) adds procedural features like loops and variables. 

---

### 98. **Execution order of clauses**

**Answer:**
Execution order: FROM → JOIN → WHERE → GROUP BY → HAVING → SELECT → ORDER BY → LIMIT. 

---

### 99. **Differences: DROP vs DELETE vs TRUNCATE**

**Answer:**

* `DELETE` removes rows individually (logged, supports WHERE).
* `TRUNCATE` deletes all rows quickly, minimal logging.
* `DROP` removes entire table. 

---

### 100. **NULL vs empty or zero**

**Answer:**
`NULL` means unknown/missing; it's not the same as 0 (numeric) or '' (empty string). 

---
