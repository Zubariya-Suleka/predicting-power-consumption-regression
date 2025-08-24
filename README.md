🔋 Power Consumption Prediction – Wellington, New Zealand
📌 Project Overview

This project focuses on predicting Zone 1 Power Consumption in Wellington, New Zealand using various environmental and meteorological factors.
The goal is to build a machine learning model that helps optimize power usage forecasting for better energy management and planning.

📊 Dataset Overview

Total Rows: 52,540

Features: 7 predictors, 1 target (Power Consumption)

Data Types: 6 numerical, 1 categorical

Missing Data: ~1.44%

Target Variable: Continuous and skewed

Predictor Variables:

Temperature

Humidity

Wind Speed

General Diffuse Flows

Diffuse Flows

Air Quality Index

Cloudiness

Target Variable:

Zone 1 Power Consumption

🧹 Data Preprocessing

Cleaning: Renamed columns, extracted numeric values, handled missing values (mean/median imputation).

Outliers: Capped using IQR method.

Scaling: StandardScaler applied on numerical features.

Train-Test Split: 80% train, 20% test.

📈 Exploratory Data Analysis (EDA)

Target (Power Consumption) is right-skewed and multimodal.

Temperature shows a bimodal pattern, reflecting mixed seasonal effects.

Humidity distribution is left-skewed (most values >60%).

Features exhibit mostly weak/nonlinear relationships with the target.

🔎 Model Development
Baseline & Linear Models
Model	R²	RMSE
Dummy Regressor	0.0000	8037.41
Linear Regression	0.3302	6577.95
Ridge Regression	0.3302	6577.93
Polynomial Regression	0.4065	6191.42
Decision Tree Regressor	0.2703	6865.89
Advanced Models
Model	R²	RMSE
KNN Regression	0.3985	6233.50
Random Forest Regression	0.6361	4848.79
XGBoost Regression	0.5507	5387.54
Stacking Ensemble	0.5928	5129.15
🌟 Feature Importance

Top features influencing power consumption:

Temperature

Humidity

Wind Speed

Cloudiness contributed marginally – removing it slightly worsened model performance.

⚙️ Hyperparameter Tuning

Random Forest: Slight performance drop after tuning (best kept at defaults).

XGBoost: Tuning did not improve results.

✅ Final Model

Chosen Model: Random Forest Regressor

Cross-Validation: R² = 0.6144, RMSE = 4977.35

Test Results: R² = 0.6361, RMSE = 4848.79

🚀 How to Run

Clone the repository:

git clone https://github.com/Zubariya-Suleka/predicting-power-consumption-regression.git
cd predicting-power-consumption-regression


📌 Future Improvements

Incorporate seasonality/time-series modeling.

Add more meteorological predictors.

Use deep learning models (LSTM, GRU) for sequential patterns.

Explore automated hyperparameter optimization (Optuna, Bayesian search).

👩‍💻 Author

Zubariya Suleka Z
