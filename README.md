# Understanding Health Risk and Medical Insurance Cost Variation

## Problem Statement
This project seeks to understand why health risk—and consequently medical insurance costs—vary significantly between individuals by identifying and quantifying demographic, lifestyle, and behavioral factors associated with chronic disease and poor health outcomes.

## Datasets Used
This project uses two complementary datasets:

1. **Medical Cost Personal Dataset (Insurance Dataset)**
   - Columns: `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`
   - Goal: Predict and interpret medical insurance charges (`charges`)

2. **BRFSS 2015 (Behavioral Risk Factor Surveillance System)**
   - Goal: Analyze population-level health risk patterns and chronic disease outcomes
   - Key variables used include: age group, sex, BMI, smoking behavior, physical activity, alcohol, diabetes, and stroke/CVD indicators

## Methods
### Insurance Dataset (Cost Prediction)
- Exploratory Data Analysis (EDA)
- Predictive Modeling:
  - Linear Regression (baseline)
  - Ridge Regression
  - Lasso Regression

### BRFSS Dataset (Health Risk + Chronic Disease)
- EDA and descriptive statistics
- Statistical tests:
  - T-test (BMI by sex)
  - Chi-square tests (risk factors vs outcomes)
- Predictive modeling:
  - Logistic Regression (binary and multiclass outcomes for diabetes and stroke/CVD)

### Cross-Dataset Analysis (No Individual-Level Merging)
Instead of merging datasets (not appropriate due to different sampling designs and units of observation), predictors associated with higher insurance charges are compared against their prevalence and patterns in BRFSS to add population-level context.

## Files in This Repository
- `Orwa_Ahmad_MidtermProject_COMP4449.ipynb` — Final notebook (EDA + modeling + cross-dataset analysis)
- `requirements.txt` — Python dependencies for running the notebook

## How to Use
Open and run the notebook:
- `Orwa_Ahmad_MidtermProject_COMP4449.ipynb`

## Tools / Libraries
pandas, numpy, matplotlib, seaborn, scikit-learn
