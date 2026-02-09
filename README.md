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
- `data/` - insurance.csv and 2015_formats.json files

## Data

All datasets are located in the `data/` folder.

### Included Files

- `insurance.csv` — Medical Cost Personal dataset used for insurance charge prediction modeling.
- `2015_formats.json` — Official BRFSS metadata file used to decode survey variables and value labels for proper interpretation and preprocessing.

⚠️ **Important Note**

The full BRFSS annual survey CSV files (2011–2015) are **not included** in this repository due to GitHub file size limitations.

To reproduce the full BRFSS analysis:

1. Download the Behavioral Risk Factor Surveillance System (BRFSS) dataset from Kaggle:  
   https://www.kaggle.com/datasets/cdc/behavioral-risk-factor-surveillance-system

2. Place the downloaded yearly CSV files (e.g., `2011.csv`, `2012.csv`, `2013.csv`, `2014.csv`, `2015.csv`) inside the `data/` folder locally before running the notebook.

These files are required to execute the BRFSS exploratory analysis, statistical testing, and logistic regression modeling sections of the notebook.


## How to Use
Open and run the notebook:
- `Orwa_Ahmad_MidtermProject_COMP4449.ipynb`

## Tools / Libraries
pandas, numpy, matplotlib, seaborn, scikit-learn
