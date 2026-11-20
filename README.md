AdventWork Commercial Data Lakehouse

Building a modern, scalable, and reliable data platform for commercial analytics.

Overview

The AdventWork Commercial Data Lakehouse is an end-to-end data engineering project designed to centralize, process, and transform commercial business data into reliable, analytics-ready datasets.

The platform integrates data from multiple commercial domains, including sales, products, inventory, purchases, and suppliers. It establishes a structured data foundation that supports data quality, scalable processing, and business intelligence.

Built on Microsoft Azure, the solution combines Azure Data Factory, Azure Databricks, PySpark, Delta Lake, and dbt to implement a modern lakehouse architecture based on the Medallion Architecture.

Business Scope

The lakehouse consolidates data across five core commercial domains:

Business Domain	Description
Sales	Sales transactions, revenue, and commercial performance
Products	Product information, categories, and attributes
Stock Levels	Inventory quantities, stock availability, and levels
Purchases	Procurement transactions and purchasing activities
Suppliers	Supplier information and business relationships

The objective is to transform operational data into consistent, trusted datasets that can support analytical workloads and business reporting.

Architecture

The solution follows the Medallion Architecture, separating data processing into three logical layers.

1. Bronze Layer – Raw Data

The Bronze layer stores source data ingested from Azure SQL Database.

Key responsibilities:

Extract data from source systems.
Support incremental data ingestion.
Preserve raw source records.
Maintain traceability and ingestion metadata.
Store data in Delta Lake format.
2. Silver Layer – Cleansed and Standardized Data

The Silver layer transforms raw data into structured and reliable datasets.

Key responsibilities:

Data cleansing and standardization.
Schema enforcement and validation.
Handling missing and inconsistent values.
Data type normalization.
Deduplication and transformation.
Maintaining data quality.
3. Gold Layer – Business-Ready Data

The Gold layer contains curated datasets designed for business consumption and analytics.

Key responsibilities:

Business-oriented data modeling.
Fact and dimension modeling where appropriate.
Aggregations and analytical transformations.
Integration of commercial business domains.
Delivery of analytics-ready datasets.
Technology Stack
Category	Technology	Purpose
Cloud Platform	Microsoft Azure	Cloud infrastructure
Source Database	Azure SQL Database	Operational data source
Data Integration	Azure Data Factory	Data ingestion and orchestration
Data Processing	Azure Databricks	Distributed data processing
Processing Language	Python / PySpark	Data engineering and transformations
Storage Format	Delta Lake	Reliable lakehouse storage
Data Transformation	dbt	SQL-based modeling and transformations
Data Quality	dbt Tests / PySpark	Data validation and quality checks
Architecture	Medallion Architecture	Layered data organization
End-to-End Data Pipeline

The overall data flow is organized as follows:

text
                 SOURCE SYSTEM
                Azure SQL Database
                        |
                        v
               AZURE DATA FACTORY
              Ingestion & Orchestration
                        |
                        v
                AZURE DATABRICKS
                        |
                        v
              +-------------------+
              |   BRONZE LAYER    |
              |   Raw Delta Data  |
              +-------------------+
                        |
                        v
              +-------------------+
              |   SILVER LAYER    |
              | Cleansed & Validated
              |   Delta Data      |
              +-------------------+
                        |
                        v
              +-------------------+
              |    GOLD LAYER     |
              | Business-Oriented |
              |    Data Models    |
              +-------------------+
                        |
                        v
                       dbt
             Modeling, Testing &
                Documentation
                        |
                        v
              ANALYTICS-READY DATA


Note: This represents the logical processing architecture. The exact execution responsibilities of Databricks and dbt may evolve during implementation.

Key Engineering Capabilities

The project focuses on implementing the following data engineering capabilities:

Automated Data Ingestion: Orchestrated ingestion workflows connecting Azure SQL Database to the lakehouse.
Incremental Processing: Loading new and modified records while minimizing unnecessary data processing.
Scalable Transformations: Distributed data processing using Azure Databricks and PySpark.
Data Quality Management: Validation, standardization, and consistency checks across processing layers.
Lakehouse Storage: Delta Lake-based storage for reliable and structured data management.
Data Modeling: Business-oriented transformations using dbt.
Documentation and Testing: Documented models and automated data quality tests.
Repository Structure

The repository is organized by technology and processing responsibility to maintain separation of concerns and simplify development.

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
│   ├── macros/
│   └── dbt_project.yml
│
├── docs/
│   └── architecture/
│
└── README.md


Directory responsibilities:

Directory	Responsibility
adf/	Azure Data Factory pipeline definitions
databricks/bronze/	Raw ingestion and Bronze transformations
databricks/silver/	Cleansing and standardization
databricks/gold/	Curated business transformations
dbt/	Data models, tests, and macros
docs/	Architecture documentation and technical references
Project Objectives

The primary objectives are to:

Build a scalable and maintainable cloud-based data engineering platform.
Centralize commercial business data into a unified lakehouse.
Establish reliable and incremental data ingestion processes.
Improve data quality through structured validation and transformation.
Implement layered data processing using the Medallion Architecture.
Develop trusted, analytics-ready datasets for business intelligence.
Project Status

Currently in development.

The project is being developed incrementally, with a focus on establishing the cloud architecture, implementing ingestion workflows, building the Medallion layers, and developing business-oriented data models.

Vision

Establish a reliable commercial data foundation that transforms operational business data into structured, trusted, and actionable information.

AdventWork Commercial Data Lakehouse

From operational data to trusted business insights.
