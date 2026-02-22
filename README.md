# TO-STUDY-HOW-TO-LOAD-AND-CREATE-DATASET-IN-PYTHON

Here is your complete **README.md** content for:

---

#  EXPERIMENT NO: 10

# TITLE: Create Dataset and Load Dataset

**Name:** Amey Waghmare
**PRN:** 25070123009
**Batch:** A1

---

#  AIM

To create a dataset using Pandas, save it in CSV and Excel formats, perform data manipulation and statistical operations, and load an external dataset for analysis.

---

#  THEORY (Very Detailed)

##  Introduction

In Data Science and Data Analysis, datasets are the foundation of all operations. A dataset is a structured collection of data stored in tabular form (rows and columns).

To work efficiently with datasets in Python, we use:

* pandas for structured data handling
* Google Colab for executing Python programs online

---

#  Creating a Dataset

A dataset can be created manually using a dictionary and converting it into a DataFrame.

Example:

```python
import pandas as pd

data = {
    "Roll_no": [1, 2, 3, 4, 5],
    "Gender": ["male", "female", "male", "female", "male"],
    "Department": ["ENTC", "CS", "IT", "AI ML", "ELECTRICAL"],
    "CGPA": [8.5, 9.2, 7.8, 9.5, 8.9]
}

df = pd.DataFrame(data)
```

Here:

* Each key represents a column.
* Each list represents column values.
* The DataFrame organizes the data in tabular form.

---

#  Saving Dataset

Datasets can be saved in different formats:

###  Save as CSV File

```python
df.to_csv("student_data.csv", index=False)
```

### Save as Excel File

```python
df.to_excel("student_data.xlsx", index=False)
```

Saving datasets allows:

* Sharing data
* Reusing data later
* Importing data into other tools

---

# 🔹 Understanding Dataset Structure

### 1️ Shape

```python
df.shape
```

Returns (rows, columns).

### 2️ Data Types

```python
df.dtypes
```

Shows datatype of each column.

Example:

* Roll_no → int64
* CGPA → float64
* Department → object

---

#  Accessing Data

###  Access a Column

```python
df["Department"]
```

###  Access Specific Row

```python
df[df["Roll_no"] == 3]
```

---

#  Statistical Operations

Statistical functions help summarize data.

### Mean

```python
df["CGPA"].mean()
```

### Median

```python
df["CGPA"].median()
```

### Mode

```python
df["CGPA"].mode()[0]
```

These operations are useful in:

* Academic analysis
* Performance evaluation
* Data summarization

---

#  Modifying Dataset

### Add New Column

```python
df["Grade"] = ["A", "A+", "B", "A+", "A"]
```

### Delete Column

```python
df = df.drop("Gender", axis=1)
```

### Find Topper CGPA

```python
topper_cgpa = df.loc[df["CGPA"].idxmax(), "CGPA"]
```

### CGPA of Specific Roll Number

```python
roll_no_2_cgpa = df.loc[df["Roll_no"] == 2, "CGPA"].values
```

---

#  Loading External Dataset

An external dataset can be loaded using:

```python
df = pd.read_csv('/content/Cars93.csv')
```

The Cars dataset contains:

* Manufacturer
* Model
* Type
* Price
* MPG.city
* AirBags
* Horsepower
* Passengers
* Rear seat room
* Luggage room

### View First 5 Rows

```python
df.head()
```

### View Last 5 Rows

```python
df.tail()
```

---

#  Importance of Loading Dataset

Loading datasets is essential for:

* Real-world data analysis
* Data cleaning
* Feature engineering
* Machine learning model training

---

#  SYNTAX

## Import Pandas

```python
import pandas as pd
```

## Create DataFrame

```python
pd.DataFrame(dictionary)
```

## Save Dataset

```python
df.to_csv("filename.csv", index=False)
df.to_excel("filename.xlsx", index=False)
```

## Load Dataset

```python
pd.read_csv("file_path")
pd.read_excel("file_path")
```

## Access Data

```python
df["column_name"]
df.loc[row_index]
```

## Statistical Functions

```python
df["column"].mean()
df["column"].median()
df["column"].mode()
```

## Drop Column

```python
df.drop("column_name", axis=1)
```



# CONCLUSION

In this experiment, a dataset was successfully created, saved, modified, and analyzed using Pandas.

We learned:

* How to create structured datasets
* How to save and load CSV and Excel files
* How to perform statistical operations
* How to access and modify dataset values
* How to work with real-world datasets

This experiment provided practical understanding of dataset handling, which is a fundamental skill in Data Science and Data Analysis.




