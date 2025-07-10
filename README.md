# cardio-risk-prediction
# Objective
This project aims to build a binary classification model to predict cardiovascular disease using health-related data from patients. The model is trained using XGBoost, a powerful gradient boosting algorithm.
# Dataset
The dataset used is cardio_train.csv, which contains medical records of 70,000 patients.
Key features include:
**age (in days)**
**gender**
**height / weight**
**ap_hi / ap_lo (systolic / diastolic pressure)**
**cholesterol, smoke, alco, active**
**cardio (target variable: 1 = has disease, 0 = healthy)**
# Data Preprocessing
Dropped columns: id, active
Filtered out unrealistic blood pressure values:
ap_hi between 80 and 200
ap_lo between 50 and 120
After cleaning: 68,602 rows remain
# Exploratory Data Analysis (EDA)
Histograms were generated to explore variable distributions
Correlation matrix heatmap was plotted:
Highest correlation with cardio: ap_hi, ap_lo, age, cholesterol
# Model: XGBoost Classifier
Data split: 80% training / 20% testing
Accuracy on test set: ~73%
# How to Run
**Install requirements:**
pip install pandas numpy matplotlib seaborn xgboost scikit-learn
**Run the Jupyter Notebook or Python script:**
jupyter notebook cardio_prediction.ipynb

