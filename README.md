# Breast Cancer Classification Using Machine Learning

## Overview

This project builds and evaluates machine learning models for breast cancer classification using the Breast Cancer Wisconsin Diagnostic dataset from scikit-learn.

The goal is to develop a reproducible machine learning workflow and compare different classification algorithms based on their ability to distinguish between malignant and benign cases.

## Dataset

The dataset contains:

- 569 samples
- 30 numerical features
- 2 target classes

Target encoding:

- `0` = Malignant
- `1` = Benign

The dataset is loaded directly from scikit-learn using `load_breast_cancer()`.

## Machine Learning Workflow

The project follows these main steps:

1. Exploratory Data Analysis (EDA)
2. Train-test split with stratification
3. Data preprocessing using pipelines
4. Stratified 5-fold cross-validation
5. Model comparison
6. Model selection based on cross-validation ROC-AUC
7. Final evaluation on an unseen test set
8. Confusion matrix analysis
9. ROC curve analysis
10. Logistic Regression feature analysis

## Models Evaluated

The following classification models were compared:

- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

Feature scaling was applied within pipelines where required.

## Evaluation Strategy

The models were compared using stratified 5-fold cross-validation on the training data.

The evaluation metrics were:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Malignant cases were treated as the class of interest when calculating precision, recall, F1-score, and ROC-AUC.

The test set was kept separate from model selection and was used only for final evaluation.

## Results

Logistic Regression achieved the highest mean cross-validation ROC-AUC and was selected as the final model.

On the unseen test set, Logistic Regression achieved:

| Metric | Score |
|---|---:|
| Accuracy | 98.25% |
| Precision (Malignant) | 97.62% |
| Recall (Malignant) | 97.62% |
| F1-score (Malignant) | 97.62% |
| ROC-AUC | 99.54% |

## Key Findings

Logistic Regression provided the strongest overall performance among the evaluated models based on mean cross-validation ROC-AUC.

The Logistic Regression coefficients were also analyzed to identify the features with the strongest influence on the model's predictions.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
Breast-Cancer-Classification/
├── Breast_Cancer_Classification.ipynb
├── README.md
└── requirements.txt
```
## Limitations

- The dataset is a benchmark dataset and may not represent real-world clinical populations.
- The results are intended for educational and machine learning practice purposes.
- Model performance on this dataset should not be interpreted as clinical diagnostic performance.

## How to Run

1. Clone or download this repository.
2. Install the required dependencies from `requirements.txt`.
3. Open `Breast_Cancer_Classification.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the notebook cells sequentially.


## Disclaimer

This project is for educational purposes only and is not intended for clinical diagnosis or medical decision-making.

