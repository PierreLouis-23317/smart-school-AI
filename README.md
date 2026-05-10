# AI Lab Project – Smart School ECAM

## Authors

- **Félix de Crouy Chanel** – 22176
- **Louis Pierre** – 23317

## Course Information

- **School:** ECAM Brussels Engineering School
- **Course:** Artificial Intelligence – 4eoai40
- **Academic year:** 2025–2026

## Project Description

This repository contains the code developed for the AI/ML lab project **Smart School ECAM**.

The project is divided into two main parts:

1. **Failure prediction**  
   The objective is to predict student exam scores from tabular data. The final goal is to identify students who may be at risk of failing, so that additional support could be proposed.

2. **Automatic correction with OCR**  
   The objective is to recognize handwritten digits and characters from image data. Two neural network approaches are tested: a Multilayer Perceptron (MLP) and a Convolutional Neural Network (CNN).

## Repository Structure

```text
.
├── 01_eda.ipynb
├── 02_hyperparameter_optimization.ipynb
├── 03_failure_prediction_model.ipynb
├── 04_ocr_image_recognition.ipynb
├── student_dataset/
│   ├── student_failure/
│   │   └── train.csv
│   └── image_data/
├── figures_tuning/
└── README.md
```

## Notebook Description

### `01_eda.ipynb`

Exploratory analysis of the student performance dataset.

Main contents:

- dataset loading and first inspection;
- missing value analysis;
- distribution of numerical and categorical variables;
- creation of the fail/risk/pass categories;
- correlation analysis;
- feature importance using Mutual Information.

This notebook supports the data exploration and feature selection parts of the report.

### `02_hyperparameter_optimization.ipynb`

Hyperparameter tuning for the failure prediction models.

Main contents:

- baseline definition;
- RandomizedSearchCV for broad exploration;
- GridSearchCV for local refinement;
- comparison of optimized models;
- selection of the best hyperparameters.

The optimized models include Ridge Regression, Decision Tree and Random Forest.

### `03_failure_prediction_model.ipynb`

Main notebook for the student score prediction task.

Main contents:

- preprocessing pipeline;
- train/test split;
- model training;
- comparison between baseline, classical ML models and deep learning model;
- evaluation using MAE, RMSE and R²;
- analysis of prediction errors;
- overfitting and underfitting analysis.

The best final model is Ridge Regression, which gives the lowest prediction error while remaining simple and stable.

### `04_ocr_image_recognition.ipynb`

Notebook for the OCR part of the project.

Main contents:

- loading IDX image and label files;
- image visualization and preprocessing;
- normalization of pixel values;
- training of an MLP model;
- training of a CNN model;
- comparison of OCR accuracy;
- analysis of the most frequent prediction errors.

The CNN gives the best OCR performance because it uses the spatial structure of the images.

## Data

The project uses two datasets:

### Student performance dataset

Path:

```text
student_dataset/student_failure/train.csv
```

This dataset is used for the failure prediction part. It contains student-related variables such as study hours, class attendance, sleep, diploma and exam score.

### OCR image dataset

Path:

```text
student_dataset/image_data/
```

This dataset contains grayscale images of handwritten digits and characters stored in IDX format.

## How to Run the Project

1. Open the project folder in VS Code or JupyterLab.
2. Install the required Python libraries if needed.
3. Run the notebooks in the following order:

```text
01_eda.ipynb
02_hyperparameter_optimization.ipynb
03_failure_prediction_model.ipynb
04_ocr_image_recognition.ipynb
```

The notebooks are organized to follow the same logic as the report: data exploration, preprocessing, model tuning, model evaluation and OCR classification.

## Main Results

### Failure prediction

Several models were compared:

- baseline model;
- Ridge Regression;
- Decision Tree Regressor;
- Random Forest Regressor;
- Deep Learning model.

Ridge Regression obtained the best overall performance. The result suggests that the dataset has a relatively regular and almost linear structure, so a simple regularized model is sufficient.

### OCR

Two models were compared:

- Multilayer Perceptron (MLP);
- Convolutional Neural Network (CNN).

The CNN obtained the best accuracy. The main errors occur between visually similar characters such as `O` and `0`, `l` and `1`, or `S` and `5`.

## Notes

Some older notebooks may still exist in the working folder, but the clean version of the project is based on the four notebooks listed above.

If the project folder is moved, paths to the datasets may need to be adapted in the notebooks.
