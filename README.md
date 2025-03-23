# Risk Analysis of TTC Delays

Data Science Institute, University of Toronto - Cohort 5 - Team Project 16

## Table of Contents

- [Requirements](#requirements)
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Methodology](#methodology)
  - [1. Exploratory Data Analysis](#1-exploratory-data-analysis)
  - [2. Understanding the Raw Data](#2-understanding-the-raw-data)
  - [3. Data Cleaning and Processing](#3-data-cleaning-and-processing)
  - [4. Model Training and Development](#4-model-training-and-development)
  - [5. Model Selection](#5-model-selection)
- [Results](#results)
- [Members](#members)


## Requirements

## Introduction

## Objectives

## Methodology
To achieve our objective, we developed the following methodology:

### 1. Exploratory Data Analysis

**Load the Dataset:**  
We imported the data (from a CSV file) into a pandas DataFrame. [`01_exploratory_data_analysis.csv`](02_data_processing/01_exploratory_data_analysis.ipynb)  

**Initial Investigation:**
- We inspected the dimensions of the dataset; the raw DataFrame had a shape of (28,571 rows × 10 columns).  
  ![Infor_df](img/01_exploratory_data/02_info_df.jpg)
- We displayed the first few rows to understand the format and general structure. In this step, we identified our target variable: `Min Delay`, and our categorical features: [`Date`, `Time`, `Code`, `Bound`, `Line`, `Vehicle`].

**Descriptive Statistics:**
- We calculated summary statistics (mean, median, standard deviation) to gain insight into the distribution of each variable.  
  ![Summary_01](img/01_exploratory_data/01_DP.jpg)
- We looked for anomalies. In our case, `Min Delay` contains outliers (e.g., 700 minutes), while 75% of observations range between 1 and 18 minutes.  
  ![Boxplot_MinDelay](img/03_MinDelay_boxplot.png)

**Visual Explorations:**

- **Potential Correlation in Min Gap and Min Delay**  
  ![Heat_Map](img/01_exploratory_data/04_matrix.png)  
  ![Scatter](img/01_exploratory_data/05_scatter.png)

**Key Observations:**  
- **Correlation in Min Gap and Min Delay:** There is a strong correlation between these two features.  
- **Codes:** The delay codes will be grouped into a `category` column to help classify the delays.  
- **Missing Values:** Missing values will be handled in the Data Cleaning section.  
- **Feature with Low Importance:** The categorical feature `Vehicle` has low importance for our analysis.  
- **SRT Line:** The SRT line is out of scope because it is not in service.  
- **Note:** Only data from 2024 and 2025 was considered for this project.

###     2. Understanding the raw data


| Feature       | Description                                      |
|--------------|--------------------------------------------------|
| `Min Delay`  | The delay in minutes for each train.            |
| `Date`       | The date when the delay occurred.               |
| `Time`       | The time of the delay event.                    |
| `Code`       | The reason code assigned to the delay.          |
| `Bound`      | The direction in which the train was traveling. |
| `Line`       | The transit line on which the delay occurred.   |
| `Vehicle`    | The train number or identifier.                 |
| `Min Gap`   | The time in minutues for the next car           |

To understand the Codes, we analyze the [`ttc-subway-delay-codes.csv`](01_raw_data/ttc-subway-delay-codes.csv)

We have grouped the codes in categories, as shown in the following file: [`code_category_description.csv`](02_data_processing/code_category_description.csv)  

###     3. Data Celaning and Processing

Handling Missing Values: We identified missing values in the dataset, particularly in the Min Delay and Code columns. Missing values were imputed using median values for numerical columns and mode for categorical columns.
Outlier Detection & Treatment: Boxplots revealed extreme outliers in Min Delay, with some delays exceeding 700 minutes. Values beyond the 99th percentile were capped to improve model performance.
Feature Engineering:
Created new categorical features by grouping similar Code values into broader categories.
Added a Peak Hours flag to differentiate rush hour delays from off-peak delays.
Extracted Day of the Week and Month from Date to identify potential time-based patterns.
Final Dataset Storage: The cleaned dataset was stored as df_cleaned.csv in the processed_data directory.

###     4. Model Training and Development
Baseline Model Selection:
We initially tested Decision Trees and Random Forests for classification but found Logistic Regression to be the best-performing model in terms of interpretability and computational efficiency.
Feature Scaling & Encoding:
Applied StandardScaler to normalize numerical features (Min Delay, Min Gap).
Used one-hot encoding for categorical features like Line, Bound, and Code Category.
Hyperparameter Tuning:
GridSearchCV was used to optimize hyperparameters such as C (regularization strength) for Logistic Regression.
Model Performance:
Achieved an F1-score of 0.81 on the test set.
Precision-recall analysis indicated that the model effectively differentiates between high and low-risk delay scenarios.
Model Deployment:
The trained model and its preprocessing pipeline were saved using joblib for easy deployment.
###     5. Model Selection

## Results

## Members

- Julian Peinado

- Kuda Wamambo

- Olga Demenina

- Omer Khan

- Rashita Makkar





