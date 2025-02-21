# Azure_Data-Analysis
**Employee Retention Analysis using Azure & Databricks**

                                                                                      **Project Overview**

This project analyzes employee retention using a dataset containing various factors influencing whether an employee stays or leaves a company. The goal is to process and analyze the data using Azure Storage, Azure Data Factory, and Azure Databricks, and to showcase best practices for data pipeline creation and analysis in the cloud.

Dataset Description

The dataset consists of employee records with key attributes related to job satisfaction, performance, and organizational factors. The main objective is to identify trends and insights into why employees leave the company.
## Dataset Variables

| Variable Name             | Type       | Description |
|---------------------------|------------|-------------|
| **left**                 | Nominal    | 0 = Stayed, 1 = Left the company |
| **promotion_last_5years** | Nominal    | 0 = Not promoted, 1 = Promoted |
| **department**            | Nominal    | Various (Sales, HR, IT, Technical, etc.) |
| **work_accident**         | Nominal    | 0 = No accident, 1 = Had an accident |
| **salary**               | Ordinal    | 1 = Low, 2 = Medium, 3 = High |
| **number_project**        | Ordinal    | 2, 3, 4, 5, 6, 7 |
| **satisfaction_level**    | Continuous | Range [0.0 - 1.0], higher values suggest more satisfied |
| **last_evaluation**       | Continuous | Range [0.0 - 1.0], higher values suggest better performance evaluation |
| **average_monthly_hours** | Continuous | 96 to 310 hours |
| **time_spend_company**    | Continuous | 2 to 10 years |

A detailed description of the variables is available in HR_Data-Definitions.pdf.

**Project Workflow**

1. Data Storage in Azure
	•	The dataset is stored in Azure Data Lake Storage (ADLS), inside a “source” container.

2. Data Ingestion with Azure Data Factory (ADF)
	•	An ADF pipeline is created to move data from the source container to the sink container after processing.
	•	A Copy Activity in ADF facilitates the data transfer.

3. Data Processing in Azure Databricks
	•	Data is loaded from Azure Storage into Azure Databricks (Spark environment).
	•	Exploratory Data Analysis (EDA) is performed to visualize and understand key trends.
	•	Data cleaning and transformation are conducted using PySpark.
	•	Potential insights include:
	•	Correlation between satisfaction levels and retention.
	•	Impact of workload (monthly hours, number of projects) on attrition.
	•	Influence of promotions and salary levels on retention rates.

4. Output Storage & GitHub Integration
	•	Processed data is saved back to Azure Data Lake (“sink” container).
	•	Python notebooks, transformation scripts, and analysis results are stored in this GitHub repository for tracking and sharing.

Technologies Used
	•	Azure Storage Account (for Data Lake Storage)
	•	Azure Data Factory (ADF) (for data movement and pipeline creation)
	•	Azure Databricks (for Spark-based data processing and analysis)
	•	GitHub (for version control and project tracking)
