# A Data driven Bayesian hierarchical variable selection method for logistic regression and sparsity estimation
Code and documentation for a flexible Bayesian logistic regression model using a hierarchical beta-Bernoulli prior for variable selection. Includes real-world applications on clinical and genomic data with MCMC inference.
## Abstract 
This study proposes a flexible and data-driven hierarchical Bayesian variable selection method that simultaneously selects variables and estimates sparsity using a beta-Bernoulli prior. The results of this model are compared to those of a standard Bayesian variable selection method employing a non-hierarchical prior with a fixed selection probability. For this study, sparsity is defined as the proportion of relevant variables among all the variables in a dataset. The method is applied to two datasets: coronary artery disease (CAD) and breast cancer (BC). The proposed method yielded a smaller deviance information criterion (DIC) than the fixed-prior model, indicating improved fit to the data while penalizing for complexity.


The method yielded more precise (i.e., narrower) credible intervals, especially for the significant predictors, than the method with fixed-prior selection probability. In the low-dimensional CAD dataset, variables such as asymptomatic chest pain, male sex, elevated fasting blood sugar, exercise-induced ST depression, and high cholesterol were found to be positively associated with CAD. Conversely, upsloping or downsloping ST slope and a higher maximum heart rate were negatively associated. For the high dimensional BC dataset, the method identified 19 genes, compared to 14 selected by the model with fixed prior. Notably, SERPINA1, GSTT2, and RGS4, previously reported in cancer literature, were detected by the model, along with five newly selected genes such as PARP3, ABCG4, CCDC57, SH3GL3 and TMEM105. The estimated sparsity values for the CAD and BC datasets were 0.88 and 0.73, respectively.

## Datasets used in this study

1. **Coronary artery disease dataset**
   **Source**: [UCI Machine Learning Repository – Heart Disease Dataset](https://ieee-dataport.org/open-access/heart-disease-dataset-comprehensive)
   Description: Contains clinical and demographic variables for CAD diagnosis.
2.  **Breast Cancer Gene Expression dataset**
   **Source**: [TCGA Breast Cancer (BRCA) cohort via UCSC Xena](https://xenabrowser.net/datapages/?cohort=TCGA\%20Breast\%20Cancer\%20(BRCA)\&removeHub=https\%3A\%2F\%2Fxena.treehouse.gi.ucsc.edu\%3A443)
    Description: High-dimensional gene expression profiles with DSS outcomes.
    
## Acknowledgment

The authors acknowledge the funding of this project by the Natural Sciences and Engineering Research Council of Canada (NSERC) to Jabed Tomal.
