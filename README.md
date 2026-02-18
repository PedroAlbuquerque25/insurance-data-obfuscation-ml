# 🛡️ Insurance Data Obfuscation & Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Linear Algebra](https://img.shields.io/badge/Focus-Linear%20Algebra-red)
![Data Privacy](https://img.shields.io/badge/Topic-Data%20Privacy-green)

Identifying similar customers and predicting insurance benefits while protecting sensitive data through mathematical obfuscation.

---

## 📌 Project Overview

The insurance company **"Protect Your Tomorrow"** needs to evaluate several Machine Learning tasks. The challenge goes beyond simple prediction: we must ensure that customer personal data is protected (masked) without compromising the performance of the predictive models.

---

## 🎯 Business Goals & Tasks

### 1. Customer Similarity (Marketing)
* Developing a k-Nearest Neighbors (kNN) based algorithm to find customers similar to a target profile.
* Evaluating the impact of **Data Scaling** (MaxAbsScaler) on the kNN distance metrics (Euclidean vs. Manhattan).

### 2. Benefit Prediction (Classification)
* Building a model to predict if a new customer is likely to receive an insurance payment.
* Comparing model performance against a **Dummy Model** to ensure true predictive power.

### 3. Claim Forecasting (Regression)
* Predicting the number of insurance claims a customer might make using **Linear Regression**.

### 4. Data Obfuscation (Security/Privacy)
* Implementing a data transformation algorithm using **Matrix Multiplication**.
* **Mathematical Proof:** Proving that multiplying the feature matrix $X$ by an invertible matrix $P$ does not change the quality of the Linear Regression predictions.

---

## 🧠 Technical Methodology

### Data Masking Algorithm
To protect the data, we transform the original feature matrix $X$ into an obfuscated version $X'$:
$$X' = X \times P$$
Where:
* **$X$**: Original feature matrix.
* **$P$**: A random invertible matrix (the "key").



### Why it works?
The Linear Regression weights change, but the final predictions $\hat{y}$ remain identical. This allows the company to store and train models on obfuscated data while keeping the original identities secure.

---

## 📊 Key Results

* **Similarity:** Data scaling proved essential for kNN, as features like "Salary" would otherwise dominate "Age" in distance calculations.
* **Classification:** The model significantly outperformed the dummy baseline, showing high F1-Score.
* **Data Protection:** The RMSE and $R^2$ metrics for the Linear Regression model remained **identical** (up to the 10th decimal place) before and after data obfuscation.

---

## 🛠️ Tech Stack

* **Python 3.10**
* **Pandas & NumPy** (Matrix operations)
* **Scikit-Learn** (kNN, Linear Regression, Metrics)
* **Matplotlib & Seaborn** (Data Visualization)

---

## 📂 Project Structure
```text
├── dataset/      # Insurance customer data
├── notebook/     # Jupyter Notebook with full analysis and proofs
├── environment.yml # Conda environment configuration
└── README.md     # Project documentation