**Overview**

End-to-end Azure data engineering project that ingests, transforms, and analyses Tokyo Olympics datasets using a modern cloud data platform.

**Architecture**

Azure Data Factory – data ingestion pipelines
Azure Data Lake Storage Gen2 – raw & curated storage
Azure Databricks (PySpark) – data transformation
Azure Synapse Analytics (SQL) – analytics & querying
Azure Active Directory – secure service authentication

**1. Data Ingestion**

-Multiple datasets (Athletes, Coaches, Teams, Medals, Entries by Gender) are ingested using Azure Data Factory Copy activities
-Pipelines are chained to ensure sequential execution

**2. Data Storage**

-Raw data is stored in ADLS Gen2
-Hierarchical namespace enabled
-Folder structure designed for scalability and analytics consumption

**3. Data Transformation**

-Azure Databricks notebooks perform:
-Schema enforcement
-Data cleansing
-Column standardisation
-Preparation for analytics consumption

**4. Analytics & Querying**

-Curated datasets are queried using Azure Synapse SQL
-Analytical queries include:
-Athlete counts by country
-Medal tallies by team
-Gender-based participation analysis

**Analytics Examples**

SELECT Country, COUNT(*) AS TotalAthletes
FROM athletes
GROUP BY Country
ORDER BY TotalAthletes DESC;

<img width="1920" height="1080" alt="Tokyo Olympic Data Engineering Pipeline" src="https://github.com/user-attachments/assets/9e76eca2-8697-40ec-a43e-0b4fd2f4fa14" />
