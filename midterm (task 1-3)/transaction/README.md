# **End-to-End Fraud Detection Pipeline (Midterm Task 1\)**

## **Identification**

* **Name:** Rizky Januar Hardi  
* **Class:** Machine Learning  
* **NIM:** 1103220166

## **1\. Project Purpose**

The objective of this project is to design and implement a robust Machine Learning pipeline to detect fraudulent online transactions. This task focuses on binary classification using real-world data with significant class imbalance.

## **2\. Dataset & Overview**

* **Dataset:** IEEE-CIS Fraud Detection (train\_transaction.csv).  
* **Target Variable:** isFraud (0 \= Legitimate, 1 \= Fraud).  
* **Key Challenge:** The dataset is highly imbalanced (fraud cases are very rare compared to normal transactions).  
* **Preprocessing Steps:**  
  * **Data Cleaning:** Removed columns with \>70% missing values to optimize memory usage.  
  * **Imputation:** Filled missing numerical values with 0 and categorical values with "Unknown".  
  * **Encoding:** Applied Label Encoding to convert categorical features into numeric format.  
  * **Scaling:** Used StandardScaler to normalize features for the Neural Network.

## **3\. Models & Results**

We implemented and compared two models, focusing on handling the class imbalance using class\_weight='balanced'.

| Model | Type | Key Configuration | Metric (ROC-AUC) |
| :---- | :---- | :---- | :---- |
| **Logistic Regression** | Linear | class\_weight='balanced' | Baseline Score |
| **Neural Network (MLP)** | Deep Learning | Layers: (64, 32), ReLU | Deep Learning Score |

**Conclusion:** The Logistic Regression model provided a stable baseline, while the Neural Network captured more complex non-linear relationships. The final predictions for the test set are saved in submission.csv.

## **4\. How to Navigate**

1. **midterm\_fraud\_detection.ipynb:** The main notebook containing all code for preprocessing, training, and evaluation.  
2. **submission.csv:** The generated probability scores for the test dataset.  
3. **Dependencies:** Python, Pandas, Scikit-Learn, Matplotlib.