# 🚀 Fabric E-Commerce Customer Analytics Platform

End-to-end **Data Engineering solution** built on **Microsoft Fabric** using Medallion Architecture (Bronze → Silver → Gold).

---

## 📌 Project Highlights

- Built a full **enterprise-grade Data Engineering pipeline**
- Implemented **batch + streaming ingestion**
- Designed **CDC and incremental data processing**
- Integrated **MongoDB (NoSQL) with analytics pipeline**
- Applied **Spark optimization (skew handling, salting, repartition, coalesce, OOM mitigation)**
- Used **Delta Lake features (ACID, Time Travel, VACUUM, compaction)**
- Implemented **CI/CD pipeline (Dev → Test → Prod)**
- Added **monitoring & logging framework**
- Built **real-time analytics using KQL**

---

## 📌 Project Overview

This project demonstrates a **real-world Data Engineering system** using Microsoft Fabric.

It covers:
- Batch + Streaming pipelines
- CDC & incremental loads
- Multi-source ingestion (API, MongoDB, files)
- Performance optimization
- CI/CD deployment
- Real-time monitoring

👉 Designed to simulate **enterprise-level data platform architecture**

---

## 🏗️ Architecture

Sources (API, MongoDB, Streaming)
↓
Bronze Layer (Raw - Delta)
↓
Silver Layer (Cleaned & Transformed)
↓
Gold Layer (Business KPIs)
↓
Analytics / Monitoring (KQL / Power BI)

---

## 🔁 CI/CD Pipeline (Dev → Test → Prod)

![CI/CD Pipeline](docs/screenshots/cicd_pipeline.png)

- Fabric Deployment Pipeline used
- Promotes artifacts across environments
- Ensures production stability

---

## 🥉 Bronze Layer (Raw Ingestion)

✔ Ingested data from:
- REST API (pagination + retry)
- MongoDB Atlas (NoSQL)
- Streaming events (JSON)

✔ Stored as **Delta tables**

---

## 🧼 Silver Layer (Transformation & Cleaning)

![Silver Transformation](docs/screenshots/silver_transformation.png)

✔ Implemented:
- Null handling (`coalesce`)
- Column standardization
- Type casting
- Deduplication
- Data quality checks

✔ Flattened nested NoSQL data using `explode()`

---

## 🥇 Gold Layer (Business Analytics)

![Gold Analytics](docs/screenshots/gold_analytics.png)

✔ Built KPI tables:
- Category-level sales
- Revenue contribution
- Product performance insights

✔ Used:
- Fact + Dimension joins
- Aggregations
- Business logic

---

## ⚡ Streaming Pipeline

![Streaming Pipeline](docs/screenshots/streaming_pipeline.png)

✔ Implemented:
- Structured Streaming
- Schema enforcement
- File-based ingestion

✔ Supports:
- Stream-static join
- Stream processing

---

## 🔗 MongoDB Integration

![MongoDB Integration](docs/screenshots/mongodb_read.png)

✔ Connected to MongoDB Atlas  
✔ Extracted real-time data into Bronze layer  

---

## 📊 Lakehouse (Medallion Architecture)

![Lakehouse Tables](docs/screenshots/lakehouse_tables.png)

✔ Organized into:
- Bronze
- Silver
- Gold

✔ Stored using Delta Lake

---

## ⚙️ Spark Optimization (Advanced)

![Spark Optimization](docs/screenshots/spark_optimization.png)

✔ Implemented:
- Data skew simulation
- Salting technique
- Repartition & coalesce
- Shuffle optimization
- OOM mitigation

---

## 📈 Monitoring & Logging

![Monitoring Logs](docs/screenshots/monitoring_logs.png)

✔ Created pipeline logging table:
- Run ID
- Status
- Rows processed
- Execution time
- Watermark tracking

---

## ⚡ Real-Time Monitoring (KQL)

![KQL Monitoring](docs/screenshots/kql_monitoring.png)

✔ Built monitoring using:
- Eventhouse
- KQL Queries

✔ Enables:
- Real-time insights
- Operational monitoring

---

## 🔄 Incremental Processing

✔ Implemented:
- Date-based watermark
- Timestamp-based incremental loads

✔ Ensures:
- Efficient processing
- No duplicate ingestion

---

## 🔧 Technologies Used

- Microsoft Fabric (OneLake, Lakehouse, Notebooks)
- Spark (PySpark)
- Delta Lake
- MongoDB Atlas
- REST APIs
- AWS S3 (Shortcuts)
- KQL (Real-time analytics)
- Eventstream (Streaming)

---

## 📊 Business Use Cases

- Customer analytics
- Product performance analysis
- Revenue insights
- Order monitoring

---

## 📁 Project Structure

notebooks/
bronze/
silver/
gold/
streaming/
optimization/

docs/
screenshots/

README.md

---

## 🧠 Key Learnings

- Spark internals (DAG, shuffle, stages)
- Data skew handling & optimization
- Delta Lake (ACID, Time Travel)
- Streaming vs Batch processing
- CI/CD in Data Engineering
- Real-time analytics using KQL

---

## ⚠️ Note

Sensitive information (credentials, connection strings) is not included and is managed securely using Fabric Variable Library.

---

## 💼 Why This Project Matters

This project simulates **real enterprise Data Engineering workflows**:

✔ Multi-source ingestion  
✔ Performance optimization  
✔ CI/CD deployment  
✔ Monitoring & observability  
✔ Real-time + batch architecture  

---

## ⭐ If you like this project, feel free to star the repository!
