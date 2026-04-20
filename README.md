# 🚀 Fabric E-Commerce Customer Analytics Platform

## 📌 Project Overview
This project demonstrates an end-to-end Data Engineering solution built on **Microsoft Fabric** using Medallion Architecture (Bronze, Silver, Gold).

It covers real-world scenarios including batch processing, streaming pipelines, CDC, incremental loading, NoSQL integration, and performance optimization.

---

## 🧱 Architecture

## 🔧 Technologies Used

- Microsoft Fabric (OneLake, Lakehouse, Notebooks)
- Spark (PySpark)
- Delta Lake
- MongoDB Atlas (NoSQL)
- REST APIs
- AWS S3 (via shortcuts)
- Power BI
- Eventstream (Streaming)

---

## ⚙️ Key Features

### 🔹 Data Ingestion
- Batch ingestion (CSV, JSON, Parquet)
- REST API ingestion (with pagination & retry)
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

---

### 🔹 Delta Lake Features
- ACID transactions
- Time Travel
- VACUUM (file cleanup)

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
└── gold/

docs/
architecture/
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

