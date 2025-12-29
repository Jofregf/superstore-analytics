# 📊 Superstore – Operational & Logistics Analysis (US)

## Business Context

The objective of this analysis is to evaluate the operational and shipping performance
of orders in the United States, focusing on delivery times, customer behavior and
geographical patterns.

This project is oriented to Business Intelligence and operational insights, not
financial performance.

## Business Questions

- How long does it take, on average, to ship an order?
- Are there differences in shipping times by ship mode or city?
- Which cities present the highest operational delays?
- What type of customers place more frequent orders?
- Are there seasonal patterns in order volume?

## EDA

### 🗓️ Date

- Date columns originally stored as strings were converted to datetime format to enable
  proper temporal analysis and feature engineering.

### 📦 Postal Code
- The Postal Code column was reviewed and 11 missing values (NaN) were identified.
  All missing postal codes correspond to records from Burlington, Vermont.
  Further inspection showed that all entries for this city and state have missing
  postal codes in the original dataset. Since no reliable information was available
  to impute these values and postal codes are not required for the scope of this analysis,
  the missing values were left unchanged.

### 📅 Lead time days

  - A new feature, `lead_time_days`, was created to measure the number of days between order placement and shipment.
  - The average shipping lead time is approximately 4 days, with most orders being shipped within a 3 to 5 day window Same-day shipments are present but represent a small portion of total orders.
  - Orders with a lead time of 0 days correspond to the "Same Day" shipping mode, confirming that same-day deliveries are correctly reflected in the data.

#### Conclutions
  - Shipping mode analysis shows that Standard Class is the most frequently used option, but also the slowest, with an average lead time of approximately 5 days.
  - Second Class shipping presents the highest average sales per order while maintaining a moderate delivery time, suggesting a balance between operational efficiency and order value.
  - Same Day shipping, while the fastest option, represents a smaller share of total orders and does not show a significantly higher average sale value.

### 💰 Sales
  - Sales analysis by region shows that the West region leads in total revenue and number of orders, while the South region has the highest average sales per order, indicating higher-value purchases despite lower volume.
  - City-level analysis reveals a strong concentration of sales in major metropolitan areas, with New York City and Los Angeles accounting for a significant share of total revenue.
  - Monthly sales analysis shows significant variability, with a pronounced peak in March. This increase is driven by both a higher number of orders and a substantial rise in average order value, suggesting the presence of high-value transactions or seasonal effects.


### 😎 Lifetime Value Customers
  - Average order value analysis reveals distinct customer purchasing behaviors. Some customers generate high lifetime value through a small number of high-value orders, while others contribute through frequent purchases with moderate order values. This distinction supports differentiated commercial strategies, such as personalized pricing for high-ticket customers and loyalty programs for recurrent buyers.

### 👜 
  - Multi-product orders represent nearly half of all orders but generate more than three times the average revenue per order compared to single-product purchases. The significantly higher median sales value indicates that this pattern is consistent across transactions and not driven by outliers.
  - These results highlight strong cross-selling opportunities and suggest that encouraging multi-product purchases could substantially increase overall revenue.

### 💾 Data Cleaning and Export
  - The processed dataset was saved after removing the Postal Code column, which contained missing values and was not required for the analysis. This cleaned version is used for all subsequent analytical steps and visualizations.

### 💵  Product Analysis: Sales Volume vs Revenue Contribution
Overview

Since the dataset does not include a profit or cost column, product performance was analyzed using sales revenue and order volume. This approach allows us to understand how different products contribute to total revenue and demand.

#### High-Volume Products (by Number of Orders)

The products with the highest number of orders are mainly low-priced office supplies, such as:
* Staples
* Envelopes
* Paper and binders
These products:
- Appear frequently across many orders
- Generate high sales volume
- Contribute relatively low revenue per order

📌 Insight:

These items drive operational volume but have limited impact on total revenue individually.
- High-Revenue Products (by Total Sales)
In contrast, the products generating the highest total sales are high-ticket items, mostly from the Technology and Furniture categories, such as:
* Copiers
* Binding machines
* Office equipment
* Specialized printers and chairs

These products:
- Are purchased less frequently
- Have a very high average order value
- Represent a significant share of total revenue

📌 Insight:

A small number of high-priced products account for a disproportionate share of total sales revenue.

Business Interpretation
The analysis reveals a clear product sales pattern:
- Low-price, high-frequency products sustain daily operations and order volume
- High-price, low-frequency products are key revenue drivers

This distinction is critical for:
- Sales strategy
- Inventory prioritization
- Revenue forecasting
- Dashboard segmentation in Power BI

