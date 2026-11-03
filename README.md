# 🛒 Flipkart E-Commerce Performance Analysis (Power BI Dashboard)

An end-to-end data analytics and business intelligence project built using **Python Web Scraping**, **Pandas Data Cleaning**, and **Power BI Interactive Reporting**. This repository provides actionable operational insights into sales performance, regional demand drivers, delivery logistics, and return/cancellation trends for Flipkart.

---

## 📊 Executive Summary
This project analyzes transactional e-commerce data to evaluate key business performance indicators (KPIs). By combining web-scraped product data with structured operational attributes, the resulting interactive 3-page Power BI report helps stakeholders optimize supply chain efficiency, target high-growth regions, and reduce order cancellation rates.

---

## 🕷️ Data Collection & Pipeline (Web Scraping & Wrangling)

### 1. Data Scraping (Python)
- **Tools:** Python, `BeautifulSoup4`, `Requests`, `Selenium`
- **Process:** Programmatically scraped Flipkart product listings, category trees, pricing structures, ratings, and estimated delivery timelines.
- **Header Management:** Implemented custom HTTP User-Agent headers and request throttling to navigate site structures smoothly.

### 2. Data Cleaning & Transformation (Pandas)
- **Tools:** Python `Pandas`, `NumPy`
- Cleaned raw currency symbols (`₹`), stripped whitespaces, handled missing/null values, and cast columns into appropriate numeric and temporal data types.
- Synthesized transactional mapping attributes (`Order_ID`, `Customer_ID`, `Order_Status`, `Cancellation_Reason`) to form a complete flat analysis dataset: **`Flipkart_Clean_Performance_Report.csv`**.

---

## 🚀 Interactive Dashboard Architecture

### 📌 Page 1: Executive Sales Overview
* **Focus:** High-level revenue performance and sales trends.
* **Key Metrics:** Total Revenue, Total Orders, Average Order Value (AOV), Profit Margins.
* **Visuals:** Monthly Revenue Trends (Line Chart), Category Revenue Split (Donut Chart).

### 📌 Page 2: Regional Performance & Customer Demographics
* **Focus:** Geographic distribution and customer loyalty analysis.
* **Key Visuals:**
  * **Top Cities by Revenue:** Clustered Bar Chart (Horizontal) highlighting top metro contributors.
  * **Order Status Breakdown by City:** Stacked Column Chart tracking Delivered vs. Cancelled vs. Returned orders.
  * **Avg Delivery Days by City:** Clustered Column Chart identifying regional supply chain bottlenecks.
  * **Regional Summary Matrix:** Table visual enhanced with **Conditional Formatting (Data Bars)** for revenue hierarchy.

### 📌 Page 3: Logistics, Delivery & Return Analysis
* **Focus:** Supply chain efficiency, delivery speed, and return drivers.
* **Key Visuals:**
  * **Order Status Share:** Donut Chart showing proportion of completed vs. dropped orders.
  * **Top Cancellation Reasons:** Horizontal Bar Chart isolating primary reasons behind lost revenue.
  * **Logistics Matrix:** Table visual tracking delivery TAT (Turnaround Time) across cities.

---

## 🛠️ Technical Stack & Tools
* **Data Extraction & Wrangling:** Python 3.x, `BeautifulSoup4`, `Requests`, `Pandas`, `NumPy`
* **BI Tool:** Power BI Desktop
* **Data Modeling:** DAX (Data Analysis Expressions) for dynamic measures, Time Intelligence, and conditional aggregation
* **Design Theme:** Customized Dark Theme (`#111C2E`) with Neon Cyan (`#00E5FF`) accents

📈 Business Insights & Strategic Recommendations
1.Regional Demand vs. Growth: While Tier-1 metros (Mumbai, Delhi, Bangalore) generate the largest gross revenue share, emerging Tier-2 hubs (Jaipur, Bareilly, Ahmedabad) exhibit higher MoM growth velocity.

2. Delivery Speed vs. Cancellation Correlation: Longer delivery timelines (>5 days) directly correlate with higher order cancellation rates, primarily driven by "Expected Delivery Time Exceeded".

3.Actionable Logistics Strategy: Establishing localized fulfillment centers in high-growth Tier-2 clusters will reduce TAT by an estimated 20–30%, directly curbing order cancellations and improving repeat buyer retention.
