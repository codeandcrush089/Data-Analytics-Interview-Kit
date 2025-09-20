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

