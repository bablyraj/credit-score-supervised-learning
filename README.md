# 📊 Supervised Learning Project: Credit Score Classification

---

## 📝 About the Data

The dataset contains a mix of **categorical and numerical features** related to customers' banking and professional details. It includes missing values and anomalies. Two datasets are provided:

- **Train Dataset**: Used to train and test the model.
- **Test Dataset**: Used for making final predictions and submitting results.

---

## 🧠 Problem Statement

You are a **Data Scientist** at a global finance company. Over the years, the company has collected detailed customer and credit-related information.

Now, the company wants to build an **intelligent system** that **classifies customers into credit score brackets** to reduce manual assessment efforts.

---

## 🎯 Objective

Build a **machine learning model** to predict the **Credit Score type** (`Poor`, `Standard`, or `Good`) based on customer features.

---

## 📁 Attributes

1. **ID** - Unique entry ID  
2. **CUSTOMER ID** - Unique person ID  
3. **MONTH** - Month of record  
4. **NAME** - Customer's name  
5. **AGE**  
6. **SSN**  
7. **OCCUPATION**  
8. **ANNUAL INCOME**  
9. **MONTHLY IN-HAND SALARY**  
10. **NUMBANK ACCOUNTS**  
11. **NUM CREDIT CARD**  
12. **INTEREST RATE**  
13. **NUM OF LOAN**  
14. **TYPE OF LOAN**  
15. **DELAY FROM DUE DATE**  
16. **NUM OF DELAYED PAYMENT**  
17. **CHANGED CREDIT LIMIT**  
18. **NUM CREDIT INQUIRIES**  
19. **CREDIT MIX**  
20. **OUTSTANDING DEBT**  
21. **CREDIT UTILIZATION RATIO**  
22. **CREDIT HISTORY AGE**  
23. **PAYMENT OF MIN AMOUNT**  
24. **TOTAL EMI PER MONTH**  
25. **AMOUNT INVESTED MONTHLY**  
26. **PAYMENT BEHAVIOUR**  
27. **MONTHLY BALANCE**

---

## 🧪 Steps to Follow

### 🔹 Step 1: Understand the Business Problem

### 🔹 Step 2: Import Libraries and Setup (Optional)

### 🔹 Step 3: Load Train & Test Datasets

- Check datatypes
- Combine train and test data for cleaning (optional)

---

### 🔹 Step 4: Data Cleaning

#### Clean Categorical Variables:
- Replace anomalies:
  - `OCCUPATION = "_______"` → Replace with mode (customer-wise)
  - `SSN = "#F%$D@*&8"` → Replace with mode
  - `PAYMENT BEHAVIOUR = "!@9#%8"` → Replace with mode

#### Clean Numerical Variables:
- `AGE > 85` → Replace with customer-wise median
- Negative values → Replace with customer-wise median
- Check and handle other anomalies per column

---

### 🔹 Step 5: Feature Engineering

- Convert `CREDIT HISTORY AGE`:  
  Example: "22 Years and 1 Month" → `22.1`

- Clean `PAYMENT OF MIN AMOUNT`: Keep only `Yes` or `No`

- Convert month names to numeric if needed

---

### 🔹 Step 6: Handle Missing Values

- Use **customer-wise median imputation**

---

### 🔹 Step 7: EDA (Exploratory Data Analysis)

- Univariate, Bivariate, and Multivariate analyses
- Identify variables affecting the **target (Credit Score)**

---

### 🔹 Step 8: Separate Train & Test Data

- Use only Train data to build and evaluate models
- Perform `train_test_split` on Train data

---

### 🔹 Step 9: Statistical Analysis

- Test if **Annual Income** differs across credit score classes (ANOVA or Kruskal-Wallis)
- Test **independence** between:
  - `OCCUPATION` and `CREDIT SCORE` (Chi-square test)
  - `PAYMENT BEHAVIOUR` and `CREDIT SCORE`
- Test if **CREDIT UTILIZATION RATIO** medians differ significantly across target classes

---

### 🔹 Step 10: Encode Categorical Variables

- Encode target:  
  - `Poor → 0`, `Standard → 1`, `Good → 2`

---

### 🔹 Step 11: Scale Numerical Features *(Optional)*

---

### 🔹 Step 12: Train-Test Split on Train Data

---

### 🔹 Step 13: Build a Baseline Model

- Try **Logistic Regression**, **Decision Tree**, or similar

---

### 🔹 Step 14: Train Other Models

- Try **Random Forest**, **XGBoost**, **SVM**, **KNN**, etc.
- Compare performance (accuracy, F1-score, etc.)

---

### 🔹 Step 15: Feature Selection

- Use feature importance, mutual information, or model-based selection

---

### 🔹 Step 16: Tune Final Model

- Use **GridSearchCV**, **RandomizedSearchCV**, or Bayesian optimization

---

### 🔹 Step 17: Cross-Validation

- Validate with **k-fold cross-validation** using best parameters

---

### 🔹 Step 18: Predict on Test Data

- Predict target for the Test dataset
- Create submission file:  
  `ID | PREDICTED CREDIT SCORE`

---

### 🔹 Step 19: Business Insights

- Summarize **key insights** from data and model
- Suggest **actions for credit risk management**

---

### 🔹 Step 20: Save Final Submission Dataset

- Save as `.csv` file

---

### 🔹 Step 21: Submit Solution

- Submit cleaned dataset + output predictions

