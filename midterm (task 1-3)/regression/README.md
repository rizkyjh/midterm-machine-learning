# **Song Year Prediction Pipeline (Midterm Task 2\)**

## **Identification**

**Name:** Rizky Januar Hardi   
**Class:** Machine Learning   
**NIM:** 1103220166

## **1\. Project Purpose**

To build an end-to-end regression system that predicts the release year of a song based on its audio characteristics (timbre, texture, etc.). This demonstrates the ability to model continuous target variables using both traditional ML and Deep Learning.

## **2\. Dataset Details**

* **Source:** midterm-regresi-dataset.csv  
* **Structure:** The first column is the Target (Year), followed by 90 continuous numerical audio features.  
* **Preprocessing:**  
  * Renamed the first column to Year.  
  * Applied StandardScaler to all feature columns to ensure Neural Network convergence.  
  * Split data into 80% Training and 20% Testing sets.

## **3\. Models Implemented**

We compared a robust ensemble method against a Deep Learning approach:

1. **Random Forest Regressor:**  
   * A non-linear model that builds multiple decision trees and averages their outputs.  
   * Configured with n\_estimators=10 (Speed Mode) to handle the large dataset size (\~500k rows) efficiently.  
2. **MLP Regressor (Deep Learning):**  
   * A Feed-Forward Neural Network.  
   * Architecture: Hidden layers of (50,) neurons with ReLU activation.

## **4\. Performance Evaluation**

We used **Root Mean Squared Error (RMSE)** to measure the average error in years.

| Model | RMSE (Lower is Better) | Performance Analysis |
| :---- | :---- | :---- |
| **Random Forest** | *\[Insert RMSE\]* | Typically handles tabular audio data better. |
| **Neural Network** | *\[Insert RMSE\]* | Requires more tuning but captures abstract patterns. |

## **5\. Files**

* **midterm\_regression.ipynb:** The complete training pipeline.  
* **midterm-regresi-dataset.csv:** The dataset used.