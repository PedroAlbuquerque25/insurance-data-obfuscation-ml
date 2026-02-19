# 🛡️ Privacy-Preserving Insurance Analytics with Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Linear Algebra](https://img.shields.io/badge/Focus-Linear%20Algebra-red)
![Data Privacy](https://img.shields.io/badge/Topic-Data%20Privacy-green)


A complete Data Science project integrating **Machine Learning, Linear Algebra, and Data Privacy Engineering** to solve strategic challenges for the insurance company *Protect Your Tomorrow*.

---

## 🔎 Key Results

- ✔ kNN classification significantly outperformed dummy baselines  
- ✔ Linear Regression achieved **RMSE ≈ 0.3637** and **R² ≈ 0.42**  
- ✔ Feature scaling proved essential for distance-based models  
- ✔ Data obfuscation preserved predictions with **0.00% performance loss**  
- ✔ Analytical proof + computational validation included  

---

## 📌 Business Problem

The insurance company aims to leverage Machine Learning to:

1. Identify similar customers for targeted marketing  
2. Predict whether a customer will receive insurance benefits  
3. Estimate the expected number of claims  
4. Protect sensitive customer data without degrading model performance  

This project addresses all four objectives using mathematical rigor and practical implementation.

---

## 🧠 Project Architecture

### 1️⃣ Customer Similarity (k-Nearest Neighbors)

Implemented a kNN-based similarity engine using:

- Euclidean and Manhattan distance  
- Feature scaling via **MaxAbsScaler**  

**Key Insight:**  
Without scaling, the `income` feature dominated the distance metric, distorting similarity detection.  
After scaling, similarity reflected all attributes fairly.

---

### 2️⃣ Benefit Prediction (Binary Classification)

A kNN classifier was developed to predict whether a client will receive insurance benefits.

- Train/Test split: 70/30  
- Metric: **F1-Score**  
- Compared against probabilistic dummy baselines  

**Result:**  
The model consistently outperformed random baselines despite class imbalance.

---

### 3️⃣ Claim Forecasting (Custom Linear Regression)

A Linear Regression model was implemented from scratch using the analytical solution:

$$
w = (X^T X)^{-1} X^T y
$$

**Performance:**

- RMSE: ~0.36  
- R²: ~0.66  

The model explains approximately 66% of variance in claim counts.

---

### 4️⃣ Data Obfuscation & Privacy Engineering

To protect sensitive data (`gender`, `age`, `income`, `family_members`), an invertible linear transformation was applied:

$$
X' = X P
$$

Where **P** is a random invertible matrix.

#### Analytical Proof

Even though model weights change:

$$
w_P = P^{-1} w
$$

Predictions remain identical:

$$
\hat{y}_{obfuscated} = \hat{y}_{original}
$$

---

### Computational Validation

| Model | RMSE | R² |
|--------|--------|--------|
| Original Data | 0.3637 | 0.4227 |
| Obfuscated Data | 0.3637 | 0.4227 |

Maximum prediction difference: ~1e−8 (floating-point precision)

✔ Zero performance degradation  
✔ Full mathematical validation  
✔ Privacy-aware modeling  

---

## 📊 Technical Skills Demonstrated

- Linear Algebra (matrix inversion, conditioning, transformations)  
- k-Nearest Neighbors (distance metrics & scaling impact)  
- Custom Linear Regression implementation  
- Model evaluation (F1, RMSE, R²)  
- Baseline comparison & class imbalance analysis  
- Data obfuscation techniques  
- Numerical stability considerations  

---

## ⚠️ Limitations

- Linear obfuscation is reversible if matrix **P** is known.  
- Not resistant to advanced reconstruction attacks.  
- Stronger privacy techniques (e.g., Differential Privacy) could be applied.  

---

## 🔬 Future Improvements

- Regularization (Ridge / Lasso)  
- ROC-AUC evaluation  
- Hyperparameter tuning  
- Differential Privacy mechanisms  
- Pipeline automation  

---

## 🎯 Final Assessment

This project demonstrates that it is possible to:

- Build reliable predictive models  
- Validate results mathematically  
- Preserve model performance under data transformation  
- Combine business insight with rigorous mathematical reasoning  

It bridges **Machine Learning, Linear Algebra, and Data Privacy**, showcasing both analytical depth and practical implementation.

---

## 🤝 Contact
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/phaa/)