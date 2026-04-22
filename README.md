# 🚀 Fabric E-Commerce Customer Analytics Platform

## 📌 Project Overview
This project demonstrates an end-to-end **Data Engineering pipeline** built using **Microsoft Fabric**.  
It simulates a real-world e-commerce analytics platform that ingests, processes, and transforms data into business-ready insights using a **Lakehouse + Medallion Architecture (Bronze → Silver → Gold)**.

The project emphasizes **scalability, performance optimization, and real-world debugging scenarios**.

---

## 🧠 Business Problem
E-commerce businesses require insights such as:
- Customer distribution across regions
- Revenue contribution by category
- Customer lifecycle trends
- Real-time order monitoring

Raw data from multiple sources is not analytics-ready.

👉 This project solves that by building a structured pipeline:
**Raw Data → Clean Data → Business Insights**

---

## 🏗 Architecture Overview

### Data Sources
- CSV / JSON / Parquet files
- MongoDB (NoSQL ingestion)
- AWS S3 (external source)
- Streaming event data (order events)

### Processing
- Microsoft Fabric (Spark Engine)
- PySpark transformations

### Storage
- OneLake (Delta Lake format)

### Serving Layer
- Semantic Model
- Power BI Report

---

## 🔄 Data Flow (Medallion Architecture)

### 🥉 Bronze Layer (Raw Ingestion)
- Ingested data from multiple sources
- Stored as Delta tables
- No transformations applied

---

### 🥈 Silver Layer (Data Cleaning & Standardization)
Applied real-world transformations:
- Trim & lowercase normalization
- Regex cleaning
- Null handling using `coalesce`
- Phone masking
- Email domain extraction
- Deduplication
- Type casting
- Data quality validation

---

### 🥇 Gold Layer (Business Aggregation)
Built curated business KPI tables.

Example:

gold_customer_summary

country
total_customers
first_customer_date
latest_customer_date


---

## ⚡ Advanced Data Engineering Features

### 🔁 Change Data Capture (CDC)
- Implemented using MERGE
- Supports incremental updates and inserts

### ⏱ Incremental Processing
- Date-based watermark
- Timestamp-based watermark (handles multiple loads/day)

### 🔄 Streaming Ingestion
- File-based streaming simulation
- Micro-batch processing
- Schema validation

---

## ⚙️ Spark Optimization & Internals

### 🔥 Data Skew Handling
- Simulated skewed data
- Implemented **salting technique**
- Improved partition balance

### 🔀 Shuffle Optimization
- Observed Spark DAG (Stages, Tasks)
- Reduced shuffle impact

### ⚡ Join Optimization
- Broadcast joins
- Sort-merge joins
- Partition tuning

---

## 🧱 Delta Lake Features

- ACID Transactions
- Time Travel (version history)
- Schema enforcement
- VACUUM (file cleanup)

---

## 🔁 CI/CD Pipeline (Fabric Deployment Pipeline)

Environment setup:
- Dev → Test → Prod

Features:
- Automated deployment
- Environment isolation
- Version control flow

---

## 📡 Monitoring & Logging

- Custom pipeline logging table
- Tracks:
  - Pipeline name
  - Run timestamps
  - Status
  - Row counts
  - Watermark

---

## 📊 KQL Monitoring (Real-Time)

- Eventhouse created for monitoring
- KQL queries for real-time analytics
- Order event tracking

---

## 📊 Power BI Reporting

Built report on top of semantic model.

### Example Insight:
Customer distribution by country:

- US → 25
- IN → 18
- UK → 12
- AU → 10
- DE → 8

---

## 🧩 Semantic Model (Star Schema)

- Gold table exposed as semantic model
- Measures created:
  - Total Customers
- Used for reporting layer

---

## 📸 Project Screenshots

Include the following:
- Lakehouse tables view
- Notebook transformations
- CI/CD pipeline (Dev → Test → Prod)
- Streaming ingestion
- MongoDB ingestion
- Semantic model view
- Power BI report output

---

## 🚀 How to Run

1. Create Microsoft Fabric workspace  
2. Create Lakehouse (OneLake)  
3. Upload datasets  
4. Run notebooks in sequence:
   - Bronze → Silver → Gold  
5. Create semantic model  
6. Build Power BI report  

---

## ⚠️ Challenges Faced

- Handling data skew in joins
- Delta schema enforcement errors
- Managing incremental loads
- Understanding Spark execution (DAG, stages)
- CI/CD workspace configuration issues

---

## 🎯 Key Learnings

- Spark internals (DAG, shuffle, joins)
- Data pipeline design (Medallion architecture)
- Performance tuning techniques
- Delta Lake fundamentals
- Fabric ecosystem usage
- Real-world debugging scenarios

---

## 🎤 Interview Talking Points

- Medallion Architecture explanation
- Data skew problem & solution (salting)
- Batch vs Streaming processing
- Incremental vs Full load
- Spark execution flow (DAG → stages → tasks)
- Delta Lake advantages
- CI/CD implementation
- Real-world troubleshooting

---

## ⭐ Why This Project Stands Out

- End-to-end Data Engineering pipeline
- Real-world problem simulation
- Includes optimization techniques
- Combines batch + streaming processing
- Multi-source ingestion (Files, MongoDB, S3)
- Built on modern Fabric ecosystem

---

## 👤 Author

Santhosh Kumar  
Data Engineer | Microsoft Fabric | Spark | Azure

## ⭐ If you like this project, feel free to star the repository!


