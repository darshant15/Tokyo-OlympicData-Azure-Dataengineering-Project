
# 🏅 Tokyo Olympic Data of 2021 – End-to-End Azure Data Engineering Project

![Azure](https://img.shields.io/badge/Platform-Microsoft%20Azure-blue)
![GitHub](https://img.shields.io/badge/Repo-Version--Controlled-lightgrey)
![Pipeline](https://img.shields.io/badge/Data-Pipeline-green)

## 📌 Project Overview

This project demonstrates an **end-to-end Azure Data Engineering pipeline** built on the **Tokyo Olympic dataset**.
It covers **data ingestion, transformation, storage, querying, and automation** using Azure cloud services.

---
## 🚀 Project Highlights

- **Automated Ingestion**: Pipelines in **Azure Data Factory (ADF)** ingest raw Tokyo Olympics datasets (athletes, medals, teams, entries, etc.) into **Azure Data Lake Storage Gen2**.  
- **Data Lake Architecture**: 
  - **Raw zone** → Ingested unprocessed datasets  
  - **Curated zone** → Cleaned, transformed Parquet/Delta data optimized for analytics  
- **Secure Pipeline Management**: Store credentials and secrets in **Azure Key Vault** for secure operations.  
- **Scalable Data Processing**: Use **Azure Databricks (PySpark)** for cleaning, deduplication, joins, and aggregations.  
- **Analytics-Ready Storage**: Query curated datasets using **Azure Synapse Analytics** (SQL serverless/dedicated pool).  
- **BI & Dashboards**: Build **Power BI** dashboards to visualize insights like medal tallies, gender participation, athlete demographics, and country performance by the data analysis(Report) using data given after ELT from data engineer .

--- 

🔗 **GitHub Repository:** [Tokyo-OlympicData-Azure-Dataengineering-Project](https://github.com/darshant15/Tokyo-OlympicData-Azure-Dataengineering-Project.git)

---
## Architect Diagram

![Architect](https://github.com/darshant15/Tokyo-OlympicData-Azure-Dataengineering-Project/blob/main/Architect-of-project.jpeg)

---

## 🎯 Objectives

* Design and implement a **cloud-based ETL pipeline** for Olympic data.
* Automate **data ingestion, transformation, and analytics**.
* Showcase integration of multiple **Azure services** with version control on GitHub.

---

## 🏗️ Architecture Workflow

1. **Data Ingestion** – CSV files ingested from GitHub using **Azure Data Factory (ADF)**.
2. **Data Lake Storage** – Raw and processed data stored in **Azure Data Lake Storage Gen2** (separate containers for `raw-data` and `transformed-data`).
3. **Data Processing** – Used **Azure Databricks (Spark)** for:

   * Data cleaning
   * Deduplication
   * Feature engineering
   * Transformations
4. **Data Warehouse** – Loaded transformed datasets into **Azure Synapse Analytics (Lake Database)** for robust SQL querying and insights.
5. **Automation & Monitoring** – Implemented **ADF scheduling and monitoring** to ensure reliable and timely pipeline refresh.
6. **Version Control** – All Databricks notebooks and ADF workflows cloned into **GitHub** for collaboration and reproducibility.

---

## ⚙️ Tech Stack & Tools

* **Azure Data Factory (ADF)** – Data ingestion, orchestration, scheduling
* **Azure Data Lake Storage Gen2 (ADLS)** – Raw and curated data storage
* **Azure Databricks (Apache Spark)** – Data cleaning, transformations, feature engineering
* **Azure Synapse Analytics** – SQL querying, analytics-ready storage
* **GitHub** – Version control and project showcase

---

## 📊 Key Insights (Examples)

* Medal distribution across countries and sports
* Athlete performance analysis
* Historical trends of Olympic participation
* Country-wise comparisons

---

## 🚀 How to Use

1. Clone the repository:

   ```bash
   git clone https://github.com/darshant15/Tokyo-OlympicData-Azure-Dataengineering-Project.git
   ```
2. Import the notebooks into **Azure Databricks**.
3. Configure **ADF pipelines** with proper linked services for GitHub and ADLS.
4. Run pipeline to ingest → transform → load data.
5. Query insights using **Synapse Analytics**.

---

## 📌 Author

👤 **Darshan T**

* 🔗 [GitHub Profile](https://github.com/darshant15)

---

✨ This project highlights **real-world Azure Data Engineering skills** – from ingestion to automation – and can be extended with **Power BI dashboards** for visualization if it's required.

---


