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

<img width="1441" height="892" alt="ADF Architecture" src="https://github.com/user-attachments/assets/317c0867-d816-4ec2-8a66-92f9ee909a1f" />


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

<img width="2395" height="2081" alt="Data Model - Copy" src="https://github.com/user-attachments/assets/be824faa-faf1-4842-8f3c-7cb2f67fe146" />




## Keys and Historical Tracking

* Surrogate keys implemented for all dimensions
* Business keys preserved for source traceability

### Slowly Changing Dimensions (SCD)

* Type 1: Overwrite changes
* Type 2: Full history tracking
* Type 3: Limited history



## Data Quality and Governance

* Data validation checks implemented
* Deduplication handled
* Late-arriving dimensions managed
* Data lineage maintained

---

## Power BI Analytics

<img width="1148" height="642" alt="image" src="https://github.com/user-attachments/assets/004ce2b9-2656-4621-b19f-e6e0bf257376" />

<img width="1114" height="647" alt="image" src="https://github.com/user-attachments/assets/b391eec9-9874-4d61-b88c-ffffd59f0d13" />

<img width="1045" height="654" alt="image" src="https://github.com/user-attachments/assets/c7fe47a0-a099-44f3-bf8c-5edea5ac0ab6" />

<img width="1036" height="652" alt="image" src="https://github.com/user-attachments/assets/6bde8928-5a8e-40f6-a29c-45084c6968ff" />

<img width="1113" height="635" alt="image" src="https://github.com/user-attachments/assets/f23d38bd-4997-4d38-b78e-db36cb44850c" />



### Key Insights:

* Trafficking trends by region
* Victim demographics analysis
* Incident patterns over time
* Agency performance metrics
