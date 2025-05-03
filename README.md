# Project Overview : Uber Fare-Prediction-Models

📖 About the Project
This project focuses on building a regression model that predicts the fare amount of Uber rides based on various factors such as pickup/drop-off coordinates, passenger count, and trip distance. The dataset is derived from NYC Uber trips and aims to demonstrate practical applications of data cleaning, feature engineering, and model evaluation.

✨ Features
- Data cleaning and preprocessing of real-world trip records
- Feature extraction from timestamps and geolocation data
- Visualization of data distributions and correlations
- Distance calculation using the Haversine formula
- Model training using Linear Regression and Random Forest Regressor
- Performance comparison using RMSE and R² metrics

## 🧰 Tech Stack
- Language: Python
- Environment: Jupyter Notebook
- Libraries Used:
- pandas for data manipulation
- numpy for numerical operations
- matplotlib and seaborn for data visualization
- scikit-learn for machine learning models and metrics
- math for Haversine distance calculation

## 📊 Data Processing
Dataset: Uber NYC fare data

## Cleaning Tasks:
- Removed missing values
- Dropped rows with negative or zero distances/fare amounts
- Filtered unrealistic coordinates

## Feature Engineering:
- Extracted hour, weekday, and month from pickup datetime
- Calculated distance between pickup and drop-off using the Haversine formula

## 🧠 Model Training
Multiple regression models were trained and evaluated to predict Uber fare amounts:
- Linear Regression: Used as a baseline model to establish a point of comparison. It used all numeric and engineered features but was limited in handling complex, non-linear relationships.
- Random Forest Regressor: An ensemble-based model that improved prediction accuracy by capturing feature interactions and reducing overfitting through averaging.
- XGBoost: A gradient boosting model known for its speed and performance, especially on structured/tabular data.
- LightGBM: A high-performance boosting framework that is faster and more efficient with large datasets. It delivered the best overall results in this project.
- CatBoost: A gradient boosting model optimized for categorical features. It performed competitively and required minimal preprocessing.

Each model was evaluated using:
Root Mean Square Error (RMSE): To measure prediction error.
R² Score: To quantify the proportion of variance explained by the model.

### Performance was evaluated using:
- RMSE (Root Mean Square Error)
- R² Score (Coefficient of Determination)

## Results
### 📊 Model Performance Comparison (Phase-1)
| Model            | RMSE  | R² Score |
|------------------|-------|----------|
| Random Forest    | 3.24  | 0.65     |
| XGBoost          | 3.07  | 0.69     |
| LightGBM         | 2.99  | 0.70     |


### 📊 Final Model Performance Comparison (Phase-2)

| Model             | RMSE     | R² Score  |
|------------------|----------|-----------|
| Linear Regression | 5.563649 | -0.026717 |
| XGBoost           | 2.777773 | 0.744068  |
| LightGBM          | 2.992365 | 0.702997  |

### 📊 Final Model Performance Comparison (Phase-3)

| Model   | Metric            | Value   |
|---------|-------------------|---------|
| **XGBoost** | RMSE              | 3.1918  |
|           | R² Score          | 0.7744  |
| **LGBM**   | RMSE              | 3.1142  |
|           | R² Score          | 0.7852  |

### 📊 Final Model Performance Comparison (Phase-4)

| Model   | Metric            | Value   |
|---------|-------------------|---------|
| **LightGBM** | RMSE              | 2.8719  |
|           | R² Score          | 0.8173  |
| **Final Model** | RMSE              | 2.8007  |
|           | R² Score          | 0.8263  |

---

### ✅ Accuracy Interpretation (from R² Score)

- **R² Score close to 1**: Model makes accurate predictions.
- **R² Score close to 0 or negative**: Poor predictive performance.

---

### 🧠 Logic Summary

> The best model is the one that:
- Minimizes **RMSE**
- Shows **consistent and stable predictions**
- Gives **predicted fares close to actual fares**


