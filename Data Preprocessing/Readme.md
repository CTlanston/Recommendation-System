# ACSE Supermarket Data Preprocessing Summary

## Background
ACSE Supermarket operates over 40 stores in North America and offers over 100,000 products in over 100 categories. Customers can join the ACSE Rewards program to benefit from sales and promotions. ACSE intends to use a recommendation system to make decisions in areas such as:

- Supply chain and logistics
- Store operations
- Supplier relations
- Pricing
- Promotions and marketing

## Problem
Your consulting firm is tasked with demonstrating deep knowledge of ACSE’s data to help develop a recommendation system. The key focus is to analyze and understand the data in three weeks, including performing text mining on product descriptions. The client expects your team to answer the following questions to prove readiness to build the system:

### Key Business Questions:
1. **Best Customers:**
   - Who are the top customers based on revenues, profits, transactions/store visits, and product variety?
   
2. **Top Products and Product Groups:**
   - What are the best-performing products and product groups in terms of volume, revenues, profits, transactions, and customer interest?

3. **Top Stores:**
   - Which stores lead in terms of volume, revenues, profits, transactions, and customer engagement?

4. **Customer Groupings:**
   - Are there meaningful customer segments such as:
     - **Most Valuable Customers:** Buy everything at any price.
     - **Cherry-pickers:** Purchase mostly on promotions.
     - Defined by specific categories, e.g., those who buy baby products but never buy milk.

5. **Product Groupings:**
   - Can we identify groups of products beyond categories, such as:
     - **Key Value Items (KVI)** and **Key Value Categories (KVC)**
     - **Traffic Drivers:** Products that drive store traffic.
     - **Promotion Analysis:** Products always on promotion versus seldom/never promoted.

6. **Store Groupings:**
   - Are there natural store clusters, such as stores frequently visited by cherry-pickers versus those visited by loyal customers?

7. **Data Quality Issues:**
   - Are there missing data points, problematic product descriptions, non-products, non-customers (those with excessive purchases), or stores with insufficient transactions?
   - How can we address these data issues?

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
- **Data Exploration and Cleaning:**
  - Investigate missing or problematic data.
  - Clean and preprocess transaction and product data.
  
- **Text Mining:**
  - Perform text analysis on product descriptions to enhance understanding and product grouping.

- **Analysis:**
  - Begin with customer, product, and store profiling.
  - Answer key business questions to identify top customers, products, and stores.

- **Reporting:**
  - Prepare an initial report summarizing insights on customer, product, and store performance.
