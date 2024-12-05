
# Product Sales Prediction and Analysis

This project focuses on predicting the quantity of products sold based on various factors such as product features, pricing, stock levels, and temporal attributes. The project involves data cleaning, feature engineering, model training, and evaluation using machine learning techniques.

## Project Overview

This analysis aims to predict the quantity of products sold using historical sales data. The steps include:

1. Data loading and exploration.
2. Feature engineering and data preparation.
3. Handling missing values and evaluating models.
4. Visualization of results and feature importance analysis.
5. Enhanced feature engineering and outlier removal.
6. Model evaluation and improvement.

## Dataset

The dataset used for this project contains product sales information, including:

- **Product Name**
- **Category**
- **Company**
- **Salt Composition**
- **Type**
- **Quantity Sold**
- **Date of Sale**
- **Price**
- **Stock Level**

The data is sourced from an Excel file (`Product_Sales.xlsx`).

## Steps Involved

### 1. Data Loading and Exploration
The dataset is loaded into a pandas DataFrame and explored for initial insights. Missing values, outliers, and distributions are examined to understand the data better.

### 2. Feature Engineering and Data Preparation
The following features were created and transformed:
- Temporal features such as Month, Day, Day of Week, Quarter, and IsWeekend.
- Price-based features like Price per Unit and Stock-Price Ratio.
- Categorical variables were encoded using Label Encoding.

### 3. Model Training and Evaluation
Models evaluated:
- Linear Regression
- Random Forest Regressor
- Support Vector Regression (SVR)

Evaluation metrics:
- Mean Squared Error (MSE)
- R² Score

### 4. Feature Importance and Visualization
The most important features for predicting quantity sold were analyzed using a Random Forest model. Visualizations such as scatter plots and bar charts were created to show actual vs predicted sales and feature importance.

### 5. Data Cleaning and Model Retraining
Outliers were removed using the IQR method, and missing values were imputed. After these steps, the models were retrained, and performance improved.

### 6. Final Results and Business Insights
The Random Forest model achieved the best performance with an R² score of 0.66, indicating that it explained 66% of the variance in the target variable. Key insights:
- **Price per unit** is the most important factor for predicting sales quantity.
- **Price** and **Stock-Price Ratio** also contribute significantly.
- **Stock Level** has a lesser impact.

## Model Performance

| Model              | Mean Squared Error | R² Score |
|--------------------|--------------------|----------|
| Linear Regression  | 226.40             | 0.65     |
| Random Forest      | 219.24             | 0.66     |
| SVR                | 682.29             | -0.05    |

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/product-sales-prediction.git
    ```

2. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook (`Product_Sales_Analysis.ipynb`) to reproduce the analysis and results.

## Requirements

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Conclusion

The project demonstrates how to preprocess sales data, engineer features, train machine learning models, and derive business insights for improving product sales prediction. Future improvements can include hyperparameter tuning, adding more complex features, or using deep learning techniques.

