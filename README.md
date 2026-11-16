AdventWork Commercial Data Lakehouse

An end-to-end data engineering project designed to build a modern cloud-based data lakehouse for AdventWork's commercial operations.

The platform centralizes and transforms business data across key domains, including sales, products, stock levels, purchases, and suppliers, providing structured, reliable, and analytics-ready datasets.

Architecture

The solution follows the Medallion Architecture, organizing data into three layers:

Bronze Layer: Raw data ingestion from Azure SQL Database.
Silver Layer: Data cleansing, standardization, validation, and transformation.
Gold Layer: Business-oriented data models and analytics-ready datasets.
Technologies
Cloud Platform: Microsoft Azure
Database: Azure SQL Database
Data Integration: Azure Data Factory
Data Processing: Azure Databricks, PySpark
Storage Format: Delta Lake
Data Transformation & Modeling: dbt
Architecture: Medallion Architecture (Bronze, Silver, Gold)
Key Features
Designed an end-to-end data pipeline to ingest and transform enterprise business data.
Implemented a Medallion Architecture with Bronze, Silver, and Gold layers.
Developed incremental data ingestion workflows.
Built scalable data transformation processes using PySpark and SQL.
Applied dbt for data modeling, testing, and documentation.
Structured business data into analytics-ready datasets.
Data Domains

The lakehouse covers the following commercial business domains:

Domain	Description
Sales	Sales transactions and commercial performance
Products	Product information and attributes
Stock Levels	Inventory levels and stock availability
Purchases	Purchase transactions and procurement data
Suppliers	Supplier information and relationships
Project Architecture
text
             Azure SQL Database
                     |
                     v
            Azure Data Factory
                     |
                     v
              Azure Databricks
                     |
                     v
              BRONZE LAYER
                Raw Data
                     |
                     v
              SILVER LAYER
       Cleaned & Standardized Data
                     |
                     v
               GOLD LAYER
          Business Data Models
                     |
                     v
                    dbt
       Modeling, Testing & Documentation
                     |
                     v
          Analytics-Ready Datasets

Project Objectives
Build a scalable and maintainable cloud data engineering solution.
Centralize commercial business data into a unified lakehouse.
Improve data quality through structured transformation and validation.
Enable reliable incremental data processing.
Deliver trusted datasets for reporting and business analytics.
Repository Structure
text
adventwork-commercial-data-lakehouse/
│
├── adf/
│   └── pipelines/
│
├── databricks/
│   ├── bronze/
│   ├── silver/
│   └── gold/
│
├── dbt/
│   ├── models/
│   ├── tests/
│   └── macros/
│
├── docs/
│   └── architecture/
│
└── README.md


Note: The repository structure represents the proposed organization of the project.

Project Status

In development.

AdventWork Commercial Data Lakehouse
Building a modern, scalable, and reliable data foundation for commercial analytics.
