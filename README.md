# ✈️ Flight Booking Data Pipeline with Airflow & CI/CD
[![GitHub Repo](https://img.shields.io/badge/GitHub-Repository-blue?logo=github)](https://github.com/Somanshu693/Flight-Booking-Data-Pipeline-with-Airflow-CICD)
[![Flight Booking CICD](https://github.com/Somanshu693/Flight-Booking-Data-Pipeline-with-Airflow-CICD/actions/workflows/ci-cd.yaml/badge.svg)](https://github.com/Somanshu693/Flight-Booking-Data-Pipeline-with-Airflow-CICD/actions/workflows/ci-cd.yaml)

An end-to-end **data pipeline project** simulating a real-world industrial use case. It uses **Apache Airflow** for workflow orchestration, runs **PySpark** jobs on **Google Cloud Dataproc Serverless** for data processing, and loads the results into **BigQuery** for analytics. Automated deployments across dev/prod environments are managed through **GitHub Actions CI/CD**.

---

## 🚀 Workflow Overview
![Flight Booking Data Pipeline with Airflow   CICD (1)](https://github.com/user-attachments/assets/85e642bf-de0c-407b-8e5a-2a684a4b69a8)

---

## 🧱 Folder Structure
```
├── .github/
|  ├── workflows/
|      ├── ci-cd.yaml                         # GitHub Actions CI/CD pipeline
├── airflow_job/
|      ├── airflow_job.py                     # Airflow DAG definition
├── spark_job/
|      ├── spark_transformation_job.py        # PySpark transformation script
├── variables/
|      ├── dev/
|        ├── variables.json                   # Dev environment variables
|      ├── prod/
|        ├── variables.json                   # Prod environment variables
├── flight_booking.csv                        # Sample flight booking dataset
├── README.md                                 # Project documentation
```

---

## ⚙️ Tech Stack
| Component       | Tool/Service         |
| --------------- | -------------------- |
| Data Processing | PySpark              |
| Orchestration   | Apache Airflow       |
| Infrastructure  | Google Cloud Storage |
| Compute Engine  | Dataproc Serverless  |
| Data Warehouse  | Google BigQuery      |
| CI/CD           | GitHub Actions       |
| Version Control | Git & GitHub         |

---

## 🔍 Execution Logic
- **Trigger DAG:** Airflow DAG is manually or automatically triggered.
- **Run PySpark job:** Job is submitted to Dataproc Serverless with input from GCS.
- **Transform data:** PySpark cleans, aggregates, and structures booking data.
- **Store results:** Output is loaded into specific BigQuery tables.
- **CI/CD pipeline:**
   - On push/merge to main or prod, GitHub Actions:
     - Validates code
     - Deploys DAG and PySpark jobs to respective environments

---

## 🌟 Key Features
- **Data Ingestion:** Load raw flight booking files from Google Cloud Storage.  
- **Data Transformation:** Process and clean data using PySpark on Dataproc Serverless.  
- **Orchestration:** Manage and schedule ETL tasks with Apache Airflow.  
- **Data Loading:** Write processed data into BigQuery tables for analytics.  
- **CI/CD Deployment:** Automated testing and deployment via GitHub Actions.  
- **Monitoring & Logging:** Track pipeline runs and logs in Airflow UI and cloud logs.

---

## 📈 Business Use Case
- This data pipeline can be used by **airlines, travel agencies, or booking platforms** to manage and analyze flight reservation data.
- **Processes daily booking data** and loads it into BigQuery for centralized analytics.
- Enables **business analysts** to:
  - Track booking trends over time
  - Analyze seat utilization rates
  - Monitor revenue patterns
- Automated **CI/CD deployment** ensures:
  - Faster updates to pipeline logic
  - Reliable, scalable data infrastructure

---
