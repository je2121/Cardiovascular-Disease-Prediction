# Cardiovascular Disease Prediction

Predicting the presence of cardiovascular disease from patient health metrics using XGBoost.

## Results

| Metric | Score |
|--------|-------|
| Accuracy | ~72% |
| ROC-AUC | ~79% |
| CV AUC (10-fold) | ~79% ± 0.003 |


## Setup

1. Clone the repo
   ```bash
   git clone https://github.com/je2121/cvd-prediction-research.git
   cd cvd-prediction-research
   ```

2. Install dependencies
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost joblib
   ```

3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset) and copy path `cardio_train.csv` 

4. Open and run

## Approach

- **Cleaning** — removed duplicate rows and biologically impossible clinical values (e.g. blood pressure outside valid range)
- **Feature engineering** — derived BMI, obesity/overweight flags, hypertension flag, pulse pressure, and an age × BMI
- **Modelling** — XGBoost classifier with stratified 10-fold cross-validation
- **Evaluation** — accuracy, ROC-AUC, confusion matrix, classification report

## Dataset

Cardiovascular Disease dataset from Kaggle — 70,000 patient records with 11 clinical features.  
Source: https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset
