
# Early Diabetes Prediction Using Machine Learning

A machine learning research project that explores diabetes status prediction using the Pima Indians Diabetes Dataset. This project compares multiple classification algorithms, applies hyperparameter tuning, performs feature selection, and evaluates model performance using standard classification metrics.

## Project Overview

Diabetes is a chronic health condition that requires timely identification and appropriate medical attention. Machine learning can help identify patterns in patient health measurements and support the analysis of diabetes-related risk factors.

This project investigates the performance of different machine learning classification algorithms for predicting diabetes status based on medical and demographic features.

**Note:** This project is an academic machine learning study and is not a clinically validated diagnostic system.

## Objectives

- Perform exploratory data analysis (EDA).
- Identify and handle missing values.
- Apply appropriate data preprocessing techniques.
- Train and compare multiple machine learning models.
- Perform hyperparameter tuning using GridSearchCV.
- Apply feature selection techniques.
- Evaluate models using classification metrics.
- Analyze feature importance and model performance.

## Dataset

The project uses the **Pima Indians Diabetes Dataset**.

- Source: [Kaggle - Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/mragpavank/diabetes)
- Total records: 768
- Input features: 8
- Target variable: `Outcome`
- Task: Binary Classification

The target variable represents diabetes status:

- `0` - Non-diabetic
- `1` - Diabetic

Refer to [`data/README.md`](data/README.md) for the dataset details.

## Machine Learning Models

The following classification algorithms are implemented:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier

### Model Development

The project follows these steps:

1. Data loading and inspection
2. Exploratory Data Analysis
3. Missing-value identification and handling
4. Train-test splitting
5. Baseline model training
6. Hyperparameter tuning using GridSearchCV
7. Feature selection using SelectKBest
8. Permutation feature importance
9. Cross-validation
10. Final model evaluation

## Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC score
- Confusion Matrix
- ROC Curve

## Results

### Baseline Model Performance

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.708 | 0.600 | 0.500 | 0.545 | 0.813 |
| Decision Tree | 0.792 | 0.696 | 0.722 | 0.709 | 0.801 |
| Random Forest | 0.747 | 0.632 | 0.667 | 0.649 | 0.817 |

### Tuned Model Performance

| Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.708 | 0.571 | 0.667 | 0.615 | 0.810 |
| Decision Tree | 0.727 | 0.611 | 0.611 | 0.611 | 0.771 |
| Random Forest | 0.734 | 0.597 | 0.741 | 0.661 | 0.820 |

### Key Observations

- The baseline Decision Tree achieved the highest test accuracy and F1-score.
- The tuned Random Forest achieved the highest test recall and ROC-AUC.
- Hyperparameter tuning affected each model differently.
- Feature selection showed model-dependent effects.
- Glucose was the most influential feature in the baseline Random Forest permutation importance analysis.

## Project Structure

```text
early-diabetes-prediction-research/
│
├── data/
│   ├── diabetes.csv
│   └── README.md
│
├── notebooks/
│   └── early_diabetes_prediction.ipynb
│
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── experiment_summary.json
│
├── research-paper/
│   ├── figures/
│   ├── main.tex
│   ├── references.bib
│   └── paper.pdf
│
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Installation and Usage

### 1. Clone the repository

```bash
git clone https://github.com/aadarsh-create/early-diabetes-prediction-research.git
```

### 2. Navigate to the project directory

```bash
cd early-diabetes-prediction-research
```

### 3. Create a virtual environment (optional)

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

### 5. Run the notebook

```bash
jupyter notebook
```

Open the notebook inside the `notebooks/` directory and execute the cells.

## Research Paper

The research paper is available in the [`research-paper/`](research-paper/) directory.

- `main.tex` - LaTeX source code
- `references.bib` - Bibliographic references
- `paper.pdf` - Compiled research paper

The paper can also be opened and edited using [Overleaf](https://www.overleaf.com/).

## Limitations

- The dataset contains only 768 records.
- The dataset represents a specific population and may not generalize to other populations.
- The target represents recorded diabetes status, not the time of disease onset.
- The models have not been clinically validated.
- Results depend on the dataset and evaluation methodology.

## Future Scope

- Evaluate models on larger and more diverse datasets.
- Explore advanced ensemble learning techniques.
- Perform external validation.
- Investigate explainable AI techniques.
- Develop a user-friendly prediction application after appropriate validation.

## Author

Developed as an academic research project in Machine Learning and Data Science.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
