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
With the purpose of achiving our objecting we have developed the following methodology:
###     1. Exploratory Data Analysis

In this section, we:

**Load the Dataset:**  
Import the data (from a CSV) into a pandas DataFrame.

**Initial Investigation:**
- Inspect the dimensions of the data in our raw data frame we had a size of (28571, 10).
![Infor_df](02_data_processing/img/02_info_df.jpg)
- Display the first few rows to understand the format and general structure. In this step we could identify ouer target variable: `Min Delay` and our categorical features [`Date`, `Time`, `Code`, `Bound`, `Line`, `Vehicle`]

**Descriptive Statistics:**
- Calculate summary statistics (mean, median, standard deviation) to get a sense of the variable distributions.
![Summary_01](02_data_processing/img/01_DP.jpg)

- Look for anomalies in our case the `Min Delay` contains outliers like 700 min, where 75% of our observaitons are in the range of 1 to 18 min.

![Boxplot_MinDelay](02_data_processing/img/03_MinDelay_boxplot.png)


**Visual Explorations:**  

**Potential Correlation in Min Gap and Min Delay**
![Heat_Map](02_data_processing/img/04_matrix.png)  
![Scatter](02_data_processing/img/05_scatter.png)  


**Key Observations:**  
- **Correlation in Min Gap and Min Delay:** There is a strong correlation between these tow features.
- **Codes:** The delay codes will be grouped in an `category` column that will help us to classify the delays.
- **Missing Values:** The missing values will be handle in the Data Cleaning Section.
- **Feature with low Importance:** Categorical features like `Vehicle` has low importance in our analysis.
- **SRT Line:** SRT line is out of the scope since is not in service.
- **Note:** Only 2024 and 2025 data was considered in this project.

###     2. Understanding the raw data

###     3. Data Celaning and Processing

###     4. Model Training and Development

###     5. Model Selection

## Results

## Members

- Julian Peinado

- Kuda Wamambo

- Olga Demenina

- Omer

- Rashita Makkar





