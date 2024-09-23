# ACSE Supermarket Data Preprocessing Summary Using BigQuery

## Background
ACSE Supermarket operates over 40 stores in North America and offers over 100,000 products in over 100 categories. Customers can join the ACSE Rewards program to benefit from sales and promotions. ACSE intends to use a recommendation system to make decisions in areas such as:

- Supply chain and logistics
- Store operations
- Supplier relations
- Pricing
- Promotions and marketing

## Problem
Your consulting firm is tasked with demonstrating deep knowledge of ACSE’s data to help develop a recommendation system. The key focus is to analyze and understand the data in three weeks using **BigQuery**, including performing text mining on product descriptions. The client expects your team to answer the following questions to prove readiness to build the system:

### Key Business Questions:
Using **BigQuery**, we will address the following critical questions:

1. **Best Customers:**
   - Who are the top customers based on revenues, profits, transactions/store visits, and product variety?
     - We will write **BigQuery** SQL queries to extract customer behavior and identify the top-performing customers across multiple metrics.

2. **Top Products and Product Groups:**
   - What are the best-performing products and product groups in terms of volume, revenues, profits, transactions, and customer interest?
     - Using **BigQuery**, we will aggregate product performance based on transactional data and compute relevant metrics such as volume and revenues.

3. **Top Stores:**
   - Which stores lead in terms of volume, revenues, profits, transactions, and customer engagement?
     - We will analyze store-specific data in **BigQuery** to rank stores based on key performance indicators.

4. **Customer Groupings:**
   - Are there meaningful customer segments such as:
     - **Most Valuable Customers:** Buy everything at any price.
     - **Cherry-pickers:** Purchase mostly on promotions.
     - Defined by specific categories, e.g., those who buy baby products but never buy milk.
     - By leveraging **BigQuery**, we can segment customers into groups based on purchasing behavior and category preferences.

5. **Product Groupings:**
   - Can we identify groups of products beyond categories, such as:
     - **Key Value Items (KVI)** and **Key Value Categories (KVC)**
     - **Traffic Drivers:** Products that drive store traffic.
     - **Promotion Analysis:** Products always on promotion versus seldom/never promoted.
     - **BigQuery** queries will enable us to classify products into various strategic groups and promotional categories.

6. **Store Groupings:**
   - Are there natural store clusters, such as stores frequently visited by cherry-pickers versus those visited by loyal customers?
     - Using **BigQuery** clustering techniques, we will analyze store-specific data to uncover store groupings based on customer types.

7. **Data Quality Issues:**
   - Are there missing data points, problematic product descriptions, non-products, non-customers (those with excessive purchases), or stores with insufficient transactions?
   - How can we address these data issues?
     - **BigQuery** data exploration will help identify and address data quality issues, such as missing values and outliers.

## Available Data

### Transactions Table
Contains transaction history from 2017 to 2020 for over 9 million customers:
- **cust_id**: Customer ID (Rewards members have ID starting with '1#########')
- **store_id**: Store ID
- **prod_id**: Product ID
- **trans_id**: Transaction ID
- **trans_dt**: Transaction date
- **sales_qty**: Quantity of the product in the transaction
- **sales_wgt**: Weight of the product if sold by weight
- **sales_amt**: Sales amount before discounts

### Products Table
Contains information about product categories and descriptions for over 100,000 products:
- **prod_id**: Product ID
- **prod_desc**: Product description
- **prod_section**: Product section description
- **prod_category**: Product category description
- **prod_subcategory**: Product subcategory description
- **prod_type**: Product type description
- **prod_mfc_brand_cd**: Manufacturer/brand code
- **prod_unit_qty_count**: Count per unit quantity of the product
- **prod_count_uom**: Unit of measure (UOM) for product count
- **prod_uom_value**: UOM value per product count

## Next Steps

### Data Exploration with BigQuery
- **Investigate missing or problematic data**:
  - Use **BigQuery** SQL queries to identify missing values or inconsistencies in both transactional and product data.
  
### Data Cleaning:
- **BigQuery** scripts will be used to handle issues such as missing values, outliers, and data discrepancies in product descriptions.

### Text Mining on Product Descriptions:
- Perform text mining on the **prod_desc** field using **BigQuery** text functions to enhance product grouping and understand potential relationships among products.

### Data Analysis:
- Start with profiling customers, products, and stores using **BigQuery** analytical functions.
- Write **BigQuery** queries to answer the seven key business questions regarding top customers, top products, and store rankings.

### Reporting:
- **BigQuery** results will be summarized and visualized to provide initial insights to the client on customer behavior, product performance, and store operations.
