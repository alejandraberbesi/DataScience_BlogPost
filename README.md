## Overview

This project involves analyzing survey results to gain insights into the adoption of AI in the development process. The analysis is performed using Python and various data science libraries. This repository contains the code and data for my analysis, and I've also written a blog post on Notion that summarizes the key findings: [link](insert link).

## Main Libraries Used

    *   `pandas` for data manipulation and analysis
    *   `numpy` for numerical computations
    *   `matplotlib` for creating static, animated, and interactive visualizations
    *   `seaborn` for statistical data visualization
    *   `scikit-learn` for model selection, hyperparameter tuning, and model evaluation 

## Project Motivation

The motivation behind this project is to understand the current state of AI adoption in the development process, including demographics, employment status, and professional development. This information can be useful for organizations looking to inform their training and development programs, as well as for individuals seeking to understand the landscape of AI adoption.

## File Descriptions

*   `project.ipynb`: This is the main Jupyter Notebook file that contains the code for data analysis, visualization, and insights.
*   `survey_results_public.zip`: This is a compressed file containing the survey results data used in the analysis.
*   `additional_documentation.zip`: This is a compressed file containing additional documentation related to the project, such as data dictionaries or survey methodology.

## Summary of Results

### Exploratory Data Analysis

The analysis reveals that:

*   78.5% of survey respondents currently use AI in their development process.
*   The majority of AI adopters are between 25 and 34 years old (33.8%), with a significant drop-off among those 55 and older (6.5%).
*   The educational background of AI adopters is predominantly Bachelor's (42.5%) and Master's degrees (27.7%).
*   72.4% of AI adopters are employed, with around 50% having less than 10 years of working experience.
*   Recent learners of new programming languages or coding techniques account for 72.2% of AI adopters.
*   The workforce is distributed with 33.2% remote workers and 84.5% individual contributors.

### Modeling Results

Two machine learning models were trained and evaluated: Random Forest and XGBoost.

*   **Random Forest:**
    *   Overall accuracy: 81%
    *   Excellent performance on the majority class (Class 1): recall = 0.95, F1 score = 0.89
    *   Poor performance on the minority class (Class 0): recall = 0.15, F1 score = 0.21
    *   The model is biased towards the majority class, which limits its usefulness for detecting minority class cases.
*   **XGBoost:**
    *   Overall accuracy: 76%
    *   More balanced performance across both classes:
        +   Minority class (Class 0): recall = 0.39, F1 score = 0.37
        +   Majority class (Class 1): recall = 0.84, F1 score = 0.86
    *   XGBoost is a more suitable model when fair performance across both classes is desired.

## Acknowledgments

 The survey data used in this analysis is publicly available and was obtained from [this source](https://survey.stackoverflow.co/)
