## 🏠 Real Estate Market Intelligence Pipeline

### End-to-End Engineering with Microsoft Fabric & PySpark

🌟 Project Strategy

This repository contains a full-scale data engineering solution designed to process and analyze high-volume real estate transactions. Using the Medallion Architecture, I built a robust pipeline that converts raw property data into a highly optimized Star Schema, enabling deep market insights through Power BI.

🏗️ The Data Journey (Medallion Architecture)

📂 1. Landing Zone (Raw Ingestion)
Notebook: Raw_To_Landing.ipynb

Process: Automated ingestion of source CSV files into the Fabric Lakehouse.

Feature: Implemented partitioned storage by Processing_date to ensure a scalable and organized landing zone.

🛡️ 2. Bronze Layer (Validation)
Notebook: Landing_to_Bronze_table.ipynb

Process: Initial schema definition and Delta table conversion.

Feature: Established the foundation for ACID transactions and time-travel capabilities within the Lakehouse.

🥈 3. Silver Layer (Optimization & Cleaning)
Notebook: Silvertransformation.ipynb

Process: Data type standardization, currency/area normalization, and record deduplication.

Logic: Leveraged Spark Window Functions to ensure the most relevant property records are promoted to the analytics layer.

🥇 4. Gold Layer (The Analytics Hub)
Notebook: Silver_to_gold_transformation.ipynb

Process: Dimensional modeling using the Kimball methodology.

Model: Developed a specialized Star Schema consisting of:

Fact Table: FactAverageHousePrice (Aggregated market metrics).

Dimension Tables: DimHouse (Property attributes) and DimDate.

🛠️ Technical Highlights

Dimensional Modeling
Designed a semantic model optimized for DAX performance, reducing query latency and ensuring accurate "Average Price per Area" calculations.

Advanced Spark Operations
Utilized complex PySpark transformations and windowing logic to maintain data integrity across 19,000+ records.

Automated Maintenance
Included OPTIMIZE and VACUUM routines within the notebooks to manage file sizes and ensure peak performance in a production-like environment.

📊 Visual Insights & Deliverables

Semantic Model (Relationship View)
This view demonstrates the logical structure of the data, ensuring clear relationships between property attributes and financial metrics.

<img width="1556" height="654" alt="semantic model" src="https://github.com/user-attachments/assets/e6c6523f-1edb-4bd9-999b-94a1c8a64c16" />

Pipeline Execution
Proof of successful end-to-end orchestration and data flow.

<img width="2237" height="1074" alt="Pipeline run" src="https://github.com/user-attachments/assets/f0dcf4d9-01cb-4e82-a0d3-ad62e30574f5" />


Executive Power BI Dashboard
An interactive interface allowing stakeholders to explore market trends, furnishing distributions, and amenity-based pricing.

<img width="2037" height="1132" alt="Dashboard" src="https://github.com/user-attachments/assets/6267f7a6-bb46-4bf5-920b-ed056835606e" />


📂 Repository Contents
Notebooks/: Complete .ipynb source code for all four stages.

Documentation/: Architecture diagrams and technical specifications.

Screenshots/: Visual evidence of pipeline success and dashboard des
