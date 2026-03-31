# 🌾 Climate Impact on Crop Availability – Automated ETL Pipeline

## 📌 Overview

This project builds a fully automated **ETL (Extract, Transform, Load) pipeline** to analyze how weather conditions affect crop availability across selected regions in Nigeria.

The system extracts historical weather data and combines it with crop yield data to uncover patterns between **climate variables (temperature & rainfall)** and **agricultural productivity**.

---

## 🎯 Objective

To determine how weather conditions influence crop yield and availability using a reproducible, automated data pipeline.

---

## 🧠 Key Features

* ✅ Modular ETL pipeline (Extract → Transform → Load)
* ✅ Automated weekly execution (Windows Task Scheduler)
* ✅ Incremental data loading (append, not overwrite)
* ✅ Data cleaning & validation
* ✅ SQLite database storage
* ✅ Logging system for monitoring
* ✅ Exploratory data analysis & visualization
* ✅ Machine learning prediction model
* ✅ Streamlit dashboard for interactive insights

---

## 📥 Data Sources

### 🌦️ Weather Data

* Source: Open-Meteo Historical API
* Endpoint: https://archive-api.open-meteo.com/v1/archive

**Features:**

* time
* temperature
* precipitation
* region
* year

---

### 🌾 Crop Data

* Source: Synthetic dataset (generated programmatically)

**Features:**

* date
* region
* crop (Maize, Rice, Sorghum)
* yield
* year

---

## 🧱 Data Schema

### Crop Dataset

| Column | Description      |
| ------ | ---------------- |
| date   | Observation date |
| region | Nigerian state   |
| crop   | Crop type        |
| yield  | Daily yield      |
| year   | Year             |

### Weather Dataset

| Column        | Description         |
| ------------- | ------------------- |
| time          | Observation date    |
| temperature   | Average temperature |
| precipitation | Rainfall            |
| region        | Nigerian state      |
| year          | Year                |

---

## 🔄 Pipeline Architecture

Crop Data + Weather Data
→ Extract
→ Clean
→ Merge
→ Store (CSV + SQLite)
→ Weekly Automation

---

## ⚙️ How to Run

```bash
pip install -r requirements.txt
python pipeline/main.py
```

---

## ⏱️ Automation

* Configured using Windows Task Scheduler
* Runs weekly
* Automatically appends new data

---

## 📊 Sample Output

```
PIPELINE EXECUTION SUMMARY
Completion Timestamp: 2026-03-31T06:18:53
Weather rows: 24
Crop rows: 72
Merged rows: 72
Database: agritech.db
Status: SUCCESS
```

---

## 📈 Analysis & Insights

Key questions explored:

* How does rainfall affect crop yield?
* Which regions are most climate-sensitive?
* Which crop is most resilient?

---

## 🤖 Machine Learning

A regression model is used to predict crop yield based on:

* Temperature
* Precipitation

---

## 📊 Dashboard

An interactive Streamlit dashboard allows users to:

* Visualize trends
* Compare regions
* Explore climate impact on crops

---

## ⚠️ Limitations

* Crop data is synthetic due to limited public datasets
* Weather data depends on API availability

---

## 🚀 Future Improvements

* Deploy to cloud (AWS/GCP)
* Add real agricultural datasets
* Build API service
* Improve ML models

---

## 🏆 Competition Value

This project combines:

* Data Engineering
* Data Analysis
* Automation
* Machine Learning

to solve a real-world agricultural problem.

---

## 👨‍💻 Author

Your Name
