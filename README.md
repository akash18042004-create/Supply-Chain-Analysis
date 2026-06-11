# 🚚 Supply Chain Performance Analysis & Late Delivery Risk Prediction

## 📌 Project Overview

This project analyzes end-to-end supply chain performance using order, shipping, customer, product, and profitability data. The objective is to identify delivery bottlenecks, understand profitability drivers, uncover operational inefficiencies, and build a machine learning model to predict late delivery risk.

The analysis combines **Exploratory Data Analysis (EDA), Business Intelligence, Root Cause Analysis, and Machine Learning** to generate actionable insights for supply chain optimization.

---

## 🎯 Business Problem

Late deliveries negatively impact:

- Customer satisfaction
- Operational efficiency
- Revenue realization
- Supply chain reliability

This project aims to answer:

- What percentage of orders are delivered late?
- Which regions experience the highest delays?
- Which shipping modes contribute most to delays?
- How do delays affect profitability?
- What operational factors drive late deliveries?
- Can we predict late delivery risk before shipment?

---

## 📊 Dataset Information

The dataset contains:

- 180,000+ supply chain transactions
- Customer information
- Product details
- Order information
- Shipping details
- Profitability metrics
- Regional and market data

### Key Variables

| Category | Variables |
|-----------|------------|
| Order | Order ID, Order Status, Order Region |
| Shipping | Shipping Mode, Delivery Status |
| Customer | Customer Segment, Country |
| Product | Category Name, Department Name |
| Financial | Sales, Profit, Discount |
| Time | Order Date, Shipping Date |

---

## 🧹 Data Cleaning & Preparation

### Data Cleaning Performed

✅ Removed cancelled orders

✅ Converted date columns to datetime format

✅ Handled missing values

✅ Removed irrelevant columns

✅ Created analytical features

### Feature Engineering

| Feature | Description |
|----------|-------------|
| order_processing_time | Shipping Date − Order Date |
| delay | Actual Days − Scheduled Days |
| is_delayed | Delay indicator |
| order_month | Month of order |
| order_day | Day of week |
| order_hour | Hour of order |
| profitability_flag | Profit / Loss / Break-even |

---

## 📈 Key Performance Indicators (KPIs)

| KPI | Value |
|------|--------|
| Total Orders | 172,765 |
| Late Deliveries | 94,523 |
| On-Time Delivery % | 45.29% |
| Late Delivery % | 54.71% |
| 90th Percentile Delay | 3 Days |
| Total Profit | $7.5 Million |
| Profit Loss Due to Delays | $2.1 Million |

### Key Insight

More than half of all completed orders were delivered late, highlighting significant opportunities for operational improvement.

---

## 💰 Profitability Analysis

### Profitability Distribution

Orders were classified into:

- Profit
- Loss
- Break-even

### Findings

- 80.7% of orders were profitable
- 18.7% generated losses
- Break-even orders represented a very small percentage

### Delay vs Profit Analysis

Analyzed:

- Mean Profit by Delay Days
- Total Profit by Delay Days
- Percentage of Orders by Delay Days

### Business Insight

Although delayed orders continue generating revenue, extended delays contribute to profitability leakage and operational inefficiencies.

---

## 🚨 Bottleneck Detection Analysis

Delay rates were analyzed across:

- Order Region
- Customer Segment
- Shipping Mode
- Order Status
- Product Type
- Department

### Major Findings

#### Regional Analysis

Central Africa emerged as the highest-risk region with the largest delay percentage.

#### Shipping Mode Analysis

Shipping mode was one of the strongest predictors of late deliveries.

Key observations:

- First Class shipping showed the highest delay rates
- Second Class shipping followed closely behind
- Same Day shipping exhibited the lowest delay risk

#### Customer Segment Analysis

Delay percentages remained relatively similar across:

- Consumer
- Corporate
- Home Office

This indicates that delays are driven primarily by operational factors rather than customer characteristics.

#### Order Status Analysis

Pending and payment-related statuses consistently exhibited higher delay percentages.

---

## 🌍 Central Africa Root Cause Analysis

A dedicated analysis was conducted for Central Africa.

### Top Driver Factors

1. First Class Shipping Mode
2. Second Class Shipping Mode
3. Pending Order Status
4. Payment Type
5. Transfer Type
6. Financial Processing Status
7. Golf Department
8. Consumer Customer Segment
9. Footwear Department
10. Corporate Customer Segment

### Key Finding

Operational and logistics factors contribute more heavily to delays than customer demographics.

---

## ⏳ Time-Based Analysis

### Monthly Delay Trend

Analyzed delay percentages across all months.

**Finding:** Delay rates fluctuate seasonally.

### Delay % by Day of Week

Compared delay performance across weekdays.

**Finding:** Delay rates remain relatively stable throughout the week.

### Delay % by Order Hour

Analyzed hourly order behavior.

**Finding:** Certain order hours consistently exhibit elevated delay risk.

---

## 🤖 Machine Learning Model

### Objective

Predict whether an order will experience late delivery.

### Target Variable

```python
late_delivery_risk
```

### Features Used

```python
Type
Days for shipment (scheduled)
Category Name
Customer Segment
Department Name
Order Region
Shipping Mode
Order Month
Order Hour
```

### Data Preprocessing

- One-Hot Encoding
- Train-Test Split
- Pipeline Workflow

### Model

```python
RandomForestClassifier
```

### Outcome

The model was trained to identify high-risk orders before shipment, enabling proactive logistics intervention.

---

## 🛠️ Technologies Used

### Python

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Machine Learning

- Random Forest Classification
- Feature Engineering
- Predictive Analytics

### Visualization

- KPI Dashboard
- Profitability Analysis
- Bottleneck Detection Dashboard
- Time-Based Analysis Dashboard

---

## 📊 Dashboard & Visualizations

### Included Visualizations

- Profitability Distribution
- Delay Distribution
- Profit Analysis by Delay Days
- Bottleneck Detection Dashboard
- Central Africa Driver Analysis
- Monthly Delay Trend
- Delay by Day of Week
- Delay by Order Hour

---

## 💡 Business Recommendations

### High Priority Actions

1. Improve logistics operations in Central Africa.
2. Review First Class and Second Class shipping processes.
3. Investigate payment and pending-order bottlenecks.
4. Reduce delays exceeding 2–3 days.
5. Deploy predictive monitoring using the machine learning model.

### Expected Benefits

- Reduced late deliveries
- Improved customer satisfaction
- Higher profitability
- Better resource allocation
- Enhanced supply chain visibility

---

## 📌 Conclusion

This project demonstrates how data analytics and machine learning can be leveraged to improve supply chain performance. Through KPI analysis, profitability assessment, bottleneck detection, regional root-cause analysis, and predictive modeling, the study identified key operational risks and provided actionable recommendations to reduce delivery delays and improve business outcomes.

---

## 👨‍💻 Author

**Akash Das**

Aspiring Data Analyst | Python | SQL | Statistics | Machine Learning | Business Analytics

*"Turning raw data into actionable business decisions."*
