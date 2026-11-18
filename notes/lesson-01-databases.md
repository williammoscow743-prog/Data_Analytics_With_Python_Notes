# Data & Databases Fundamentals

## What is Data?
- **Data (information):** a collection of facts.
- We use data to make decisions, and we need data to make good decisions.

### Types of Data

| Structured Data | Unstructured Data |
|---|---|
| Data stored in a table with rows and columns | Social media posts, PDF documents, music and videos |
| Consistent format | Does **not** have a consistent format |
| Stored in spreadsheets | Not recommended for use directly in business analysis |

## Relational Database (RDB)
- A storage place for structured data.
- A database is where we store the data.
- Structured data that can be related/joined together to become a relational database.
- In a relational database, we store structured data that can be connected to one another using a **primary key** and **foreign key** (linking dimension tables and fact tables).

### Example: Shop Database

**Customers Table**

| Cust_Id | Name | Age | City |
|---|---|---|---|
| 1 | Moscow | 25 | NY |
| 2 | Rofhiwa | 28 | LA |
| 3 | William | 18 | MP |

**Transactions (Fact) Table**

| Order_Id | Cust_Id | Prod_Id | Rev |
|---|---|---|---|
| 324 | 2 | 104 | 70 |
| 333 | 1 | 102 | 60 |
| 401 | 3 | 101 | 100 |

**Products (Dimension) Table**

| Product_Id | Product_Category | Product_Name |
|---|---|---|
| 101 | Fruits | Banana |
| 102 | Fruits | Apples |
| 103 | Electronics | Laptop |
| 104 | Clothing | Jeans |

### Keys
- **Primary Key:** a column that uniquely identifies each row in a table (a unique identifier that differentiates each record from the rest of the table, e.g. an ID number).
- **Foreign Key:** a column that links one table to another — it is a primary key found in another table but also exists in this table.

## Database Management System (DBMS)
- A system we use to access the database.
- Serves as an intermediary between users and the physical database.
- Allows users to interact with the database.
- Also used for the creation, organization, management, and manipulation of the database.

## Data Warehouse (DW)
- A central place/central data store where we store multiple databases.
- It houses multiple databases.

### ETL (Extract, Transform, Load)
- The data pipeline used to retrieve data / data collection process, moving data from source databases (DB1, DB2, DB3 — OLTP) into the data warehouse (OLAP).

### OLTP — Online Transactional Processing (database)
- Used during operating/business hours.
- Follows **CRUD**: Create, Retrieve, Update, Delete.
- Allows basic data processing operations (data capturing).

### OLAP — Online Analytical Processing
- Used to perform analytical work on data stored in the data warehouse.
- Allows complex SQL / complex data processing.

## Schema, Tables, and Data Marts
- Within a data warehouse there is a **database**, and within the database there is a **schema**.
- A **schema** is how we separate things/tables — like a folder used to separate different types of tables.
- Within a schema there are **tables**.

### Two Main Table Types
- **Dimension Table (Dim Table):** stores descriptive information. Does not change consistently.
- **Fact Table:** stores transactional/quantitative information. Contains numbers, has foreign keys, used for analysis.

### Research terms (for further reading)
1. What is a Data Lake
2. Data Mart
3. Foreign Key
4. Primary Key
5. Database
6. Data Warehouse
7. Schema
8. Prompt Engineering
9. AI
10. Snowflake
11. Microsoft SQL Server
12. Databricks

## Why We Code (Purpose of DBMS/SQL)
- For data inspection: to see what data is available.
- Data / Exploratory Analysis: to understand the relationship between our data points.
- To retrieve and manipulate the data.
- To amend, update, and delete data.
- To clean, join, and aggregate data — with the goal of extracting actionable insights.
- **Feature Building:** creating features used in data for predictions.

### When creating a Power BI dashboard, you need:
- A summarized table
- An aggregated table
- A combined table
- A unified table
- An insight table

Guiding questions: *What story do you want to tell? What do you want to show? What ideas do you want to convey?*
