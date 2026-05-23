# Hypertension Prediction

## Overview
This project explores machine learning methods for predicting hypertension from demographic, lifestyle, and health-related features. The notebook compares a regression-style Random Forest approach with a classification-oriented logistic regression pipeline. The project is a practical exercise in preprocessing mixed feature types, choosing metrics, and evaluating model fit.

## Motivation
Health prediction tasks require careful framing because predictive performance does not imply medical validity or causality. This project demonstrates applied ML skills while also showing the importance of honest limitations, appropriate target framing, and reproducible evaluation. It is intended as an educational data science project, not a diagnostic tool.

## Dataset
- **Source:** Kaggle Hypertension Dataset.
- **File:** `data/hypertension_dataset.csv`
- **Size:** 1,985 records.
- **Target variable:** `Has_Hypertension`, represented as `Yes`/`No` and converted for modeling.
- **Important features:** `Age`, `Salt_Intake`, `Stress_Score`, `BP_History`, `Sleep_Duration`, `BMI`, `Medication`, `Family_History`, `Exercise_Level`, and `Smoking_Status`.
- **Known limitations:** Dataset collection details, representativeness, clinical validation, and measurement procedures are not documented in this repository.

## Methods
- Loaded and inspected the dataset with pandas.
- Encoded categorical variables with one-hot encoding.
- Scaled numeric variables for the logistic regression pipeline.
- Tested a Random Forest regressor and evaluated it with MSE and R-squared.
- Tested logistic regression and evaluated it with accuracy, precision, recall, and F1-score.
- Used visualizations to inspect feature distributions and relationships.

## Results
The notebook reports:

- Random Forest regression-style evaluation: **MSE = 0.04**, **R-squared = 0.82**
- Logistic Regression classification accuracy: **0.8824**

Classification report from the notebook:

| Class | Precision | Recall | F1-score | Support |
| --- | ---: | ---: | ---: | ---: |
| `False` | 0.85 | 0.87 | 0.86 | 101 |
| `True` | 0.90 | 0.89 | 0.90 | 137 |

## Key Insights
- Logistic regression is a more natural baseline than regression for the binary hypertension target.
- Age, lifestyle, and health-history features provide measurable predictive signal in this dataset.
- The reported metrics suggest balanced performance across both classes in the test split.
- Health prediction projects require stronger validation before any real-world interpretation.

## Limitations
- This is not a medical diagnostic model.
- The dataset source and collection process are not sufficiently documented for clinical conclusions.
- The notebook uses a single split and should be validated with cross-validation.
- The Random Forest regressor framing is less appropriate for a binary target than classification models.
- Potential bias across demographic or lifestyle groups has not been evaluated.

## Future Improvements
- Reframe all modeling around classification metrics.
- Add cross-validation and confidence intervals.
- Compare logistic regression, Random Forest classifier, gradient boosting, and calibrated models.
- Add feature importance or coefficient interpretation with caution.
- Add a model card with intended use, non-use cases, and ethical limitations.

## How to Run
```bash
git clone https://github.com/BobbY-24/Hypertension-Prediction-Improvement-2.0.git
cd Hypertension-Prediction-Improvement-2.0
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
pip install -r requirements.txt
jupyter notebook notebooks/hypertension_prediction.ipynb
```

Run the notebook cells from top to bottom. The notebook expects the dataset at `data/hypertension_dataset.csv`.
