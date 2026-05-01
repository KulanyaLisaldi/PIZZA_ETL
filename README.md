# 🍕 Pizza Sales Data Warehouse & ETL Pipeline

## 📌 Project Overview

This project focuses on the design and implementation of a Data Warehouse for pizza sales transactions using an ETL pipeline.

The solution extracts data from flat CSV files, processes it through a staging layer, and loads it into a structured star schema to support analytical processing and business intelligence reporting.

---

## 🎯 Objectives

* Design a data warehouse architecture
* Implement ETL pipelines using SSIS
* Transform raw transactional data into analytical data
* Support business intelligence and reporting

---

## 📂 Dataset

* **Source:** Kaggle (PIZZA Sales Restaurant Dataset)
* **Records:** ~48,000 transactions
* **Type:** OLTP dataset (transaction-level data)

---

## 🏗️ System Architecture

The solution follows a **3-layer architecture**:

### 🔹 Source Layer

* CSV files (pizza orders, order details, completion data)

### 🔹 Staging Layer (Staging_DB)

* Stores raw data
* Performs data cleaning and validation
* Handles duplicates and missing values

### 🔹 Data Warehouse Layer (Pizza_DW)

* Star schema design
* Optimized for analytical queries

---

## ⭐ Data Warehouse Design

### 🔸 Fact Table

**Fact_Pizza_Sales**

* Stores transactional sales data
* Includes:

  * Quantity
  * Total Price
  * Order ID

### 🔸 Dimension Tables

* **Dim_Customer**
* **Dim_Pizza**
* **Dim_Date**
* **Dim_Time**

---

## 🔄 ETL Process

### 📦 Package 1: Staging Load

* Load CSV data into staging tables
* Perform data cleaning and validation

### 📦 Package 2: Data Warehouse Load

* Populate dimension tables
* Load fact table using surrogate keys

### 📦 Package 3: Accumulating Fact Update

* Updates order processing details
* Tracks order lifecycle

---

## 🔁 ETL Execution Order

1. Load Staging Data
2. Load Dim_Date
3. Load Dim_Time
4. Load Dim_Customer
5. Load Dim_Pizza
6. Load Fact Table

---

## 🧠 Key Concepts Used

* Data Warehousing
* Star Schema
* ETL (Extract, Transform, Load)
* SSIS Packages
* Slowly Changing Dimensions (SCD)
* Accumulating Fact Table

---

## 🛠️ Technologies Used

* Microsoft SQL Server
* SQL Server Integration Services (SSIS)
* Visual Studio
* CSV Data Sources

---

## 📊 Features

* Handles transactional sales data
* Supports analytical queries
* Tracks order lifecycle
* Ensures data consistency and accuracy

---

## ⚠️ Assumptions

* Order IDs are unique
* Source data is consistent
* Minimal missing values
* Dimension data is relatively stable

---

## ✅ Conclusion

This project demonstrates a complete end-to-end Data Warehouse solution, including data extraction, transformation, loading, and analytical modeling for pizza sales data.

---

## 👩‍💻 Author

Kulanya Lisaldi

SLIIT – Data Warehousing & Business Intelligence
