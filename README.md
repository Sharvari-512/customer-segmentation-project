# 🧠 Customer Segmentation using Machine Learning

## 📌 Project Overview
This project focuses on **customer segmentation** using transaction, behavioral, and demographic data.
The goal is to group customers into meaningful segments to help businesses understand customer behavior and design targeted strategies.

## 🎯 Objectives
* Perform data cleaning and preprocessing
* Convert transaction-level data into customer-level insights
* Apply clustering techniques to segment customers
* Create customer personas
* Generate actionable business insights

## 📂 Dataset Description
The dataset contains the following categories:
### 🔹 Order Information
* Order_ID
* Date
### 🔹 Customer Demographics
* Customer_ID
* Age
* Gender
* City
### 🔹 Product Information
* Product_Category
* Unit_Price
* Quantity
### 🔹 Transaction Details
* Discount_Amount
* Total_Amount
* Payment_Method
### 🔹 Customer Behavior
* Device_Type
* Session_Duration_Minutes
* Pages_Viewed
* Is_Returning_Customer
### 🔹 Post-Purchase Metrics
* Delivery_Time_Days
* Customer_Rating

## ⚙️ Workflow
### 🔹 Step 1: Data Cleaning & Preparation
* Converted date columns to datetime
* Handled missing values
* Removed inconsistencies
* Encoded categorical variables
### 🔹 Step 2: Feature Engineering
Transformed transaction-level data into **customer-level features**:
* **Value**: Total Spend, Avg Order Value
* **Frequency**: Number of Orders
* **Recency**: Days since last purchase
* **Behavior**: Session duration, pages viewed
* **Loyalty**: Returning rate
* **Experience**: Customer rating, delivery time
### 🔹 Step 3: Feature Selection
Selected relevant numerical and categorical features for clustering.
### 🔹 Step 4: Clustering
* Applied **K-Means clustering** using scikit-learn
* Used the **Elbow Method** to determine optimal clusters
* Final model: **K = 3 clusters**
### 🔹 Step 5: Cluster Analysis
* Calculated average metrics for each cluster
* Identified behavioral patterns
* Analyzed cluster size and distribution
### 🔹 Step 6: Customer Personas
Customers were grouped into meaningful personas:
| Cluster | Persona                      |
| ------- | ---------------------------- |
| 0       | Premium Loyal Customers      |
| 1       | Budget / Low-Value Customers |
| 2       | Window Shoppers / Browsers   |

## 📊 Visualizations
The project includes:
* Customer distribution by cluster
* Persona distribution
* Average spending per segment
* Recency vs spending analysis
* Engagement analysis (session vs pages)
* PCA visualization for cluster separation

## 🔍 Key Insights
* **Premium Customers** generate the highest revenue and show strong loyalty
* **Budget Customers** are price-sensitive and require promotions
* **Window Shoppers** show high engagement but low conversion

## 💡 Business Recommendations
* 🎯 Target premium customers with loyalty programs and exclusive offers
* 💸 Offer discounts and bundles to budget customers
* 🛒 Improve conversion strategies for browsing customers
* 🚀 Enhance user experience for better engagement

## 🛠️ Tools & Technologies
* Python
* pandas
* numpy
* scikit-learn
* matplotlib
