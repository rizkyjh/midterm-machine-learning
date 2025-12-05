# **Customer Segmentation Analysis (Midterm Task 3\)**

## **Identification**

**Name:** Rizky Januar Hardi   
**Class:** Machine Learning   
**NIM:** 1103220166

## **1\. Project Purpose**

This project applies Unsupervised Learning techniques to segment credit card customers based on their usage behavior. The goal is to identify distinct customer groups (clusters) to inform targeted marketing strategies.

## **2\. Workflow Overview**

* **Dataset:** clusteringmidterm.csv (Credit Card usage data).  
* **Preprocessing:**  
  * Removed non-predictive CUST\_ID column.  
  * Imputed missing values with the column mean.  
  * **Standardization:** Crucial step using StandardScaler to ensure features like 'Balance' (0-10000) don't dominate features like 'Frequency' (0-1).

## **3\. Methodology**

1. **Elbow Method:** Used to scientifically determine the optimal number of clusters (k). We analyzed the inertia graph and selected **k=4**.  
2. **K-Means Algorithm:** The primary algorithm used to group customers based on feature similarity.  
3. **PCA Visualization:** Applied Principal Component Analysis (PCA) to reduce the 17-dimensional data into 2D for visual interpretation.

## **4\. Cluster Interpretation**

The model successfully identified 4 distinct customer archetypes:

* **Cluster 0:** Inactive/Low-value users (Low balance, low spending).  
* **Cluster 1:** High-Risk Borrowers (High balance, frequent cash advances).  
* **Cluster 2:** Big Spenders (High balance, high purchase frequency).  
* **Cluster 3:** Standard Users (Average behavior across all metrics).

## **5\. Files**

* **midterm\_clustering.ipynb:** Code for preprocessing, K-Means training, and PCA visualization.  
* **clustering\_plot.png:** Visual representation of the customer segments.