
# Dataset

## Source

Dataset: Pima Indians Diabetes Database

Kaggle:
https://www.kaggle.com/datasets/mragpavank/diabetes

Alternative source (OpenML):
https://www.openml.org/search?type=data&status=active&id=43483

## Dataset Overview

- Total records: 768
- Input features: 8
- Target variable: `Outcome`
- Problem type: Binary Classification

## Features

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure |
| SkinThickness | Triceps skin fold thickness |
| Insulin | 2-hour serum insulin |
| BMI | Body Mass Index |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age in years |
| Outcome | Diabetes status (0 = No, 1 = Yes) |

## Data Preprocessing

Zero values in the following columns are treated as missing values:

- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI

Missing values are handled using median imputation within the machine learning pipelines to avoid data leakage.

`Pregnancies = 0` is retained because it is a valid value.

## Dataset Usage

Place the downloaded `diabetes.csv` file inside this directory:

```text
data/
└── diabetes.csv
```

The dataset is used for exploratory data analysis, preprocessing, model training, feature selection, and evaluation.

## License and Attribution

The Pima Indians Diabetes Database originates from
the National Institute of Diabetes and Digestive
and Kidney Diseases (NIDDK).

An OpenML version of the dataset is listed under
CC0: Public Domain.

The license of the exact Kaggle copy used in this
project should be verified separately before
redistribution.

The dataset is used for academic machine learning
research, with attribution to its original source.