# Azure-Data-Pipeline-for-Customer-Insights
Developed a comprehensive data pipeline using Azure Data Factory, Databricks, and Synapse to extract, transform, and load customer and sales data from an on-premises SQL database into Azure. Implemented a Bronze-Silver-Gold architecture, optimizing data processing and ensuring daily updates for real-time insights and analysis.
![image](https://github.com/user-attachments/assets/7810391e-b3f6-454b-8905-80b81a14da0d)

Here's a professional and detailed **README.md** file for your project, formatted with proper headings, bullet points, and emojis for use on GitHub. You can copy and paste this directly to your Git repository.

---

# 🚀 Azure End-to-End Data Engineering Project

### **Overview**
This project demonstrates the development of a robust, automated data pipeline using **Azure Data Factory**, **Databricks**, and **Synapse Analytics** to extract, transform, and load customer and sales data from an on-premises SQL database into Azure. The goal is to optimize data processing through the **Bronze-Silver-Gold** architecture, enabling high-performance querying, real-time insights, and seamless daily updates. 

---

## 📋 **Business Requirements**

The company identified a gap in understanding customer demographics and how they influence product purchases. Key stakeholders requested a solution that:
- **Visualizes Sales** by product category and gender.
- **Filters Data** by product category, gender, and date.
- Provides a **user-friendly** querying interface.
- Ensures **daily automated data updates** for up-to-date insights.

---

## 🛠️ **Solution Overview**
The solution is structured into several components, each contributing to the end-to-end data pipeline:

1. **Data Ingestion**:
   - Extract data from on-premises SQL Server using **Azure Data Factory**.
   - Load the data into **Azure Data Lake Storage (ADLS)**.

2. **Data Transformation**:
   - Use **Azure Databricks** to process raw data, transforming it through **Bronze-Silver-Gold** architecture.
     - **Bronze**: Raw data stored as-is.
     - **Silver**: Cleaned and transformed data.
     - **Gold**: Aggregated, query-optimized data for reporting.

3. **Data Loading & Reporting**:
   - Load transformed data into **Azure Synapse Analytics** for high-performance querying.
   - Schedule the pipeline to ensure daily updates, with secure and efficient data movement.

4. **Automation**:
   - Automated daily pipeline execution using Azure Data Factory, ensuring continuous data refresh.

---

## 💻 **Technology Stack**

| Technology              | Description                                                  |
|-------------------------|--------------------------------------------------------------|
| **Azure Data Factory**   | Orchestrates data ingestion and movement across services     |
| **Azure Databricks**     | Transforms data with Apache Spark-based processing           |
| **Azure Synapse**        | Handles data warehousing and querying                        |
| **Azure Data Lake (ADLS)**| Stores raw, cleaned, and aggregated data (Bronze, Silver, Gold) |
| **Azure Key Vault**      | Manages secrets and credentials securely                     |
| **SQL Server (On-Prem)** | Source of customer and sales data                            |

---

## 📂 **Project Structure**

```
📦 Azure-End-to-End-Data-Engineering
 ┣ 📂 notebooks
 ┃ ┣ 📜 storagemount.ipynb                  # Mounts data lake storage
 ┃ ┣ 📜 bronze_to_silver.ipynb              # Transforms data from Bronze to Silver
 ┃ ┗ 📜 silver_to_gold.ipynb                # Transforms data from Silver to Gold
 ┣ 📜 README.md                             # Project readme file
 ┗ 📜 Business_Req.docx                     # Business requirements for the project
```

---

## 🚀 **Setup Instructions**

### **Prerequisites**
- An **Azure account** with sufficient credits.
- Access to **on-premises SQL Server** for data extraction.
- Installed tools: **Azure CLI**, **Azure Databricks**, **Azure Synapse**, **SQL Server Management Studio (SSMS)**.

### **Steps to Run the Project**

1. **Azure Environment Setup**:
   - Create a **Resource Group** and provision the following services:
     - **Azure Data Factory**
     - **Azure Data Lake Storage (ADLS)**
     - **Azure Databricks**
     - **Azure Synapse Analytics**
     - **Azure Key Vault** (for secret management)

2. **Data Ingestion**:
   - Use Azure Data Factory to create a pipeline that ingests data from the on-premises SQL database into the **Bronze** layer of ADLS.

3. **Data Transformation**:
   - Mount the ADLS storage in Databricks and execute the **notebooks** to transform the data from Bronze to Silver and Silver to Gold.
   
4. **Data Loading & Querying**:
   - Load the transformed data into Azure Synapse Analytics for further analysis and querying.

5. **Automation**:
   - Set up **scheduled triggers** in Data Factory to run the pipelines daily and update the datasets automatically.

---

## 🎯 **Key Features**
- **Automated Data Pipeline**: Runs daily for continuous data refresh.
- **Bronze-Silver-Gold Architecture**: Ensures optimized data storage and processing.
- **Secure & Scalable**: Managed access with **Azure Key Vault** and **Azure Active Directory** (Entra ID).
- **High-Performance Querying**: Integrated with **Azure Synapse Analytics** for fast data access and reporting.

---

## 📈 **Results**

The project delivers an efficient, automated solution for understanding customer demographics and analyzing sales trends. The optimized pipeline ensures real-time data processing, improving decision-making for over **200+ stakeholders**.

---

## 🔒 **Security & Governance**
- **Role-Based Access Control (RBAC)** is managed through **Azure Active Directory**.
- **Secrets** (e.g., database credentials) are securely stored and accessed via **Azure Key Vault**.


