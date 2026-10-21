# Heart Disease Prediction Using Machine Learning

## Overview

This project uses machine learning techniques to predict the presence of heart disease from patient health-related features. It includes exploratory data analysis, data preprocessing, model training, and performance evaluation using Python and Scikit-learn.

The goal is to compare different classification algorithms and identify a model that performs well on the available dataset.

## Objectives

- Explore and visualize heart disease data.
- Clean and preprocess numerical and categorical features.
- Train multiple machine learning classification models.
- Compare models using accuracy and F1 score.
- Save the selected model and preprocessing artifacts for potential reuse.

## Dataset

The notebook loads a dataset named `heart.csv` containing 918 records and 12 columns.

Features include:

- Age
- Sex
- ChestPainType
- RestingBP
- Cholesterol
- FastingBS
- RestingECG
- MaxHR
- ExerciseAngina
- Oldpeak
- ST_Slope

**Target variable:** `HeartDisease`

The target represents the heart disease classification in the dataset.

## Technologies Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

## Project Workflow

1. **Exploratory Data Analysis:** Inspect the dataset, check missing values and duplicates, and visualize feature distributions and relationships.
2. **Data Cleaning:** Replace zero values in cholesterol and resting blood pressure with the corresponding nonzero-value means.
3. **Feature Encoding:** Convert categorical features into numerical columns using one-hot encoding.
4. **Data Splitting:** Divide the dataset into training and testing sets using an 80:20 split.
5. **Feature Scaling:** Standardize features using `StandardScaler`.
6. **Model Training:** Train Logistic Regression, K-Nearest Neighbors, Gaussian Naive Bayes, Decision Tree, and Support Vector Machine classifiers.
7. **Evaluation:** Compare model performance using accuracy and F1 score.
8. **Model Saving:** Save the KNN model, fitted scaler, and feature-column names using Joblib.

## Model Performance

Results recorded in the notebook:

| Model | Accuracy | F1 Score |
|---|---:|---:|
| Logistic Regression | 87.50% | 88.78% |
| K-Nearest Neighbors (KNN) | 88.59% | 89.86% |
| Gaussian Naive Bayes | 86.96% | 87.88% |
| Decision Tree | 76.09% | 77.78% |
| Support Vector Machine (RBF) | 86.41% | 88.04% |

KNN achieved the highest accuracy and F1 score among the evaluated models in this experiment.

## Saved Artifacts

The notebook saves the following files:

- `KNN_heart.pkl` — trained KNN classifier
- `scaler.pkl` — fitted feature scaler
- `columns.pkl` — list of input feature names and their order

## How to Run

1. Clone or download this repository.
2. Install the required Python packages.
3. Place `heart.csv` in the same directory as the notebook, or update the dataset path.
4. Open `HeartdiseaseFinal.ipynb` in Jupyter Notebook or JupyterLab.
5. Run the notebook cells from top to bottom.

Install the core dependencies with:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn joblib jupyter
```

The notebook also includes an installation step for `sheryanalysis==0.1.0`.

## Limitations

- Performance is evaluated using a single train-test split.
- Additional validation and testing on independent data are needed.
- Accuracy and F1 score alone do not establish clinical usefulness.
- The model is intended for educational and research purposes, not medical diagnosis or treatment decisions.

## Future Improvements

- Use cross-validation and hyperparameter tuning.
- Evaluate precision, recall, ROC-AUC, and the confusion matrix.
- Build a simple prediction interface using Streamlit or Flask.
- Package preprocessing and prediction into a single reusable pipeline.
- Document the dataset source and licensing information.

## Disclaimer

This project is for educational purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment.
