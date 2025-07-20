# 🫀 Coronary Artery Disease (CAD) Risk Factor Analysis

This folder contains the cleaned data and R scripts used for analyzing **low-dimensional clinical data** related to **coronary artery disease (CAD)** using the Bayesian hierarchical variable selection framework.

## 📑 Dataset Summary

- **Source**: [UCI Machine Learning Repository – Heart Disease Dataset](https://ieee-dataport.org/open-access/heart-disease-dataset-comprehensive)
- **Samples**: 1190 patients
- **Features**: 11 clinical predictors (e.g., chest pain type, cholesterol, ST depression)
- **Outcome**: Presence or absence of CAD (binary)

## 🧪 Analysis Pipeline

1. **Preprocessing**:
   - Handled missing values (~14% in cholesterol) using MICE (Multiple Imputation by Chained Equations)
   - Cleaned and recoded categorical variables for modeling

2. **Modeling**:
   - Bayesian logistic regression with:
     - Fixed prior: constant inclusion probability (θ = 0.5)
     - Flexible prior: hierarchical Beta–Bernoulli structure that learns θ from data

3. **Variable Selection**:
   - Posterior Selection Probabilities (PSP) used to rank clinical risk factors
   - Credible interval to check the precision of the estimates
   - Model comparison based on Deviance Information Criterion (DIC)

## 📊 Output

- Risk factors such as ST depression, FBS, and chest pain identified with high confidence
- Flexible prior model improved model fit and interpretability (lower DIC)
- Posterior estimates of sparsity (θ) and credible intervals included

## 📁 Files

- `heart_statlog_cleveland_hungary_final.csv`: Cleaned clinical dataset used for modeling
- `cad_ .R`: R script implementing MCMC-based Bayesian logistic regression


## 💡 Notes

This low-dimensional example helps demonstrate how the proposed **flexible sparsity model** adapts to simpler clinical datasets and provides more reliable variable selection than fixed prior approaches.

