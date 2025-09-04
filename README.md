# 🏅 Tokyo Olympic Data of 2021 – End-to-End Azure Data Engineering Project

![Azure](https://img.shields.io/badge/Platform-Microsoft%20Azure-blue)
![GitHub](https://img.shields.io/badge/Repo-Version--Controlled-lightgrey)
![Pipeline](https://img.shields.io/badge/Data-Pipeline-green)

---

##  Project Overview

This project demonstrates an **end-to-end Azure Data Engineering pipeline (ELT)** built on the **Tokyo Olympic dataset (2021)**.  
It comprehensively covers **data ingestion, transformation, storage in efficient formats, cloud scheduling, secure operations, and advanced visual dashboards**, all powered by Azure services.

---

##  Project Highlights

- **Automated Ingestion**  
  - Orchestrated via **Azure Data Factory (ADF)** to pull raw datasets (athletes, events, medals, entries) and store them in **ADLS Gen2**.  
  - Ingestion scheduled with **GitHub triggers** enabling continuous pipeline updates.

- **Data Lake Architecture (Medallion)**  
  - **Bronze (Raw Zone)** 🟤: Unprocessed CSV/JSON data as-is.  
  - **Silver (Curated Zone)** ⚪: Standardized and validated Parquet/Delta datasets.  
  - **Gold (Analytics Zone)** 🟡: Aggregated, partitioned datasets optimized for Power BI and Synapse analytics.

- **Secure Workflow Management**  
  - All service credentials managed securely via **Azure Key Vault**.  
  - Implemented fault-tolerant data pipelines with **retry logic** and error monitoring through ADF alerts.

- **Scalable Data Processing**  
  - Used **Azure Databricks (PySpark)** for schema enforcement, cleansing, enrichment, and feature engineering (e.g. athlete age groups, medal tallies, country performance scores).

- **Analytics-Ready Storage**  
  - Transformed datasets ingested into **Azure Synapse Analytics** (dedicated SQL pool) to enable performant querying with partition optimization by Olympic year and event category.

- **Power BI Dashboards**  
  - Visualized Olympic insights:  
    - Top-performing countries  
    - Gender-wise participation  
    - Event-category heatmaps  
    - Medal trends over time

---

## 🗂️ Data Lake Architecture (Medallion)

- **Bronze (Raw Zone) 🟤**  
  - Houses ingested data as-is for auditability and traceability.

- **Silver (Curated Zone) ⚪**  
  - Enforces clean schema, duplicates removed, calculated fields added (e.g. Raw to standardized events).

- **Gold (Analytics Zone) 🟡**  
  - Stores query-ready data with event and country aggregates, partitioned by year/event type.

---

## 🏗️ Architecture Workflow (with Medallion Layers)

1. **Ingestion → Bronze**  
   - ADF pipelines ingest raw Olympic data into Bronze container.

2. **Transform → Silver**  
   - Databricks jobs clean and normalize data, stored in the Silver layer.

3. **Aggregate → Gold**  
   - Pivotal metrics (e.g., medal counts, top athletes) calculated and stored in Gold for analytics.

4. **Visualization**  
   - Power BI dashboards draw insights directly from the Gold layer.

---

##  Tech Stack & Tools

| Component                   | Tool / Service                    |
|----------------------------|-----------------------------------|
| Orchestration              | Azure Data Factory (ADF)          |
| Storage Layer              | Azure Data Lake Storage Gen2      |
| Processing & Transformation | Azure Databricks (PySpark)       |
| Data Warehouse             | Azure Synapse Analytics           |
| Secret Management          | Azure Key Vault                   |
| Dashboarding               | Power BI                          |
| Version Control            | GitHub                            |

---

##  Key Insights Visualized

- **Top medal-winning countries**  
- **Athlete participation by age & gender**  
- **Event-based medal distribution**  
- **Performance trends across Olympic categories**

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


