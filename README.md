# EEG Seizure Classification using Machine Learning

## Project Overview

This project presents a comparative evaluation of machine learning models for **multiclass EEG seizure classification** using the **BEED (Bangalore EEG Epilepsy Dataset)**.

The aim of this project is to investigate how different machine learning algorithms perform in distinguishing between different EEG seizure types.

The evaluated models include:

- Logistic Regression
- Support Vector Machine (SVM)
- Multilayer Perceptron (MLP)

The models were trained using preprocessing techniques, feature engineering, dimensionality reduction, and hyperparameter optimization.

---

## Project Note

This project was developed as part of a university course project by a team.

---

## Dataset

**Dataset:** BEED (Bangalore EEG Epilepsy Dataset)

The dataset contains:

- 8,000 EEG segments
- 16 EEG channel features
- 4 balanced classes
- No missing values

### Classes

| Label | Class |
|------:|----------------------------|
| 0 | Healthy |
| 1 | Generalized Seizure |
| 2 | Focal Seizure |
| 3 | Seizure Events |

---

## Methodology

The project pipeline consists of:

```
Dataset
   ↓
Data Preprocessing
   ↓
Feature Engineering
   ↓
Feature Scaling
   ↓
PCA Dimensionality Reduction
   ↓
Model Training
   ↓
Hyperparameter Tuning
   ↓
Model Evaluation
```

---

## Feature Engineering

Additional statistical features were extracted from EEG signals:

- Mean signal value
- Standard deviation
- Maximum value
- Minimum value
- Signal energy

These features were combined with the original EEG features to improve classification performance.

---

## Machine Learning Models

### Logistic Regression

Used as a baseline linear classifier.

### Support Vector Machine (SVM)

Evaluated with different kernels to capture non-linear patterns.

### Multilayer Perceptron (MLP)

A neural network model used to learn complex EEG patterns.

---

## Hyperparameter Optimization

Model parameters were optimized using:

- GridSearchCV
- 5-fold Stratified Cross Validation

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curves (One-vs-Rest)
- Learning Curves

---

## Results

| Model | Test Accuracy |
|------|---------------:|
| Logistic Regression | 62.7% |
| Support Vector Machine | 81.5% |
| Multilayer Perceptron | 95% |

### Best Performing Model

The **Multilayer Perceptron (MLP)** achieved the highest performance with:

- Test Accuracy: **95%**
- Macro F1-score: **95%**
- Strong classification performance across all seizure classes

---

## Repository Structure

```
machine-learning-eeg-seizure-classification/
│
├── notebook/
│   └── EEG_Seizure_Classification.ipynb
│
├── report/
│   └── EEG_Seizure_Classification_Report.pdf
│
├── results/
│   ├── confusion_matrix_logistic_regression.png
│   ├── confusion_matrix_svm.png
│   ├── confusion_matrix_mlp.png
│   ├── learning_curve_mlp.png
│   └── roc_curves/
│
├── requirements.txt
└── README.md
```

---

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/Shahad-AlGhassani/eeg-seizure-classification-ml.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebook:

```bash
jupyter notebook notebook/EEG_Seizure_Classification.ipynb
```

---

## Skills Demonstrated

- Data preprocessing
- Feature engineering
- PCA dimensionality reduction
- Machine learning pipelines
- Hyperparameter tuning
- Cross-validation
- Multiclass classification
- Model evaluation
- Biomedical signal analysis

---

## Report

The complete project report is available in:

```
report/EEG_Seizure_Classification_Report.pdf
```

---

## License

This project was developed for educational purposes.
