# Pandas & Data Analysis (Databricks / Google Colab)

## Working in Databricks
- Tables are stored in the Workspace (default → Tables).
- Always import libraries first.

```python
# Import data
# Convert to pandas
```

## Displaying a Table
- `display(rs)`
- `print(rs)` — gives a snapshot/summary of the data.
- `rs.head()` — shows the first few rows of the table.
- `rs.tail()` — shows the last few rows of the table.

## Working with Dates
```python
date_column = pd.DatetimeIndex(rs['Date'])
rs['Year'] = date_column.year
rs['Month'] = date_column.month
rs['Day'] = date_column.day
```

## Grouping Data
```python
display(rs)
# Grouping data by month
rs.groupby('Month')['TotalAmounts'].sum()
```

## Introduction to Pandas
Pandas is a library used for:
- Reading data / data processing
- Cleaning data
- Analyzing data

### Google Colab
Google Colab is a cloud-based Jupyter Notebook environment that allows you to:
- Write Python code
- Analyze data
- Create visualizations

### Importing Libraries
```python
import pandas as pd
import numpy as np
```
- **pandas** → for data analysis
- **numpy** → numerical calculations
- **matplotlib** → visualization

### Data Ingestion
```python
data_path = "..."
df = pd.read_csv(data_path)
df.columns    # shows you all the columns in your dataset
```

## Building a DataFrame from a Dictionary
```python
import pandas as pd

dict_data = {
    "Name": ["Alice", "John", "Carol"],
    "Age": [25, 30, 22],
    "City": ["Cape Town", "Joburg", "Durban"]
}

df = pd.DataFrame(dict_data)
print(df)

# Give the top rows of data
df.head(2)
```

## Selecting Columns / Rows
```python
df["Product Category"]

# Creating a list of columns we want to access
access_column = ["Product Category", "Price Per Unit"]
print(df[access_column])
```

## Exploring Data
```python
df.head(2)
df.shape             # shape of data (rows and columns)
df.info()            # grabs the data information
df.describe()        # stats: min, max, etc.

# Sum / total amount in data
print(df["Total Amount"].sum())
print(df["Total Amount"].mean())
```

## Reading a CSV File
```python
df = pd.read_csv("retail_sales.csv")
df.head()
```

## Exploring Categories
```python
df["Product Category"].unique()
df["Gender"].unique()

# Count unique values
df["Product Category"].nunique()

# Frequency count
df["Gender"].value_counts()

# Sorting and ranking
df.sort_values(by="Total Amount", ascending=False)
df.head()
```

## GroupBy Analytics
```python
# Total revenue by category — groupby is used to split data
df.groupby("Product Category")["Total Amount"].sum()

# Average spend by gender
df.groupby("Gender")["Total Amount"].mean()
```

## Feature Engineering
```python
df.head()

# Create discount column
df["Discount"] = df["Total Amount"] * 0.10
df.head()

df["Final Amount"] = df["Total Amount"] - df["Discount"]
df.head()
```
- Related concept: **Upsell / Cross-sell**

## Working with Spark
```python
df = spark.read...
df = df.head(100)
```

### EDA Workflow
- Shape, dtypes, missing values, stats
- Visualization / comparison
- Exercises

## Pivot Table Notes
- Highlight the entire table → Insert Pivot Table.
- Drag "Purchase Date" into Rows.
- Drag "Revenue Per Day" into Values (number of sales).
- Drag "Store Id" into Legend/Columns.
- Month field goes into Filters.
