# Mice Protein Expression Analysis

## Overview
This project explores the **Mice Protein Expression** dataset from the UCI Machine Learning Repository. The goal is to identify protein-level patterns that distinguish **control** and **trisomic (Down syndrome model)** mice using statistical and machine learning approaches in R.

## Dataset
- **Source:** UCI Machine Learning Repository  
- **Samples:** 1080 measurements from 72 mice  
- **Features:** 77 protein expression levels (continuous)  
- **Labels:** 8 experimental classes based on genotype, treatment, and behavior  
- **License:** CC BY 4.0  

Each sample corresponds to protein expression in the mouse cerebral cortex, measured under different experimental conditions.

## Objectives
1. Clean and preprocess the dataset for analysis.  
2. Visualize protein expression differences between genotypes.  
3. Apply logistic regression, Bayesian modeling, and random forest classification.  
4. Compare accuracy and interpret the most predictive proteins.  

## Methods
1. **Data Cleaning:** Removed incomplete rows, extracted genotype from class labels.  
2. **Exploratory Data Analysis:** Examined summary statistics, correlations, and distribution differences.  
3. **Modeling Approaches:**  
   - *Logistic Regression* to estimate interpretable coefficients.  
   - *Bayesian Logistic Regression* with posterior credible intervals.  
   - *Random Forest* to capture nonlinear patterns and feature importance.  
4. **Evaluation:** Measured accuracy and confusion matrices on a 70/30 train-test split.

## Key Findings
- Proteins **DYRK1A**, **ITSN1**, and **SOD1** were consistently the strongest predictors of trisomy, matching their known biological roles on chromosome 21.  
- Logistic and Bayesian models achieved high interpretability with strong predictive accuracy.  
- The Random Forest classifier reached ~98% accuracy and ranked the same proteins as top contributors.  

## Technologies Used
- **Language:** R  
- **Packages:** `readxl`, `dplyr`, `ggplot2`, `randomForest`, `rstanarm`  
- **Output:** Automated PDF report with integrated visualizations and analyses.  

## How to Run
```r
# Install required packages
install.packages(c("readxl", "dplyr", "ggplot2", "randomForest", "rstanarm"))

# Knit the R Markdown file to generate the PDF report
rmarkdown::render("mice_protein_analysis.Rmd")
