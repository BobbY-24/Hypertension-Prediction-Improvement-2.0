Hypertension Prediction Project
📌 Overview

This project explores different machine learning methods to predict hypertension based on demographic, lifestyle, and health-related features. The dataset was sourced from Kaggle and analyzed using Python with pandas, scikit-learn, and visualization libraries.

The notebook includes:

Data loading and exploration

Preprocessing (encoding categorical variables, scaling numerical features)

Model building with two approaches:

Random Forest Regressor + OneHotEncoder

Logistic Regression + OneHotEncoder & StandardScaler

Model evaluation with metrics such as MSE, R², Accuracy, and Classification Report

⚙️ Installation

Clone the repository and install dependencies:

git clone <your_repo_url>
cd hypertension-prediction
pip install -r requirements.txt


requirements.txt should include:

pandas
numpy
matplotlib
seaborn
scikit-learn

📂 Dataset

Source: Kaggle (Hypertension Dataset)

Target Variable: Has_Hypertension (Yes/No → converted to Boolean)

Features Used:

Numerical: Age, Salt_Intake, Stress_Score, Sleep_Duration, BMI

Categorical: BP_History, Medication, Family_History, Exercise_Level, Smoking_Status

🔬 Methods
1. Random Forest Approach

Preprocessing: One-hot encoding for categorical features, passthrough for numerical.

Model: RandomForestRegressor (100 estimators, random_state=42).

Evaluation:

Mean Squared Error (MSE)

R² Score

2. Logistic Regression Approach

Preprocessing:

StandardScaler for numerical features

OneHotEncoder for categorical features

Model: LogisticRegression (max_iter=1000, random_state=42).

Evaluation:

Accuracy

Classification Report (Precision, Recall, F1-score)

📊 Results

Random Forest: Provided regression-based evaluation with MSE and R².

Logistic Regression: Better suited for classification, offering accuracy and detailed performance metrics.

Method 1: 

Mean Squared Error: 0.04
R^2 Score: 0.82

Method 2: 

Accuracy: 0.8823529411764706
Classification Report:
               precision    recall  f1-score   support

       False       0.85      0.87      0.86       101
        True       0.90      0.89      0.90       137

    accuracy                           0.88       238
   macro avg       0.88      0.88      0.88       238
weighted avg       0.88      0.88      0.88       238


🚀 Next Steps

Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)

Try alternative models (XGBoost, SVM, Neural Networks)

Feature importance analysis

Cross-validation for robust evaluation

✍️ Author

Bob Yan
