# Kellogg Project: Targeting Customers for General Mills Product Promotion

## Project Objective
The main goal of this project was to build a recommendation system for Kellogg to identify customers who have purchased General Mills (GM) products but not Kellogg products. These customers will be targeted for personalized promotions to increase Kellogg's market share.

## Project Workflow Overview
The project is divided into several key stages, which are depicted in the process flow diagram:

1. **Sampling the Transaction Dataset:**
   - We sampled 50,000 observations from the whole dataset, stratified by customers. This ensures a balanced representation of customers for further analysis.
  
2. **Exploratory Data Analysis (EDA):**
   - We performed EDA on the sampled dataset to uncover key patterns related to customer purchasing behavior, product performance, and store operations.
  
3. **Preprocessing:**
   - Applied Natural Language Processing (NLP) with domain knowledge to clean and fix missing/incorrect labels in the product table (e.g., focusing on brand, subcategory, size, and unit of measure).
   - Implemented Association Rule Learning (ARL) to filter out subcategories with a confidence threshold (K[G|GM] >= 0.3).
   - Identified various customer segments:
     - Full-value customers
     - Cherry-pickers
     - Customers with low purchasing frequency
     - Customers with low spending
     - Customers with low average spending

4. **Feature Engineering:**
   - Engineered new features, such as spending, frequency, and full-value indicators for two key subcategories, to enrich the data and improve model performance.

5. **Modeling:**
   - Built three different recommendation models:
     1. **Naive Bayes**
     2. **Collaborative Filtering**
     3. **Content-Based SVD**
   - These models predicted the top 5 recommended items for each customer.

6. **Model Evaluation:**
   - Extracted products from 9/2021 to 12/2021 for testing purposes.
   - Tuned the models to increase their accuracy and assessed them based on three key metrics:
     - **Recommendation Accuracy**
     - **Transaction Hit Rate**
     - **Customer Purchase Rate**

7. **Profit Estimation:**
   - After model evaluation, we selected the Naive Bayes model for profit estimation due to its superior **Transaction Hit Rate** (1.68%).

## Model Results
The table below summarizes the results from the three models:

| Model             | Recommendation Accuracy | Transaction Hit Rate | Customer Purchase Rate |
|-------------------|-------------------------|----------------------|------------------------|
| **Naive Bayes**    | 21.24%                  | **1.68%**            | 72.64%                 |
| **Content-Based**  | 20.77%                  | 0.42%                | 57.39%                 |
| **Collaborative Filtering** | **25.36%**        | 1.23%                | 65.14%                 |

- Although the **Collaborative Filtering** model had the highest **Recommendation Accuracy** (25.36%), we chose the **Naive Bayes** model due to its highest **Transaction Hit Rate** of 1.68%. This metric is particularly crucial for the promotion campaign as it reflects the likelihood of successfully converting a recommendation into a transaction.

## Conclusion
In this project, we developed a personalized promotion recommendation system for Kellogg, specifically targeting customers who purchased General Mills products but not Kellogg products. The final model chosen for this task was the **Naive Bayes** model due to its superior performance in **Transaction Hit Rate**, making it the best choice for driving immediate sales conversion through targeted promotions.
