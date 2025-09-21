<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png" alt="SQL Logo" width="130"/>

# Top 100 SQL Interview Q&A  
💡 With Real-World Examples + Company Context (FAANG & Startups)

</div>




---

# **SQL Interview Questions (Q1–Q20 – Basics)**

**Q1. What is SQL?**
**Answer:** SQL (Structured Query Language) is used to interact with relational databases.
**Example:**

```sql
SELECT * FROM Employees;
```

**Context:** Asked at **TCS (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q2. What are the different types of SQL statements?**
**Answer:**

* DDL (Data Definition Language) → CREATE, ALTER, DROP
* DML (Data Manipulation Language) → INSERT, UPDATE, DELETE
* DQL (Data Query Language) → SELECT
* TCL (Transaction Control) → COMMIT, ROLLBACK
  **Context:** Asked at **Infosys (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q3. What is the difference between SQL and MySQL?**
**Answer:**

* SQL → Language for querying databases.
* MySQL → A database management system that uses SQL.
  **Context:** Asked at **Capgemini (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q4. What are Primary Key and Foreign Key?**
**Answer:**

* Primary Key: Uniquely identifies a record.
* Foreign Key: Refers to primary key in another table.
  **Example:**

```sql
CREATE TABLE Orders (
  OrderID INT PRIMARY KEY,
  CustomerID INT FOREIGN KEY REFERENCES Customers(CustomerID)
);
```

**Context:** Asked at **Wipro (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q5. What is the difference between CHAR and VARCHAR?**
**Answer:**

* CHAR: Fixed-length storage.
* VARCHAR: Variable-length storage.
  **Context:** Asked at **Deloitte (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q6. What are the different types of JOINs?**
**Answer:**

* INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN.
  **Example:**

```sql
SELECT e.Name, d.DeptName
FROM Employees e
INNER JOIN Departments d ON e.DeptID = d.DeptID;
```

**Context:** Asked at **Microsoft (2022)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q7. What is the difference between WHERE and HAVING?**
**Answer:**

* WHERE: Filters rows before grouping.
* HAVING: Filters groups after aggregation.
  **Example:**

```sql
SELECT DeptID, COUNT(*) 
FROM Employees 
GROUP BY DeptID 
HAVING COUNT(*) > 5;
```

**Context:** Asked at **EY (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q8. What is the difference between UNION and UNION ALL?**
**Answer:**

* UNION: Removes duplicates.
* UNION ALL: Keeps duplicates.
  **Context:** Asked at **Accenture (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q9. What is a View in SQL?**
**Answer:** A virtual table based on the result of a query.
**Example:**

```sql
CREATE VIEW ActiveEmployees AS
SELECT Name, DeptID FROM Employees WHERE Status = 'Active';
```

**Context:** Asked at **Capgemini (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q10. What is the difference between DELETE, TRUNCATE, and DROP?**
**Answer:**

* DELETE: Removes rows (can be rolled back).
* TRUNCATE: Removes all rows (cannot roll back in some DBs).
* DROP: Deletes the entire table.
  **Context:** Asked at **Infosys (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q11. What is a Subquery?**
**Answer:** Query inside another query.
**Example:**

```sql
SELECT Name FROM Employees 
WHERE Salary > (SELECT AVG(Salary) FROM Employees);
```

**Context:** Asked at **Deloitte (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q12. What is the difference between Clustered and Non-Clustered Index?**
**Answer:**

* Clustered Index: Sorts and stores rows physically.
* Non-Clustered Index: Stores pointer to data.
  **Context:** Asked at **Microsoft (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q13. What is the difference between NULL and 0?**
**Answer:**

* NULL = Unknown / Missing value.
* 0 = Numeric value.
  **Context:** Asked at **Wipro (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q14. What is the difference between DROP and TRUNCATE?**
**Answer:**

* DROP: Deletes entire table structure.
* TRUNCATE: Deletes all rows but keeps structure.
  **Context:** Asked at **TCS (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q15. What is a Stored Procedure?**
**Answer:** A precompiled collection of SQL statements.
**Example:**

```sql
CREATE PROCEDURE GetEmployees AS
SELECT * FROM Employees;
```

**Context:** Asked at **Infosys (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q16. What is the difference between COUNT(\*), COUNT(1), and COUNT(column)?**
**Answer:**

* COUNT(\*) → Counts all rows.
* COUNT(1) → Same as COUNT(\*).
* COUNT(column) → Counts only non-NULL values.
  **Context:** Asked at **EY (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q17. What are Constraints in SQL?**
**Answer:** Rules applied to columns (NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY, CHECK, DEFAULT).
**Context:** Asked at **Capgemini (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q18. What is Normalization?**
**Answer:** Process of structuring data to reduce redundancy.

* 1NF → Atomic values.
* 2NF → Remove partial dependency.
* 3NF → Remove transitive dependency.
  **Context:** Asked at **Deloitte (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q19. What is Denormalization?**
**Answer:** Adding redundancy for faster queries (opposite of normalization).
**Context:** Asked at **Accenture (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q20. What are Transactions in SQL?**
**Answer:** A set of SQL operations executed as a single unit.
**Properties:** ACID (Atomicity, Consistency, Isolation, Durability).
**Context:** Asked at **TCS (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q21. What are Aggregate Functions in SQL?**
**Answer:** Functions that perform calculations on a set of values and return a single value (SUM, AVG, MIN, MAX, COUNT).
**Example:**

```sql
SELECT AVG(Salary) FROM Employees;
```

**Context:** Infosys (2021) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q22. What is the difference between IN and EXISTS?**
**Answer:**

* IN → Compares a value to a list of values.
* EXISTS → Checks if subquery returns any row.
  **Example:**

```sql
SELECT Name FROM Employees 
WHERE DeptID IN (SELECT DeptID FROM Departments);
```

**Context:** TCS (2020) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q23. What is the difference between RANK(), DENSE\_RANK(), and ROW\_NUMBER()?**
**Answer:**

* ROW\_NUMBER(): Sequential without duplicates.
* RANK(): Leaves gaps if duplicates exist.
* DENSE\_RANK(): No gaps for duplicates.
  **Example:**

```sql
SELECT Name, Salary,
RANK() OVER (ORDER BY Salary DESC) AS Rnk
FROM Employees;
```

**Context:** Deloitte (2021) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q24. What are Scalar Functions?**
**Answer:** Functions that return a single value (LEN, UPPER, LOWER, GETDATE).
**Context:** Capgemini (2020) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q25. What is a Self-Join?**
**Answer:** A join where a table is joined with itself.
**Example:**

```sql
SELECT A.Name, B.Name
FROM Employees A, Employees B
WHERE A.ManagerID = B.EmployeeID;
```

**Context:** Wipro (2021) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q26. What are Correlated Subqueries?**
**Answer:** Subquery that refers to the outer query.
**Example:**

```sql
SELECT Name FROM Employees e
WHERE Salary > (SELECT AVG(Salary) 
                FROM Employees 
                WHERE DeptID = e.DeptID);
```

**Context:** EY (2020) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q27. What is the difference between COALESCE and ISNULL?**
**Answer:**

* ISNULL → Works with two arguments.
* COALESCE → Works with multiple arguments, returns first non-NULL.
  **Context:** Microsoft (2021) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q28. What is the difference between Primary Key and Unique Key?**
**Answer:**

* Primary Key → One per table, doesn’t allow NULLs.
* Unique Key → Multiple allowed, allows one NULL.
  **Context:** Accenture (2020) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q29. What is a Trigger in SQL?**
**Answer:** A stored procedure that executes automatically on events (INSERT, UPDATE, DELETE).
**Example:**

```sql
CREATE TRIGGER trg_AfterInsert
ON Employees
AFTER INSERT
AS
PRINT 'New Employee Added!';
```

**Context:** TCS (2021) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q30. What is the difference between a View and a Table?**
**Answer:**

* Table → Stores data physically.
* View → Logical representation (virtual table).
  **Context:** Infosys (2020) ➡️<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q31. What is an Index? Why is it used?**
**Answer:** An index speeds up searches by creating a pointer to data.
**Context:** Deloitte (2021) ➡️<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q32. What are the different types of Indexes?**

**Answer:**

* Clustered Index
* Non-Clustered Index
* Unique Index
* Composite Index
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q33. What is a Composite Key?**

**Answer:** Combination of two or more columns that uniquely identify a row.

**Example:**

```sql
PRIMARY KEY (StudentID, CourseID)
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q34. What is a Candidate Key?**

**Answer:** A set of attributes that can uniquely identify a record (Primary Key is chosen from Candidate Keys).
<p align="right"><b><i>Context:</b> Asked at <b>EV (2021)</b>.</i></p>

---

**Q35. What is the difference between DELETE and TRUNCATE?**

**Answer:**

* DELETE → Removes rows conditionally, logged.
* TRUNCATE → Removes all rows, faster, resets identity.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q36. What are ACID properties in SQL?**

**Answer:**

* Atomicity, Consistency, Isolation, Durability – ensure reliable transactions.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q37. What is a Cursor in SQL?**

**Answer:** A pointer used to fetch rows one by one.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q38. What are Joins vs. Subqueries?**

**Answer:**

* Join → Combines data from multiple tables in a single query.
* Subquery → Query inside another query.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q39. What is a Constraint CHECK?**

**Answer:** Ensures values meet a condition.

**Example:**

```sql
Salary INT CHECK (Salary > 0)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q40. What is the difference between Clustered Index and Non-Clustered Index?**

**Answer:**

* Clustered → Sorts and stores rows physically.
* Non-Clustered → Stores a pointer to data.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2020)</b>.</i></p>

---

**Q41. What is a CTE (Common Table Expression)?**

**Answer:** A temporary named result set used within a query.

**Example:**

```sql
WITH DeptCount AS (
   SELECT DeptID, COUNT(*) AS EmpCount 
   FROM Employees 
   GROUP BY DeptID
)
SELECT * FROM DeptCount WHERE EmpCount > 5;
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p></b>.</i></p>

---

**Q42. What is the difference between CTE and Subquery?**

**Answer:**

* Subquery: Written inline.
* CTE: Defined separately, improves readability and reuse.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q43. What are Window Functions in SQL?**

**Answer:** Functions that perform calculations across a set of rows related to the current row.

**Example:**

```sql
SELECT Name, Salary, 
       AVG(Salary) OVER (PARTITION BY DeptID) AS DeptAvg
FROM Employees;
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q44. What is the difference between RANK() and NTILE()?**

**Answer:**

* RANK(): Assigns rank with gaps.
* NTILE(n): Divides rows into n groups.
<p align="right"><b><i>Context:</b> Asked at <b>EV (2021)</b>.</i></p>

---

**Q45. What are Stored Functions?**

**Answer:** A function that returns a single value and can be reused in SQL queries.

**Example:**

```sql
CREATE FUNCTION GetBonus(@salary INT)
RETURNS INT
AS
BEGIN
   RETURN @salary * 0.1
END
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q46. What is the difference between Stored Procedure and Function?**

**Answer:**

* Procedure → Can return multiple values, support transactions.
* Function → Returns a single value, used in queries.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q47. What are Transactions in SQL?**

**Answer:** Group of operations executed together. Controlled by COMMIT and ROLLBACK.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q48. What is the difference between COMMIT and ROLLBACK?**

**Answer:**

* COMMIT → Saves changes permanently.
* ROLLBACK → Reverts changes to last savepoint.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q49. What is a Savepoint in SQL?**

**Answer:** Intermediate point in a transaction to which we can roll back.

**Example:**

```sql
SAVEPOINT sp1;
ROLLBACK TO sp1;
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q50. What are Triggers?**

**Answer:** Special stored procedures executed automatically on events (INSERT/UPDATE/DELETE).
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q51. What is the difference between AFTER and INSTEAD OF Triggers?**

**Answer:**

* AFTER: Runs after event execution.
* INSTEAD OF: Replaces the action.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q52. What are Materialized Views?**

**Answer:** Views that store results physically and can be refreshed.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q53. What is the difference between Primary Key and Composite Key?**

**Answer:**

* Primary Key → Single column identifier.
* Composite Key → Multiple columns combined as key.
<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q54. What is a Deadlock in SQL?**

**Answer:** Situation where two transactions wait for each other’s resources.
<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q55. What is the difference between UNION and JOIN?**

**Answer:**

* UNION → Combines rows vertically (same structure).
* JOIN → Combines rows horizontally (related columns).
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q56. What are the Isolation Levels in SQL?**

**Answer:**

* Read Uncommitted
* Read Committed
* Repeatable Read
* Serializable
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q57. What is the difference between OLTP and OLAP?**

**Answer:**

* OLTP → Transactional databases (insert/update).
* OLAP → Analytical databases (reporting).
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q58. What is Index Fragmentation?**

**Answer:** Condition where index pages are not stored sequentially, reducing performance.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q59. What is the difference between Temp Table and Table Variable?**

**Answer:**

* Temp Table → Stored in tempdb, supports indexes.
* Table Variable → Stored in memory, limited scope.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q60. What are Common Performance Tuning Techniques in SQL?**

**Answer:**

* Use Indexes
* Avoid SELECT \*
* Optimize Joins
* Partition Large Tables
* Analyze Execution Plan
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---


**Q61. What is Query Optimization in SQL?**

**Answer:** Process of choosing the most efficient execution plan to improve performance.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021))</b>.</i></p>

---

**Q62. What is the Execution Plan in SQL?**

**Answer:** Visual or textual representation of how SQL Server executes a query.

**Command:**

```sql
SET SHOWPLAN_ALL ON;
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q63. What is Index Partitioning?**

**Answer:** Dividing large indexes into smaller pieces for faster queries.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q64. What is Table Partitioning?**

**Answer:** Splitting a table into smaller parts based on a column (e.g., date).
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q65. What is Sharding in SQL Databases?**

**Answer:** Horizontal partitioning where data is distributed across multiple servers.
<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q66. What is Denormalization?**

**Answer:** Adding redundancy to improve read performance at the cost of storage.
<p align="right"><b><i>Context:</b> Asked at <b>Flipkart (2021)</b>.</i></p>

---

**Q67. What are Windowed Aggregate Functions?**

**Answer:** Aggregates used with OVER() for partitioning.

**Example:**

```sql
SELECT DeptID, Name, 
       SUM(Salary) OVER (PARTITION BY DeptID) AS DeptTotal
FROM Employees;
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q68. What are Recursive CTEs?**

**Answer:** CTEs that reference themselves to process hierarchical data.

**Example:**

```sql
WITH EmpHierarchy AS (
   SELECT EmpID, ManagerID, Name FROM Employees WHERE ManagerID IS NULL
   UNION ALL
   SELECT e.EmpID, e.ManagerID, e.Name 
   FROM Employees e 
   JOIN EmpHierarchy h ON e.ManagerID = h.EmpID
)
SELECT * FROM EmpHierarchy;
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q69. What is the difference between Clustered and Non-Clustered Index with Example?**

**Answer:**

* Clustered → Orders table data physically (only one allowed).
* Non-Clustered → Creates a separate structure (many allowed).
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q70. What is a Covering Index?**

**Answer:** An index that includes all columns required by a query, avoiding table lookup.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q71. What is Query Hint in SQL?**

**Answer:** Special instruction to influence query optimizer.

**Example:**

```sql
SELECT * FROM Employees WITH (NOLOCK);
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q72. What is a Pivot in SQL?**

**Answer:** Technique to convert rows into columns.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q73. What is the difference between PIVOT and UNPIVOT?**

**Answer:**

* PIVOT → Rows → Columns.
* UNPIVOT → Columns → Rows.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q74. What are Temporary Stored Procedures?**

**Answer:** Procedures stored in tempdb, removed automatically when session ends.
<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q75. What is Dynamic SQL?**

**Answer:** SQL code built and executed at runtime.

**Example:**

```sql
EXEC('SELECT * FROM Employees WHERE DeptID = 10');
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q76. What is the difference between CHAR and VARCHAR?**

**Answer:**

* CHAR(n) → Fixed length.
* VARCHAR(n) → Variable length, saves space.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q77. What are SQL Joins vs. UNION?**

**Answer:**

* JOIN → Combines columns.
* UNION → Combines rows.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q78. What is a CROSS APPLY vs OUTER APPLY?**

**Answer:**

* CROSS APPLY → Works like INNER JOIN with table-valued function.
* OUTER APPLY → Works like LEFT JOIN with function.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q79. What is the difference between NVARCHAR and VARCHAR?**

**Answer:**

* NVARCHAR → Stores Unicode (multi-language).
* VARCHAR → Non-Unicode.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q80. What is a Surrogate Key?**

**Answer:** A system-generated key (like identity column) used as primary key instead of natural keys.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q81. What is Query Profiling in SQL?**

**Answer:** Process of analyzing queries to detect performance bottlenecks using tools like `EXPLAIN` or `SET STATISTICS IO`.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q82. What is Parameter Sniffing in SQL Server?**

**Answer:** When SQL Server caches execution plan using initial parameter values, which may not work efficiently for later queries.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q83. What is a Bitmap Index?**

**Answer:** Index storing bitmaps for column values, often used in data warehouses for categorical data.
<p align="right"><b><i>Context:</b> Asked at <b>Oracle (2020)</b>.</i></p>

---

**Q84. What are Filtered Indexes?**
**Answer:** Indexes created with a WHERE clause to cover a subset of rows.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021))</b>.</i></p>

---

**Q85. What is a Hash Join?**

**Answer:** Join that uses hash tables to match rows efficiently for large datasets.
<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q86. What is Query Recompilation?**

**Answer:** When SQL Server discards cached execution plan and compiles a new one.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2020)</b>.</i></p>

---

**Q87. What is Parallel Execution in SQL?**

**Answer:** Splitting a query into multiple threads for faster execution on large datasets.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q88. What are Indexed Views?**

**Answer:** Views with a clustered index created to improve performance.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q89. What is a Dead Tuple in PostgreSQL?**

**Answer:** Rows marked as deleted/updated but still consuming space until VACUUM runs.
<p align="right"><b><i>Context:</b> Asked at <b>Flipkart (2021)</b>.</i></p>

---

**Q90. What is the difference between ACID and BASE properties?**

**Answer:**

* **ACID** → Strong consistency (OLTP).
* **BASE** → Basically Available, Soft state, Eventual consistency (NoSQL).
<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2021)</b>.</i></p>

---

**Q91. What is a Foreign Data Wrapper (FDW) in PostgreSQL?**

**Answer:** Allows PostgreSQL to query external data sources like MySQL, MongoDB.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q92. What is SQL Injection? How to prevent it?**

**Answer:** Malicious code injection in queries. Prevent using **parameterized queries** and **stored procedures**.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q93. What is Database Sharding vs Partitioning?**

**Answer:**

* Partitioning → Within single DB server.
* Sharding → Across multiple servers.
<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q94. What is PolyBase in SQL Server?**

**Answer:** Feature to query external data (Hadoop, Azure Blob, Oracle) using T-SQL.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---

**Q95. What is the difference between Snowflake Schema and Star Schema?**

**Answer:**

* Star → Denormalized, fewer joins, faster queries.
* Snowflake → Normalized, more joins, less storage.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q96. What are Columnstore Indexes?**

**Answer:** Indexes storing data column-wise instead of row-wise, improving analytics queries.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q97. What is a CDC (Change Data Capture)?**

**Answer:** SQL Server feature to track data changes for ETL or auditing.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q98. What is the difference between SQL on-premise vs SQL on Cloud (Azure SQL, AWS RDS)?**

**Answer:**

* On-premise → Full control, manual scaling.
* Cloud → Managed services, auto-scaling, high availability.
<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q99. What is Query Store in SQL Server?**

**Answer:** Feature that captures history of query execution plans and runtime stats for tuning.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---

**Q100. What are the Latest Trends in SQL Databases?**

**Answer:**

* Integration with Big Data (Spark, Hadoop)
* Cloud-native SQL (Snowflake, BigQuery)
* AI-driven query optimization
* HTAP (Hybrid Transactional/Analytical Processing)
<p align="right"><b><i>Context:</b> Asked at <b>Google (2022)</b>.</i></p>

---

