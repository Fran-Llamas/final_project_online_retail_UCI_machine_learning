# Online Retail Dataset Business Case

This README provides an overview of the business case found in the [Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail), detailing the dataset's structure and analysis methodologies applied.

## Understanding the Data

The dataset consists of transactional records from an online retail store, encompassing various attributes:

- **InvoiceNo**: A unique identifier for each transaction, where a 'c' prefix indicates cancellations.
- **Stockcode**: Unique code assigned to each product.
- **Description**: Name and brief description of the product.
- **Quantity**: Quantity of each product per transaction.
- **InvoiceDate**: Date and time of transaction.
- **UnitPrice**: Price per unit of the product.
- **CustomerID**: Unique identifier for each customer.
- **Country**: Country of residence for each customer.

## Data Cleaning and Preprocessing

Several preprocessing steps were undertaken to ensure data quality and consistency:

- Handling duplicates and null values.
- Matching descriptions with stock codes.
- Managing cancelled transactions and zero unit prices.

## Feature Engineering

Feature engineering aimed to enrich the dataset with new insights:

- Aggregating customer data to derive metrics such as recency, frequency, and monetary value.
- Creating additional features like cancelled transactions frequency and favorite time slots.

## Correlation Analysis with Heatmap

A correlation analysis was conducted to identify relationships between variables, focusing on aggregate customer data and newly engineered features. This analysis helps detect multicollinearity.

## Normalize Features

Normalization was performed to scale the added variables in the new dataframe, ensuring comparability and eliminating biases.

## K-Means Clustering

K-Means clustering, an unsupervised learning technique, was employed to segment customers into distinct clusters. However, K-Means has limitations:

- Sensitivity to the number of clusters specified.
- Dependence on initial centroid placement.
- Assumption of spherical and equal-sized clusters.

To address these, the Elbow and Silhouette methods were utilized for optimal cluster determination.

## Application of the Algorithm

The K-Means algorithm was applied to segment customers based on their transactional behavior.

## Evaluation Metrics

Evaluation metrics such as Silhouette score, within-cluster sum-of-squares (WCSS), Davies–Bouldin index (DBI), and Calinski-Harabasz index were employed to assess the clustering performance.

## Recommendation System

A recommendation system was devised to suggest the top three products for each customer within their respective clusters, focusing on products not previously purchased.

This README outlines the comprehensive analysis and methodologies applied to derive insights from the Online Retail Dataset, offering valuable insights for business decisions and strategy formulation.