
<div align="center">

# 📊 Top 100 Power BI Interview Q&A  
💡 With Real-World Examples + Company Context (FAANG & Startups)

</div>


---

**Q1. What is Power BI?**

**Answer:** A Microsoft BI tool for data visualization, ETL, and reporting.

**Context:** **TCS (2021)**.

---

**Q2. Difference between Power BI Desktop and Power BI Service?**
**Answer:**

* Desktop → Development & report creation.
* Service → Cloud sharing, collaboration, dashboards.
  
**Context:** **Accenture (2020)**.

---

**Q3. What are Power BI data sources?**

**Answer:** Excel, SQL Server, Azure, SharePoint, APIs, CSV, cloud sources.

**Context:** **Infosys (2022)**.

---

**Q4. What are calculated columns vs measures in Power BI?**

**Answer:**

* Calculated column → Row-level, stored in table.
* Measure → Calculated on the fly, efficient for aggregations.

**Context:** **EY (2021)**.

---

**Q5. What is DAX in Power BI?**

**Answer:** Data Analysis Expressions – formula language for calculations.

**Context:** **Wipro (2019)**.

---

**Q6. How do you handle relationships in Power BI?**

**Answer:** Using model view → define one-to-one, one-to-many, many-to-many.

**Context:** **Cognizant (2020)**.

---

**Q7. Difference between direct query and import mode?**

**Answer:**

* Import → Data stored in Power BI, faster queries.
* Direct Query → Queries source in real-time, no data stored.

**Context:** **Deloitte (2021)**.

---

**Q8. What is Power Query Editor?**

**Answer:** A tool in Power BI for ETL (cleaning, shaping, transforming data).

**Context:** **Capgemini (2022)**.

---

**Q9. Explain role of filters in Power BI.**

**Answer:** Report-level, page-level, and visual-level filters to restrict data.

**Context:** **HCL (2021)**.

---

**Q10. How do you publish Power BI reports?**

**Answer:** From Desktop → Publish to Power BI Service → Share with users.

**Context:** **Microsoft (2019)**.

---

**Q11. What is a dashboard in Power BI?**

**Answer:** A 1-page canvas with visuals pinned from reports.

**Context:** **Amazon (2022)**.

---

**Q12. What is row-level security (RLS)?**

**Answer:** Restricts data visibility for specific users using DAX filters.

**Context:** **EY (2020)**.

---

**Q13. What are slicers in Power BI?**

**Answer:** Visual filters for dynamic report interaction.

**Context:** **Infosys (2019)**.

---

**Q14. How do you schedule data refresh in Power BI?**

**Answer:** In Power BI Service → Dataset settings → Schedule refresh.

**Context:** **TCS (2021)**.

---

**Q15. Difference between Power BI and Tableau?**

**Answer:**

* Power BI → Cheaper, integrates with MS ecosystem.
* Tableau → Stronger visuals, better for large data.

**Context:** **Deloitte (2022)**.

---

**Q16. What is the difference between a report and a dashboard?**

**Answer:**

* Report → Multiple pages, interactive visuals.
* Dashboard → Single page, summary view.

**Context:** **Cognizant (2020)**.

---

**Q17. What is Power BI Gateway?**

**Answer:** Connects on-premises data with cloud Power BI Service.

**Context:** **Accenture (2021)**.

---

**Q18. Can Power BI connect to real-time data?**

**Answer:** Yes, via DirectQuery, streaming datasets, and APIs.

**Context:** **Flipkart (2022)**.

---

**Q19. What are custom visuals in Power BI?**

**Answer:** Visuals imported from AppSource or custom-built using SDK.

**Context:** **Microsoft (2020)**.

---

**Q20. How do you handle performance issues in Power BI?**

**Answer:** Use star schema, avoid complex DAX, optimize visuals, aggregate data.

**Context:** **PwC (2022)**.

---

**Q21. What are KPIs in Power BI?**

**Answer:** Key Performance Indicators – visuals that compare actual vs target values.

**Context:** **EY (2021)**.

---

**Q22. Difference between star schema and snowflake schema in Power BI?**

**Answer:**

* Star → Fact table in center, direct dimension tables.
* Snowflake → Dimensions normalized into multiple related tables.

**Context:** **Deloitte (2020)**.

---

**Q23. What are bookmarks in Power BI?**

**Answer:** Snapshots of report state, used for storytelling and navigation.

**Context:** **Microsoft (2021)**.

---

**Q24. What are hierarchies in Power BI?**

**Answer:** Levels of drill-down (e.g., Year → Quarter → Month → Day).

**Context:** **Infosys (2020)**.

---

**Q25. What is Q\&A visual in Power BI?**

**Answer:** Allows natural language queries like *“show sales by region”*.

**Context:** **TCS (2019)**.

---

**Q26. Explain composite models in Power BI.**

**Answer:** Combines Import and DirectQuery modes in one dataset.

**Context:** **Accenture (2022)**.

---

**Q27. What are drillthrough filters?**

**Answer:** Allow user to right-click and navigate to a detailed page for selected data.

**Context:** **Wipro (2021)**.

---

**Q28. Difference between append and merge in Power Query?**

**Answer:**

* Append → Stack tables (rows).
* Merge → Join tables (columns).

**Context:** **Capgemini (2020)**.

---

**Q29. What is Quick Insights in Power BI Service?**

**Answer:** AI-powered automatic analysis of datasets.

**Context:** **Microsoft (2019)**.

---

**Q30. Explain ALL() function in DAX.**

**Answer:** Removes filters from a column or table.

**Example:**

```DAX
TotalSales = CALCULATE(SUM(Sales[Amount]), ALL(Sales))
```

**Context:** **Cognizant (2021)**.

---

**Q31. What is the difference between SUM() and SUMX() in DAX?**

**Answer:**

* SUM() → Aggregates column values.
* SUMX() → Row-wise calculation, then aggregation.

**Context:** **Deloitte (2021)**.

---

**Q32. What are live connections in Power BI?**

**Answer:** Real-time connection to SSAS, Azure Analysis Services, or datasets without importing.

**Context:** **EY (2022)**.

---

**Q33. What is Power BI Embedded?**

**Answer:** Service to embed Power BI reports into custom apps/websites.

**Context:** **Microsoft (2020)**.

---

**Q34. What are themes in Power BI?**

**Answer:** JSON-based color, font, and layout styles for consistent report design.

**Context:** **Infosys (2019)**.

---

**Q35. Explain difference between ALL() and ALLEXCEPT() in DAX.**

**Answer:**

* ALL() → Removes all filters.
* ALLEXCEPT() → Removes all filters except specified columns.

**Context:** **Accenture (2021)**.

---

**Q36. What are parameters in Power BI?**

**Answer:** Used for dynamic queries, filter inputs, and scenario analysis.

**Context:** **Capgemini (2022)**.

---

**Q37. What is incremental refresh in Power BI?**

**Answer:** Refreshes only new or changed data instead of entire dataset.

**Context:** **Amazon (2021)**.

---

**Q38. What is drill-down vs drill-up in Power BI?**

**Answer:**

* Drill-down → Go deeper into detail (Year → Month).
* Drill-up → Go back to summary view.

**Context:** **TCS (2020)**.

---

**Q39. How do you use DAX RELATED() function?**

**Answer:** Fetches values from related tables.

**Example:**

```DAX
Region = RELATED(Regions[Name])
```

**Context:** **Wipro (2021)**.

---

**Q40. How do you optimize DAX calculations?**

**Answer:** Use variables, avoid nested IFs, reduce row context, prefer SUMX over FILTER-heavy queries.

**Context:** **Deloitte (2022)**.

---


**Q41. What is the difference between Remove Duplicates in Power Query vs DISTINCT in DAX?**

**Answer:**

* Power Query Remove Duplicates → physically removes duplicate rows.
* DISTINCT in DAX → returns unique values virtually during calculation.

**Context:** **EY (2020)**.

---

**Q42. What is CALCULATE() in DAX?**

**Answer:** Evaluates an expression in a modified filter context.

**Example:**

```DAX
Sales_2022 = CALCULATE(SUM(Sales[Amount]), Sales[Year]=2022)
```

**Context:** **Microsoft (2021)**.

---

**Q43. How do you implement dynamic titles in Power BI?**

**Answer:** Create a measure with selected value and bind it to title property.

**Context:** **Accenture (2022)**.

---

**Q44. What are Tooltips in Power BI?**

**Answer:** Hover-over visuals that show extra info. Custom tooltips can be built as report pages.

**Context:** **TCS (2019)**.

---

**Q45. Difference between calculated tables and calculated columns?**

**Answer:**

* Calculated Table → Whole new table from DAX.
* Calculated Column → Extra column in existing table.

**Context:** **Deloitte (2021)**.

---

**Q46. What are roles in Power BI?**

**Answer:** Define security rules (e.g., region-wise data restriction) using DAX filters.

**Context:** **Wipro (2020)**.

---

**Q47. What is the purpose of HASONEVALUE() in DAX?**

**Answer:** Checks if a column has only one value in current context.

**Example:**

```DAX
IF(HASONEVALUE(Region[Name]), VALUES(Region[Name]), "Multiple")
```

**Context:** **Capgemini (2021)**.

---

**Q48. What are quick measures in Power BI?**

**Answer:** Pre-built DAX templates for calculations like running totals, YOY growth.

**Context:** **Microsoft (2019)**.

---

**Q49. Difference between ALLSELECTED() and ALL() in DAX?**

**Answer:**

* ALL() → Ignores all filters.
* ALLSELECTED() → Ignores filters but respects user selections (slicers).

**Context:** **Cognizant (2021)**.

---

**Q50. What are paginated reports in Power BI?**

**Answer:** Pixel-perfect reports (like invoices) created with Power BI Report Builder.

**Context:** **EY (2022)**.

---

**Q51. What is CROSSJOIN() in DAX?**

**Answer:** Returns Cartesian product of two tables.

**Context:** **Infosys (2021)**.

---

**Q52. How do you perform conditional formatting in Power BI?**

**Answer:** Apply rules or DAX measures to control color/formatting of visuals.

**Context:** **Accenture (2020)**.

---

**Q53. What is USERELATIONSHIP() in DAX?**

**Answer:** Activates an inactive relationship temporarily.

**Example:**

```DAX
SalesByShipDate = CALCULATE(SUM(Sales[Amount]), USERELATIONSHIP(Sales[ShipDate], Calendar[Date]))
```

**Context:** **Deloitte (2021)**.

---

**Q54. What are aggregations in Power BI?**

**Answer:** Pre-computed summary tables used to speed up DirectQuery datasets.

**Context:** **Microsoft (2020)**.

---

**Q55. How to handle circular dependencies in Power BI?**

**Answer:** Restructure model, reduce calculated columns, or use measures instead.

**Context:** **PwC (2022)**.

---

**Q56. What is RLS with dynamic security in Power BI?**

**Answer:** Security rules driven by user login (e.g., filter by user email).

**Context:** **Amazon (2022)**.

---

**Q57. What is difference between VALUES() and DISTINCT() in DAX?**

**Answer:**

* VALUES() → Returns unique values but keeps blank row (for missing relationships).
* DISTINCT() → Returns only unique values, no blank row.

**Context:** **Infosys (2020)**.

---

**Q58. What is SELECTEDVALUE() in DAX?**

**Answer:** Returns selected value from column; returns alternate result if multiple values.

**Example:**

```DAX
SelectedRegion = SELECTEDVALUE(Region[Name], "Multiple")
```

**Context:** **Wipro (2021)**.

---

**Q59. What are dataflows in Power BI?**

**Answer:** ETL processes in the cloud using Power Query, reusable across datasets.

**Context:** **Microsoft (2019)**.

---

**Q60. How do you enable drillthrough with multiple fields?**

**Answer:** Add multiple fields in drillthrough filters area; user can drill based on selected fields.

**Context:** **Deloitte (2022)**.

---


**Q61. What is the difference between implicit and explicit measures in Power BI?**

**Answer:**

* Implicit → Auto-created when dragging fields into visuals (SUM, COUNT).
* Explicit → User-defined using DAX.

**Context:** **EY (2020)**.

---

**Q62. How do you use TOPN() in DAX?**

**Answer:** Returns top N rows by expression.

**Example:**

```DAX
Top3Products = TOPN(3, Products, Products[Sales], DESC)
```

**Context:** **Infosys (2021)**.

---

**Q63. What is Power BI Mobile App used for?**

**Answer:** View, interact, and share dashboards/reports on mobile devices.

**Context:** **Microsoft (2019)**.

---

**Q64. What is the difference between REMOVEFILTERS() and ALL() in DAX?**

**Answer:**

* REMOVEFILTERS() → Removes filters but doesn’t add extra rows.
* ALL() → Removes filters and adds back “blank” row.

**Context:** **Accenture (2022)**.

---

**Q65. What is drillthrough with Keep All Filters option?**

**Answer:** Carries all applied filters to the drillthrough page along with the selected one.

**Context:** **Deloitte (2021)**.

---

**Q66. What is the purpose of GENERATE() in DAX?**

**Answer:** Combines each row of one table with rows from another table expression.

**Context:** **TCS (2020)**.

---

**Q67. What is Publish to Web in Power BI?**

**Answer:** Creates a public URL/embed code for sharing reports externally.

**Context:** **Microsoft (2020)**.

---

**Q68. What are calculation groups in Power BI?**

**Answer:** Allow reusing common calculations (like YTD, QoQ) across multiple measures.

**Context:** **EY (2022)**.

---

**Q69. What is performance analyzer in Power BI Desktop?**

**Answer:** Tool to measure DAX, visual, and query execution times.

**Context:** **Capgemini (2021)**.

---

**Q70. What is difference between Many-to-Many and One-to-Many in Power BI relationships?**

**Answer:**

* One-to-Many → Common star schema relationship.
* Many-to-Many → Requires bridge tables or bi-directional filtering.

**Context:** **Wipro (2020)**.

---

**Q71. What is drillthrough detail report in Power BI Service?**

**Answer:** Allows clicking a data point and opening a pre-defined detail report page.

**Context:** **Infosys (2021)**.

---

**Q72. How do you hide and unhide fields in Power BI?**

**Answer:** In Fields pane → Right click → Hide/Unhide in report view.

**Context:** **Accenture (2019)**.

---

**Q73. What is the use of GROUPBY() in DAX?**

**Answer:** Creates summary tables grouped by columns with aggregated results.

**Context:** **Deloitte (2020)**.

---

**Q74. What is Power BI Premium?**

**Answer:** Dedicated capacity for large datasets, paginated reports, AI features, and enterprise sharing.

**Context:** **Microsoft (2021)**.

---

**Q75. What are parameters vs slicers in Power BI?**

**Answer:**

* Parameters → Used for queries/model control.
* Slicers → User filters in report UI.

**Context:** **EY (2020)**.

---

**Q76. What is CALCULATETABLE() in DAX?**

**Answer:** Returns a table expression filtered by given conditions.

**Example:**

```DAX
HighSales = CALCULATETABLE(Sales, Sales[Amount]>1000)
```

**Context:** **Capgemini (2021)**.

---

**Q77. What is difference between SUMMARIZE() and SUMMARIZECOLUMNS()?**

**Answer:**

* SUMMARIZE() → More flexible, but can create unwanted rows.
* SUMMARIZECOLUMNS() → Optimized for grouping with no unwanted rows.

**Context:** **TCS (2019)**.

---

**Q78. What is Power BI REST API used for?**

**Answer:** Automates tasks like dataset refresh, embed, and report management.

**Context:** **Microsoft (2022)**.

---

**Q79. What is row context vs filter context in DAX?**

**Answer:**

* Row context → Evaluates per row.
* Filter context → Result after applying filters.

**Context:** **Deloitte (2021)**.

---

**Q80. What are quick insights limitations in Power BI?**

**Answer:** Limited dataset size, no DirectQuery support, AI-driven only (no custom logic).

**Context:** **EY (2021)**.

---

**Q81.** How do you handle circular dependencies in Power BI?

**Answer:**

* Avoid bi-directional relationships.
* Use **CALCULATE with CROSSFILTER** to control filter direction.
* Break the loop by introducing a bridge table.

**Example:** `CALCULATE(SUM(Sales[Amount]), CROSSFILTER(Customer[ID], Sales[CustomerID], OneWay))`

**Context:** Asked at **TCS (2023)**.

---

**Q82.** What are Aggregations in Power BI?

**Answer:** Pre-calculated summaries of large tables to optimize performance.

**Example:** Store daily sales totals instead of transaction-level data.

**Context:** Asked at **Adobe (2022)**.

---

**Q83.** What is Row-Level Security (RLS) with dynamic filters?

**Answer:** RLS restricts data access per user. Dynamic filters adjust based on login credentials.

**Example:** `USERNAME()` function to filter region-wise sales.

**Context:** Asked at **Flipkart (2021)**.

---

**Q84.** Difference between Measures and Calculated Columns?

**Answer:**

* **Measure:** Calculated at query time, lightweight.
* **Column:** Stored in the model, consumes memory.
  **Example:**
* Measure → `SUM(Sales[Amount])`
* Column → `Profit = Sales[Revenue] - Sales[Cost]`

**Context:** Asked at **Cognizant (2022)**.

---

**Q85.** What are Synonyms in Power BI Q\&A?

**Answer:** Alternative terms defined for fields/tables to improve natural language queries in **Q\&A visual**.

**Example:** Defining “Revenue” as a synonym for “SalesAmount”.

**Context:** Asked at **Microsoft (2020)**.

---

**Q86.** How do you handle data refresh failures in Power BI Service?

**Answer:**

* Check gateway connection.
* Validate credentials.
* Optimize queries for performance.
* Use refresh history logs.

**Context:** Asked at **Infosys (2023)**.

---

**Q87.** What is the difference between Import Mode and Live Connection in terms of performance?

**Answer:**

* **Import Mode:** Faster queries, supports DAX, consumes memory.
* **Live Connection:** Real-time but depends on source performance.

**Context:** Asked at **Deloitte (2021)**.

---

**Q88.** What are Hierarchies in Power BI?

**Answer:** Logical grouping of fields for drill-down analysis.

**Example:** Date → Year → Quarter → Month → Day.

**Context:** Asked at **Accenture (2020)**.

---

**Q89.** What is the difference between Personal Gateway and On-Premises Gateway (Standard)?

**Answer:**

* **Personal:** Works for one user, no shared connections.
* **Standard:** Shared, supports multiple users and scheduled refresh.

**Context:** Asked at **KPMG (2022)**.

---

**Q90.** How do you optimize DAX queries?

**Answer:**

* Avoid `CALCULATE` inside `FILTER` unnecessarily.
* Use **variables (VAR)**.
* Use `SUMX` only when required.
  **Example:**

```DAX
VAR totalSales = SUM(Sales[Amount])
RETURN totalSales * 0.1
```

**Context:** Asked at **Capgemini (2021)**.

---

**Q91.** What is Drillthrough in Power BI?

**Answer:** A feature that allows users to right-click on a data point and navigate to a detailed report page.

**Context:** Asked at **EY (2023)**.

---

**Q92.** What is the difference between DirectQuery and Dual Storage Mode?

**Answer:**

* **DirectQuery:** Queries source directly.
* **Dual:** Acts as both Import and DirectQuery, depending on query context.

**Context:** Asked at **PwC (2021)**.

---

**Q93.** How do you enable incremental refresh in Power BI?
**Answer:**

* Define **RangeStart** and **RangeEnd** parameters.
* Configure **incremental refresh policy** in Power BI Desktop.

**Context:** Asked at **Amazon (2023)**.

---

**Q94.** What are Bookmarks in Power BI?

**Answer:** Capture current report view, including filters and visuals, for navigation and storytelling.

**Context:** Asked at **Adobe (2022)**.

---

**Q95.** What is the difference between ALL, ALLEXCEPT, and ALLSELECTED in DAX?

**Answer:**

* **ALL:** Ignores all filters.
* **ALLEXCEPT:** Ignores all except specified columns.
* **ALLSELECTED:** Ignores filters but respects user selections.

**Context:** Asked at **Infosys (2020)**.

---

**Q96.** How do you publish reports securely to Power BI Service?

**Answer:**

* Use **App Workspaces**.
* Apply **RLS**.
* Share via **apps**, not direct reports.

**Context:** Asked at **HCL (2021)**.

---

**Q97.** What are KPI visuals in Power BI?

**Answer:** Visuals that track performance against a target.

**Example:** Actual vs. Target Sales.

**Context:** Asked at **Deloitte (2022)**.

---

**Q98.** What is the difference between Calculated Table and Calculated Column?

**Answer:**

* **Table:** Entire table generated with DAX.
* **Column:** Added to existing table.
  **Example:**
* Table → `SUMMARIZE(Sales, Sales[Region], "Total", SUM(Sales[Amount]))`
* Column → `Profit = Revenue - Cost`

**Context:** Asked at **IBM (2021)**.

---

**Q99.** How do you handle many-to-many relationships in Power BI?

**Answer:**

* Use **bridge tables**.
* Use **DAX functions** like `TREATAS`.
  **Example:** `CALCULATE(SUM(Sales[Amount]), TREATAS(VALUES(Products[Category]), Sales[Category]))`

**Context:** Asked at **Wipro (2020)**.

---

**Q100.** What are some limitations of Power BI?

**Answer:**

* Dataset size limit (1 GB for Pro).
* Limited real-time refresh.
* RLS not supported in all scenarios.

**Context:** Asked at **TCS (2022)**.


