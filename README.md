# Titanic Survival Prediction: Exploratory Data Analysis & Machine Learning

A beginner machine-learning project using the **Titanic: Machine Learning from Disaster** competition on Kaggle. The goal is to predict whether a passenger survived using passenger information such as class, age, sex, fare, family relationships, embarkation port, cabin deck, and passenger title.

> **Project status:** First end-to-end model completed; a Logistic Regression submission was accepted by Kaggle.

## Project highlights

- Explored passenger survival patterns with Pandas, Matplotlib, and Seaborn.
- Investigated missing values and relationships between survival and passenger features.
- Engineered features including `FamilySize`, `Deck`, and `Title`.
- Built preprocessing pipelines for missing-value imputation, scaling, and categorical encoding.
- Compared Logistic Regression with Random Forest.
- Used stratified train/validation splitting, cross-validation, and hyperparameter search.
- Generated predictions for Kaggle's competition test data.

## Results

| Evaluation | Result |
|---|---:|
| Logistic Regression validation accuracy (179-passenger holdout) | **82.12%** |
| Best Logistic Regression 5-fold CV accuracy during training-only tuning | **82.45%** |
| Random Forest validation accuracy | 79.89% |
| Kaggle public leaderboard score | **0.77272** |

The Kaggle leaderboard score is a separate evaluation from the local validation accuracy. It should not be interpreted as the same metric on the same passengers.

## Repository structure

```text
.
├── README.md
├── requirements.txt
├── .gitignore
└── notebooks/
    └── titanic-survival-prediction.ipynb
```

## Notebook

The main project notebook is intended to be stored at:

`notebooks/titanic-survival-prediction.ipynb`

It documents the workflow from exploratory data analysis through preprocessing, model evaluation, and Kaggle prediction generation.

## Tools and libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

Install the dependencies with:

```bash
pip install -r requirements.txt
```

## Dataset

The data comes from the [Titanic: Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic) competition on Kaggle.

The competition data is **not included in this repository**. Download it from Kaggle after accepting the competition rules. When running the notebook on Kaggle, attach the Titanic competition dataset as an input. The original Kaggle notebook uses Kaggle's input directory paths, so paths may need to be updated when running outside Kaggle.

## How to reproduce

1. Open the Kaggle competition page and accept the competition rules.
2. Download `train.csv` and `test.csv`, or attach the competition data to a Kaggle Notebook.
3. Open `notebooks/titanic-survival-prediction.ipynb` in Jupyter or Kaggle.
4. Install the dependencies listed in `requirements.txt` if running locally.
5. Update the dataset paths for your environment, then run the notebook from top to bottom.

The notebook uses a fixed random seed (`42`) for the train/validation split and cross-validation setup where specified. Small differences may occur with different library versions or execution environments.

## Notes

- `submission.csv` is a generated competition output and is intentionally not included.
- Competition datasets and credentials (including `kaggle.json`) should not be committed to this repository.
- The reported leaderboard score belongs to the submitted model version described in the notebook.

## Acknowledgements

Dataset and competition: [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic).
