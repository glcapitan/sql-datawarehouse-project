# SQL Server Data Warehouse Project

## Project Snapshot

This project delivers a SQL Server data warehouse that consolidates ERP and CRM sales data into a clean, structured, and reporting-ready model.

The goal is to transform raw business data into a reliable warehouse using a Bronze, Silver, and Gold architecture. The final Gold layer is modeled using fact and dimension tables, making the data easier to analyze for customer behavior, product performance, and sales trends.

---

## Business Problem

Sales data is often stored across different systems, making it difficult for teams to create reliable reports.

In this project, the source data comes from ERP and CRM CSV files. Before the data can be used for analysis, it needs to be loaded, cleaned, standardized, and organized into a proper data model.

This data warehouse solves that problem by creating a single source of structured and reliable data for reporting.

---

## Solution Overview

The solution follows a layered data warehouse approach:

```text
Source CSV Files
      ↓
Bronze Layer
Raw ERP and CRM data loaded into SQL Server
      ↓
Silver Layer
Cleaned, standardized, and validated data
      ↓
Gold Layer
Business-ready fact and dimension tables
      ↓
Reporting and Analysis
Customer, product, and sales insights
```

---

## Data Architecture

![Data Architecture](docs/Data%20architecture.png)

The project uses a Medallion Architecture:

| Layer | Purpose |
|---|---|
| Bronze | Stores raw ERP and CRM data as loaded from the source files |
| Silver | Cleans, standardizes, and prepares data for modeling |
| Gold | Contains business-ready fact and dimension tables for reporting |

---

## Key Deliverables

- Built a SQL Server data warehouse using Bronze, Silver, and Gold layers
- Loaded ERP and CRM CSV files into the Bronze layer
- Cleaned and standardized raw data in the Silver layer
- Created business-ready fact and dimension tables in the Gold layer
- Applied data quality checks to improve accuracy and consistency
- Designed a star schema to support reporting and analysis
- Documented the data flow, data model, and naming conventions

---

## Tools and Skills Used

| Area | Tools / Skills |
|---|---|
| Database | SQL Server |
| Query Language | T-SQL |
| Data Sources | ERP and CRM CSV files |
| Architecture | Bronze, Silver, and Gold Layers |
| Data Modeling | Star Schema, Fact and Dimension Tables |
| Data Quality | Cleansing, Standardization, Validation |
| Documentation | Draw.io, Markdown |
| Version Control | Git and GitHub |

---

## Data Modeling

The Gold layer is designed using a star schema.

This structure separates measurable business events from descriptive business information.

Examples:

- Fact tables for sales transactions and business metrics
- Dimension tables for customers, products, and related attributes

This makes the warehouse easier to query and ready for reporting tools or SQL-based analysis.

---

## Data Quality Checks

Data quality checks were added to make sure the final reporting layer is reliable.

Examples of checks include:

- Duplicate record checks
- Null or missing value checks
- Invalid date checks
- Standardized value checks
- Relationship checks between tables
- Consistency checks between raw and transformed data

---

## Repository Structure

```text
data-warehouse-project/
│
├── datasets/                           # Raw ERP and CRM source files
│
├── docs/                               # Project documentation and diagrams
│   ├── etl.drawio                      # ETL process documentation
│   ├── data_architecture.drawio        # Data warehouse architecture diagram
│   ├── data_catalog.md                 # Dataset and field documentation
│   ├── data_flow.drawio                # Data flow diagram
│   ├── data_models.drawio              # Star schema data model
│   ├── naming-conventions.md           # Naming standards for database objects
│
├── scripts/                            # SQL scripts for warehouse development
│   ├── bronze/                         # Raw data loading scripts
│   ├── silver/                         # Data cleaning and transformation scripts
│   ├── gold/                           # Analytical model creation scripts
│
├── tests/                              # Data quality and validation checks
│
├── README.md                           # Project overview and documentation
├── LICENSE                             # License information
├── .gitignore                          # Git ignore rules
└── requirements.txt                    # Project requirements and dependencies
```

---

## Business Questions Supported

The warehouse is designed to support analysis such as:

- Which customers generate the most sales?
- Which products are performing well or underperforming?
- How are sales changing over time?
- What customer patterns can be identified?
- Which business areas need more attention?

---

## Results

The final output is a structured SQL Server data warehouse that turns raw ERP and CRM files into clean, usable, and analysis-ready data.

Key outcomes:

- Centralized sales-related data from ERP and CRM sources
- Improved data quality through cleaning and standardization
- Created a clear Bronze, Silver, and Gold data flow
- Built a star schema for reporting
- Prepared the data for customer, product, and sales analysis
- Documented the solution for technical and business users

---

## Future Improvements

Possible future improvements include:

- Connect the Gold layer to Power BI
- Build an executive sales dashboard
- Add automated ETL scheduling
- Add incremental loading instead of full refresh
- Add historical tracking for customer and product changes
- Deploy the warehouse to a cloud database platform

---

## About Me

I am Erwin Glenn L. Capitan II, a Data Analyst focused on turning raw data into clear, useful, and decision-ready insights.

My core skills include SQL, Excel, Power BI, and Python. I enjoy building data projects that combine technical execution with business understanding.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/erwin-glenn-capitan-ii/)

---

## License

This project is licensed under the [MIT License](LICENSE).
