# IEC - 03 Estimating Aqueous Solubility Directly From Molecular Structure

## Project Overview

This project focuses on predicting the aqueous solubility of compounds directly from their molecular structures. Solubility prediction is crucial in various fields, including pharmaceuticals and material sciences. This repository contains the code and data used to develop and evaluate various machine learning models for this task.

## Dataset

The dataset used for this project is "delaney solubility with descriptors.csv". The target variable is "logS", representing the solubility of the compounds.

## Data Preprocessing

The following data preprocessing steps were performed:

*   Splitting the dataset into training and testing sets.
*   Standardizing the features using StandardScaler.

## Exploratory Data Analysis (EDA)

EDA was conducted to investigate the relationships between molecular features and their solubility. 

**Key findings from the EDA** include:

*   Negative correlations were observed between solubility (logS) and features such as MolLogP and MolWt, suggesting that molecules with higher values for these features tend to have lower solubility.
*   The feature NumRotatableBonds showed a weaker negative correlation with logS.
*   AromaticProportion exhibited a binary nature (mostly 0 or 1), indicating that most compounds were either fully aromatic or non-aromatic.

## Model Selection and Evaluation

Several machine learning models were evaluated, including:

*   Neural Network
*   Random Forest
*   Gradient Boosting
*   Support Vector Machine
*   Linear Regression
*   Ridge Regression
*   Lasso Regression

Model performance was assessed using **RMSE, MAE, and the R-squared (R2) score**.

## Results

*   The **Neural Network model consistently outperformed other models** across different stages of the project, achieving the lowest RMSE and MAE values and the highest R2 scores.
*   Random Forest and Gradient Boosting models also demonstrated strong performance, highlighting the effectiveness of ensemble methods for this task.
*   Linear models (Linear Regression, Ridge, and Lasso) performed less effectively, indicating the non-linear nature of the data.

## Hyperparameter Tuning

Hyperparameter tuning was conducted using **Randomized Search for Random Forest and Gradient Boosting models and manual experimentation for Neural Network** to optimize model performance. Although some improvements were observed, the overall gains from tuning were modest.

## Outlier Detection

**Isolation Forest algorithm** was used to detect and remove outliers from the training data. While outlier removal resulted in a cleaner dataset, it did not lead to significant improvements in model performance metrics.

## Feature Scaling

Feature scaling was found to be **crucial for improving model performance**. Models trained without feature scaling exhibited a noticeable decrease in performance metrics.

## Visualization

Visualizations, including **predicted vs. actual solubility plots and feature importance graphs**, were generated to analyze model performance and gain insights into the factors driving predictions.

## Contributions

The project involved contributions from four team members, each focusing on specific aspects such as:

*   Outlier detection and data analysis
*   Model selection, evaluation, and hyperparameter tuning
*   Implementation of the Neural Network and visualization.
