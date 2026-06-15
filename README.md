# Marketing ROI Analysis Using Simple Linear Regression

## Project Overview

This project investigates the relationship between marketing expenditure and sales performance using Simple Linear Regression. The objective was to identify which advertising channel had the strongest association with Sales and to provide data-driven recommendations for marketing budget allocation.

The analysis involved data cleaning, exploratory data analysis (EDA), feature selection, model development using Ordinary Least Squares (OLS), regression diagnostics, and interpretation of results from a business perspective.

---

## Business Problem

Organizations invest heavily in multiple advertising channels, but determining which channel contributes most effectively to sales growth remains a critical challenge.

This project answers the question:

> Which marketing channel demonstrates the strongest relationship with Sales, and how can this insight inform marketing budget allocation?

---

## Dataset Information

The dataset consists of **4,572 observations** and four numerical variables:

| Variable     | Description                          |
| ------------ | ------------------------------------ |
| TV           | TV advertising expenditure           |
| Radio        | Radio advertising expenditure        |
| Social_Media | Social media advertising expenditure |
| Sales        | Sales generated                      |

After handling missing values and removing records with missing target values, **4,566 observations** remained for analysis.

---

## Project Workflow

### 1. Data Cleaning

* Checked dataset structure and summary statistics.
* Verified duplicate records.
* Identified missing values.
* Applied mean imputation for TV expenditure.
* Applied median imputation for Radio and Social Media expenditure.
* Removed rows with missing Sales values.

### 2. Exploratory Data Analysis

* Examined variable distributions.
* Generated pairplots to explore relationships.
* Computed correlation matrices.

### 3. Feature Selection

Correlation analysis revealed that **TV advertising exhibited the strongest positive relationship with Sales** and was therefore selected as the predictor variable for the Simple Linear Regression model.

### 4. Model Development

* Split the dataset into training and testing sets using an 80:20 ratio.
* Built an Ordinary Least Squares (OLS) regression model using Statsmodels.

### 5. Diagnostic Evaluation

Regression assumptions were assessed using:

* Residuals vs Fitted Plot (Linearity)
* Residual Distribution Plot (Normality)
* Scale-Location Plot (Homoscedasticity)

---

## Key Findings

| Metric            |  Result |
| ----------------- | ------: |
| R-squared         |   0.995 |
| TV Coefficient    |    3.56 |
| TV p-value        | < 0.001 |
| Observations Used |   4,566 |

### Interpretation

* TV advertising expenditure alone explained approximately **99.5% of the variation in Sales**.
* A one-unit increase in TV advertising expenditure was associated with an estimated **3.56-unit increase in Sales**.
* The relationship between TV expenditure and Sales was highly statistically significant.

---

## Business Insight

TV advertising emerged as the strongest predictor of Sales within this dataset.

Although the correlation heatmap displayed a value of 1.00 between TV and Sales, this is likely attributable to rounding in the visualization. The relationship is more appropriately interpreted as an extremely strong positive association rather than a perfect correlation.

These findings demonstrate the importance of relying on empirical evidence rather than assumptions when making marketing investment decisions.

---

## Recommendation

Based on the results of this analysis:

* Prioritize TV advertising when the primary objective is maximizing sales performance.
* Consider allocating a larger share of the marketing budget toward effective TV campaigns.
* Validate these findings alongside broader strategic objectives and additional analyses before implementing long-term budget decisions.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* Scikit-learn
* Jupyter Notebook

---

## Installation

Clone this repository and install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn
```

## Author

**Latifah Bashir**

Completed as part of the **3MTT Data Science Program**, demonstrating the practical application of Simple Linear Regression for marketing ROI analysis and business decision-making.
