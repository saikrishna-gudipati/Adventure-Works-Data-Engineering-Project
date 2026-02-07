Azure ETL Pipeline: Data Extraction, Transformation & Load

🚀 Project Overview
This project implements an end-to-end ETL pipeline using Azure Data Factory (ADF), Azure Databricks, and PySpark. The pipeline extracts data from SQL Server and GitHub, processes it using Medallion Architecture (Bronze, Silver, Gold layers), and supports incremental data loading using SCD Type 1 (Upsert). The solution is designed to ensure data reliability, scalability, and optimized performance for analytics workloads.

 Architecture and Workflow

📂 Data Sources
• SQL Server is used as the structured relational database source.
• GitHub is used as a source for extracting raw JSON data.

⚙️ Pipeline Workflow
• Data ingestion is performed using Azure Data Factory to extract data from source systems.
• Raw data is copied into staging tables for further processing.
• Incremental load management is handled using SCD Type 1 Upsert logic.
• Data transformation is performed in Azure Databricks using PySpark and Delta Lake.
• Final processed data is stored in fact and dimension tables optimized for reporting and analytics.

🪙 Medallion Architecture Implementation
• Bronze layer stores raw ingested data without transformation.
• Silver layer contains cleaned and structured data after transformation.
• Gold layer contains aggregated and analytics-ready data used for reporting and business insights.

🛠️ Technologies Used
• Azure Data Factory is used for data orchestration and pipeline execution.
• Azure Databricks is used for data transformation using PySpark.
• Delta Lake and Delta Tables are used for optimized storage, ACID transactions, and schema evolution.
• SQL Server is used for structured data storage.

⭐ Key Features
• Incremental data loading is implemented using a watermark column.
• SCD Type 1 Upsert logic is used for efficient record updates.
• Pipeline execution is optimized using parallel processing.
• Error handling and schema evolution are implemented using Delta Tables.

🧩 Challenges and Solutions

📌 Handling Incremental Loads
• A watermark table is implemented to track the last load timestamp.
• SCD Type 1 Upsert ensures efficient updates and avoids duplicate records.

📌 Parallel Execution Issues
• Data conflicts were resolved by implementing proper merge logic and partition strategies.
• Schema evolution was managed effectively using Delta Lake features.

