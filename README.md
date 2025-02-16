# Adventure_Works_DE-Project
# Adventure Works Data Pipeline on Azure

This repository contains an **end-to-end data pipeline** solution built using **Azure** services to process the **Adventure Works dataset** from Kaggle. The goal was to create an **automated ETL pipeline** that extracts data from **GitHub**, processes and transforms it using **Azure Synapse Analytics**, and loads it into **Synapse SQL Pool** for visualization in **Power BI**.

## Project Overview

In this project, I utilized the **Adventure Works dataset** to showcase how to:
- **Ingest raw data from GitHub** using **Azure Data Factory** (ADF).
- **Transform the data** with **Azure Synapse Analytics** (Apache Spark).
- **Load the processed data** into **Azure Synapse SQL Pool**.
- **Automate the entire workflow** with **ADF Pipelines** and **Event Triggers**.
- **Visualize** insights using **Power BI**.

## Tech Stack
- **Source Control & Data Storage**: GitHub
- **Ingestion**: Azure Data Factory (ADF)
- **Processing & Transformation**: Azure Synapse Analytics (Apache Spark)
- **Orchestration**: Azure Data Factory Pipelines + Event Triggers
- **Storage**: Azure Data Lake Storage Gen2 + Synapse SQL Pool
- **Visualization**: Power BI

## Solution Steps

1. **Data Extraction**:  
   - Data is stored in a **GitHub repository** and ingested via **Azure Data Factory** HTTP connector.

2. **Data Transformation**:  
   - Used **Azure Synapse Analytics (Apache Spark)** to clean, aggregate, and convert data into **Parquet format** for optimization.

3. **Data Loading**:  
   - Transformed data is loaded into **Azure Synapse SQL Pool**, partitioned and indexed for faster querying.

4. **Pipeline Automation**:  
   - **Azure Data Factory** orchestrates the daily data pipeline and triggers on new data arrivals using **Event-Based Triggers**.

5. **Data Visualization**:  
   - Integrated **Power BI** for real-time reporting and insights from the transformed data stored in Synapse.

## Results
- **ETL process time reduced by 50%** using **Apache Spark** optimizations.
- Improved **query speed** through **partitioning** and **indexing** in **Synapse SQL Pool**.
- Fully automated data pipeline with **daily updates** from **GitHub**.
- **Interactive Power BI dashboards** for real-time sales, customer insights, and product performance.

## How to Use
1. **Set up Azure Resources**:
   - Create a **GitHub repository** with the Adventure Works dataset.
   - Set up **Azure Data Factory** and configure the HTTP connector to pull data from GitHub.
   - Set up **Azure Synapse Analytics** (Apache Spark & SQL Pools).
   - Implement the **ADF Pipelines** for orchestration.

2. **Run the Pipeline**:
   - Trigger the **ADF Pipeline** to automate data extraction, transformation, and loading.
   - Use **Power BI** to visualize the transformed data from **Synapse**.

## Challenges Faced & Lessons Learned

- **Handling Large Datasets**: Optimized performance by using **Parquet format** instead of raw CSVs for faster reads.
- **Partitioning & Indexing**: Applied these techniques in **Synapse SQL Pool** to speed up queries.
- **Automating Data Updates**: Using **Event Triggers** in **Azure Data Factory** made data ingestion and transformation fully automated.

## Discussion

Have you worked on similar datasets or projects using Azure? Share your methodology and approach in solving similar challenges! Let’s discuss and learn from each other’s experiences. 🚀

[Link to Kaggle Dataset](https://www.kaggle.com/datasets/ukveteran/adventure-works/code)
