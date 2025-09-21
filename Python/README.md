<div align="center">

<img src="https://www.python.org/static/community_logos/python-logo.png" alt="Python Logo" width="150"/>

# Top 100 Python Interview Q&A  
💡 With Real-World Examples + Company Context (FAANG & Startups)

</div>


---

**Q1. What are Python’s main data types used in data science?**

**Answer:** Common ones are `int`, `float`, `str`, `bool`, `list`, `tuple`, `dict`, `set`. For data science, `list`, `dict`, and `tuple` are often used for data manipulation.

**Example:**

```python
x = [1, 2, 3]   # list
y = (1, 2, 3)   # tuple
z = {"a":1, "b":2} # dict
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q2. Difference between list and tuple in Python?**

**Answer:** Lists are mutable, tuples are immutable.

**Example:**

```python
lst = [1, 2, 3]
lst[0] = 10   # works
tup = (1, 2, 3)
# tup[0] = 10 -> Error
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q3. What is the difference between `is` and `==` in Python?**

**Answer:** `==` checks value equality, `is` checks identity (same memory reference).

**Example:**

```python
a = [1,2,3]
b = [1,2,3]
print(a == b) # True
print(a is b) # False
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2019)</b>.</i></p>

---

**Q4. Explain Python’s `None` object.**

**Answer:** `None` represents absence of a value. It’s not `0` or `False`.

**Example:**

```python
def func():
    return None
print(func()) # None
```

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2020)</b>.</i></p>

---

**Q5. How is Python’s memory management handled?**

**Answer:** Python uses reference counting and garbage collection to free unused memory.

<p align="right"><b><i>Context:</b> Asked at <b>Google (2022))</b>.</i></p>

---

**Q6. What are Python’s key libraries for data analysis?**

**Answer:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn.

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2023)</b>.</i></p>

---

**Q7. Explain Pandas `DataFrame` vs `Series`.**

**Answer:** `Series` is 1D labeled array, `DataFrame` is 2D table of rows & columns.

**Example:**

```python
import pandas as pd
s = pd.Series([1,2,3])
df = pd.DataFrame({"A":[1,2], "B":[3,4]})
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q8. How do you handle missing values in Pandas?**

**Answer:** Using `dropna()`, `fillna()`, or interpolation.

**Example:**

```python
df['col'].fillna(df['col'].mean(), inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2022)</b>.</i></p>

---

**Q9. Difference between Python’s `append()` and `extend()` for lists?**

**Answer:** `append()` adds a single element, `extend()` adds multiple elements.

**Example:**

```python
lst = [1,2]
lst.append([3,4])  # [1,2,[3,4]]
lst.extend([3,4])  # [1,2,3,4]
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2021)</b>.</i></p>

---

**Q10. What is Python’s GIL (Global Interpreter Lock)?**

**Answer:** GIL ensures only one thread executes Python bytecode at a time, limiting true multithreading for CPU-bound tasks.

<p align="right"><b><i>Context:</b> Asked at <b>Adobe (2020)</b>.</i></p>

---

**Q11. What’s the difference between `loc` and `iloc` in Pandas?**

**Answer:** `loc` = label-based, `iloc` = integer-based indexing.

**Example:**

```python
df.loc[0, 'A']
df.iloc[0, 0]
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2023)</b>.</i></p>

---

**Q12. How do you merge/join DataFrames in Pandas?**

**Answer:** Using `merge()`, `join()`, or `concat()`.

**Example:**

```python
pd.merge(df1, df2, on="id")
```

<p align="right"><b><i>Context:</b> Asked at <b>KPMG (2022))</b>.</i></p>

---

**Q13. What’s the difference between Python’s `deepcopy` and `shallow copy`?**

**Answer:** Shallow copy copies references, deep copy creates independent objects.

**Example:**

```python
import copy
a = [[1,2],[3,4]]
b = copy.copy(a)     # shallow
c = copy.deepcopy(a) # deep
```

<p align="right"><b><i>Context:</b> Asked at <b>Paytm (2021)</b>.</i></p>

---

**Q14. What is the use of Python’s `with` statement?**

**Answer:** Used for context managers (e.g., file handling), ensures cleanup.

**Example:**

```python
with open("file.txt","r") as f:
    data = f.read()
```

<p align="right"><b><i>Context:</b> Asked at <b>Oracle (2019)</b>.</i></p>

---

**Q15. How do you check data types of a DataFrame?**

**Answer:** Using `df.dtypes` or `df.info()`.

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q16. Explain lambda functions in Python.**

**Answer:** Small anonymous functions using `lambda`.

**Example:**

```python
square = lambda x: x*x
print(square(5)) # 25
```

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2022)</b>.</i></p>

---

**Q17. What’s the difference between `iterrows()` and `itertuples()` in Pandas?**

**Answer:** `iterrows()` returns index + row as Series, `itertuples()` is faster, returns namedtuples.

<p align="right"><b><i>Context:</b> Asked at <b>HCL (2021)</b>.</i></p>

---

**Q18. How do you remove duplicates in Pandas?**

**Answer:** Using `drop_duplicates()`.

**Example:**

```python
df.drop_duplicates(subset=["col"], inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2023)</b>.</i></p>

---

**Q19. Explain difference between Python’s `@staticmethod` and `@classmethod`.**

**Answer:** `staticmethod()` doesn’t access class/instance, `classmethod()` takes `cls` as first arg and modifies class state.

<p align="right"><b><i>Context:</b> Asked at <b>IBM (2022))</b>.</i></p>

---

**Q20. How do you improve performance of large Pandas DataFrames?**

**Answer:** Use vectorization, `categorical` dtype, chunking, parallelization.

<p align="right"><b><i>Context:</b> Asked at <b>Uber (2020))</b>.</i></p>

---



**Q21. What are Python decorators?**

**Answer:** Functions that modify the behavior of other functions or methods.
 
**Example:**

```python
def decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@decorator
def hello():
    print("Hello")

hello()
```

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2021)</b>.</i></p>

---

**Q22. Difference between NumPy array and Python list?**

**Answer:** NumPy arrays are faster, support vectorized operations, and consume less memory compared to lists.

**Example:**

```python
import numpy as np
arr = np.array([1,2,3])
print(arr*2)  # [2 4 6]
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2020)</b>.</i></p>

---

**Q23. How to handle categorical variables in Python for ML?**

**Answer:** Use One-hot encoding (`pd.get_dummies`), Label Encoding, or libraries like Scikit-learn.

<p align="right"><b><i>Context:</b> Asked at <b>Uber (2022)</b>.</i></p>

---

**Q24. What is the use of Python’s `zip()`?**

**Answer:** Combines multiple iterables into tuples.

**Example:**

```python
a = [1,2,3]
b = ['a','b','c']
print(list(zip(a,b))) # [(1,'a'), (2,'b'), (3,'c')]
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q25. Explain `*args` and `**kwargs`.**

**Answer:** `*args` passes variable number of positional arguments, `**kwargs` passes variable keyword arguments.

**Example:**

```python
def func(*args, **kwargs):
    print(args, kwargs)
func(1,2, a=10, b=20)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2022)</b>.</i></p>

---

**Q26. How do you filter rows in Pandas DataFrame?**

**Answer:** Using Boolean indexing.

**Example:**

```python
df[df['col'] > 10]
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2023)</b>.</i></p>

---

**Q27. What are Python’s iterators and generators?**

**Answer:** Iterators use `__iter__()` and `__next__()`. Generators use `yield` and are memory efficient.

**Example:**

```python
def gen():
    for i in range(3):
        yield i
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q28. What is pickling in Python?**

**Answer:** Process of serializing Python objects into byte streams using `pickle` module.

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q29. Difference between `apply()`, `map()`, and `applymap()` in Pandas?**

**Answer:**

* `map()` → element-wise for Series.
* `apply()` → applies function along axis of DataFrame.
* `applymap()` → element-wise for DataFrame.
  
<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2022)</b>.</i></p>

---

**Q30. What are Python comprehensions?**

**Answer:** Short syntax for creating lists, dicts, and sets.

**Example:**

```python
squares = [x*x for x in range(5)]
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2021)</b>.</i></p>

---

**Q31. How do you check unique values in a Pandas column?**

**Answer:** Using `df['col'].unique()` or `df['col'].nunique()`.

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q32. Explain Python’s `enumerate()` function.**

**Answer:** Returns index and value while iterating.

**Example:**

```python
for i,v in enumerate(['a','b']):
    print(i,v)
```

<p align="right"><b><i>Context:</b> Asked at <b>Oracle (2019)</b>.</i></p>

---

**Q33. How do you measure execution time of Python code?**

**Answer:** Using `time` module or `timeit`.

**Example:**

```python
import time
start = time.time()
sum(range(100000))
print(time.time()-start)
```

<p align="right"><b><i>Context:</b> Asked at <b>Google (2021)</b>.</i></p>

---

**Q34. Explain broadcasting in NumPy.**

**Answer:** Technique to perform arithmetic on arrays of different shapes.

**Example:**

```python
import numpy as np
a = np.array([1,2,3])
b = 2
print(a+b) # [3 4 5]
```

<p align="right"><b><i>Context:</b> Asked at <b>NVIDIA (2022))</b>.</i></p>

---

**Q35. Difference between `.ix`, `.loc`, and `.iloc` in Pandas?**

**Answer:** `.ix` is deprecated; use `.loc` for labels, `.iloc` for integer positions.

<p align="right"><b><i>Context:</b> Asked at <b>PwC (2020)**</b>.</i></p>

---

**Q36. How to concatenate strings efficiently in Python?**

**Answer:** Use `join()` instead of `+` for large strings.

**Example:**

```python
"".join(["Data","Science"])
```

<p align="right"><b><i>Context:</b> Asked at <b>IBM (2021)</b>.</i></p>

---

**Q37. What is Python’s `Counter` from collections?**

**Answer:** A dict subclass to count elements.

**Example:**

```python
from collections import Counter
print(Counter("analytics"))
```

<p align="right"><b><i>Context:</b> Asked at <b>Flipkart (2022)</b>.</i></p>

---

**Q38. Explain `groupby()` in Pandas.**

**Answer:** Groups data and applies aggregate functions.

**Example:**

```python
df.groupby("col")["value"].mean()
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q39. What are Python’s f-strings?**

**Answer:** String formatting method introduced in Python 3.6.

**Example:**

```python
name="Data"
print(f"Hello {name}")
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q40. How do you check Python version in code?**

**Answer:**

```python
import sys
print(sys.version)
```

<p align="right"><b><i>Context:</b> Asked at <b>HCL (2019)</b>.</i></p>

---


**Q41. What are Python’s built-in data structures?**

**Answer:** List, Tuple, Set, Dictionary.

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q42. How do you convert a list to a NumPy array?**

**Answer:** Use `np.array(list)`.

**Example:**

```python
import numpy as np
arr = np.array([1,2,3])
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q43. Difference between shallow copy and assignment in Python?**

**Answer:** Assignment makes both variables point to the same object; shallow copy makes a new object but references nested objects.

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q44. How do you drop a column in Pandas?**

**Answer:**

```python
df.drop("col", axis=1, inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q45. What is Python’s `__init__` method?**

**Answer:** Constructor method used to initialize objects in classes.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2019)</b>.</i></p>

---

**Q46. How do you create pivot tables in Pandas?**

**Answer:** Using `pd.pivot_table()`.

**Example:**

```python
pd.pivot_table(df, values='sales', index='region', aggfunc='sum')
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2023)</b>.</i></p>

---

**Q47. Explain difference between `head()` and `tail()` in Pandas.**

**Answer:** `head()` shows first n rows, `tail()` shows last n rows.

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q48. How do you handle outliers in data?**

**Answer:** Methods: IQR, Z-score, capping, transformation.

<p align="right"><b><i>Context:</b> Asked at <b>KPMG (2022))</b>.</i></p>

---

**Q49. Difference between `numpy.nan` and `None`?**

**Answer:** `nan` is numeric missing value, `None` is Python object type missing value.

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2021)</b>.</i></p>

---

**Q50. How do you merge DataFrames with different keys?**

**Answer:** Use `merge(left_on=..., right_on=...)`.

**Example:**

```python
pd.merge(df1, df2, left_on="id1", right_on="id2")
```

<p align="right"><b><i>Context:</b> Asked at <b>PwC (2023)</b>.</i></p>

---

**Q51. What is the use of `assert` in Python?**

**Answer:** Debugging tool to check conditions during execution.

**Example:**

```python
x = 5
assert x > 0
```

<p align="right"><b><i>Context:</b> Asked at <b>Google (2020)</b>.</i></p>

---

**Q52. How do you reset index in Pandas?**

**Answer:**

```python
df.reset_index(drop=True, inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2019)</b>.</i></p>

---

**Q53. Difference between `any()` and `all()` in Python?**

**Answer:**

* `any()` → True if at least one element is True.
* `all()` → True if all elements are True.

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---

**Q54. Explain Python’s `range()` vs NumPy’s `arange()`.**

**Answer:** `range()` supports integers only, `arange()` supports floats and step sizes.

**Example:**

```python
import numpy as np
print(np.arange(0,1,0.2))  # [0. 0.2 0.4 0.6 0.8]
```

<p align="right"><b><i>Context:</b> Asked at <b>NVIDIA (2022)</b>.</i></p>

---

**Q55. How to check missing values in Pandas?**

**Answer:** Use `df.isnull().sum()`.

<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q56. Difference between `.values` and `.to_numpy()` in Pandas?**

**Answer:** `.to_numpy()` is recommended; `.values` may return inconsistent types.

<p align="right"><b><i>Context:</b> Asked at <b>Oracle (2021)</b>.</i></p>

---

**Q57. How do you sort a DataFrame?**

**Answer:** Use `sort_values()` or `sort_index()`.

**Example:**

```python
df.sort_values("col", ascending=False)
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q58. Explain Python’s `id()` function.**

**Answer:** Returns unique identifier (memory address) of an object.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2019)</b>.</i></p>

---

**Q59. How do you check correlation between variables in Pandas?**

**Answer:** Use `df.corr()`.

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2022)</b>.</i></p>

---

**Q60. What is the difference between `pop()` and `remove()` in Python lists?**

**Answer:**

* `pop(index)` removes element at index (default last) and returns it.
* `remove(value)` removes first matching value.
  
<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2021)</b>.</i></p>

---



**Q61. What is the difference between `.ix`, `.loc`, and `.iloc` in Pandas?**

**Answer:** `.ix` is deprecated; `.loc` is label-based; `.iloc` is integer-location-based.

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2020)</b>.</i></p>

---

**Q62. How do you drop NA rows only for specific columns?**

**Answer:**

```python
df.dropna(subset=["col1", "col2"], inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q63. What’s the difference between Python’s `copy()` and `deepcopy()`?**

**Answer:** `copy()` = shallow, `deepcopy()` = independent full copy.

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2019)</b>.</i></p>

---

**Q64. How do you find duplicates in Pandas?**

**Answer:**

```python
df.duplicated().sum()
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q65. Explain `np.dot()` vs `np.matmul()`.**

**Answer:** Both are matrix multiplication; `np.matmul()` works with stacks of matrices too.

<p align="right"><b><i>Context:</b> Asked at <b>NVIDIA (2022)</b>.</i></p>

---

**Q66. How to remove whitespace from strings in Python?**

**Answer:** Use `strip()`, `lstrip()`, `rstrip()`.

**Example:**

```python
" data ".strip()
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q67. What are Python’s `namedtuple`s?**

**Answer:** Tuple subclass with named fields for readability.

**Example:**

```python
from collections import namedtuple
Point = namedtuple("Point","x y")
p = Point(1,2)
```

<p align="right"><b><i>Context:</b> Asked at <b>IBM (2021)</b>.</i></p>

---

**Q68. How do you check data types in NumPy array?**

**Answer:** Using `arr.dtype`.

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2020)</b>.</i></p>

---

**Q69. Difference between JSON and Pickle in Python?**

**Answer:** JSON = human-readable, cross-language; Pickle = Python-specific, binary.

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q70. How do you create dummy variables in Pandas?**

**Answer:**

```python
pd.get_dummies(df["category"])
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2023)</b>.</i></p>

---

**Q71. What are Python’s `global` and `nonlocal` keywords?**

**Answer:**

* `global` → modifies variable outside current scope.
* `nonlocal` → modifies variable in nearest enclosing scope (not global).

<p align="right"><b><i>Context:</b> Asked at <b>Oracle (2019)</b>.</i></p>

---

**Q72. How do you check the shape of a DataFrame?**

**Answer:** `df.shape`.

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2021)</b>.</i></p>

---

**Q73. Explain Python’s `staticmethod`.**

**Answer:** Method bound to class, not instance; doesn’t access `self` or `cls`.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q74. How do you select random samples from DataFrame?**

**Answer:** Using `df.sample(n=5)` or with `frac`.

<p align="right"><b><i>Context:</b> Asked at <b>EV (2021)</b>.</i></p>

---

**Q75. What is the difference between `isnull()` and `notnull()` in Pandas?**

**Answer:** `isnull()` detects missing values, `notnull()` detects non-missing.

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q76. How do you combine multiple CSV files in Python?**

**Answer:** Use `glob` + `pd.concat()`.

**Example:**

```python
import pandas as pd, glob
files = glob.glob("*.csv")
df = pd.concat([pd.read_csv(f) for f in files])
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2023)</b>.</i></p>

---

**Q77. Difference between Python’s `int()` and `float()` casting?**

**Answer:** `int()` converts to integer (truncates decimals), `float()` converts to floating-point.

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2019)</b>.</i></p>

---

**Q78. How to detect outliers with Z-score in Python?**

**Answer:**

```python
from scipy import stats
z = np.abs(stats.zscore(df["col"]))
df[z < 3]
```

<p align="right"><b><i>Context:</b> Asked at <b>KPMG (2021)</b>.</i></p>

---

**Q79. What is the difference between `@classmethod` and instance methods?**

**Answer:** Instance methods take `self`, classmethods take `cls`.

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2020)</b>.</i></p>

---

**Q80. How do you convert DataFrame to NumPy array?**

**Answer:** `df.to_numpy()`.

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---



**Q81. How do you rename columns in Pandas?**

**Answer:**

```python
df.rename(columns={"old":"new"}, inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q82. What are Python’s context managers?**

**Answer:** They manage resources (like files, DB connections) using `with` statement.

<p align="right"><b><i>Context:</b> Asked at <b>Google (2020)</b>.</i></p>

---

**Q83. How to create multi-index DataFrame in Pandas?**

**Answer:** Using `set_index()` with multiple columns.

**Example:**

```python
df.set_index(["col1","col2"], inplace=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q84. What is the difference between `numpy.linspace()` and `numpy.arange()`?**

**Answer:** `linspace()` generates evenly spaced values with fixed number of points; `arange()` uses step size.

<p align="right"><b><i>Context:</b> Asked at <b>NVIDIA (2021)</b>.</i></p>

---

**Q85. How do you check memory usage of a DataFrame?**

**Answer:** `df.memory_usage(deep=True).sum()`.

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q86. Explain difference between Python’s `sort()` and `sorted()`.**

**Answer:**

* `sort()` → in-place, for lists only.
* `sorted()` → returns new list, works with any iterable.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2019)</b>.</i></p>

---

**Q87. How do you select top N rows per group in Pandas?**

**Answer:**

```python
df.groupby("group").head(3)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q88. What are Python’s dataclasses?**

**Answer:** Introduced in Python 3.7, provide boilerplate-free class creation.

**Example:**

```python
from dataclasses import dataclass
@dataclass
class Item:
    name: str
    price: float
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2020)</b>.</i></p>

---

**Q89. How do you export a DataFrame to Excel?**

**Answer:**

```python
df.to_excel("output.xlsx", index=False)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2023)</b>.</i></p>

---

**Q90. Explain difference between `inner`, `left`, `right`, and `outer` joins in Pandas.**

**Answer:**

* inner = intersection
* left = all from left + matches from right
* right = all from right + matches from left
* outer = union

<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q91. How do you check if a column contains only unique values?**

**Answer:**

```python
df["col"].is_unique
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q92. What is Python’s `defaultdict`?**

**Answer:** A dict subclass that provides default values for missing keys.

**Example:**

```python
from collections import defaultdict
d = defaultdict(int)
d["x"] += 1
```

<p align="right"><b><i>Context:</b> Asked at <b>Flipkart (2021)</b>.</i></p>

---

**Q93. How do you check data types and convert them in Pandas?**

**Answer:** `df.dtypes`, `df.astype()`.

<p align="right"><b><i>Context:</b> Asked at <b>IBM (2020)</b>.</i></p>

---

**Q94. Difference between `.ix` and `.at` in Pandas?**

**Answer:** `.ix` is deprecated; `.at` is label-based fast scalar accessor.

<p align="right"><b><i>Context:</b> Asked at <b>PwC (2019)</b>.</i></p>

---

**Q95. How do you create a heatmap in Python?**

**Answer:** Using Seaborn.

```python
import seaborn as sns
sns.heatmap(df.corr(), annot=True)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2022))</b>.</i></p>

---

**Q96. What is vectorization in NumPy?**

**Answer:** Performing operations on entire arrays without explicit loops.

**Example:**

```python
a = np.array([1,2,3])
b = a*2
```

<p align="right"><b><i>Context:</b> Asked at <b>Google (2021))</b>.</i></p>

---

**Q97. How do you handle large CSV files efficiently in Python?**

**Answer:** Use `chunksize` in Pandas, Dask, or PySpark.

**Example:**

```python
for chunk in pd.read_csv("file.csv", chunksize=10000):
    process(chunk)
```

<p align="right"><b><i>Context:</b> Asked at <b>Uber (2023))</b>.</i></p>

---

**Q98. What are Python’s frozen sets?**

**Answer:** Immutable version of sets; elements cannot be modified.

**Example:**

```python
fs = frozenset([1,2,3])
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q99. How do you rank values in Pandas?**

**Answer:** Using `df["col"].rank()`.

<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q100. What is the difference between `.query()` and Boolean indexing in Pandas?**

**Answer:** Both filter rows; `.query()` uses string expressions, Boolean indexing uses logical conditions directly.

**Example:**

```python
df.query("age > 30")
df[df["age"] > 30]
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

