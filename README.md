# Authors

- **Félix de Crouy Chanel** – 22176
- **Louis Pierre** – 23317


# AI Lab Project – Smart School ECAM

This repository contains the code developed for the Artificial Intelligence lab project at ECAM Brussels Engineering School.

The project was carried out as part of the course **Artificial Intelligence – 4eoai40** during the academic year **2025–2026**.



## Project Overview

The objective of this project is to apply machine learning and deep learning methods to two practical problems related to the Smart School ECAM project.

The work is divided into two main parts:

1. **Failure prediction**  
   The goal is to predict student exam scores using tabular data. The final objective is to identify students who may be at risk of failing, so that additional support could be provided.

2. **Automatic correction with OCR**  
   The goal is to recognize handwritten digits and characters from images. This part uses image classification models, including a simple neural network and a convolutional neural network.

   
## Project Structure

- analyse_donnée.ipynb: exploratory data analysis on the student dataset
- modele_updated_clean.ipynb: cleaned end-to-end modeling pipeline for score/failure prediction
- hyperparameter_optimization_clean.ipynb: hyperparameter tuning and comparison of regression models
- image.ipynb: loading, preprocessing, and modeling for image-based character recognition
- student_dataset/student_failure/train.csv: tabular dataset for student performance
- student_dataset/image_data/: raw IDX image and label files
- figures_tuning/: generated figures used during tuning

## Notebook Guide

### 1) analyse_donnée.ipynb
Purpose:
- Explore distributions and relationships in the student dataset
- Build an interpretable target grouping (fail/risk/pass)
- Visualize key correlations and variable effects

Typical outputs:
- Class distributions
- Boxplots and regression plots
- Correlation heatmaps

### 2) modele_updated_clean.ipynb
Purpose:
- Build and compare predictive models for exam performance
- Apply preprocessing consistently (missing values, encoding, feature handling)
- Evaluate model quality with standard regression metrics

Typical outputs:
- MAE, RMSE, and R2 comparisons
- Final model performance visualizations

### 3) hyperparameter_optimization_clean.ipynb
Purpose:
- Tune model hyperparameters with cross-validation
- Select best configurations based on validation performance
- Produce summary tables and figures for reporting

Typical outputs:
- Best parameter sets
- Cross-validated score summaries
- Comparison plots saved in figures_tuning/

### 4) image.ipynb
Purpose:
- Load raw IDX image files and labels
- Preprocess image tensors for training
- Train and evaluate image classifiers

Typical outputs:
- Dataset shape checks
- Sample image visualizations
- Classification performance summaries

## Data Notes

- Student data path used by notebooks:
  - student_dataset/student_failure/train.csv
- Image data path used by notebooks:
  - student_dataset/image_data/

If you move the project folder, update any absolute paths in notebooks to relative paths for portability.

## How to Use

1. Open the repository in VS Code.
2. Open the notebook you want to present.
3. Run cells in order when execution is needed.

For presentation-only review, notebooks can also be read without execution.

## Report-Oriented Summary

This project demonstrates:

- Practical EDA and feature interpretation on tabular data
- Regression model building and evaluation
- Hyperparameter optimization with cross-validation
- Basic image recognition workflow on raw IDX data

Together, these notebooks provide a complete pipeline from data understanding to model comparison and communication-ready visual results.
