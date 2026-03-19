# Titanic Dataset - Exploratory Data Analysis & Data Preprocessing
This repository contains my submission for the **ISM8X04 - Learning from Data** assignment. The project focuses on performing a comprehensive Exploratory Data Analysis (EDA) and applying various data preprocessing techniques to the classic Titanic dataset.

## Project Overview
The goal of this project was to prepare the Titanic dataset for potential machine learning models by:
- Conducting an in-depth exploratory data analysis to understand data structure, distributions, and patterns.
- Identifying, quantifying, and visualizing missing data.
- Applying appropriate data encoding techniques (Label Encoding, One-Hot Encoding) to categorical variables.
- Implementing and comparing multiple imputation methods (Mean, Median, Mode, KNN) to handle missing values.

## Dataset
- **Source:** [Kaggle - Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)
- **Description:** The dataset provides information on 891 passengers aboard the RMS Titanic, including features like age, sex, passenger class, fare, and survival status.
- **Challenges:** The dataset contains a mix of numerical and categorical variables, as well as naturally occurring missing values, making it ideal for demonstrating data preprocessing workflows.

## Files in this Repository
- `Titanic_EDA_Assignment.ipynb`: The Jupyter notebook containing all the Python code for the analysis, from data loading to final imputation.
- `Report.pdf`: The final written report detailing the methodology, findings, and justifications for each step of the analysis.
- `titanic-dataset.csv`: The original dataset used for this project.

## Key Libraries Used
- **pandas:** For data manipulation and analysis.
- **numpy:** For numerical operations.
- **matplotlib & seaborn:** For data visualization.
- **scikit-learn:** For data encoding (`LabelEncoder`) and KNN imputation (`KNNImputer`).

## Key Findings & Methodology
- **EDA:** The analysis revealed significant patterns, such as the higher survival rate of female passengers and the impact of passenger class on survival. The `Fare` variable was found to be heavily right-skewed with several outliers.
- **Missing Data:** The `Cabin` column was dropped due to its high percentage of missing values (77%). Missingness in `Age` was treated as Missing at Random (MAR), and the two missing values in `Embarked` were considered Missing Completely at Random (MCAR).
- **Encoding:** Label Encoding was used for the binary `Sex` variable. One-Hot Encoding was applied to the nominal `Embarked` variable to avoid introducing a false ordinal relationship.
- **Imputation:** Four imputation methods were applied and their implications discussed:
    - **Mean/Median Imputation:** Simple but can distort data distribution and reduce variance.
    - **Mode Imputation:** A safe and logical choice for the two missing `Embarked` values.
    - **KNN Imputation:** A more sophisticated, multivariate approach that preserves relationships between variables.

## Conclusion
This project successfully demonstrates a structured and robust workflow for data preprocessing, a critical step in any data science pipeline. The Titanic dataset was thoroughly analyzed and transformed into a clean, analysis-ready format, ready for use in predictive modeling tasks.

## Author
**Andile Gift Shabalala**
