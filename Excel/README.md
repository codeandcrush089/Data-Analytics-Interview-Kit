<div align="center">

#  Top 100 Excel Interview Q&A  
💡 With Real-World Examples + Company Context (FAANG & Startups)

</div>

---

## **Excel Interview Questions (Q1–Q20)**

**Q1.** What are the main differences between Excel and Google Sheets?

**Answer:**

* **Excel:** More advanced formulas, VBA, better for large datasets.
* **Google Sheets:** Cloud-based, real-time collaboration.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q2.** How do you use VLOOKUP in Excel?

**Answer:**
Formula: `=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])`

**Example:**
`=VLOOKUP(101, A2:D20, 3, FALSE)` → Finds employee 101’s salary.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q3.** What is the difference between VLOOKUP and INDEX-MATCH?

**Answer:**

* **VLOOKUP:** Only searches left to right.
* **INDEX-MATCH:** More flexible (can search left or right).

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q4.** How do you use Pivot Tables in Excel?

**Answer:**

* Summarize, filter, and analyze data quickly.

**Example:**
  Show **Total Sales by Region** using Pivot Table.

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q5.** What are Named Ranges in Excel?

**Answer:**

* Assign a name to a cell/range for easy use in formulas.

**Example:**
  If A1\:A10 is named “Sales”, then `=SUM(Sales)` works.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q6.** What is the difference between Relative, Absolute, and Mixed references?

**Answer:**

* Relative: `A1` (changes when copied).
* Absolute: `$A$1` (fixed).
* Mixed: `A$1` or `$A1` (partially fixed).

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q7.** What is Conditional Formatting in Excel?

**Answer:**

* Highlights cells based on rules.

**Example:** Highlight sales > 1000 in green.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q8.** How do you use IF function in Excel?

**Answer:**
Formula: `=IF(condition, value_if_true, value_if_false)`

**Example:** `=IF(A2>50,"Pass","Fail")`
<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q9.** What is the difference between COUNT, COUNTA, COUNTIF, COUNTIFS?

**Answer:**

* COUNT: Numbers only.
* COUNTA: Numbers + text.
* COUNTIF: One condition.
* COUNTIFS: Multiple conditions.
<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q10.** How do you remove duplicates in Excel?

**Answer:**

* Data → Remove Duplicates.
* Or use `UNIQUE()` in Excel 365.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q11.** What is Data Validation in Excel?

**Answer:**

* Restricts data entry (e.g., dropdown lists, numbers only).
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q12.** How do you use CONCATENATE or TEXTJOIN?

**Answer:**

* `=CONCATENATE(A1," ",B1)`
* `=TEXTJOIN(" ", TRUE, A1:A3)` (better for ranges).
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q13.** How do you use LEFT, RIGHT, MID functions?

**Answer:**

* LEFT: Extracts characters from left.
* RIGHT: From right.
* MID: Extracts from middle.
  **Example:** `=LEFT("Excel",2)` → "Ex"
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q14.** What is the difference between TRIM, CLEAN, and SUBSTITUTE?

**Answer:**

* TRIM: Removes extra spaces.
* CLEAN: Removes non-printable chars.
* SUBSTITUTE: Replaces text.
<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q15.** How do you protect a sheet in Excel?

**Answer:**

* Review → Protect Sheet → Set password.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q16.** How do you use MATCH function in Excel?

**Answer:**
Formula: `=MATCH(lookup_value, lookup_array, [match_type])`

**Example:** `=MATCH(50, A1:A10, 0)` → Position of 50.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q17.** What is the difference between HLOOKUP and VLOOKUP?

**Answer:**

* VLOOKUP: Vertical lookup.
* HLOOKUP: Horizontal lookup.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q18.** What is the difference between Charts and Sparklines?

**Answer:**

* Chart: Full visual representation.
* Sparkline: Tiny chart inside a cell.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2022)</b>.</i></p>

---

**Q19.** How do you transpose data in Excel?

**Answer:**

* Paste Special → Transpose.
* Or `=TRANSPOSE(A1:B3)`.
<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q20.** What are Dynamic Arrays in Excel (Excel 365)?

**Answer:**

* Functions like `FILTER()`, `SORT()`, `UNIQUE()`, `SEQUENCE()` that spill results automatically.
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q21.** What is Power Query in Excel?

**Answer:**

* Power Query is used for **data cleaning, transformation, and automation**.
* Found under **Data → Get & Transform**.
<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q22.** How do you use Power Pivot in Excel?
**Answer:**

* Power Pivot helps build **data models, relationships, and DAX calculations**.
  **Context:** Asked at **Deloitte (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q23.** What is the difference between a Table and a Range in Excel?

**Answer:**

* **Table:** Structured, auto-expands, supports slicers.
* **Range:** Static cell selection.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2020)</b>.</i></p>

---

**Q24.** What is the difference between FILTER and Advanced Filter?

**Answer:**

* **Filter:** Quick, applied on data.
* **Advanced Filter:** Extracts filtered results to another location.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q25.** What is the difference between FIND and SEARCH?

**Answer:**

* **FIND:** Case-sensitive.
* **SEARCH:** Case-insensitive.

**Example:** `=FIND("X","Excel")` → Error, but `=SEARCH("x","Excel")` → 1.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q26.** How do you use What-If Analysis in Excel?

**Answer:**
Includes:

* **Scenario Manager** (different business cases).
* **Goal Seek** (find input for target output).
* **Data Tables** (sensitivity analysis).
<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q27.** What is the difference between One-variable and Two-variable Data Tables?

**Answer:**

* One-variable: Impact of one input.
* Two-variable: Impact of two inputs.
<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q28.** What is the difference between Exact Match and Approximate Match in VLOOKUP?

**Answer:**

* **Exact Match (FALSE):** Finds exact value.
* **Approx Match (TRUE):** Finds closest value.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q29.** How do you use Array Formulas in Excel?

**Answer:**

* Perform multiple calculations at once.

**Example:** `=SUM(A1:A3*B1:B3)` (Ctrl+Shift+Enter in old Excel).
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q30.** What is the difference between LEN and LENB?

**Answer:**

* **LEN:** Counts characters.
* **LENB:** Counts bytes (useful in double-byte languages like Chinese).
<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2020)</b>.</i></p>

---

**Q31.** How do you highlight duplicate values using Conditional Formatting?

**Answer:**

* Conditional Formatting → Highlight → Duplicate Values.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q32.** How do you use TEXT function in Excel?

**Answer:**

* Converts values to text in specific formats.

**Example:** `=TEXT(TODAY(),"DD-MMM-YYYY")`
<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q33.** How do you calculate running totals in Excel?

**Answer:**
Formula: `=SUM($B$2:B2)` (copy down).
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q34.** What is the difference between RANK and RANK.EQ?

**Answer:**

* **RANK:** Old function.
* **RANK.EQ:** Modern, ties given same rank.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q35.** How do you split text into multiple columns?

**Answer:**

* Data → Text to Columns.
* Or `=TEXTSPLIT()` in Excel 365.
<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q36.** How do you use the INDIRECT function?

**Answer:**

* Returns a reference from text.

**Example:** `=INDIRECT("A"&1)` → Value in A1.
<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q37.** How do you use OFFSET function in Excel?

**Answer:**

* Returns a range offset from a cell.

**Example:** `=OFFSET(A1,1,2)` → Cell C2.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q38.** How do you use Dynamic Dropdowns in Excel?

**Answer:**

* Create list → Data Validation → List.
* For dependent dropdown: Use INDIRECT with Named Ranges.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q39.** What is the difference between SUBSTITUTE and REPLACE?

**Answer:**

* **SUBSTITUTE:** Replaces text based on match.
* **REPLACE:** Replaces text based on position.
<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q40.** How do you calculate percentage change in Excel?

**Answer:**
Formula: `=(New Value - Old Value)/Old Value`
Format as Percentage.
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---


**Q41.** What is the difference between Workbook and Worksheet?
**Answer:**

* Workbook = Entire Excel file.
* Worksheet = Individual tab inside a workbook.
  **Context:** Asked at **Capgemini (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q42.** What is the difference between Cell, Range, and Named Range?
**Answer:**

* Cell = One value (A1).
* Range = Group of cells (A1\:C5).
* Named Range = User-defined name for a range.
  **Context:** Asked at **TCS (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q43.** What is Power BI vs Power Pivot in Excel?
**Answer:**

* Power Pivot = In-Excel data modeling.
* Power BI = Separate visualization tool, more advanced.
  **Context:** Asked at **EY (2022)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q44.** What is Solver in Excel?
**Answer:**

* Optimization tool → finds best solution under constraints.
  **Example:** Maximize profit with limited resources.
  **Context:** Asked at **Deloitte (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q45.** What is the difference between SUBSTITUTE and TRANSLATE (Excel 365)?
**Answer:**

* SUBSTITUTE: Replace text.
* TRANSLATE: Automatically converts language (newer Excel 365 AI).
  **Context:** Asked at **Microsoft (2022)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q46.** How do you track changes in Excel?
**Answer:**

* Review → Track Changes.
* Or Version History in Excel Online.
  **Context:** Asked at **Accenture (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q47.** What is the difference between Manual vs Automatic Calculation mode?
**Answer:**

* Automatic: Excel recalculates on every change.
* Manual: You need to press F9.
  **Context:** Asked at **Infosys (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q48.** What are Array Constants in Excel?
**Answer:**

* Hard-coded values inside `{}` braces.
  **Example:** `=SUM({1,2,3}*{10,20,30})`
  **Context:** Asked at **EY (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q49.** What is the difference between VALUE() and NUMBERVALUE()?
**Answer:**

* VALUE: Converts text to number.
* NUMBERVALUE: Lets you define decimal & thousands separators.
  **Context:** Asked at **Capgemini (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q50.** What is Flash Fill in Excel?
**Answer:**

* Predictive autofill based on pattern recognition (Ctrl+E).
  **Context:** Asked at **Deloitte (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q51.** How do you use OFFSET with COUNTA for Dynamic Ranges?
**Answer:**
Formula:
`=OFFSET($A$1,0,0,COUNTA($A:$A),1)` → Expands automatically as data grows.
**Context:** Asked at **EY (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q52.** What is the difference between SUMPRODUCT and SUMIFS?
**Answer:**

* SUMPRODUCT: More flexible, can multiply arrays.
* SUMIFS: Works only with conditions.
  **Context:** Asked at **Infosys (2022)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q53.** How do you handle large datasets in Excel?
**Answer:**

* Convert to Table.
* Use Power Query & Power Pivot.
* Avoid volatile formulas.
  **Context:** Asked at **Microsoft (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q54.** How do you create a Dashboard in Excel?
**Answer:**

* Use Pivot Tables, Charts, Slicers, KPIs.
* Link with Named Ranges.
  **Context:** Asked at **Capgemini (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q55.** What is the difference between Active Cell and Active Sheet?
**Answer:**

* Active Cell: The cell currently selected.
* Active Sheet: The worksheet currently displayed.
  **Context:** Asked at **TCS (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q56.** What is the difference between RAND() and RANDBETWEEN()?
**Answer:**

* RAND(): Random number between 0–1.
* RANDBETWEEN(a,b): Random integer between a and b.
  **Context:** Asked at **EY (2022)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q57.** What is VBA in Excel?

**Answer:**

* Visual Basic for Applications → used for automation (Macros).
  **Context:** Asked at **Deloitte (2020)**.<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q58.** How do you record and run a Macro?

**Answer:**

* Developer → Record Macro → Perform actions → Stop.
* Run via Alt+F8.
<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q59.** What is the difference between .XLS, .XLSX, and .XLSM?

**Answer:**

* XLS: Old Excel format (97–2003).
* XLSX: Modern XML-based format.
* XLSM: Macro-enabled file.
<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q60.** How do you import data from external sources into Excel?

**Answer:**

* Data → Get Data (CSV, SQL, Web, API).
* Use Power Query for transformations.
<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

