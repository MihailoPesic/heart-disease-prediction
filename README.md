# Heart Disease Prediction

Predicting heart disease risk using patient clinical data. Working with the UCI Heart Disease dataset to build classification models and understand which factors are most important.

## About

Dataset from [Kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset) with medical measurements like age, cholesterol, blood pressure, etc. The goal is to predict presence of heart disease.

Main things I want to explore:
- What features are actually useful for prediction
- How different models compare (logistic regression, random forest, etc.)
- Can we make the models interpretable for a medical context

## Structure

```
heart-disease/
├── data/              # datasets
├── notebooks/         # analysis notebooks
├── src/              # helper functions
├── models/           # saved models
└── reports/          # plots and results
```

## Setup

Create venv and install packages:

```bash
python -m venv venv
source venv/Scripts/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
```

## Tech Stack

Python 3.13, pandas, scikit-learn, matplotlib, seaborn, jupyter

---

## Status
next: hyperparameter tuning, cross-validation

## Results

After removing duplicates (723 duplicate rows), cleaned dataset contains 302 unique patients(these are big improvements).

**Model Performance:**
- Logistic Regression: **80.3% accuracy**, 0.871 ROC-AUC
- Random Forest: 75.0% accuracy, 0.861 ROC-AUC

**Most Important Features:**
1. Chest pain type (cp)
2. Max heart rate (thalach)
3. Number of vessels colored (ca)

**Key Findings:**
- Categorical features showed stronger predictive power than continuous ones
- Dataset exhibits sampling bias - clinical patients vs general population
- Cholesterol and blood pressure had weak signals due to treatment effects

## Limitations & Considerations

This dataset has known limitations:
- Small sample size (~300 patients from Cleveland clinic only)
- Sampling bias - clinical population, not general screening
- Some counterintuitive patterns due to treatment effects
- Model predicts diagnostic classification, not future risk

