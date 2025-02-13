# ML Regression Challenge

## 📌 Project Overview
This project focuses on solving a **machine learning regression problem** by exploring multiple regression models, applying **feature engineering**, and evaluating models using **Mean Absolute Error (MAE)** as the primary metric.

## 🚀 Steps Followed

### 1️⃣ Data Loading & Inspection
- Load dataset with and without supplemental data.
- Perform initial inspection using `df.head()`, `df.shape`, `df.info()`, and `df.describe()`.
- Apply domain knowledge to understand the context of the data.

### 2️⃣ Exploratory Data Analysis (EDA)
- Analyze distributions of numerical features using **histograms & box plots**.
- Check **correlation** between numerical features and target variable.
- Identify unique values in categorical features.
- Detect noise and anomalies in dataset (e.g., negative values, missing spaces).

### 3️⃣ Feature Engineering
#### **Feature Extraction**
- Extracted **year/month/day/hour** from `Timeutc` to capture seasonal effects.
- Created new features from `ResponseValue` and `UserID`.
- Imputed missing values for users not present in both training and test sets.

#### **Feature Transformation**
- **Label Encoding**: Applied to `QuestionTiming`, `Timeutc`.
- **One-Hot Encoding**: Applied to `CurrentGameMode`, `CurrentTask`, `LastTask`.
- **Standardization**: Applied to `CurrentSessionLength`.

### 4️⃣ Train-Test Splitting
- **Hold-out approach**: 80% training, 20% validation.
- **K-Fold Cross-Validation**: Attempted but faced memory/capacity limitations.

### 5️⃣ Model Training & Evaluation
#### **Models Used**
- Dummy Regressor (Baseline)
- **Linear Regression**
- **DecisionTreeRegressor**
- **RandomForestRegressor** ✅ (Best Model)
- **Neural Network**
- **GradientBoostingRegressor**
- **MLPRegressor (2nd Polynomial)**
- **KNeighborsRegressor**
- **Support Vector Regressor (SVR)**
- **Lasso, Ridge, ElasticNet**

#### **Model Selection & Hyperparameter Tuning**
- Faced memory/capacity issues while tuning.
- Selected the **best model** using MAE:
  - **RandomForestRegressor achieved MAE = 111**.
  - **Baseline Dummy Regressor MAE = 172**.
  - **Best performance in class: MAE = 100**.

### 6️⃣ Discussion & Performance Evaluation
- **RandomForestRegressor** demonstrated strong generalization.
- **Gradient Boosting & Neural Network** performed well but lacked interpretability.
- Compared to class benchmark (MAE = 100), our model had a competitive performance.

## 🔥 Key Findings
✅ Feature Engineering significantly improved model performance.  
✅ **RandomForestRegressor** was the best trade-off between accuracy and interpretability.  
✅ More computational power could enhance hyperparameter tuning and K-Fold testing.  

## 📈 Future Enhancements
- Implement **advanced hyperparameter tuning**.
- Optimize feature selection for better model interpretability.
- Experiment with **ensemble techniques** for better performance.

## 📬 Contact
For queries, feel free to reach out via **GitHub Issues** or email!

_⭐ If you find this project useful, please give it a star! ⭐_
