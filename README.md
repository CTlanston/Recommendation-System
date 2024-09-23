# ACSE Supermarket Recommendation System Project

## Part 1: Data Preprocessing (Exploratory Data Analysis)
The first part of the project focused on understanding and preparing the dataset for modeling. This stage laid the foundation for building a recommendation system tailored to ACSE Supermarket's needs, specifically targeting insights from their large retail dataset.

### Key Steps in Data Preprocessing:
1. **Sampling Transaction Dataset:**
   - A stratified sample of 50,000 observations was drawn from over 9 million customer transactions, ensuring customer behavior patterns were well-represented.
   
2. **Exploratory Data Analysis (EDA):**
   - EDA was performed on the transaction dataset to extract insights about customer purchase behavior, product sales, and store performance.
   - The goal was to answer critical business questions regarding the top customers, products, and stores in terms of volume, revenue, transactions, and other key metrics.
   
3. **NLP-based Data Cleaning:**
   - Natural Language Processing (NLP) techniques were applied to clean and correct missing or inaccurate product descriptions, focusing on attributes like brand, subcategory, size, and unit of measure (UOM).

4. **Association Rule Learning (ARL):**
   - We applied ARL to identify significant subcategories with a confidence threshold (K[G|GM] >= 0.3), helping to filter key product groups for further analysis.

5. **Customer Segmentation:**
   - Based on purchase behavior, customers were segmented into various groups, including:
     - Full-value customers
     - Cherry-pickers
     - Low-purchasing frequency customers
     - Low-spending and low-average-spending customers
   
6. **Feature Engineering:**
   - New features were engineered from customer and product data, such as spending frequency and value indicators, to enhance the predictive power of the eventual models.

### Outcomes of Data Preprocessing:
This thorough EDA provided a comprehensive understanding of the ACSE dataset. By identifying trends, customer segments, and product groupings, we established a strong foundation for building the recommendation system. The data was cleaned, preprocessed, and enriched to ensure it was suitable for modeling.

---

## Part 2: Modeling (Building the Recommendation System)
With a solid understanding of the dataset from the preprocessing phase, we proceeded to build a personalized recommendation system aimed at helping ACSE optimize product recommendations and promotions.

### Key Steps in Modeling:
1. **Model Selection:**
   - We built three types of recommendation models:
     - **Naive Bayes**
     - **Collaborative Filtering**
     - **Content-Based SVD**
   
2. **Predicting Customer Preferences:**
   - The goal was to recommend the top 5 products for each customer. We specifically focused on identifying customers who purchased General Mills (GM) products but had not yet bought Kellogg products for personalized promotions.
   
3. **Model Evaluation:**
   - The models were evaluated using three key metrics:
     - **Recommendation Accuracy**
     - **Transaction Hit Rate**
     - **Customer Purchase Rate**
   - Based on these evaluations, the **Naive Bayes** model was selected as the best-performing model due to its highest **Transaction Hit Rate** (1.68%).

4. **Profit Estimation:**
   - After finalizing the model, we used the **Naive Bayes** model to estimate potential revenue increases from targeted promotions.

### Model Results:
| Model             | Recommendation Accuracy | Transaction Hit Rate | Customer Purchase Rate |
|-------------------|-------------------------|----------------------|------------------------|
| **Naive Bayes**    | 21.24%                  | **1.68%**            | 72.64%                 |
| **Content-Based**  | 20.77%                  | 0.42%                | 57.39%                 |
| **Collaborative Filtering** | **25.36%**        | 1.23%                | 65.14%                 |

### Conclusion:
The **Naive Bayes** model, with its superior **Transaction Hit Rate**, was selected for the promotion recommendation system. This model will help ACSE Supermarket target customers effectively for personalized promotions, specifically encouraging Kellogg purchases among General Mills customers.

---

## Overall Project Summary
This project was divided into two critical parts:

1. **Data Preprocessing**:
   - Provided foundational insights through EDA, identifying key trends and segmenting customers and products. Preprocessing helped clean and enrich the data, making it ready for modeling.

2. **Modeling**:
   - Built and evaluated multiple recommendation models to personalize product recommendations for ACSE's promotion strategy. The **Naive Bayes** model, chosen based on its high **Transaction Hit Rate**, will guide targeted promotions for Kellogg products.

Together, these two parts culminated in a recommendation system designed to boost ACSE Supermarket's profitability by leveraging customer and product data to deliver personalized promotions.
