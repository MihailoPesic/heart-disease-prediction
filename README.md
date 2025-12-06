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

Work in progress - check back for updates
