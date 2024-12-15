# **E-commerce Data Analysis and Dashboard** 📊

## **Table of Contents** 📑
1. [Overview](#overview)  
2. [Objective](#objective)  
3. [Data Source](#data-source)  
4. [Data Preparation](#data-preparation)  
   - [Step 1: Data Cleaning and Transformation in Excel](#step-1-data-cleaning-and-transformation-in-excel)  
   - [Step 2: Transition to SQL for Large-Scale Data Handling](#step-2-transition-to-sql-for-large-scale-data-handling)  
   - [Step 3: Optimizing Data Import with CSV Lint](#step-3-optimizing-data-import-with-csv-lint)  
5. [Dashboard Overview](#dashboard-overview)  
6. [Key Insights](#key-insights)  
7. [Technical Challenges and Solutions](#technical-challenges-and-solutions)  
8. [Tools Used](#tools-used)  
9. [Conclusion](#conclusion)  
10. [Access](#access)  

## **Overview** 🌟
This project involves a comprehensive analysis of a Brazilian e-commerce dataset (2017–2018), leveraging tools like Excel, SQL, and Power BI to derive actionable insights into sales performance, customer behavior, shipping logistics, and seller activity. The project culminates in an interactive Power BI dashboard designed to support business decisions with key metrics and trends.

## **Objective** 🎯
The primary goal of this project was to perform a comprehensive analysis of the Brazilian e-commerce dataset from 2017–2018, focusing on several key aspects of the business:

1. **Analyze Sales Trends**: Identify patterns in sales performance over time, including seasonal fluctuations, top-selling categories, and revenue distribution across different regions.
2. **Evaluate Shipping Efficiency**: Assess the performance of the logistics and shipping processes, analyzing factors like shipping costs, delivery times, and regional differences.
3. **Examine Order Lifecycle**: Track the entire journey of an order, from purchase to delivery, and identify areas where delays occur or performance could be improved.
4. **Provide Insights into Customer Behavior**: Segment customers based on their purchasing patterns, frequency, and lifetime value to understand customer retention and acquisition strategies.
5. **Assess Seller Contributions**: Analyze seller performance, focusing on sales volume, product categories, and geographic distribution to identify top-performing sellers and opportunities for improvement.




## **Data Source** 📊
The dataset was sourced from the [Brazilian E-commerce Public Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). It contains anonymized data from 100,000 orders made between 2016 and 2018 across multiple marketplaces in Brazil. The dataset includes information on order status, pricing, payments, freight performance, customer locations, product attributes, and customer reviews.

### **Data Schema** 
*(Insert image here)*

## **Data Preparation** 
The data preparation phase was the backbone of this project, requiring careful handling of large datasets to ensure accuracy, consistency, and efficiency. Here's how the process unfolded:

### **Step 1: Data Cleaning and Transformation in Excel** 
The project began in Excel, where the raw data was explored, cleaned, and prepped for further analysis. This step was crucial for addressing issues that could impact data quality:

- **Handling Missing Values** :  
  Null values in critical columns, like product names, were replaced with "Other" to ensure completeness.  
  *(Insert screenshot here)*  

- **Translation of Product Categories** :  
  Brazilian product names were translated into English using a custom table generated with ChatGPT. The VLOOKUP function was applied to map these translations across the dataset.  
  Formula used:  
  `=VLOOKUP(B2, product_category_name_translati!$A$2:$B$100, 2, FALSE)`  
  *(Insert screenshot here)*  

- **Removing Duplicates and Invalid Records** :  
  Duplicate rows were eliminated from tables like orders and products. Invalid rows with missing or corrupted data in key fields, such as order status, were identified and removed.  
  *(Insert screenshot here)*  
