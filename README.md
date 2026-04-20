
# 🛒 Retail Sales Analytics & Demand Forecasting

## 📌 Project Overview

This project performs an end-to-end **retail analytics pipeline** on multi-source sales data to extract insights, segment stores, analyze promotions, and build predictive demand forecasting models.

The goal is to understand **what drives weekly sales**, identify **customer/store behavior patterns**, and generate **data-driven business recommendations**.

---

## 📊 Datasets Used

The project integrates three datasets:

* **Sales Data**: Weekly sales by store and department
* **Features Data**: Economic and promotional variables (CPI, unemployment, fuel price, markdowns, holidays)
* **Stores Data**: Store type and size information

---

## 🎯 Objectives

* Clean and preprocess retail datasets
* Handle missing values (especially promotional markdowns)
* Engineer meaningful features for prediction
* Perform exploratory data analysis (EDA)
* Conduct statistical hypothesis testing
* Segment stores/departments using clustering
* Perform market basket analysis
* Build demand forecasting models
* Generate strategic business insights

---

## 🧹 Data Preprocessing

* Merged multiple datasets into a unified analytical table
* Converted date features into time-based components
* Handled missing values:

  * Markdown variables → filled with 0
  * Economic indicators → forward fill
* Encoded categorical variables (Store Type, Size categories)

---

## 🛠 Feature Engineering

Key engineered features:

* Time features: Week, Month, Quarter, Year
* Store segmentation: Small / Medium / Large
* Promotion intensity: Total Markdown, PromoActive
* Economic stress index: Unemployment × Fuel Price
* Holiday indicator impact

---

## 📈 Exploratory Data Analysis (EDA)

Key insights explored:

* Sales trends over time
* Seasonal patterns (weekly/monthly)
* Holiday vs non-holiday performance
* Store size vs sales relationship
* Impact of promotions on revenue
* Economic indicators vs sales behavior

Visualizations include:

* Line charts (trend analysis)
* Scatter plots (correlation patterns)
* Bar charts (group comparisons)

---

## 🧪 Statistical Analysis

Hypothesis testing performed:

### 1. T-Test

* Holiday vs Non-Holiday sales
* Promotion vs No Promotion sales

### 2. ANOVA

* Sales across store types
* Sales across store sizes

📌 Key outcome:

* Promotions and holidays significantly impact sales
* Store structure influences performance distribution

---

## 👥 Customer Segmentation

Since customer-level data is unavailable, segmentation is done at:

* Store-Department level

Method:

* K-Means clustering

Features used:

* Average sales
* Markdown exposure
* Economic conditions (CPI, unemployment)

Segments identified:

* High-performing promotional stores
* Economically sensitive stores
* Stable demand stores

---

## 🧺 Market Basket Analysis

Approach:

* Transactions approximated using Store-Dept combinations
* Apriori algorithm applied

Output:

* Frequent itemsets
* Association rules using lift metric

Use case:

* Cross-selling strategies
* Product bundling opportunities

---

## 📉 Demand Forecasting

Models used:

* Random Forest Regressor (baseline ML model)
* Feature-based regression using:

  * Promotions
  * Economic indicators
  * Store attributes
  * Time features

Evaluation metrics:

* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)

---

## 🔍 Key Insights

* 📌 Store size strongly correlates with sales volume
* 📌 Promotions significantly increase revenue
* 📌 Holidays create predictable demand spikes
* 📌 Economic stress reduces purchasing behavior
* 📌 Certain departments consistently outperform others

---

## 💡 Business Recommendations

### 1. Promotion Strategy

* Increase markdown activity during peak seasonal periods
* Target underperforming stores with strategic discounts

### 2. Inventory Optimization

* Stock high-performing departments aggressively
* Reduce overstock in low-demand segments

### 3. Store Strategy

* Expand or invest in large-format stores
* Customize strategies per store cluster

### 4. Economic Sensitivity

* Adjust pricing in high unemployment regions
* Monitor fuel price fluctuations for demand planning

### 5. Forecasting Usage

* Use predictive models for weekly planning
* Align staffing and inventory with demand forecasts

### 6. Cross-Selling Strategy

* Bundle frequently co-purchased departments
* Optimize product placement in stores

---

## 📁 Project Structure

```
Retail-Analytics/
│
├── data/
│   ├── sales.csv
│   ├── features.csv
│   ├── stores.csv
│
├── notebooks/
│   └── retail_analysis.ipynb
│
├── outputs/
│   ├── segmentation_results.csv
│   ├── market_basket_rules.csv
│
├── README.md
└── requirements.txt
```

---

## ⚙️ Requirements

```bash
pandas
numpy
matplotlib
scikit-learn
mlxtend
scipy
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run

1. Clone repository:

```bash
git clone https://github.com/your-username/retail-analytics.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run notebook:

```bash
jupyter notebook
```

---

## 📌 Conclusion

This project demonstrates a complete **data science pipeline for retail analytics**, including:

* Data engineering
* Statistical analysis
* Machine learning
* Market basket analysis
* Business strategy formulation

It provides actionable insights for improving **sales performance, promotions, and inventory planning**.

---

## 📈 Future Improvements

* Implement LSTM / Prophet for advanced forecasting
* Build interactive dashboard (Power BI / Tableau)
* Add geospatial store performance analysis
* Integrate real-time demand prediction system

---

⭐ If you found this project useful, consider starring the repository!

