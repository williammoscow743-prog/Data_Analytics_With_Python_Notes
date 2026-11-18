# Machine Learning & AI

## Recap: Prompting Concepts
- Prompt Engineering
- Zero-shot prompting
- Few-shot prompting
- Contextual prompting → context is background data.

## Overview
The focus is on understanding AI tools, training, prompt strategies, and methods to optimize AI responses for various applications.

## Machine Learning Process
- **Algorithm:** the outcome of a machine learning process is an AI tool/system.
- In order to build a machine learning model, we need data (data-dependent).
- The role of the **Data Engineer** is to make the data available in the data warehouse (building pipelines to store data: App → ETL → Storage → ETL → Data Warehouse; Web sources also feed in).

### Steps in the ML Process

1. **Data Collection**
2. **Stakeholder — Define the problem.**
   Before building an AI/ML solution, we need to define the problem we want to solve.
   *Example (Bank):* Predict the likelihood of a customer leaving the bank and going to another. **Goal:** retain the customers.
3. **Explore and Understand Data**
   - **EDA (Exploratory Data Analysis):** analyzing the data to understand patterns, trends, and relationships.
   - Ask data-driven questions:
     - Which customers are leaving?
     - Does age affect churn?
     - Do customers with many complaints leave?
4. **Preparing Data for Machine Learning**
   - Feature building
   - Converting text into numbers (encoding)
   - Scaling numeric values
   - Creating new useful columns
   - Splitting data into features → **Feature Engineering** / **Feature Selection**
5. **Split the Data**
   - **Training Data:** used to teach/train the model.
   - **Testing Data:** used to check if the model works.
6. **Choosing a Machine Learning Algorithm**

```
                Machine Learning (ML)
                /                   \
   Supervised ML                Unsupervised ML
        |
  Classification → Yes/No (predicting a category/possibility)
  Regression → Predict one value (e.g. salary)
```

## RAG (Retrieval Augmented Generation)
A method where an AI system first retrieves relevant information and then generates an answer using that information.

### How RAG Works
```
User Prompt/Query
      ↓
Search relevant information (Knowledge Base / Vector Store)
      ↓
Retrieve query + context
      ↓
LLM generates response
      ↓
Answer
```

Simplified flow:
```
Prompt → Retrieved documents (Document Store / Vector Store / Vector Database) → Prompt + Context → LLM → Answer
```

## Vector Embeddings
- A vector embedding is a numerical representation of data points that represents different data types — including non-mathematical data such as words or images.
- It can be an array of numbers that a machine learning model can process.

```
"Rofhiwa Moscow" ─┐
                  ├─→ Embedding Model → [0.6, 0.3, 0.1, ...]
"William"        ─┘                  → [0.7, 0.9, 0.2, ...]
     (Objects)                             (Vectors)
```
- We store the resulting vectors in a **vector store**.

### Vector Store
A specialized digital system used to store, manage, and retrieve high-dimensional vector embeddings for fast similarity searches.
