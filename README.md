# IBM HR Employee Attrition Prediction

A machine learning project that predicts whether an employee is likely to leave a company based on HR data.

## Overview

Employee attrition is an important challenge for organizations. This project uses employee information to explore attrition patterns, build classification models, and identify factors associated with employees leaving a company.

The main focus is on comparing different models and improving **Recall** to identify as many employees at risk of leaving as possible.

## Dataset

The project uses the IBM HR Analytics Employee Attrition dataset.

- **Target:** `Attrition`
- **Classes:** `Yes` (leaves) and `No` (stays)
- **Problem Type:** Binary Classification

Dataset file: `WA_Fn-UseC_-HR-Employee-Attrition.csv`

## Project Workflow

1. **Exploratory Data Analysis (EDA):** Examine the dataset, class distribution, and relationships between HR features and attrition.
2. **Data Cleaning:** Remove constant columns and the employee identifier.
3. **Feature Engineering:** Create additional features based on employee age and company tenure.
4. **Preprocessing:** Handle missing values, scale numerical features, and encode categorical features.
5. **Model Training:** Train and compare multiple classification algorithms.
6. **Class Imbalance Handling:** Compare class weights, SMOTE, and random undersampling.
7. **Hyperparameter Tuning:** Use `RandomizedSearchCV` to optimize Logistic Regression for Recall.
8. **Model Evaluation:** Evaluate performance using classification metrics, confusion matrices, and feature importance.
9. **Error Analysis:** Examine false positives, false negatives, and different classification thresholds.

## Models

The project compares the following models:

- Dummy Classifier (baseline)
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)

It also evaluates different strategies for handling class imbalance.

## Evaluation Metrics

- **Recall:** Primary metric for identifying employees who leave.
- **F1-score:** Balances Precision and Recall.
- **Precision:** Measures the accuracy of positive predictions.
- **ROC-AUC:** Evaluates the model's ability to distinguish between classes.
- **Accuracy:** Measures overall prediction accuracy.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- SciPy
- Jupyter Notebook

## How to Run

1. Clone this repository.
2. Install the required packages:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn scipy jupyter
   ```

3. Place `WA_Fn-UseC_-HR-Employee-Attrition.csv` in the project directory, or update `DATA_PATH` in the notebook.
4. Open and run the Jupyter Notebook.

## Results

The notebook compares model performance on a stratified validation set and sorts the results by Recall.

It also includes:
- Model comparison tables
- Class imbalance strategy comparison
- Hyperparameter tuning results
- Confusion matrix and classification report
- Permutation feature importance
- False positive and false negative analysis
- Classification threshold comparison

Final model performance depends on the validation data and selected configuration.

## Disclaimer

This project is for educational and portfolio purposes. Predictions should not be used as the sole basis for employment decisions.
