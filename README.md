# NYC Taxi Tip Prediction and Insight 🚖💰

This project analyzes New York City taxi trip data to extract insights, uncover travel patterns, and build a predictive model for tipping behavior. It combines large-scale data cleaning, analytical querying, and machine learning using Pandas and Scikit-learn in a Spark-like DataFrame workflow.

---

## 📊 Project Overview

This project was completed as part of a Big Data course and is structured into three key phases:

### ✅ Phase 1: Data Cleaning & Feature Engineering
- Cleaned missing, zero, and anomalous values from `trip_data.csv`
- Dropped duplicates and unrealistic records (e.g., 24-hour trips)
- Created:
  - `trip_duration_minutes`
  - `total_trip_cost` (sum of fare, extras, tax, tips, and tolls)
- Enriched data using `taxi_zone_geo.csv` to include pickup/dropoff boroughs and zones

---

### ✅ Phase 2: Analytical Queries
Executed key data queries to explore trip and revenue patterns:
- **Most common payment method per time of day**
- **Top boroughs by revenue and trip count**
- **Average tip per passenger count**
- **Best pickup zones and times for drivers**
- **Longest valid trips with fare/tip analysis**
- **Most frequent inter-borough travel routes**

---

### ✅ Phase 3: Machine Learning – Tip Prediction
- Created binary label `high_tip` for trips with tips >15% of fare
- Selected key features: `trip_distance`, `duration`, `fare_amount`, etc.
- Trained and compared:
  - Logistic Regression
  - Decision Tree
  - ✅ Random Forest (chosen final model: 54% accuracy, 0.62 F1-score)
- Extracted and visualized **feature importance**
  - `trip_distance` was the strongest predictor of high tips

---

## 🧰 Tech Stack

- Python (Pandas, Scikit-learn, NumPy)
- Jupyter/Colab Notebook
- Spark-like DataFrame logic (without full Spark cluster)
- Matplotlib/Seaborn (optional for visualization)

---

## 📁 Files

- `Big_Data_Project.ipynb` – main notebook with all phases
- `trip_data.csv` – taxi trip records
- `taxi_zone_geo.csv` – zone-to-borough mapping

---

## 📝 Author

This project was developed by Adham Hisham, as part of coursework in Big Data Analytics.

---

## 📌 Note

This is an educational project built using Spark-like logic in Pandas. The dataset used is a subset/sample of real NYC Taxi data.
