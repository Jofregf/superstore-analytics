# Superstore Sales Analytics 📊

End-to-end **Business Intelligence & Data Analysis project** using **Python** and **Power BI**, focused on sales performance, customer behavior, and operational efficiency.
This project simulates a real-world retail analytics scenario, from data cleaning and feature engineering to dashboarding and executive insights.

## 🧠 Project Objective

The goal of this project is to:
- Analyze sales trends and seasonality
- Evaluate geographic performance by region, state, and city
- Identify high-value customers and product performance
- Assess shipping efficiency and its impact on sales
- Build an executive-level dashboard for decision-making

## 🛠️ Tools & Technologies

- **Python**
  - Pandas
  - NumPy
  - Jupyter Notebook
- **Power BI**
  - DAX measures
  - Interactive dashboards
  - Geographic and operational analysis
- **Git & GitHub**

## 📂 Project Structure
superstore-analytics/
│



├── data/
│ ├── raw/
│ └── processed/
│ └── superstore_processed.csv
│
├── notebook/
│ └── superstore_analysis.ipynb
│
│── superstore_dashboard.pbix
│
├── documentation.md
└── README.md

## 🔄 Data Preparation (Python)

Key transformations performed in Jupyter Notebook:
- Converted date columns to proper datetime format
- Created **lead time** feature (Ship Date − Order Date)
- Analyzed and documented missing postal codes
- Aggregated data for:
  - Monthly sales and orders
  - Customer lifetime value (LTV)
  - Multi-product vs single-product orders
- Exported a clean, analysis-ready dataset for Power BI

## 📊 Power BI Dashboard Overview

The dashboard is organized into four main pages:

### 1️⃣ Executive Summary
- Total Sales
- Number of Orders
- Average Order Value
- Average Shipping Lead Time
- High-level trends for fast decision-making

### 2️⃣ Geographic Performance
- Sales by State (map)
- Top cities by total sales
- Regional sales comparison

### 3️⃣ Operations & Logistics Performance
- Lead time distribution
- Shipping mode analysis
- Relationship between shipping speed and sales

### 4️⃣ Customers & Products Performance
- Top customers by lifetime value
- Average order value per customer
- Most sold products vs highest revenue products
- Single-product vs multi-product order analysis

## 📈 Key Insights

- Standard Class shipping has the longest lead time but represents the highest order volume
- Multi-product orders generate significantly higher revenue per order
- Sales show clear seasonality with strong peaks toward year-end
- A small group of customers contributes disproportionately to total revenue
- High-priced technology products drive revenue despite lower order frequency

## 🚀 Next Improvements

- Add profit-based analysis (if data available)
- Customer segmentation using RFM
- Forecasting monthly sales
- Optimize dashboard for mobile view

## 👤 Author

**Guillermo Jofré**  
Data Analyst | Business Intelligence | Python | Power BI  
📍 Argentina  

## 📌 Notes

This project is designed for **portfolio and interview purposes**, showcasing:
- Analytical thinking
- Data storytelling
- BI dashboard design
- End-to-end workflow from raw data to insights
