# Hotel Booking Cancellation Prediction

## Overview

Hotel booking cancellations significantly impact revenue, operations, and customer satisfaction in the hospitality industry. This project uses machine learning and time-series forecasting techniques to predict cancellations and identify key factors influencing booking behavior.

The goal is to enable data-driven decision-making to reduce cancellations and improve operational efficiency.

---

## Problem Statement

The objective of this project is to:

* Predict whether a hotel booking will be canceled
* Identify key factors influencing cancellations
* Forecast future cancellation trends

---

## Dataset

* Source: Hotel Bookings Dataset
* Records: 119,390
* Features: 32
* Time Period: 2015–2017

### Target Variable

* `is_canceled`

  * 0 → Not canceled
  * 1 → Canceled

---

## Project Pipeline

1. Data Preprocessing

   * Handled missing values
   * Removed inconsistencies
   * Data type corrections

2. Feature Engineering

   * Total guests
   * Total stay nights
   * Booking cost
   * Family and long-stay indicators

3. Exploratory Data Analysis (EDA)

   * Correlation analysis
   * Cancellation trends
   * Seasonal patterns

4. Predictive Modeling

   * Logistic Regression (baseline)
   * XGBoost (best performing model)
   * Additional models for comparison

5. Time-Series Forecasting

   * Prophet model for trend and seasonality analysis

6. Model Evaluation

   * Accuracy
   * ROC-AUC
   * Precision, Recall, F1-score

---

## Key Insights

* Lead time is the strongest predictor of cancellations
* Longer lead times increase cancellation probability
* Customer type is not a significant predictor
* More special requests reduce cancellations
* Seasonal trends influence booking behavior

---

## Model Performance

| Model               | Accuracy | ROC-AUC |
| ------------------- | -------- | ------- |
| XGBoost             | 76.63%   | 0.7797  |
| Gradient Boosting   | 76.04%   | 0.7617  |
| Random Forest       | 75.39%   | 0.7616  |
| SVM                 | 75.95%   | 0.7264  |
| Logistic Regression | 64.81%   | 0.7185  |
| Naive Bayes         | 35.54%   | 0.6592  |

Best Model: XGBoost

---

## Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Prophet
* Matplotlib, Seaborn
* Imbalanced-learn (SMOTE)

---

## How to Run

1. Clone the repository

2. Install dependencies

```
pip install -r requirements.txt
```

3. Run the notebook

```
jupyter notebook predictive_modeling.ipynb
```

4. Outputs (predictions, metrics, visualizations) will be generated automatically

---

## Project Structure

```
hotel-booking-cancellation/
│
├── hotel_bookings.csv
├── predictive_modeling.ipynb
├── model_comparison_results.csv
├── requirements.txt
└── README.md
```

---

## Conclusion

This project demonstrates how machine learning and time-series forecasting can be used to predict hotel booking cancellations and generate actionable insights.

XGBoost achieved the best performance by capturing complex patterns, while Prophet provided valuable insights into seasonal trends and future forecasts.

---

## Future Improvements

* Further hyperparameter tuning
* Deployment as a web application
* Integration with real-time booking systems
* Incorporating external factors such as events and pricing trends
