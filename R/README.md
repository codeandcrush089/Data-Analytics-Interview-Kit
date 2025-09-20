<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/R_logo.svg" alt="R Logo" width="120"/>

# Top 100 R Interview Q&A  
💡 With Real-World Examples + Company Context 

</div>

---

**Q1. What is R and why is it used in Data Science?**

**Answer:** R is an open-source programming language mainly used for statistical analysis, data visualization, and machine learning.

**Example:**

```R
summary(c(1,2,3,4,5))
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q2. What are Vectors in R?**

**Answer:** One-dimensional array that stores elements of the same type.

**Example:**

```R
v <- c(1, 2, 3, 4, 5)
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q3. What is the difference between List and Vector in R?**

**Answer:**

* **Vector:** Homogeneous data.
* **List:** Heterogeneous data.

**Example:**

```R
list(1, "abc", TRUE)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q4. What are Data Frames in R?**

**Answer:** Tabular data structure where columns can have different data types.

**Example:**

```R
df <- data.frame(Name=c("A","B"), Age=c(21,25))
```

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2021)</b>.</i></p>

---

**Q5. What are Factors in R?**

**Answer:** Used to represent categorical data with levels.

**Example:**

```R
factor(c("Male","Female","Male"))
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2021)</b>.</i></p>

---

**Q6. What is the difference between Matrix and Data Frame?**

**Answer:**

* **Matrix:** Homogeneous, numeric data.
* **Data Frame:** Heterogeneous data, like a table.

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q7. How do you import CSV data in R?**

**Answer:** Using `read.csv()` function.

**Example:**

```R
data <- read.csv("file.csv")
```

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2020)</b>.</i></p>

---

**Q8. What are apply(), lapply(), sapply(), and tapply()?**

**Answer:** Family of functions to apply operations over data structures.

* **apply:** Array/matrix.
* **lapply:** List (returns list).
* **sapply:** List (returns vector).
* **tapply:** Grouped data.

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2022)</b>.</i></p>

---

**Q9. How do you handle missing values in R?**

**Answer:** Using `is.na()`, `na.omit()`, or replacing with mean/median.

**Example:**

```R
data[is.na(data)] <- mean(data, na.rm=TRUE)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q10. What are Packages in R?**

**Answer:** Collections of R functions, data, and documentation.

**Example:** `install.packages("ggplot2")`

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q11. What is the difference between R and Python in Data Science?**

**Answer:**

* **R:** Strong in statistics & visualization.
* **Python:** Strong in general-purpose programming & ML libraries.

<p align="right"><b><i>Context:</b> Asked at <b>Flipkart (2022)</b>.</i></p>

---

**Q12. How do you merge/join two data frames in R?**

**Answer:** Using `merge()` function.

**Example:**

```R
merge(df1, df2, by="ID")
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q13. What are dplyr functions in R?**

**Answer:** Functions for data manipulation: `select()`, `filter()`, `mutate()`, `summarise()`, `arrange()`.

**Example:**

```R
library(dplyr)
df %>% filter(Age > 20)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q14. What are ggplot2 features in R?**

**Answer:** Grammar of Graphics-based visualization library.

**Example:**

```R
library(ggplot2)
ggplot(df, aes(x=Age, y=Salary)) + geom_point()
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---

**Q15. What is the difference between melt() and cast() in R?**

**Answer:**

* **melt():** Converts wide data to long format.
* **cast():** Converts long data to wide format.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q16. How do you check the structure of a data frame in R?**

**Answer:** Using `str()` function.

**Example:**

```R
str(df)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q17. What are R Markdown files?**

**Answer:** Documents that combine code, output, and text for reporting.

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2020)</b>.</i></p>

---

**Q18. How do you create functions in R?**

**Answer:** Using `function()` keyword.

**Example:**

```R
add <- function(x,y){ return(x+y) }
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q19. What is R Shiny?**

**Answer:** A framework to build interactive web apps using R.

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q20. What are Time Series functions in R?**

**Answer:** Functions like `ts()`, `acf()`, `pacf()` for forecasting and analysis.

**Example:**

```R
ts(data, start=c(2020,1), frequency=12)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---
**Q21. What is the difference between `seq()` and `rep()` in R?**

**Answer:**

* **seq():** Generates sequences.
* **rep():** Repeats values.

**Example:**

```R
seq(1,10,2)     # 1 3 5 7 9
rep(1:3, times=2) # 1 2 3 1 2 3
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q22. What is the difference between `==` and `%in%` in R?**

**Answer:**

* **==:** Element-wise comparison.
* **%in%:** Checks if elements belong to a vector.

**Example:**

```R
3 == c(2,3,4)   # FALSE TRUE FALSE
3 %in% c(2,3,4) # TRUE
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q23. How do you sort data in R?**

**Answer:** Using `sort()` for vectors, `order()` for data frames.

**Example:**

```R
sort(c(5,2,9,1))
df[order(df$Age), ]
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2022)</b>.</i></p>

---

**Q24. What is the use of `with()` and `by()` in R?**

**Answer:**

* **with():** Simplifies accessing variables in data frames.
* **by():** Applies function on subsets of data.

**Example:**

```R
with(mtcars, mean(mpg))
by(mtcars$mpg, mtcars$cyl, mean)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q25. How do you concatenate strings in R?**

**Answer:** Using `paste()` or `paste0()`.

**Example:**

```R
paste("Hello","World")   # "Hello World"
paste0("Hello","World")  # "HelloWorld"
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q26. What are environments in R?**

**Answer:** Collections of symbol-value pairs, used for variable scoping.

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2021)</b>.</i></p>

---

**Q27. What are R’s data types?**

**Answer:** Numeric, Integer, Character, Logical, Complex, Raw.

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q28. How do you sample random data in R?**

**Answer:** Using `sample()` function.

**Example:**

```R
sample(1:10, 5)
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q29. What are control structures in R?**

**Answer:** Conditional and looping statements like `if`, `for`, `while`, `repeat`.

**Example:**

```R
for(i in 1:3){ print(i) }
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q30. How do you remove duplicates in R?**

**Answer:** Using `unique()` function.

**Example:**

```R
unique(c(1,2,2,3,3,4))
```

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2021)</b>.</i></p>

---

**Q31. What is vector recycling in R?**

**Answer:** When performing operations with unequal-length vectors, shorter vector repeats.

**Example:**

```R
c(1,2,3,4) + c(10,20)   # (1+10, 2+20, 3+10, 4+20)
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2022)</b>.</i></p>

---

**Q32. What is the difference between shallow copy and deep copy in R?**

**Answer:**

* **Shallow Copy:** Points to same memory until modified.
* **Deep Copy:** Creates a completely new object.

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---

**Q33. How do you create a histogram in R?**

**Answer:** Using `hist()` function.

**Example:**

```R
hist(mtcars$mpg)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q34. What is the use of `aggregate()` in R?**

**Answer:** Splits data into subsets, applies function, and returns results.

**Example:**

```R
aggregate(mpg ~ cyl, data=mtcars, mean)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q35. What are outliers and how do you detect them in R?**

**Answer:** Extreme values differing from rest of data. Detect using boxplot or IQR method.

**Example:**

```R
boxplot(mtcars$mpg)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2022)</b>.</i></p>

---

**Q36. What is R’s workspace and how do you save it?**

**Answer:** Workspace stores all user-defined objects. Save using `save.image()`.

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q37. How do you check data types in R?**

**Answer:** Using `class()`, `typeof()`, `is.numeric()`, etc.

**Example:**

```R
class(5)     # "numeric"
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q38. What is the difference between correlation and covariance in R?**

**Answer:**

* **Covariance:** Measure of joint variability.
* **Correlation:** Normalized covariance between -1 and 1.

**Example:**

```R
cor(mtcars$mpg, mtcars$hp)
cov(mtcars$mpg, mtcars$hp)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q39. How do you create bar plots in R?**

**Answer:** Using `barplot()` function.

**Example:**

```R
counts <- table(mtcars$cyl)
barplot(counts)
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020)</b>.</i></p>

---

**Q40. What is the difference between `install.packages()` and `library()` in R?**

**Answer:**

* **install.packages():** Downloads and installs packages.
* **library():** Loads the package into memory for use.

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2022)</b>.</i></p>

---

**Q41. What is the difference between `data()` and `datasets` package in R?**

**Answer:**

* `data()` loads built-in datasets.
* `datasets` is the package that contains these datasets.

**Example:**

```R
data(mtcars)
head(mtcars)
```

**Context:** Asked at **TCS (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q42. How do you merge data frames in R?**

**Answer:** Using `merge()` function (like SQL join).

**Example:**

```R
merge(df1, df2, by="ID", all=TRUE)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2022)</b>.</i></p>

---

**Q43. What is the difference between `apply()`, `lapply()`, and `sapply()`?**

**Answer:**

* **apply():** Works on arrays/matrices.
* **lapply():** Returns list.
* **sapply():** Simplifies result (vector/matrix).

**Example:**

```R
apply(matrix(1:6, nrow=2), 1, sum)
lapply(1:3, sqrt)
sapply(1:3, sqrt)
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q44. How do you handle NA values in R?**

**Answer:**

* Remove: `na.omit()`
* Replace: `is.na()` with value

**Example:**

```R
x <- c(1, NA, 3)
mean(x, na.rm=TRUE)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q45. What is the difference between `factor` and `character` in R?**

**Answer:**

* **factor:** Stores categorical data with levels.
* **character:** Stores plain string values.

**Example:**

```R
factor(c("Male","Female","Male"))
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q46. What is the difference between `matrix` and `data.frame`?**

**Answer:**

* **matrix:** Homogeneous data type.
* **data.frame:** Heterogeneous data types.

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q47. What is the difference between supervised and unsupervised learning in R?**

**Answer:**

* **Supervised:** Training with labels (`lm()`, `glm()`).
* **Unsupervised:** No labels (`kmeans()`).

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2022)</b>.</i></p>

---

**Q48. How do you perform linear regression in R?**

**Answer:** Using `lm()` function.

**Example:**

```R
model <- lm(mpg ~ hp + wt, data=mtcars)
summary(model)
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2021)</b>.</i></p>

---

**Q49. How do you perform logistic regression in R?**

**Answer:** Using `glm()` with `family=binomial`.

**Example:**

```R
model <- glm(vs ~ mpg + hp, data=mtcars, family=binomial)
summary(model)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2020)</b>.</i></p>

---

**Q50. What is the difference between `ggplot2` and `plot()`?**

**Answer:**

* **plot():** Base R graphics.
* **ggplot2:** Advanced, layered visualization system.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2022)</b>.</i></p>

---

**Q51. How do you check missing values count in R?**

**Answer:** Using `sum(is.na(data))`.

**Example:**

```R
sum(is.na(mtcars))
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020))</b>.</i></p>

---

**Q52. What is the difference between AIC and BIC in model selection?**

**Answer:**

* **AIC (Akaike):** Focuses on predictive accuracy.
* **BIC (Bayesian):** More penalty for complexity.

**Context:** Asked at **EY (2021)**.<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q53. What is cross-validation in R?**

**Answer:** Technique to evaluate model performance by splitting data into folds. Implemented with `caret` or `cv.glm()`.

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q54. How do you standardize or normalize data in R?**

**Answer:**

* Standardize: `(x - mean(x)) / sd(x)`
* Normalize: `(x - min(x)) / (max(x) - min(x))`

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2021)</b>.</i></p>

---

**Q55. What is the use of `reshape2` package in R?**

**Answer:** Used for reshaping data with `melt()` and `dcast()`.

**Example:**

```R
library(reshape2)
melt(mtcars, id.vars="cyl")
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q56. What is the difference between `inner_join` and `left_join` in R (dplyr)?**

**Answer:**

* **inner\_join:** Only matching rows.
* **left\_join:** All rows from left + matching from right.

**Example:**

```R
dplyr::left_join(df1, df2, by="ID")
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q57. How do you perform k-means clustering in R?**

**Answer:** Using `kmeans()` function.

**Example:**

```R
set.seed(123)
kmeans(mtcars[,c("mpg","hp")], centers=3)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q58. What is the difference between `summary()` and `str()` in R?**

**Answer:**

* **summary():** Statistical summary.
* **str():** Structure of object.

**Example:**

```R
summary(mtcars)
str(mtcars)
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020))</b>.</i></p>

---

**Q59. How do you export data from R to CSV?**

**Answer:** Using `write.csv()`.

**Example:**

```R
write.csv(mtcars, "mtcars.csv", row.names=FALSE)
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q60. How do you read Excel files in R?**

**Answer:** Using `readxl` or `openxlsx` package.

**Example:**

```R
library(readxl)
df <- read_excel("file.xlsx")
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q61. What is the difference between `head()` and `tail()` in R?**

**Answer:**

* `head()`: Shows first rows.
* `tail()`: Shows last rows.

**Example:**

```R
head(mtcars, 3)
tail(mtcars, 3)
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q62. How do you rename columns in R?**

**Answer:** Using `colnames()` or `dplyr::rename()`.

**Example:**

```R
colnames(mtcars)[1] <- "MilesPerGallon"
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2022)</b>.</i></p>

---

**Q63. How do you create dummy variables in R?**

**Answer:** Using `model.matrix()` or `fastDummies` package.

**Example:**

```R
model.matrix(~ cyl, data=mtcars)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q64. What is the difference between `which()` and `match()`?**

**Answer:**

* `which()`: Returns index of TRUE condition.
* `match()`: Returns first matching position.

**Example:**

```R
which(c(2,4,6)==4)   # 2
match(4, c(2,4,6))   # 2
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q65. How do you calculate correlation matrix in R?**

**Answer:** Using `cor()` function.

**Example:**

```R
cor(mtcars[,c("mpg","hp","wt")])
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q66. What is PCA in R and how is it performed?**

**Answer:** PCA = Principal Component Analysis for dimensionality reduction, done with `prcomp()`.

**Example:**

```R
pca <- prcomp(mtcars[,c("mpg","hp","wt")], scale.=TRUE)
summary(pca)
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q67. What is the difference between `prop.table()` and `table()`?**

**Answer:**

* `table()`: Frequency count.
* `prop.table()`: Proportion of counts.

**Example:**

```R
table(mtcars$cyl)
prop.table(table(mtcars$cyl))
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2020))</b>.</i></p>

---

**Q68. How do you bind rows and columns in R?**

**Answer:**

* Rows: `rbind()`
* Columns: `cbind()`

**Example:**

```R
rbind(c(1,2), c(3,4))
cbind(c(1,2), c(3,4))
```

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2021)</b>.</i></p>

---

**Q69. How do you check normality of data in R?**

**Answer:** Using `shapiro.test()` or QQ plots.

**Example:**

```R
shapiro.test(mtcars$mpg)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q70. What is the difference between one-hot encoding and label encoding in R?**

**Answer:**

* One-hot: Creates separate binary columns.
* Label: Assigns numeric code to each category.

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q71. How do you perform hypothesis testing in R?**

**Answer:** Using t-test, chi-square, ANOVA functions.

**Example:**

```R
t.test(mpg ~ am, data=mtcars)
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q72. What is the difference between `cat()` and `print()` in R?**

**Answer:**

* `print()`: Adds quotes/newlines.
* `cat()`: Concatenates and prints without quotes.

**Example:**

```R
print("Hello")
cat("Hello")
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2020)</b>.</i></p>

---

**Q73. How do you split data into training and testing sets in R?**

**Answer:** Using `sample()` or `caret::createDataPartition()`.

**Example:**

```R
set.seed(123)
trainIndex <- sample(1:nrow(mtcars), 0.7*nrow(mtcars))
train <- mtcars[trainIndex, ]
test <- mtcars[-trainIndex, ]
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2021)</b>.</i></p>

---

**Q74. What is the difference between `summary()` and `describe()` in R?**
**Answer:**

* `summary()`: Base R function.
* `describe()`: From `Hmisc/psych` package with more detailed stats.

<p align="right"><b><i>Context:</b> Asked at <b>EY (2020)</b>.</i></p>

---

**Q75. How do you calculate quantiles in R?**

**Answer:** Using `quantile()` function.

**Example:**

```R
quantile(mtcars$mpg, probs=c(0.25,0.5,0.75))
```

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q76. What is the difference between `any()` and `all()` in R?**

**Answer:**

* `any()`: Returns TRUE if at least one element is TRUE.
* `all()`: Returns TRUE only if all elements are TRUE.

**Example:**

```R
any(c(TRUE,FALSE))   # TRUE
all(c(TRUE,FALSE))   # FALSE
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2020)</b>.</i></p>

---

**Q77. How do you visualize correlation heatmap in R?**

**Answer:** Using `corrplot` or `ggcorrplot`.

**Example:**

```R
library(corrplot)
corrplot(cor(mtcars))
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q78. What is the difference between long and wide format data in R?**

**Answer:**

* **Long:** Each row is one observation.
* **Wide:** One subject spread across columns.

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q79. How do you impute missing values in R?**

**Answer:** Using mean, median, mode, or packages like `mice`.

**Example:**

```R
x[is.na(x)] <- mean(x, na.rm=TRUE)
```

<p align="right"><b><i>Context:</b> Asked at <b>Wipro (2021)</b>.</i></p>

---

**Q80. How do you create boxplots for multiple groups in R?**

**Answer:** Using `boxplot()` or `ggplot2`.

**Example:**

```R
boxplot(mpg ~ cyl, data=mtcars)
```

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q81. What is the difference between supervised and unsupervised packages in R (caret vs cluster)?**

**Answer:**

* **caret:** Focused on supervised ML (classification/regression).
* **cluster:** Focused on unsupervised ML (clustering).

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q82. How do you calculate variance inflation factor (VIF) in R?**

**Answer:** Using `car` package.

**Example:**

```R
library(car)
model <- lm(mpg ~ wt + hp + disp, data=mtcars)
vif(model)
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q83. What is the difference between `set.seed()` and random sampling in R?**

**Answer:**

* `set.seed()`: Ensures reproducibility.
* Random sampling: Produces different results without seed.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q84. How do you calculate confusion matrix in R?**

**Answer:** Using `caret::confusionMatrix()`.

**Example:**

```R
library(caret)
pred <- factor(c("yes","no","yes"), levels=c("yes","no"))
obs  <- factor(c("yes","yes","no"), levels=c("yes","no"))
confusionMatrix(pred, obs)
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2021)</b>.</i></p>

---

**Q85. What is the difference between parametric and non-parametric tests in R?**

**Answer:**

* **Parametric:** Assumes distribution (t-test, ANOVA).
* **Non-parametric:** No distribution assumption (Wilcoxon, Kruskal-Wallis).

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q86. How do you calculate ROC curve in R?**

**Answer:** Using `pROC` or `ROCR` package.

**Example:**

```R
library(pROC)
roc(response, predictor)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2022)</b>.</i></p>

---

**Q87. How do you check multicollinearity in R?**

**Answer:** Using **VIF** from `car` package.

<p align="right"><b><i>Context:</b> Asked at <b>EY (2021)</b>.</i></p>

---

**Q88. What is time series analysis in R?**

**Answer:** Process of analyzing sequential data using `ts` object and forecasting with `forecast` package.

**Example:**

```R
tsdata <- ts(AirPassengers, frequency=12)
plot(tsdata)
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2022)</b>.</i></p>

---

**Q89. How do you perform ARIMA modeling in R?**

**Answer:** Using `forecast::auto.arima()`.

**Example:**

```R
library(forecast)
fit <- auto.arima(AirPassengers)
forecast(fit, 12)
```

<p align="right"><b><i>Context:</b> Asked at <b>Cognizant (2021)</b>.</i></p>

---

**Q90. What is the difference between `by()` and `aggregate()`?**

**Answer:**

* `by()`: Applies function on subsets.
* `aggregate()`: Summarizes data by groups.

**Example:**

```R
aggregate(mpg ~ cyl, data=mtcars, mean)
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2020)</b>.</i></p>

---

**Q91. How do you perform Chi-square test in R?**

**Answer:** Using `chisq.test()`.

**Example:**

```R
chisq.test(table(mtcars$cyl, mtcars$am))
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q92. How do you save and load R objects?**

**Answer:**

* Save: `saveRDS()`
* Load: `readRDS()`

**Example:**

```R
saveRDS(mtcars, "mtcars.rds")
readRDS("mtcars.rds")
```

<p align="right"><b><i>Context:</b> Asked at <b>TCS (2021)</b>.</i></p>

---

**Q93. What is the difference between `attach()` and `with()`?**

**Answer:**

* `attach()`: Makes variables directly accessible but risky.
* `with()`: Temporary evaluation without modifying workspace.

<p align="right"><b><i>Context:</b> Asked at <b>Accenture (2020)</b>.</i></p>

---

**Q94. How do you handle categorical variables in regression in R?**

**Answer:** By converting to factors, R automatically creates dummy variables.

<p align="right"><b><i>Context:</b> Asked at <b>Deloitte (2021)</b>.</i></p>

---

**Q95. How do you detect outliers in R?**

**Answer:** Using boxplots, z-scores, or `car::outlierTest()`.

**Example:**

```R
boxplot(mtcars$mpg)
```

<p align="right"><b><i>Context:</b> Asked at <b>Capgemini (2021)</b>.</i></p>

---

**Q96. How do you do text mining in R?**

**Answer:** Using `tm` and `wordcloud` packages.

**Example:**

```R
library(tm)
corpus <- Corpus(VectorSource(c("R is great","Data science with R")))
```

<p align="right"><b><i>Context:</b> Asked at <b>Infosys (2022)</b>.</i></p>

---

**Q97. How do you perform sentiment analysis in R?**

**Answer:** Using `syuzhet` or `tidytext`.

**Example:**

```R
library(syuzhet)
get_sentiment("R is amazing!")
```

<p align="right"><b><i>Context:</b> Asked at <b>EY (2022)</b>.</i></p>

---

**Q98. What is the difference between Bagging and Boosting in R?**

**Answer:**

* **Bagging:** Reduces variance (Random Forest).
* **Boosting:** Reduces bias (XGBoost, AdaBoost).

<p align="right"><b><i>Context:</b> Asked at <b>Amazon (2021)</b>.</i></p>

---

**Q99. How do you parallelize operations in R?**

**Answer:** Using `parallel` or `foreach` package.

**Example:**

```R
library(parallel)
mclapply(1:5, sqrt, mc.cores=2)
```

<p align="right"><b><i>Context:</b> Asked at <b>Microsoft (2022)</b>.</i></p>

---

**Q100. What are the latest trends in R for data science?**
**Answer:**

* Integration with **Python & Spark**
* **Shiny apps** for dashboards
* **Tidymodels** for ML workflows
* **Arrow** for big data handling
* Growing **AI/ML + NLP support**

<p align="right"><b><i>Context:</b> Asked at <b>Google (2023)</b>.</i></p>

