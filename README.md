# Capstone-2-ML-Engineering-Financial-Forecasting-Frontier-Distributed-MLE 1

# 🚀 Banking Data Analytics, Machine Learning & Big Data Projects

A collection of projects demonstrating the use of **Apache Spark, Spark MLlib, Structured Streaming, Hadoop/Hive concepts, and Distributed Machine Learning** for large-scale banking data analysis using the **UCI Bank Marketing Dataset**.

---

## 📌 Project Overview

This repository showcases multiple big data and machine learning implementations focused on banking customer analytics, subscription prediction, real-time processing, and distributed computing.

### Technologies Used

* Apache Spark
* PySpark
* Spark SQL
* Spark MLlib
* Spark Structured Streaming
* Hadoop & Hive Concepts
* Python
* Pandas
* Matplotlib
* Google Colab

---

# 📂 Projects Included

## 1️⃣ Distributed Machine Learning with Apache Spark

### Objective

Demonstrate how Spark's distributed architecture and data parallelism can efficiently process large-scale banking datasets.

### Key Tasks

* Data partitioning using `repartition()`
* Parallel aggregations using `groupBy()`
* Average balance analysis by job category
* Age-group loan distribution analysis
* Logistic Regression model training
* Distributed model evaluation
* Resource monitoring using `psutil`

### Results

* Highest loan holders: Age group **30–39**
* Highest average balances: **Retired** and **Student** clients
* Successful distributed model training using Spark MLlib

---

## 2️⃣ Machine Learning with Spark ML

### Objective

Build a binary classification model to predict term deposit subscriptions.

### Workflow

* Data preprocessing
* Categorical feature encoding
* Feature engineering
* Logistic Regression training
* Cross-validation and hyperparameter tuning

### Model Performance

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 89.17% |
| Precision | 87.07% |
| Recall    | 89.17% |
| F1 Score  | 87.07% |

### Key Insights

* Previous campaign outcome (`poutcome`) is the strongest predictor.
* Housing loan customers are more likely to subscribe.
* Personal loans negatively impact subscriptions.

---

## 3️⃣ Spark Data Processing & Analytics

### Objective

Perform large-scale client behavior analysis using Spark SQL and DataFrame operations.

### Tasks Performed

* Data filtering and transformation
* GroupBy aggregations
* User Defined Functions (UDFs)
* Spark SQL queries
* Correlation analysis
* Data visualization

### Key Findings

* Clients above 60 years have the highest balances.
* Most common profession: Management
* Cellular contact method produced better campaign success rates.
* Credit defaults were extremely rare.

---

## 4️⃣ Real-Time Machine Learning with Spark Streaming

### Objective

Simulate and analyze live banking transactions using Spark Structured Streaming.

### Features

* Real-time data ingestion
* Streaming aggregations
* Real-time prediction pipeline
* Window-based trend analysis
* Watermarking for late-arriving data

### Streaming Analytics

* Average account balance by job
* Transaction duration analysis
* Real-time subscription prediction
* 10-second and 1-minute trend windows

### Benefits

* Handles continuous data streams efficiently
* Supports near real-time business intelligence
* Demonstrates scalable stream processing architecture

---

## 5️⃣ Data Analysis & Management (Hadoop/Hive Concepts)

### Objective

Perform Hive-style analytical queries using Pandas and Python.

### Analysis Performed

* Average balance by job
* Housing loan analysis by education
* Monthly campaign performance
* Subscription trends
* Correlation analysis
* Anomaly detection
* Customer segmentation

### Sample Business Insights

* Top 10 highest-balance clients identified
* Most successful campaign months detected
* Education-level balance anomalies analyzed
* Previous campaign outcomes strongly influenced future subscriptions

---

# 📊 Dataset

### UCI Bank Marketing Dataset

The dataset contains customer information collected during direct marketing campaigns.

### Key Features

| Feature   | Description                 |
| --------- | --------------------------- |
| age       | Client age                  |
| job       | Occupation                  |
| marital   | Marital status              |
| education | Education level             |
| balance   | Account balance             |
| housing   | Housing loan status         |
| loan      | Personal loan status        |
| contact   | Communication type          |
| duration  | Last contact duration       |
| campaign  | Number of contacts          |
| pdays     | Days since previous contact |
| poutcome  | Previous campaign outcome   |
| y         | Term deposit subscription   |

---

# 📈 Learning Outcomes

Through these projects, the following concepts were implemented:

* Distributed Data Processing
* Data Parallelism
* Spark SQL
* Machine Learning Pipelines
* Feature Engineering
* Hyperparameter Tuning
* Structured Streaming
* Window Operations
* Watermarking
* Hadoop & Hive Analytics
* Real-Time Data Processing
* Resource Monitoring

---

# ▶️ How to Run

### Install Dependencies

```bash
pip install pyspark pandas matplotlib scikit-learn psutil
```

### Start Spark Session

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Banking Analytics") \
    .getOrCreate()
```

### Load Dataset

```python
df = spark.read.csv("bank.csv", header=True, inferSchema=True)
df.show()
```

---

# 📁 Repository Structure

```text
├── Distributed-Machine-Learning/
├── Spark-ML/
├── Spark-Data-Processing/
├── Spark-Streaming/
├── Hadoop-Hive-Analytics/
├── bank.csv
├── README.md
```

---

# 🎯 Conclusion

This repository demonstrates how modern big data technologies such as Apache Spark, Spark MLlib, Structured Streaming, and Hadoop-inspired analytics can be applied to solve real-world banking problems. The projects showcase scalable data processing, predictive modeling, real-time analytics, and business intelligence workflows that can be extended to enterprise-level financial applications.
