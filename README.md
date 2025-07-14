# 📈 Contract Awards Prediction (World Bank Investment Projects)
This project analyzes procurement and supplier-related data from World Bank–funded investment projects to predict the Supplier Contract Amount (USD). It leverages regression-based machine learning algorithms to model contract value using project metadata, procurement strategy, supplier details, and geographic factors.

## 📊 Dataset
- Source: World Bank Investment Project Financing - Contract Awards Dataset
- Records: ~294,000 (reduced after preprocessing and outlier removal)
- Features: Region, Country, Project ID, Procurement Method, Supplier Info, Signing Date, etc.

##🔧 Key Steps
**Data Preprocessing**
-Removed duplicates
-Handled missing values (mode for categorical, median for numerical)
-Converted date columns to datetime format
-Label encoded categorical columns
-Removed outliers in target using the IQR method
-Standardized numerical features using StandardScaler

**Feature Engineering**
-Extracted relevant numerical features for modeling
-Label-encoded all object-type features
-Prepared training/test split with scaled data

**Modeling**
-Algorithms: Linear Regression, Random Forest Regressor
-Evaluated using: MAE, MSE, R² Score
-Visual Tools: Residual plots, Actual vs Predicted scatter, Learning Curves
-Cross-validation (10-fold) for robustness
-Hyperparameter tuning using GridSearchCV for Random Forest
-Model Interpretation
-Feature importance extracted from best Random Forest model
-Residual analysis plotted for error distribution

**🧠 Results**
-Best model(s): Random Forest Regressor (tuned)
-R² Scores:
-Linear Regression: ~0.076 (baseline)
-Random Forest (default): ~0.210
-Random Forest (tuned via GridSearchCV): 0.366 (CV Avg)
-Best RF Hyperparameters:
-n_estimators=100, max_depth=None, min_samples_split=5

##📁 Project Structure
-contract_awards_modeling.ipynb – Main Jupyter Notebook
-contract_data.csv – Dataset
-README.md – Project Overview

