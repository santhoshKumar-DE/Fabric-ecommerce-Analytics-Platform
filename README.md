# 🚀 Fabric E-Commerce Customer Analytics Platform

End-to-end Data Engineering solution built on Microsoft Fabric using Medallion Architecture.

---

## 📌 Project Highlights

- Built an end-to-end Data Engineering platform using Microsoft Fabric
- Implemented batch + streaming pipelines
- Designed CDC and incremental data processing
- Integrated NoSQL (MongoDB) with analytics pipeline
- Applied Spark optimization (skew handling, salting, repartition, coalesce, OOM mitigation)
- Used Delta Lake features (ACID, Time Travel, VACUUM, file compaction)
- Implemented governance (RLS, semantic model)

---

## 📌 Project Overview

This project demonstrates an end-to-end Data Engineering solution built on **Microsoft Fabric** using Medallion Architecture (Bronze, Silver, Gold).

It covers real-world scenarios including batch processing, streaming pipelines, CDC, incremental loading, NoSQL integration, and performance optimization.

Multiple Lakehouses were used to simulate environment isolation (Bronze/Silver/Gold separation).

KQL was used for real-time query exploration and monitoring scenarios.

CI/CD pipeline implemented using Fabric Deployment Pipelines (Dev → Test → Prod), demonstrating real-world artifact promotion and environment management.

👉 This solution enables scalable, optimized, and real-time analytics for e-commerce business insights.

---

## 🧱 Architecture

The architecture follows Medallion design:

- **Bronze Layer** → Raw ingestion (MongoDB, APIs, files)
- **Silver Layer** → Data cleaning, transformation, flattening
- **Gold Layer** → Aggregated business-ready analytics

---

## 🔧 Technologies Used

- Microsoft Fabric (OneLake, Lakehouse, Notebooks)
- Spark (PySpark)
- Delta Lake
- MongoDB Atlas (NoSQL)
- REST APIs
- AWS S3 (via shortcuts)
- Power BI
- Eventstream (Streaming)
- KQL (Real-time querying)

---

## ⚙️ Key Features

### 🔹 Data Ingestion
- Batch ingestion (CSV, JSON, Parquet)
- REST API ingestion (pagination & retry logic)
- MongoDB NoSQL ingestion
- Streaming ingestion using Eventstream

---

### 🔹 Data Processing
- Medallion Architecture (Bronze, Silver, Gold)
- Data cleaning and transformation
- Flattening nested NoSQL data using `explode()`
- Data validation and schema enforcement

---

### 🔹 Advanced Data Engineering
- CDC (Change Data Capture) using MERGE
- Incremental loads (date + timestamp watermark)
- Streaming pipelines (stream-stream & stream-static join)

---

### 🔹 Performance Optimization
- Data skew simulation
- Salting technique
- Repartitioning
- Coalesce (small file optimization)
- OOM mitigation strategies

---

### 🔹 Delta Lake Features
- ACID transactions
- Time Travel
- VACUUM (file cleanup)
- File compaction

---

### 🔹 Governance & Security
- Row-Level Security (RLS)
- Semantic model
- Secure credential handling (Fabric Variable Library)

---

## 📊 Business Use Cases

- Customer analytics
- Product performance analysis
- Revenue insights
- Order tracking and status analysis

---

## 📁 Project Structure

notebooks/
├── bronze/
├── silver/
├── gold/
├── streaming/
├── optimization/

docs/
├── architecture/

screenshots/

---

## 📌 Key Learnings

- Handling nested NoSQL data for analytics
- Optimizing Spark jobs for performance
- Designing scalable data pipelines
- Implementing real-time and batch processing together

---

## ⚠️ Note

Sensitive information such as credentials and connection strings are not included in this repository and are securely managed using Fabric Variable Library.

---

## ⭐ If you like this project, feel free to star the repository!
