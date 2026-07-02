# Heart Disease Prediction Project

This project analyzes heart disease data to predict the presence and severity of the condition using machine learning techniques, specifically comparing Decision Trees and Random Forests.

## Project Features

### 1. Visualizing Decision Trees
We generated a graphical representation of the trained **Decision Tree** model. This visualization allows us to:
* **Understand Logic**: Trace the exact 'if-then' rules the model uses (e.g., thresholding `thalch` or `oldpeak`).
* **Analyze Purity**: Observe the Gini impurity and sample distribution at each node.
* **Interpret Path**: Identify the most critical early splits that lead to high-confidence classifications.

### 2. Comparing Single Tree vs. Forest
We evaluated two models to understand the benefit of ensemble learning:
* **Decision Tree**: A single model that is easy to interpret but prone to overfitting. In this project, it achieved lower accuracy (~51%) and showed more sensitivity to noise.
* **Random Forest**: An ensemble of 100 trees. It significantly outperformed the single tree (~60% accuracy), demonstrating better generalization and more robust recall across different disease stages.

### 3. Plotting Feature Importance
Using the Random Forest model, we extracted and visualized **Feature Importance Scores**. Key findings include:
* **Risk Factors**: Features like `thalch` (maximum heart rate achieved), `age`, and `chol` (cholesterol) were identified as the strongest predictors.
* **Clinical Value**: This visualization helps healthcare providers identify which patient metrics are most critical when assessing heart disease risk.
## Project Overview
This analytical study focuses on the **UCI Heart Disease Dataset**, which contains patient records from four different geographic locations. The goal is to move beyond simple binary classification (disease vs. no disease) and predict the **severity (stages 0-4)** of coronary artery disease.

### Workflow Summary:
1.  **Data Acquisition**: Loading multi-center clinical data via `kagglehub`.
2.  **Data Cleaning**: Handling significant missing values in columns like `trestbps`, `chol`, and `oldpeak` using median/mode imputation.
3.  **Feature Engineering**: Encoding categorical variables (`sex`, `cp`, `thal`, etc.) into a machine-readable format.
4.  **Model Benchmarking**: Training and comparing a robust **Random Forest** ensemble against a baseline **Decision Tree**.
5.  **Interpretability**: Utilizing feature importance and tree visualization to understand which biological markers most heavily influence clinical outcomes
