## 🏠 Real Estate Market Intelligence Platform
End-to-End Engineering on Microsoft Fabric

### 🌟 Project Overview
This project delivers a comprehensive data platform for real estate market analysis. Using Microsoft Fabric, I engineered a scalable Medallion Architecture pipeline that ingests raw property data and transforms it into a highly optimized Star Schema. The solution focuses on data integrity, automated orchestration, and self-service BI.

## 🏗️ The Medallion Pipeline
The data flows through four distinct stages of refinement, ensuring high-quality insights at the Gold layer.

### 1. Ingestion & Bronze (Raw)
Notebooks: Raw_To_Landing.ipynb | Landing_to_Bronze_table.ipynb

Process: Automated CSV ingestion into the OneLake environment.

Storage: Data is converted to Delta format, enabling ACID transactions and efficient file management.

### 2. Silver (Refined)
Notebook: Silvertransformation.ipynb

Process: Data type standardization, currency normalization, and deduplication logic.

Feature: Utilized Spark Window Functions to ensure the "Golden Record" is maintained for every property.

### 3. Gold (Curated Analytics)
Notebook: Silver_to_gold_transformation.ipynb

Process: Dimensional modeling (Kimball) to create a high-performance Star Schema.

Deliverables: FactAverageHousePrice, DimHouse, and DimDate.

## 🛠️ Microsoft Fabric Engineering 

Data Lineage & Traceability
The visual map below shows the end-to-end lifecycle of the data, from the initial landing zone files through the Spark transformations to the final Power BI report.

<img width="1809" height="1173" alt="Lineage view" src="https://github.com/user-attachments/assets/ef42414a-1c85-4859-ab25-fa6bfe481565" />


This Image shows the Lake house explorer

<img width="485" height="810" alt="Lakehouse Explorer" src="https://github.com/user-attachments/assets/e4950c9f-b01f-46ae-9a27-28abd6ae20f1" />


Automated Orchestration

The pipeline is orchestrated using Fabric Data Pipelines, ensuring that notebook executions follow a logical dependency order with built-in monitoring.

<img width="2237" height="1074" alt="Pipeline run" src="https://github.com/user-attachments/assets/5f87cfa2-a8da-4f80-9793-92df8c8bb9bc" />


SQL Endpoint & Accessibility

To support cross-functional teams, the Gold layer is exposed via a SQL Endpoint, allowing analysts to query the Delta tables directly using T-SQL.

<img width="2006" height="1114" alt="SQL EnD point view" src="https://github.com/user-attachments/assets/f90b6f4d-783d-45af-b66d-7c59da1d182b" />


## 📊 Business Intelligence Dashboard

The final dashboard provides stakeholders with instant visibility into market trends and inventory metrics.

Total Listings: Real-time count of property inventory.

Market Mix: Breakdown of property distribution by Furnishing Status.

Price Drivers: Identification of premium value amenities (Parking, AC, and Area).

<img width="2037" height="1132" alt="Dashboard" src="https://github.com/user-attachments/assets/9f2d612c-3b2d-4ca0-9e84-9bd0f1fc5e19" />


## 📂 Repository Contents

Notebooks/: Full PySpark source code for all Medallion layers.

Screenshots/: Technical evidence of pipeline success and architecture.

Schema/: Documentation of the Star Schema semantic model.
