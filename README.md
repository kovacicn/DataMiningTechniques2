# Data Mining Techniques 2
# Expedia Hotel Ranking

This repository contains the code for Assignment 2 of the **Data Mining Techniques** course at Vrije Universiteit Amsterdam.

## Project Overview

The goal of this project was to rank hotel properties returned for an Expedia search according to how likely a user is to interact with or book them. Performance was evaluated using **NDCG@5**.

The project covers the complete data-mining pipeline, including:

- Exploratory data analysis (EDA)
- Missing-value handling and preprocessing
- Search-relative and popularity-based feature engineering
- Feature evaluation and selection
- Collaborative filtering (CF) features
- Learning-to-rank models using LightGBM, XGBoost and CatBoost
- Hyperparameter tuning with Optuna
- Neural-network embeddings using autoencoders and supervised MLPs
- Generation of ranked Kaggle submissions

The final approach combined **LightGBM and XGBoost using RidgeCV**, together with embeddings learned by a supervised MLP. This was the best-performing approach in our experiments.

## Repository Structure

The main notebooks roughly follow the project workflow:

- `1task2.ipynb` – Exploratory data analysis and investigation of booking/click behavior.
- `2missing_values.ipynb` – Missing-value analysis and data imputation.
- `3feature_framework_final.ipynb` – Feature engineering, evaluation and feature selection.
- `4CFKF.ipynb` – Collaborative filtering and destination-specific hotel popularity.
- `5lightgbm_optuna_tuning.ipynb` – LightGBM ranking and hyperparameter tuning.
- `5popularityCF.ipynb` – Creation and application of collaborative-filtering popularity scores.
- `xgboost_ranker_optuna_Used.ipynb` – XGBoost ranking model with Optuna tuning.
- `xgboost_submission.ipynb` – Generation of ranked predictions for Kaggle submission.

Additional notebooks contain intermediate experiments and alternative versions of the feature-engineering and modeling pipelines.

## Data

The project uses the Expedia hotel-search dataset provided for the VU Data Mining Techniques Kaggle competition. The raw dataset is not included in this repository.

For additional details about the methodology, experiments and results, see the included project report:

`VU-DM-2025-Group-14-A2 (1).pdf`
