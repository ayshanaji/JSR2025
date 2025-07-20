# 🧬 Breast Cancer Gene Expression Analysis

This folder contains the data and R scripts used for applying the **Bayesian hierarchical variable selection model** to **high-dimensional breast cancer gene expression data**.

## 📑 Dataset Summary

- **Source**: [TCGA Breast Cancer (BRCA) cohort via UCSC Xena](https://xenabrowser.net/datapages/?cohort=TCGA\%20Breast\%20Cancer\%20(BRCA)\&removeHub=https\%3A\%2F\%2Fxena.treehouse.gi.ucsc.edu\%3A443)
- **Samples**: 1,218 patients
- **Features**: 20,531 genes (RNA-seq expression levels)
- **Outcome**: Disease-specific survival (DSS)

## 🧪 Analysis Pipeline

1. **Preprocessing**:
   - Gene filtering based on univariate p-values

2. **Modeling**:
   - Bayesian logistic regression with hierarchical Beta–Bernoulli priors
   - MCMC sampling via Metropolis–Hastings and Gibbs steps

3. **Variable Selection**:
   - Posterior Selection Probability (PSP) computed
   - Comparison of fixed vs. flexible sparsity priors

## 📊 Output

- Top genes with high PSPs under both models
- Posterior estimates of sparsity
- DIC comparison with baseline model

## 📁 Files

- `rnaseq_top50.csv`: Selected top 50 genes based on univariate filtering
- `brca_model.R`: Code for running Bayesian model
- `brca_results.pdf`: Posterior summaries and plots

## 🔍 Notes

This analysis supports the thesis work on **flexible Bayesian variable selection**. The flexible model adapts better to high-dimensional omics data by estimating sparsity directly and enhancing interpretability.

