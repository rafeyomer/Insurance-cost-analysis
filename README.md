# Project 1: Exploring Key Predictors of U.S. Health-Insurance Charges with Linear Regression

## Overview
This project investigates the factors that drive medical insurance costs using the **insurance.csv** dataset. 
The dataset contains **1,338 records**, each representing an individual policyholder with demographic, lifestyle, and regional information. 
The main objective is to identify which variables most strongly influence insurance charges and to develop a simple linear regression model to predict costs.

## Dataset
- **Source:** Kaggle - *Medical Cost Personal Dataset*
- **Rows:** 1,338  
- **Columns:**
  - `age`: Age of primary beneficiary (in years)
  - `sex`: Gender (`male`, `female`)
  - `bmi`: Body mass index, kg/m²
  - `children`: Number of dependents covered by health insurance
  - `smoker`: Smoking status (`yes`, `no`)
  - `region`: Residential region in the U.S. (`northeast`, `northwest`, `southeast`, `southwest`)
  - `charges`: Annual medical insurance cost (USD)

## Project Goals
1. Perform **data wrangling** to prepare categorical variables and check for missing values.
2. Conduct **exploratory data analysis (EDA)** with descriptive statistics and visualizations.
3. Fit a **multiple linear regression model** to identify predictors of medical charges.
4. Evaluate model performance using **RMSE** and **R²** on a test set.
5. Communicate findings through a report and presentation.

## Methods
- **Data Wrangling:** Converted `sex`, `smoker`, and `region` to categorical factors. Verified no missing values.
- **EDA:** Summary statistics, histograms, boxplots, scatterplots with regression lines.
- **Modeling:** Multiple linear regression including an interaction between `bmi` and `smoker`.
- **Evaluation:** Train/test split (80/20). Computed RMSE (~$5,000) and R² (~0.82).

## Key Findings
- **Smoking** is the strongest driver of insurance charges, adding ~$22,600 annually.
- **Age** increases charges by ~$274 per year.
- **BMI** has a modest effect, but when combined with smoking, each unit increase adds ~$1,500.
- **Children** have a smaller positive effect, while sex and region effects are minor.
- The model explains ~82% of the variance in charges.

## Files Submitted
- `insurance_project.Rmd` – Main R Markdown analysis file
- `Project 1.pdf` – Knitted PDF report
- `insurance.csv` – Dataset file
- `README.md` – This project overview file
- `Project1_Presentation.mp4` – Video presentation (to be recorded)

## How to Reproduce
1. Place `insurance_project.Rmd` and `insurance.csv` in the same directory.
2. Open the `.Rmd` file in **RStudio**.
3. Install required R libraries if not already installed:  
   ```r
   install.packages(c("dplyr", "ggplot2", "readr", "stringr", "tidyr", "knitr"))
   ```
4. Knit the R Markdown file to produce the PDF report.

## Conclusion
Demographics and lifestyle factors, particularly **smoking** and **BMI**, play a major role in driving medical insurance costs. 
This project demonstrates how linear regression can provide interpretable insights and reasonably accurate predictions for insurance charges.

---
*Author: Muhammad Rafey Omer*  
*Date: 09/28/2025*
