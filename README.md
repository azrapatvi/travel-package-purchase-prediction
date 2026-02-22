# 🧳 Travel Package Purchase Prediction

## 📌 Project Description
This project predicts whether a customer will purchase a travel package using machine learning techniques.  
The goal is to help travel companies identify potential customers and improve targeted marketing strategies.

The complete workflow — from data preprocessing to model evaluation and prediction — is implemented inside a single Jupyter Notebook.

---

## 🎯 Objective
To build a classification model that predicts:

- `1` → Customer **will purchase** the travel package  
- `0` → Customer **will not purchase** the travel package  

---

## 📂 Dataset Information
The dataset consists of customer demographic and behavioral data.

### Target Variable
- **ProdTaken**
  - `1` → Purchased
  - `0` → Not Purchased

### Key Features
- Age  
- Gender  
- Marital Status  
- Type of Contact  
- Occupation  
- Monthly Income  
- Number of Trips  
- Duration of Pitch  
- Product Feedback Score  

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  

---

## 📓 Notebook Explanation (`travel-package-purchase-prediction.ipynb`)

### 1. Importing Libraries
All necessary Python libraries for data analysis, visualization, preprocessing, and machine learning are imported.

---

### 2. Loading the Dataset
- Dataset is loaded using `pandas.read_csv()`
- Basic inspection is done using:
  - `.head()`
  - `.shape`
  - `.info()`
  - `.describe()`

---

### 3. Data Cleaning

#### Handling Missing Values
- Numerical columns → Filled using **median**
- Categorical columns → Filled using **mode**

#### Fixing Inconsistent Entries
- `Fe Male` → `Female`
- `Unmarried` → `Single`

#### Dropping Irrelevant Columns
- `CustomerID` is removed as it does not contribute to prediction.

---

### 4. Exploratory Data Analysis (EDA)
- Distribution of missing values is visualized using histograms
- Helps in understanding data spread and skewness

---

### 5. Feature Engineering
- A new feature **Total_Visitors** is created by combining:
  - `NumberOfPersonVisiting`
  - `NumberOfChildrenVisiting`
- Original columns are dropped to avoid redundancy.

---

### 6. Feature Separation
- Numerical features and categorical features are separated
- Required for applying different preprocessing techniques

---

### 7. Train-Test Split
- Dataset is split into:
  - **80% Training data**
  - **20% Testing data**

---

### 8. Data Preprocessing Pipeline
A `ColumnTransformer` pipeline is used:

- Numerical Features → `StandardScaler`
- Categorical Features → `OneHotEncoder`

This ensures consistent preprocessing during training and prediction.

---

### 9. Model Training
The following models are trained and evaluated:

- Logistic Regression  
- Decision Tree Classifier  
- Random Forest Classifier  
- Gradient Boosting Classifier  
- AdaBoost Classifier  

---

### 10. Model Evaluation
Each model is evaluated using:
- Accuracy Score
- Classification Report

---

### 11. Hyperparameter Tuning
- `RandomizedSearchCV` is used to optimize model performance
- Best parameters are selected for each model

---

### 12. Best Model Selection
- **Gradient Boosting Classifier** performs best
- Selected as the final model

---

### 13. Final Prediction
- Model predicts purchase decision for new customer data
- Output includes:
  - Prediction (0 or 1)
  - Probability score

---
