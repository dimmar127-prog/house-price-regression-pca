<a href="https://colab.research.google.com/github/dimmar127-prog/house-price-regression-pca/blob/main/house_pricing_model.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# 🏡 House Price Prediction & PCA Analysis

## 📌 Project Overview
This project tackles a classic regression problem: predicting house prices based on various property features. Beyond building predictive models, this analysis heavily focuses on data engineering techniques—specifically exploring how dimensionality reduction (PCA) impacts the performance of both linear and tree-based machine learning models.

## 💾 The Dataset
The dataset consists of housing records with various descriptive features (e.g., square footage, number of rooms, location metrics) and a continuous target variable: **Price**. 
* **Preprocessing applied:** Categorical encoding (One-Hot/Label encoding), handling missing values, and feature scaling (Standardization) to prepare the data for distance-based algorithms and PCA.

## 🛠️ Methods & Technologies Used
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Techniques:** Feature Engineering, Dimensionality Reduction (Principal Component Analysis)
* **Model Validation:** 5-Fold Cross-Validation to ensure robust performance metrics and prevent overfitting.
* **Models Evaluated:** Linear Regression, Ridge, Lasso, Decision Trees, Random Forest

## 📊 Key Findings & Mathematical Intuition
* **Model Performance:** Random Forest was the best-performing model overall, achieving an R² score of 0.87 before PCA.
* **The Impact of PCA:** Applying PCA to reduce the dataset to 10 principal components actually *decreased* model performance across the board. The Random Forest R² dropped to 0.79, indicating that the discarded components contained crucial variance needed for accurate pricing.
* **Tree Models vs. PCA:** The Decision Tree suffered the most significant performance loss after PCA. This highlights a key mathematical intuition: because PCA rotates axes to create abstract, linearly independent feature combinations, decision trees struggle to find meaningful, orthogonal split points. They lose their ability to isolate non-linear patterns effectively.
* **Linear Models:** Interestingly, Linear, Ridge, and Lasso regressions converged to the exact same score (0.66) after PCA, likely due to the perfectly uncorrelated nature of the principal components.


---
*Note: This project was co-authored with Kaptanis as part of the Machine Learning coursework at International Hellenic University.*
