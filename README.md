# Used Car Price Prediction — Rusty Bargain

## Overview
Rusty Bargain is a used car sales service developing an app that allows customers to quickly estimate the market value of their vehicle. Using past listings, I built and compared multiple machine learning models to predict used car prices and determine the most reliable approach for accurate, fast predictions.

## Business Problem
The goal is to provide accurate predictions while keeping training and prediction times fast enough to be used in a real app.
An automated pricing model helps the company:  
- Quickly generate fair market estimates for any vehicle  
- Improve customer trust and experience  
- Support decision-making for buying, selling, and pricing strategies  

**Objective** Create a pricing model that gives reliable estimates while staying quick enough to train and use in practice.

## Highlights & Key Results
- Compared Linear Regression, Random Forest, LightGBM, and CatBoost
- Evaluated models on prediction quality (RMSE), training time, and prediction speed
- LightGBM achieved the best overall balance between accuracy and efficiency
- High-cardinality features (ex: PostalCode) were tested and removed after degrading performance

## Model Performance (Best Runs)

| Model | Relative RMSE | Training Time (s) | Prediction Speed (s) |
|------|---------------|------------------|---------------------|
| Linear Regression | 51.3% | 12.26 | 0.17 |
| Random Forest | 34.4% | 68.71 | 0.25 |
| **LightGBM** | **30.2%** | **19.29** | **5.11** |
| CatBoost | 32.1% | 89.60 | 0.34 |

## Final Model
**LightGBM** was selected as the final model due to:
- Lowest RMSE (30.2%)
- Fast training time
- Fast enough to use in an app without noticeable delays

## Tools & Technologies
Python, pandas, NumPy, scikit-learn, LightGBM, CatBoost, Matplotlib, Jupyter Notebook

## Dataset
The dataset can be downloaded here:  
[Car Data CSV](https://practicum-content.s3.us-west-1.amazonaws.com/datasets/car_data.csv)

After downloading, place the file in the `data/` folder before running the notebook.
## How to Run
1. Clone or download the repository.
2. Ensure `car_data.csv` is in the `data/` folder.
3. Open `price_prediction.ipynb` in Jupyter Notebook or VS Code.
4. Run the cells to replicate the analysis and model results.
