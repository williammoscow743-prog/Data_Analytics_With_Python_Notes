# Data Visualization

## Data Visualization Bootcamp — Core Idea
- Data = information.
- You need to be able to tell a story from your data.
- You need to derive/extract actionable insights from your data to drive business decisions.

**Flow:** Employees create big data → Data Analyst analyzes it → tells a story / conveys insight → CEO/decision-maker uses it to make decisions.

**Data process:** raw data tables → data warehouse (structured, cleaned tables).

## Business Requirements & Data-Driven Questions

1. **BRS (Business Requirements) — "The Ask"**
   Example: CEO — "I want to understand the revenue for our coffee shop for different products."
2. **Analyst:** before you answer the ask, ask data-driven questions to understand what is really needed.
   - "Would you like to see the daily revenue?"
   - "Would you like to see the repeat customers, to analyze the frequency?"
   - "Do you want to see the revenue with VAT included or excluded?"
3. **Data Processing** (code)
4. **Data Analysis** → insight generation
5. **Data Visualization** → creating graphs
6. **Data Presentation** → putting things together

## Data Management System (DMS)
- An interface that allows us to interact with our data.

## The Data Design Blueprint — Choosing the Right Chart

### Bar Graph / Chart
- **When to use:** comparing categories. Use a legend when there is a split (e.g. Female vs Male).
- X-axis: categorical data. Y-axis: metric.

### Line Chart
- **When to use:** showing trends over time (continuous trends).
- X-axis: date/time (month, year, date). Y-axis: metric.

### Key Definitions
- **Metric:** refers to something that we are measuring — e.g. revenue, number of sales/transactions, number of customers. Metrics are numerical/quantitative data, typically on the y-axis.
- **Categorical data:** data that puts our information into groups (mainly words) — e.g. product category, day of week.

## Showing Proportions / Proportion of a Whole
- Pie charts and donut charts show a **categorical breakdown** — metric to proportion.

**Example — Revenue breakdown by category (donut chart):**
- Electronics: 60%
- Clothing: 20%
- Beauty: 20%

**Example — Stacked bar chart by day, showing category proportions:**

| Day | Clothing | Beauty | Electronics |
|---|---|---|---|
| Mon | ... | ... | ... |
| Tue | ... | ... | ... |
| Wed | 10% | 20% | 70% |

Used for showing proportions for two different categorical data points by a specific metric.

**Example category fields:**
- Product Category → Clothing, Beauty, Electronics
- Day of Week Category → Mon, Tue, Wed
