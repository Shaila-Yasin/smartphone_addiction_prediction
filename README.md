# Smartphone Addiction Prediction

A machine learning project developed for the **Kaggle Playground Series S6E8: Predicting Smartphone Addiction** competition.

The goal of the competition is to predict the probability of `addicted_label` for each individual in the test dataset.

## Dataset

https://www.kaggle.com/competitions/playground-series-s6e8/data

## Competition

* **Competition:** Playground Series - Season 6, Episode 8
* **Task:** Binary classification
* **Target:** `addicted_label`
* **Evaluation:** Predictions are submitted as probabilities
* **Platform:** Kaggle

## Project Overview

This project follows a complete beginner-friendly machine learning workflow:

1. Exploratory Data Analysis (EDA)
2. Missing-value analysis
3. Data preprocessing
4. Feature analysis
5. Model training
6. Model evaluation
7. Model comparison
8. Prediction probability generation
9. Kaggle submission

## Dataset Features

The dataset contains information related to smartphone usage and lifestyle, including:

* Age
* Daily screen time
* Social media usage
* Gaming hours
* Work/study hours
* Sleep hours
* Notifications per day
* App opens per day
* Weekend screen time
* Gender
* Stress level
* Academic/work impact

The target variable is:

```text
addicted_label
```

## Missing-Value Analysis

The dataset contains missing values across several features. Instead of immediately dropping all rows containing missing values, the project first investigates the pattern and proportion of missing data before deciding how to handle it.

This was important because simply applying `dropna()` could remove a substantial amount of potentially useful training data.

## Models

Multiple machine learning approaches were experimented with and compared.

### Selected Model

The `model HistGradientBoosting` used for the better-performing submission was selected based on validation/competition performance.

### LightGBM Experiment

LightGBM was also tested as an additional experiment. Although it was included as part of the model experimentation process, its submission performed worse than the earlier submission, so it was not selected as the final approach.

This project keeps the experiment documented because comparing approaches and learning from lower-performing models is an important part of the machine learning workflow.

## Submission

The competition requires a probability prediction for each `id` rather than a hard `0`/`1` prediction.

The submission format is:

```text
id,addicted_label
691369,0.2
691370,0.3
691371,0.1
```

Predictions are generated using the model's class probabilities.

## Results

## Competition Results

| Experiment | Validation ROC-AUC | Kaggle Result | Status |
|------------|-------------------:|--------------:|--------|
| HistGradientBoosting | **0.95793** | **0.95** | Selected |
| LightGBM | **0.96014** | — | Experiment |

- Kaggle leaderboard rank: 2,901/3531


## What I Learned

Through this competition, I practiced:

* Exploratory data analysis
* Handling missing values
* Feature-target analysis
* Classification
* Probability-based predictions
* Model comparison
* Kaggle submissions
* Iterative experimentation
* Maintaining a reproducible machine learning project

## Repository Structure

```text
smartphone-addiction-prediction/
│
├── data 
|   ├── test.csv
|   └── train.csv
|
├── notebooks/
│   ├── 00_eda.ipynb
│   ├── 01_data_cleaning.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_training.ipynb
│   ├── 04_model_tunning.ipynb
│   ├── 05_final_submission.ipynb
│   └── 06_lightbgm_model.ipynb
│
├── models
|   └── tuned_hist_gradient_model.ipynb
|
├── README.md
├── requirements.txt
└── .gitignore
```

Competition data is not included in this repository.

## Kaggle

Competition: https://www.kaggle.com/competitions/playground-series-s6e8

## Author

**Shaila Yasin**

## GitHub

https://github.com/Shaila-Yasin

Built as a learning project while developing skills in Data Science and Machine Learning.
