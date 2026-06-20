# Customer Segmentation Analysis Using K-Means Clustering

## Overview

This project focuses on customer segmentation using machine learning techniques to identify distinct customer groups based on purchasing behavior, engagement metrics, and demographic characteristics.

By applying K-Means Clustering, customers are categorized into meaningful segments that can help businesses improve marketing strategies, customer retention, and personalized recommendations.

---

## Objectives

* Analyze customer purchasing behavior.
* Create customer-level features using transaction data.
* Perform customer segmentation using K-Means Clustering.
* Identify high-value and low-value customer groups.
* Generate actionable business insights for targeted marketing.

---

## Dataset

**File:** `customer_behavior_data.csv`

The dataset contains transaction-level customer data including:

* Customer ID
* Order Information
* Purchase Amount
* Product Category
* Session Duration
* Pages Viewed
* Device Type
* Customer Ratings
* Delivery Time
* Demographic Information

### Dataset Size

* Original Records: **17,049 transactions**
* Unique Customers: **5,000 customers**

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn

---

## Project Workflow

### 1. Data Cleaning & Preparation

* Removed duplicate records
* Converted date fields into datetime format
* Created derived variables
* Encoded categorical variables
* Verified transaction totals

### 2. Feature Engineering

Customer-level metrics were generated:

#### RFM Features

* **Recency** – Days since last purchase
* **Frequency** – Number of orders
* **Monetary Value** – Total customer spend

#### Behavioral Features

* Average Session Duration
* Average Pages Viewed
* Returning Customer Rate
* Average Customer Rating
* Average Delivery Time

#### Demographic Features

* Age
* Gender
* City

---

### 3. Feature Selection

Numeric features used for clustering:

* Total Spend
* Average Order Value
* Total Quantity
* Number of Orders
* Recency
* Average Session Duration
* Average Pages Viewed
* Returning Rate
* Average Customer Rating
* Average Delivery Time
* Age
* Purchase Frequency

Categorical features were retained for profiling purposes but excluded from clustering calculations.

---

### 4. Outlier Treatment

Since K-Means is sensitive to extreme values:

* Outliers were identified using boxplots.
* Extreme values in:

  * Total Spend
  * Average Order Value

were capped at the **99th percentile** before scaling.

---

### 5. Customer Segmentation

Features were standardized using:

```python
StandardScaler()
```

K-Means Clustering was applied to the scaled dataset.

### Optimal Cluster Selection

Two evaluation methods were used:

* Elbow Method
* Silhouette Score

The optimal number of clusters was selected as:

```text
K = 2
```

---

## Model Performance

### Silhouette Scores

| K | Score |
| - | ----- |
| 2 | 0.201 |
| 3 | 0.199 |
| 4 | 0.156 |
| 5 | 0.127 |

### Final Model

```text
Clusters: 2
Silhouette Score: 0.201
```

The score indicates moderate separation, which is expected because customer behavior often exists on a continuous spectrum rather than forming perfectly distinct groups.

---

## Customer Segments

### Cluster 0 — Low Value Customers

**Characteristics**

* Lower spending
* Fewer purchases
* Longer inactivity periods

**Statistics**

* Average Spend: $2,333
* Average Orders: 2.29
* Segment Size: 3,540 customers
* Population Share: 70.8%

**Recommended Actions**

* Discount campaigns
* First-purchase incentives
* Free shipping offers
* Win-back marketing campaigns

---

### Cluster 1 — High Value Customers

**Characteristics**

* Higher spending
* More frequent purchases
* More recent activity

**Statistics**

* Average Spend: $9,036
* Average Orders: 6.13
* Segment Size: 1,460 customers
* Population Share: 29.2%

**Recommended Actions**

* Loyalty rewards
* Personalized promotions
* Early product access
* VIP customer programs

---

## Visualizations

The project includes:

* Elbow Method Curve
* Silhouette Score Analysis
* Customer Distribution by Cluster
* Customer Distribution by Persona
* Average Spend per Cluster
* Recency vs Total Spend Scatter Plot
* Age vs Spending Analysis
* Engagement Behavior Analysis
* PCA-Based Cluster Visualization

---

## PCA Validation

Principal Component Analysis (PCA) was used to visualize customer segments in two dimensions.

```text
Variance Explained: 43.6%
```

This helps validate that the identified customer groups are behaviorally distinct.

---

## Key Insights

### Low Value Customers

* Represent the majority of customers.
* Generate lower revenue.
* Require engagement and activation strategies.

### High Value Customers

* Represent less than one-third of customers.
* Generate significantly higher revenue.
* Should be prioritized for retention efforts.

---

## Business Impact

Customer segmentation enables organizations to:

* Improve marketing ROI
* Increase customer retention
* Personalize promotions
* Enhance customer lifetime value (CLV)
* Support data-driven business decisions
