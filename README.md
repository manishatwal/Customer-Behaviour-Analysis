# Amazon Customer Behavior Analysis (PySpark + RFM Segmentation)

This repository contains an end-to-end data science pipeline to analyze customer purchasing behavior on Amazon.com using PySpark. The project explores **transactional data, survey demographics, and RFM-based clustering** to derive actionable business insights for e-commerce optimization.

---

##  Project Objective

To analyze large-scale Amazon customer transaction data (2018–2022) and uncover patterns in purchasing trends, customer demographics, product demand, and engagement, with the goal of supporting **inventory planning, pricing strategies, marketing allocation, and customer retention initiatives**.

---

##  Business Goal

This project helps e-commerce businesses to:

* Understand seasonal and demographic purchasing patterns.
* Segment customers into value-based groups using RFM analysis.
* Identify top products, categories, and high-value regions.
* Detect anomalies in purchasing behavior (potential fraud).
* Develop strategies for customer retention, personalized pricing, and marketing optimization.

---

##  Pipeline Highlights

### 1. Data Preparation

* **Dataset**: 3 CSV files (`amazon-purchases.csv`, `survey.csv`, `fields.csv`).
* **Size**: 5,027 customers, transactions spanning **2018–2022**.
* Features: Order date, product details, category, pricing, quantity, state, and demographics.
* Merged transactional and survey datasets via `Survey ResponseID`.
* Missing values imputed (Unknown for product/state; No for life-changes).

### 2. Exploratory Data Analysis (EDA)

* **Temporal Trends**: Monthly, yearly, and weekday/weekend analysis.
* **Demographics**: Purchases analyzed across age, gender, income.
* **Product & Category Insights**: Top-selling products, bulk purchases, market basket pairs.
* **Geographic Distribution**: State-level revenue patterns.
* **KPIs**: Average spend per customer, repeat purchase behavior.

### 3. Feature Engineering & Cleaning

* Extracted `Order Month`, `Order Year` from dates.
* Encoded demographics (income, gender).
* Removed duplicates, standardized schema.

### 4. RFM Segmentation & Clustering

* **RFM Metrics**: Recency, Frequency, Monetary calculated per customer.
* Applied **log transformation + StandardScaler**.
* Used **K-Means clustering** (optimal k=3 via elbow method).
* Segments identified:

  * **Champions** – frequent, high spenders.
  * **Moderates** – mid-range engagement.
  * **At-Risk** – long recency, low frequency.

### 5. Business Insights

* **Seasonality**: Purchases peak in **Nov–Dec** (holiday season).
* **Demographics**: Females aged 55–64 and mid-income (\$50k–\$75k) buyers are strong repeat purchasers.
* **Regions**: CA, TX, NY dominate in volume; WA, MA show highest per-capita spend.
* **Products**: Books, Gift Cards, Electronics drive sales; Groceries dominate bulk purchases.

---

##  Business Recommendations

* **Inventory**: Stock-up electronics before holidays; bundle consumables in seasonal offers.
* **Retention**: Loyalty programs for Champions; reactivation campaigns for At-Risk customers.
* **Pricing**: Tiered volume discounts, flash sales, surge pricing for high-demand SKUs.
* **Marketing**: Prioritize ad spend in CA/TX/NY; premium targeting in WA/MA.

---

##  Visualizations

* Purchases by hour, day, and month.
* Monthly & yearly revenue trends.
* Purchases by age, gender, and income.
* Weekday vs weekend purchases.
* Top 10 products by quantity & revenue.
* State-wise revenue distribution.
* Market basket analysis (top 20 product pairs).
* RFM cluster distribution & spending comparison.

---

##  Repository Contents

| File Name                                 | Description                                                             |
| ----------------------------------------- | ----------------------------------------------------------------------- |
| `cleaned_customer_data.csv`               | Processed dataset after cleaning and feature engineering                |
| `Customer_Behavior_Analysis.ipynb`        | Full PySpark notebook with data prep, EDA, RFM clustering, and insights |
| `Report_Manish_Atwal.pdf`                 | Executive business report with insights and recommendations             |

---

##  Dataset Access

The original raw dataset (too large to host directly on GitHub) can be downloaded from **Harvard Dataverse**:

[Amazon Customer Behavior Dataset (2018–2022)](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/YGLYDY&version=1.0)

This includes the following CSV files:

* `amazon-purchases.csv` – Transactional purchase data
* `survey.csv` – Demographic and survey data
* `fields.csv` – Metadata for survey questions

---

##  Author

**Manish Atwal**

