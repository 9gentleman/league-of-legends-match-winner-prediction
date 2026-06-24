# League of Legends Match Winner Prediction

This project focuses on predicting the winner of League of Legends matches using early-game statistics from the first 10 minutes.

The main objective is to build a machine learning-based decision support system that analyzes early-game economic, tactical, and map-control indicators to estimate the final match outcome.

## Project Overview

League of Legends is a competitive MOBA game where two teams compete to destroy the opponent's Nexus. Since early-game decisions strongly affect the rest of the match, analyzing the first 10 minutes can provide valuable insights for players, coaches, and esports analysts.

This project uses match data from high-level competitive games and applies machine learning models to predict whether the blue team will win or lose based on early-game metrics.

## Dataset

The dataset contains high-level League of Legends match statistics.

The analysis focuses only on the first 10 minutes of each match. The dataset includes variables related to gold difference, experience difference, kills, assists, deaths, first blood, dragons, heralds, minions, and vision control.

After data cleaning, the final dataset contains 9,686 matches and 40 variables.

The dataset itself is not included in this repository due to external dataset access and file size considerations.

## Data Preprocessing

The project includes the following preprocessing steps:

* Missing value check
* Duplicate row check
* Outlier detection using IQR method
* Removal of extreme match records
* Feature selection
* Train / validation / test split
* Class balance control

The final split strategy:

* Training set: 80%
* Validation set: 10%
* Test set: 10%

## Exploratory Data Analysis

The project examines early-game indicators and their relationship with match outcome.

Key analysis topics include:

* Correlation between early-game variables and match result
* Gold difference and experience difference analysis
* First blood impact on win rate
* Dragon and Herald objective control
* Vision and map-control statistics
* Early-game strategic advantage indicators

## Models Compared

The following machine learning models were trained and compared:

* Logistic Regression
* Random Forest
* XGBoost
* Artificial Neural Network
* Support Vector Machine

## Results

The models achieved similar validation performance, with accuracy values around 72%.

| Model                     | Accuracy | ROC-AUC |
| ------------------------- | -------: | ------: |
| Logistic Regression       |   72.37% |  81.08% |
| Random Forest             |   72.47% |  81.06% |
| XGBoost                   |   72.57% |  80.93% |
| Artificial Neural Network |   72.27% |  80.44% |
| Support Vector Machine    |   72.17% |  79.04% |

The results show that early-game metrics can provide meaningful predictive power for match outcome prediction.

## Project Files

* `notebooks/match-winner-prediction.ipynb`
  Jupyter Notebook containing data preprocessing, exploratory data analysis, model training, and performance evaluation.

* `report/project-report.pdf`
  Full project report including dataset explanation, EDA, model comparison, benchmark results, and software requirements analysis.

## Repository Structure

```text
league-of-legends-match-winner-prediction/
│
├── README.md
│
├── notebooks/
│   └── match-winner-prediction.ipynb
│
└── report/
    └── project-report.pdf
```

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* scikit-learn
* XGBoost
* TensorFlow / Keras

## Notes

The dataset is not included in this repository because it is externally sourced and may be subject to dataset distribution limitations.

This repository contains the notebook and project report prepared for machine learning-based esports analytics.
