# Titanic Survival Prediction

This project analyzes the Titanic dataset and compares different machine learning models to predict passenger survival.

The main goal is not only to maximize overall accuracy, but also to identify which model performs best when predicting passengers who did not survive. For this reason, recall for class 0 was considered an important metric in the final model selection.

## Dataset

The dataset contains passenger information from the Titanic, including variables such as:

* Passenger class
* Sex
* Age
* Number of siblings/spouses aboard
* Number of parents/children aboard
* Fare
* Embarkation information
* Survival status

The target variable is:

* `survived = 0`: the passenger did not survive
* `survived = 1`: the passenger survived

## Models Tested

The following machine learning models were trained and compared:

* Random Forest Classifier
* Logistic Regression
* Support Vector Classifier

Each model was implemented using a Scikit-learn pipeline that included preprocessing steps for numerical and categorical features.

## Preprocessing

The preprocessing pipeline included:

* Median imputation for numerical variables
* Standard scaling for numerical variables
* Most frequent imputation for categorical variables
* One-hot encoding for categorical variables

## Model Selection

The models were tuned using `GridSearchCV` with cross-validation.

Although different scoring metrics were explored during training, the final model comparison focused on recall for class 0, because the main objective was to correctly identify passengers who did not survive.

## Final Result

Logistic Regression was selected as the final model because it achieved the highest recall for class 0.

Final selected model:

* Model: Logistic Regression
* Recall for class 0: 0.89

This means that Logistic Regression was the best model in this analysis for correctly identifying passengers who did not survive.

## Tools and Libraries

This project uses:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Project Structure

```text
titanic-survival-prediction/
│
├── titanic_survival_prediction.ipynb
├── README.md
└── requirements.txt
```

## How to Run

Install the required libraries:

```bash
pip install -r requirements.txt
```

Then open the notebook:

```bash
jupyter notebook titanic_survival_prediction.ipynb
```

## Conclusion

This project shows a complete machine learning workflow for a binary classification problem. Several models were trained, tuned, and evaluated. Based on the final comparison, Logistic Regression was selected because it performed best according to the main objective of the analysis: correctly identifying passengers who did not survive.
