# 🌍 Travel Package Purchase Prediction

A Machine Learning classification project that predicts whether a customer will purchase a travel package based on their demographic and behavioral information.

---

## 📌 Project Overview

This project analyzes customer data from a travel company and applies multiple machine learning models to predict **purchase behavior**.  
The best-performing model is selected based on evaluation metrics.

---

## 🎯 Objective

To predict whether a customer will purchase a travel package.

**Target Variable:**
- `ProdTaken`
  - `1` → Customer will buy the travel package
  - `0` → Customer will not buy the travel package

---

## 📂 Dataset Description

The dataset contains customer information such as:
- Age
- Gender
- Marital Status
- Occupation
- Monthly Income
- Number of Trips
- Preferred Property Type
- Pitch Satisfaction Score
- Product Taken (Target)

---

## 🛠️ Technologies Used

- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn  

---

## 🔍 Exploratory Data Analysis (EDA)

EDA was performed to:
- Understand data distribution
- Identify missing values
- Separate categorical and numerical features
- Analyze feature influence on purchase behavior

---

## 🧹 Data Preprocessing

- Missing value handling  
- Categorical feature encoding using **OneHotEncoder**  
- Numerical feature scaling using **StandardScaler**  
- **ColumnTransformer** for applying transformations efficiently  

---

## 🤖 Machine Learning Models Used

The following classification models were trained and evaluated:

### 1️⃣ Logistic Regression
- Simple and interpretable linear model
- Used as a **baseline** classifier

### 2️⃣ Decision Tree Classifier
- Captures non-linear relationships
- Easy to visualize and understand

### 3️⃣ Random Forest Classifier
- Ensemble of multiple decision trees
- Reduces overfitting
- Handles complex feature interactions well

---

## ✂️ Train-Test Split

- **Training Data:** 70%  
- **Testing Data:** 30%  

This ensures unbiased evaluation on unseen data.

---

## 📊 Model Evaluation

Models were evaluated using:
- Accuracy Score
- Classification Report
- Probability Predictions

Each model’s performance was compared on the same test dataset.

---

## 🏆 Best Performing Model

### ✅ **Random Forest Classifier**

**Why Random Forest performed best:**
- Higher accuracy compared to other models
- Better generalization on unseen data
- Handles both categorical and numerical features effectively
- Less prone to overfitting than a single decision tree

Hence, **Random Forest was selected as the final model** for prediction.

---

## 🔮 Prediction on New Customer Data

The final model was used to predict purchase behavior for new customer data.

**Prediction Output:**
- `1` → Customer will buy the travel package
- `0` → Customer will not buy the travel package

---

## 📁 Project Structure

```text
travel-package-purchase-prediction/
│
├── travel.ipynb
├── Travel.csv
└── README.md
```
