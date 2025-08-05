# CORAL-Siblings

This repository contains code and analysis related to a metagenomic study investigating the association between siblings, infant microbiome composition, and protection from allergic sensitization. Sequencing files are available under BioProject ID PRJNA1274946 and subject metadata is available at FigShare (DOI 10.6084/m9.figshare.24922716).

#
# KEGG Pathway ML Evaluation
**Overview**

This repository contains a Jupyter Notebook that performs exploratory feature correlation analysis and compares multiple machine learning models for classification. The aim is to identify patterns in the data (via correlation coefficients) and evaluate a variety of ML approaches on classifying samples into groups of healthy/unhealthy.

The analysis uses a filtered KEGG pathway abundance file as input. This file was generated from metagenomic sequencing data and pre-filtered to include only KEGG orthologs significantly higher in infants with siblings (assessed via Maaslin2). 

**Methods Summary**

1. Feature Correlation Analysis
- Pearson correlation: Identifies top 10 positive and 10 negative correlations between features.
- Spearman correlation: Identifies top 10 positive and negative rank-based correlations.

2. Model Comparison
The following models were trained and evaluated:

- L1 (Lasso) Logistic Regression
- L2 (Ridge) Logistic Regression
- Elastic Net Logistic Regression
- XGBoost
- Random Forest
- Support Vector Machine (SVM)
- Light Gradient Boosting Machine (LightGBM)

  Evaluation Metrics:

  - Accuracy
  - ROC AUC
  - Log Loss
  - Confusion Matrix
  - Precision, Recall, and F1-score (Classification Report)
