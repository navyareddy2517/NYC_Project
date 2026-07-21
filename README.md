# NYC Payroll Data Analytics Pipeline

## Overview

This project demonstrates an end-to-end Azure Data Engineering solution for processing and analyzing New York City payroll data. The solution ingests payroll and master datasets from Azure Data Lake Storage Gen2, loads them into Azure SQL Database, performs transformations using Azure Data Factory Mapping Data Flows, and publishes aggregated payroll data for reporting through Azure Synapse Analytics.

The project focuses on building automated, scalable, and reusable data pipelines for data integration and analytics.

---

## Architecture

Azure Data Lake Storage Gen2
        │
        ▼
Azure Data Factory
        │
        ▼
Azure SQL Database
        │
        ▼
Mapping Data Flows
        │
        ▼
Aggregated Payroll Summary
        │
        ├────────► Azure SQL Summary Table
        │
        └────────► Azure Data Lake Staging
                           │
                           ▼
                Azure Synapse External Table

---

## Technologies Used

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure SQL Database
- Azure Synapse Analytics (Serverless SQL Pool)
- SQL
- GitHub

---

## Project Features

- Created Azure Data Lake Storage Gen2 for payroll and master datasets.
- Developed Linked Services connecting Azure Data Lake and Azure SQL Database.
- Created reusable datasets for source CSV files and SQL tables.
- Built Mapping Data Flows to load master and payroll data into Azure SQL Database.
- Implemented payroll aggregation using Union, Filter, Derived Column, and Aggregate transformations.
- Calculated TotalPaid using:

```

TotalPaid = RegularGrossPaid + TotalOTPaid + TotalOtherPay

```

- Exported aggregated payroll data to Azure Data Lake staging.
- Created an external table in Azure Synapse Analytics to query staged data.
- Designed and executed an end-to-end Azure Data Factory pipeline.
- Successfully monitored and validated pipeline execution.

---

## Pipeline Workflow

1. Load Employee Master Data
2. Load Agency Master Data
3. Load Job Title Master Data
4. Load Payroll 2020 Data
5. Load Payroll 2021 Data
6. Merge historical and current payroll datasets
7. Calculate TotalPaid
8. Aggregate payroll data by Fiscal Year and Agency
9. Store summary data in Azure SQL Database
10. Export summary data to Azure Data Lake
11. Query aggregated data using Azure Synapse Analytics

---

## Data Flow Components

- Source
- Select
- Union
- Filter
- Derived Column
- Aggregate
- SQL Sink
- Azure Data Lake Sink

---

## Azure Services Used

- Azure Data Lake Storage Gen2
- Azure Data Factory
- Azure SQL Database
- Azure Synapse Analytics

---

## Learning Outcomes

This project helped me gain practical experience in:

- Building ETL/ELT pipelines
- Data integration using Azure Data Factory
- Mapping Data Flow transformations
- SQL data loading and validation
- Azure Synapse external tables
- Azure cloud storage and data orchestration
- Pipeline monitoring and debugging

---

## Project Status

Completed

---

## Author

Navya Gujjula
