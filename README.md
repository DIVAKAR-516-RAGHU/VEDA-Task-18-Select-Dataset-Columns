# VEDA Task 18 – Selecting Dataset Columns and Rows Using Pandas

## 📌 Project Overview

This task demonstrates how to select and access specific rows and columns from a dataset using **Pandas**.

The **Iris dataset** is used to understand the practical difference between:

* `loc[]` – Label-based indexing
* `iloc[]` – Integer-position-based indexing

The task covers selecting single columns, multiple columns, specific rows and columns, and comparing `loc` with `iloc`.

---

## 🎯 Objectives

The main objectives of this task are:

* Load a dataset using Pandas.
* Understand the structure of a DataFrame.
* Select a single column using `loc`.
* Select multiple columns using `loc`.
* Select specific rows and columns using `loc`.
* Select a single column using `iloc`.
* Select multiple columns using `iloc`.
* Select specific rows and columns using `iloc`.
* Understand the difference between `loc` and `iloc`.
* Display selected records from the dataset.

---

## 🛠️ Technologies Used

| Technology       | Purpose                        |
| ---------------- | ------------------------------ |
| Python           | Programming language           |
| Pandas           | Data manipulation and analysis |
| Jupyter Notebook | Development environment        |
| Iris Dataset     | Dataset used for analysis      |

---

## 📂 Dataset

The **Iris dataset** is a commonly used dataset for demonstrating data analysis and machine learning concepts.

It contains measurements of iris flowers belonging to different species.

### Main Features

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width
* Species

The dataset contains **150 records** and **5 columns**.

---

## 📥 Import Pandas

```python
import pandas as pd
```

Pandas is imported to perform DataFrame creation, indexing, selection, and analysis operations.

---

## 📊 Loading the Dataset

The Iris dataset is loaded into a Pandas DataFrame.

```python
df = pd.read_csv("iris.csv")
```

The DataFrame is then used for all row and column selection operations.

---

## 🔍 Exploring the Dataset

### Display Dataset Shape

```python
df.shape
```

This returns the number of rows and columns in the dataset.

### Display Column Names

```python
df.columns
```

This displays the column names available in the DataFrame.

---

# 📌 Selecting Data Using `loc`

`loc[]` is used for **label-based indexing**.

It allows rows and columns to be selected using their labels.

---

## 1. Selecting a Single Column Using `loc`

```python
df.loc[:, "sepal_length"]
```

This selects the `sepal_length` column from all rows.

---

## 2. Selecting Multiple Columns Using `loc`

```python
df.loc[:, ["sepal_length", "sepal_width"]]
```

This selects multiple columns using their column labels.

---

## 3. Selecting Rows and Columns Using `loc`

```python
df.loc[0:4, ["sepal_length", "sepal_width"]]
```

This selects rows from index `0` to `4` and the specified columns.

**Important:** With `loc`, the ending label is generally included when using label-based slices.

---

# 📌 Selecting Data Using `iloc`

`iloc[]` is used for **integer-position-based indexing**.

It selects rows and columns based on their numerical positions.

---

## 4. Selecting a Single Column Using `iloc`

```python
df.iloc[:, 0]
```

This selects the first column of the DataFrame.

---

## 5. Selecting Multiple Columns Using `iloc`

```python
df.iloc[:, [0, 1]]
```

This selects the first and second columns based on their integer positions.

---

## 6. Selecting Rows and Columns Using `iloc`

```python
df.iloc[0:5, 0:2]
```

This selects the first five rows and the first two columns.

**Important:** With `iloc`, the ending position is excluded, similar to normal Python slicing.

---

# 📋 `loc` vs `iloc`

| Feature             | `loc`               | `iloc`                 |
| ------------------- | ------------------- | ---------------------- |
| Indexing type       | Label-based         | Integer-position-based |
| Rows selected by    | Labels              | Positions              |
| Columns selected by | Column names/labels | Column positions       |
| Example             | `df.loc[0:4]`       | `df.iloc[0:5]`         |
| End of slice        | Usually included    | Excluded               |
| Best used when      | Labels are known    | Positions are known    |

---

## 🔎 Key Difference

### `loc`

```python
df.loc[0:4]
```

Selects rows with labels **0, 1, 2, 3, and 4**.

### `iloc`

```python
df.iloc[0:5]
```

Selects rows at positions **0, 1, 2, 3, and 4**.

Although these examples produce the same rows when the DataFrame has the default integer index, the indexing methods are fundamentally different.

---

# 📌 Final Selected Records

The task also demonstrates selecting specific records using both indexing methods.

Example using `loc`:

```python
df.loc[0:4, ["sepal_length", "petal_length"]]
```

Example using `iloc`:

```python
df.iloc[0:5, [0, 2]]
```

These operations allow specific portions of a DataFrame to be extracted efficiently.

---

# 💡 What I Learned

Through this task, I learned:

1. How to load and work with a dataset using Pandas.
2. How to inspect DataFrame shape and columns.
3. How to select individual columns.
4. How to select multiple columns.
5. How to select specific rows and columns.
6. The difference between label-based and position-based indexing.
7. How `loc` and `iloc` behave differently during slicing.
8. How Pandas makes structured data selection simple and efficient.

---

# ✅ Conclusion

This task provided practical experience with **Pandas DataFrame indexing and selection**.

The `loc[]` method is useful when working with **row and column labels**, while `iloc[]` is useful when selecting data based on **integer positions**.

Understanding both methods is important for efficient data manipulation and analysis using Pandas.

---

## 📁 Project Structure

```text
VEDA-Task-18-Select-Dataset-Columns/
│
├── VEDA_Task_18_Select_Dataset_Columns.ipynb
├── README.md
└── iris.csv
```

> If the `iris.csv` file is not included in your repository because the notebook loads it directly from an online source, remove `iris.csv` from the project structure above.

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/DIVAKAR-516-RAGHU/VEDA-Task-18-Select-Dataset-Columns.git
```

### 2. Open the Repository

```bash
cd VEDA-Task-18-Select-Dataset-Columns
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open

```text
VEDA_Task_18_Select_Dataset_Columns.ipynb
```

Run the notebook cells sequentially to reproduce the results.

---

## 👨‍💻 Author

**Divakar R**

B.E. Electronics and Communication Engineering
Adithya Institute of Technology, Coimbatore

---

## 📚 Internship

**VEDA AI/ML Internship**

**Task:** 18 – Selecting Dataset Columns and Rows Using Pandas

---

## ⭐ Skills Practiced

`Python` `Pandas` `DataFrames` `Data Selection` `loc` `iloc` `Data Analysis` `Jupyter Notebook`
