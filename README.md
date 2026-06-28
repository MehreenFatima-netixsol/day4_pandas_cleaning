# Titanic Data Cleaning and Transformation with Pandas

## Project Overview

This project demonstrates essential **data cleaning**, **transformation**, and **reshaping** techniques using the Pandas library in Python. Working with the Titanic dataset, the notebook follows a structured data preprocessing workflow to prepare raw data for further analysis and machine learning.

The project emphasizes best practices in handling missing values, correcting data types, removing duplicates, engineering new features, summarizing data, and combining datasets using merge operations.

---

## Dataset

**Dataset:** Titanic Passenger Dataset

The dataset contains demographic and travel information for passengers aboard the RMS Titanic, including:

* Passenger ID
* Survival status
* Passenger class
* Name
* Gender
* Age
* Fare
* Cabin
* Port of embarkation
* Family information

**Source:**
https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

---

## Project Objectives

The primary objectives of this project are to:

* Inspect and clean raw data
* Handle missing values with appropriate strategies
* Verify and correct data types
* Remove duplicate records
* Create new meaningful features
* Summarize data using pivot tables
* Merge datasets to enrich information
* Document each preprocessing step with clear explanations

---

## Technologies Used

* Python 3
* Pandas
* Jupyter Notebook / Google Colab

---

## Tasks Performed

### 1. Data Inspection

* Loaded the Titanic dataset
* Examined dataset structure
* Reviewed column data types
* Identified missing values

---

### 2. Missing Value Handling

The following strategies were applied:

* **Cabin** column was removed because it contained a large number of missing values.
* Missing values in **Age** were replaced with the **median** to reduce the effect of outliers.
* Missing values in **Embarked** were filled using the **mode** (most frequent value).

---

### 3. Data Type Validation

All columns were inspected to ensure they had appropriate data types for analysis.

If required, numerical columns can be converted using:

```python
df["Fare"] = pd.to_numeric(df["Fare"])
```

---

### 4. Duplicate Removal

Duplicate rows were identified and removed to improve data quality and prevent biased analysis.

---

### 5. Feature Engineering

Two new derived columns were created:

#### Age Group

Passengers were categorized into:

* Child
* Adult
* Senior

using the `.apply()` function.

#### Fare With Tax

A new fare column was created by adding a 10% service tax using vectorized operations.

---

### 6. Data Reshaping

A pivot table was generated to summarize the **average fare** paid by passengers based on:

* Passenger Class
* Gender

This provides a concise overview of fare distribution across different groups.

---

### 7. Data Merging

A manually created lookup table was merged with the original dataset to map passenger class numbers to descriptive class names:

| Pclass | Class Name   |
| ------ | ------------ |
| 1      | First Class  |
| 2      | Second Class |
| 3      | Third Class  |

The merge operation was performed using a **left join**.

---

## Pandas Concepts Demonstrated

This project covers the following Pandas operations:

* Data Loading
* Data Inspection
* `.drop()`
* `.dropna()`
* `.fillna()`
* `.astype()`
* `pd.to_numeric()`
* `.duplicated()`
* `.drop_duplicates()`
* `.apply()`
* Vectorized Operations
* `.pivot_table()`
* `.groupby()`
* `.merge()`
* Boolean Indexing

## Author

**Mehreen Fatima**
