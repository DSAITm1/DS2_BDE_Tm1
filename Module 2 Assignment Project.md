# Module 2 Assignment Project

## Overview
In this project, as part of the data-engineering team, you are tasked to build an **end-to-end data pipeline and analysis workflow** for a company.  
You'll start with raw data files, load them into a data warehouse, perform **ELT processes**, ensure **data quality**, and conduct analysis in **Python**.

---

## Project Brief

### 1. Data Ingestion

**Source data** (pick any one of these):  
- [Brazilian E-Commerce Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)  
- [Instacart Market Basket Analysis Dataset](https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis/data) *(Data dictionary not available, but most columns are easily interpretable)*  
- [London Bicycles dataset](https://console.cloud.google.com/bigquery?p=bigquery-public-data&d=london_bicycles&page=dataset) *(BigQuery dataset located in EU, set DBT project’s location to EU)*  

**Notes:**
- Limit to the core datasets; you do not have to use all of them.  
- You are **not limited** to what you learned in the course; you can use any database technology.  
- Ingest the data into your database/data warehouse:  
  - Write Python scripts to load the CSV and Excel files into database tables, **or**  
  - Use any suitable ingestion method.

---

### 2. Data Warehouse Design
- Design a **star schema** for the e-commerce data.  
- Create **dimension tables** (e.g., `DimCustomer`, `DimProduct`, `DimDate`) and **fact tables** (e.g., `FactSales`).  
- Implement the schema in your chosen database.

---

### 3. ELT Pipeline
- You can use **dbt** to transform the raw data into the star schema (not limited to DBT).  
- Implement **data cleaning** and **validation** steps.  
- Create derived columns (e.g., `total_sale_amount`, `customer_lifetime_value`).  

---

### 4. Data Quality Testing
- Use **[Great Expectations](https://greatexpectations.io/)** or custom SQL queries to define and test data quality rules.  
- Implement tests for:
  - Null values
  - Duplicates
  - Referential integrity
  - Business logic  

---

### 5. Data Analysis with Python
When designing a data pipeline, always consider the **end goal**: making the data in your data warehouse accessible and usable for BI analysts, data scientists, and business stakeholders to extract valuable insights.

Tasks:
- Connect to the data warehouse using **SQLAlchemy**.  
- Perform simple **EDA** using `pandas`.  
- Calculate key metrics such as:
  - Monthly sales trends
  - Top-selling products
  - Customer segmentation by purchase behavior

---

### 6. Pipeline Orchestration *(Optional)*
Use any orchestration framework to automate the entire pipeline, schedule ELT processes, and run data quality checks.

Possible tools:
- Orchestration tools: **dagster**, **airflow**  
- Managed services: **Google Cloud Composer**  
- **Cron jobs**  
- **CI/CD** via GitHub Actions  

---

### 7. Documentation
- Document your **code**, **data lineage**, and **pipeline architecture** using tools like:  
  - [Draw.io](http://draw.io)  
  - [Excalidraw](https://excalidraw.com/)  
- Prepare a report summarizing:
  - Technical approach
  - Findings/insights
  - Relevant tables, charts, and graphs  
- Include:
  - Why certain tools were chosen
  - Schema design justification and how it supports efficient querying

---

## Deliverables
1. GitHub repository in a single main branch with all code and documentation.  
2. Jupyter notebooks with basic analysis.  
3. Slide deck with executive summary and key findings.

---

## Evaluation Criteria

### **Focus:**
- Accuracy and integrity of the data pipeline  
- Quality of code and adherence to best practices  
- Overall architecture and scalability of the solution  
- Good documentation of the system and reasoning behind design/tool choices  

### **Good to Have:**
- Depth of data analysis and insights generated  
