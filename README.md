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

Target Audience

•	What are the most common causes of subway delays?
•	How do delay patterns vary by time of day or day of the week?
•	Are there any seasonal trends in subway delays?
•	How do delays impact ridership and customer satisfaction?


Required Libraries
Pandas: For data manipulation and analysis.
Numpy: For numerical operations and handling arrays.
Scikit-learn: For building and evaluating machine learning models.
Matplotlib.pyplot: For creating visualizations like charts and plots.
Seaborn: For statistical data visualization, providing an interface for creating complex visualizations easily.
Shap: For model explainability, to analyze how individual features contribute to model predictions.

## Methodology

###     1. Exploratory Data Analysis


###     2. Understanding the raw data

* Date Range: Jan, 01 2024 to Jan 31, 2025
* Company:The Toronto subway, operated by the TTC (Toronto Transit Commission), consists of three lines: Line 1 (Yonge-University), Line 2 (Bloor-Danforth), and Line 4 (Sheppard). 
* Data Points: 28,571 entries 
* Adjustments: 17,653 entries in dataset 'df_delay.csv'
* Additional source: 'code_category_description.csv' (130 entries)



Based on typical delay datasets, expect columns like:

- Date and Time: Indicates when the delay occurred.
- Station: Specifies the station where the delay happened.
- Duration (Min Delay): Describes the length of the delay.
- Reason/Category: Explains the cause of the delay (e.g., mechanical, weather).
- Line: Identifies the subway line affected.
- Category: Describes the categories associated with the codes that specify the underlying reasons for TTC delays


Tis file  categorize various delay codes related to transportation operations. 

Categories :
* Mechanical/Electrical/Vehicle Equipment: Issues like HVAC malfunctions (EUAC), brake problems (EUBK), or door sensor failures (EUDO).
* Signaling/Communication/Power: Problems such as signal control failures (PUCSC) or traction power distribution issues (PUTTP).
* Track/Infrastructure/Debris: Includes track-level debris (PUTD) and structural problems at stations or tunnels (PUTS).
* Operations/Staffing/Scheduling: Delays caused by staff shortages (MUESA) or scheduling errors (MUCL).
* Door/Passenger/Platform Incidents: Situations like doors blocked by debris (MUDD) or passengers interfering with train operations (MUD).
* Weather/External: Delays due to severe weather events (MUFM) or snow buildup (PUTIS).
* Medical/Injury/Safety: Instances involving ill passengers or injuries, both for staff and passengers (MUI, MUIE).
* Security/Policing: Emergency situations such as unauthorized individuals on tracks (SUUT) or vandalism (SUG).
* Transportation/Operator: Operator-related issues like overshooting platforms (TUOS) or procedural errors (TUATC).
* Miscellaneous: General or uncategorized delays (MUGD).

###     3. Data Celaning and Processing

Data Cleaning for the Team Project TTC Delay

This code prepares the data for analysis by merging datasets for period Jan, 01, 2024 to Jan 31, 2025, cleaning up unnecessary columns, and standardizing date formats. It sets the foundation for further exploration and visualization of TTC subway delays.
The  the result for years 2024 and 2025 datasets are concatenated into a single DataFrame named 'df_delay.csv' and saved at directory  '../data/processed_data/df_delay.csv'.

Files Used:
1. ttc-subway-delay-data-2024.csv:
 - this file contains TTC subway delay data for the year 2024.
 - it is loaded into a DataFrame named df_2024 using pd.read_csv().

2. TTC Subway Delay Data since 2025.csv:
 - this file contains TTC subway delay data for month of January of 2025.

3. code_category_description.csv 
- file to categorize various delay codes related to transportation operations




###     4. Model Training and Development




###     5. Model Selection

## Results

## Members

- Julian Peinado

- Kuda Wamambo

- Olga Demenina

- Omer

- Rashita Makkar





