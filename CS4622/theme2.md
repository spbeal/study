# Data Engineering Lecture Notes – Compressed Study Guide

## Lecture 6: NumPy

**Core Concepts:**

* `numpy` arrays are faster and more memory-efficient than Python lists.
* **Array creation:**

```python
import numpy as np
a = np.array([1,2,3])
b = np.zeros((2,3))
c = np.ones((3,3))
d = np.arange(0,10,2)
```

* **Array operations:** element-wise operations, broadcasting, reshaping.
* **Indexing & slicing:** similar to Python lists but supports multi-dimensional arrays.
* **Linear algebra:** `np.dot`, `np.matmul`, `np.linalg.inv`, `np.linalg.det`.
* **Random numbers:** `np.random.rand`, `np.random.randint`, `np.random.seed`.
* **Statistics:** `np.mean`, `np.std`, `np.sum`, `np.min`, `np.max`.

## Lecture 7: Pandas

**Core Concepts:**

* Main structures: **Series** (1D), **DataFrame** (2D).
* **Creation:**

```python
import pandas as pd
df = pd.DataFrame({'A':[1,2], 'B':[3,4]})
s = pd.Series([1,2,3])
```

* **Indexing & selection:** `.loc[]` (label-based), `.iloc[]` (integer-based).
* **Data cleaning:** `.dropna()`, `.fillna()`, `.replace()`.
* **Aggregation:** `.groupby()`, `.agg()`, `.mean()`, `.sum()`.
* **Merging & joining:** `pd.merge(df1, df2, on='key')`, `pd.concat([df1, df2])`.
* **Reading/writing files:** `.read_csv()`, `.to_csv()`, `.read_excel()`, `.to_excel()`.

## Lecture 8: Matplotlib

**Core Concepts:**

* Basic plotting:

```python
import matplotlib.pyplot as plt
plt.plot(x, y)
plt.scatter(x, y)
plt.bar(categories, values)
plt.hist(data, bins=10)
plt.show()
```

* **Labels & titles:** `plt.xlabel()`, `plt.ylabel()`, `plt.title()`.
* **Subplots:** `plt.subplot()`.
* **Customization:** colors, markers, line styles, legends.

## Lecture 9: Seaborn

**Core Concepts:**

* Built on Matplotlib; better for statistical plots.
* **Plot types:**

```python
import seaborn as sns
sns.histplot(data)
sns.boxplot(x='category', y='value', data=df)
sns.scatterplot(x='x', y='y', hue='category', data=df)
sns.heatmap(correlation_matrix, annot=True)
```

* **Themes:** `sns.set_style('whitegrid')`
* **Pair plots:** `sns.pairplot(df, hue='category')`

## Lecture 10: SQL

**Core Concepts:**

* **Database structure:** tables, rows, columns, primary keys.
* **Basic queries:**

```sql
SELECT column1, column2 FROM table;
SELECT * FROM table WHERE condition;
SELECT COUNT(*), AVG(column) FROM table;
```

* **Joins:**

```sql
SELECT * FROM table1
INNER JOIN table2 ON table1.key = table2.key;
LEFT JOIN, RIGHT JOIN
```

* **Aggregations:** `GROUP BY`, `HAVING`, `ORDER BY`.
* **Insert/update/delete:**

```sql
INSERT INTO table (col1, col2) VALUES (val1, val2);
UPDATE table SET col1 = val WHERE condition;
DELETE FROM table WHERE condition;
```

## Lecture 11: Data Exploration & Preprocessing

**Core Concepts:**

* **Exploration:** `.describe()`, `.info()`, `.value_counts()`.
* **Missing values:** `.isnull()`, `.fillna()`, `.dropna()`.
* **Categorical data:** `.astype('category')`, encoding (`pd.get_dummies`).
* **Normalization & scaling:** MinMaxScaler, StandardScaler.
* **Outliers:** Detect via boxplots or z-scores; remove or cap.
* **Feature engineering:** combine, transform, or create new features from existing ones.
