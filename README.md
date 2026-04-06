# Human Trafficking Intelligence Platform (Azure Data Engineering Project)

## Overview

This project presents an end-to-end data engineering and analytics solution built on Microsoft Azure to analyze and uncover patterns related to human trafficking.

The platform is designed to support policymakers, NGOs, and law enforcement agencies by transforming raw, fragmented data into structured, reliable, and actionable insights.

It follows enterprise-grade data warehousing principles using the Kimball methodology and delivers analytics through Power BI dashboards.

---

## Objectives

* Build a scalable end-to-end data pipeline on Azure
* Implement a robust dimensional model using Kimball methodology
* Enable historical tracking and data consistency
* Deliver executive-ready dashboards for decision-making

---

## Architecture Overview

![Architecture](./architecture/architecture.png)

### Data Flow

1. Data ingestion using Azure Data Factory
2. Raw storage in Azure Data Lake (Bronze Layer)
3. Data transformation and cleansing (Silver Layer)
4. Dimensional modeling using Star Schema (Gold Layer)
5. Data visualization using Power BI

---

## Tech Stack

* Azure Data Factory (ADF)
* Azure Data Lake Storage Gen2 (ADLS)
* Azure Synapse Analytics
* Power BI
* SQL / PySpark

---

## Data Architecture (Medallion + Kimball)

### Bronze Layer (Raw)

* Stores ingested raw data from multiple sources
* Maintains original structure for traceability

### Silver Layer (Cleaned)

* Data cleansing, standardization, and validation
* Handles null values, duplicates, and schema consistency

### Gold Layer (Curated)

* Business-ready data modeled using Star Schema
* Optimized for analytical queries

---

## Dimensional Modeling (Kimball Approach)

### Star Schema Design

![Data Model](./architecture/data_model.png)

* Fact Tables:

  * FactCases
  * FactIncidents

* Dimension Tables:

  * DimVictim
  * DimLocation
  * DimDate
  * DimAgency
  * DimTraffickingType

---

## Bus Matrix

![Bus Matrix](./architecture/bus_matrix.png)

* Defines business processes and conformed dimensions
* Ensures consistency across fact tables

---

## Keys and Historical Tracking

* Surrogate keys implemented for all dimensions
* Business keys preserved for source traceability

### Slowly Changing Dimensions (SCD)

* Type 1: Overwrite changes
* Type 2: Full history tracking
* Type 3: Limited history

---

## Data Pipeline (ADF)

![ADF Pipeline](./architecture/adf_pipeline.png)

### Features:

* Incremental data loading
* Parameterized pipelines
* Error handling and logging

---

## Data Quality and Governance

* Data validation checks implemented
* Deduplication handled
* Late-arriving dimensions managed
* Data lineage maintained

---

## Power BI Analytics

![Dashboard](./screenshots/powerbi_dashboard.png)

### Key Insights:

* Trafficking trends by region
* Victim demographics analysis
* Incident patterns over time
* Agency performance metrics
