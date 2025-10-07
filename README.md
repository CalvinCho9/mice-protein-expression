# Mice Protein Expression Analysis in R

## Overview
This project analyzes the Mice Protein Expression dataset from the UCI Machine Learning Repository using R. The dataset contains protein expression levels measured in the cerebral cortex of control and trisomic (Down syndrome model) mice. The project demonstrates a complete bioinformatics data science workflow, including data cleaning, exploratory visualization, statistical modeling, and machine learning classification.

## Dataset
- **Source:** UCI Machine Learning Repository  
- **Samples:** 1080 observations from 72 mice  
- **Features:** 77 protein expression measurements  
- **Labels:** 8 experimental groups based on genotype, treatment, and behavioral conditions  
- **License:** CC BY 4.0  

## Objectives
- Identify key proteins that differentiate control and trisomic mice.  
- Compare regression, Bayesian, and ensemble learning methods.  
- Evaluate model interpretability and performance.  

## Methods
1. **Data Preprocessing**
   - Imported Excel dataset and removed missing values.  
   - Encoded categorical variables (Genotype, Treatment, Behavior).  
   - Scaled continuous protein expression features for consistency.  

2. **Exploratory Data Analysis**
   - Computed summary statistics for selected proteins.  
   - Visualized distributions using `ggplot2` boxplots.  
   - Explored pairwise correlations between protein features.  

3. **Modeling**
   - **Logistic Regression:** Baseline model predicting genotype using selected protein features.  
   - **Bayesian Logistic Regression:** Implemented via `rstanarm` to estimate posterior credible intervals for coefficients.  
   - **Random Forest:** Full-feature ensemble model to classify genotypes and identify top protein predictors.  

4. **Evaluation**
   - Accuracy and confusion matrix on held-out test data.  
   - Feature importance ranking from random forest.  
   - Comparison of model interpretability and predictive performance.  

## Key Findings
- Proteins **DYRK1A**, **ITSN1**, and **SOD1** are the strongest predictors of the trisomic genotype, consistent with their biological roles on chromosome 21.  
- Logistic and Bayesian models achieved similar coefficient estimates with high confidence intervals.  
- Random forest achieved over 97% classification accuracy, confirming robustness and consistency across modeling methods.  

## Technologies Used
- **Language:** R  
- **Libraries:** `tidyverse`, `readxl`, `ggplot2`, `randomForest`, `rstanarm`  
- **Environment:** RStudio / Jupyter with R kernel  

## Results Summary
| Model Type             | Key Features Used                 | Accuracy | Notes |
|------------------------|----------------------------------|-----------|-------|
| Logistic Regression    | DYRK1A, ITSN1, SOD1, BRAF, pERK  | ~97%      | Simple, interpretable |
| Bayesian Regression    | Same as above                    | ~97%      | Adds uncertainty quantification |
| Random Forest          | All 77 protein features           | ~98%      | Highest performance, feature ranking |

## How to Run
```r
# Install dependencies
install.packages(c("readxl", "dplyr", "ggplot2", "randomForest", "rstanarm"))

# Run the analysis
source("mice_protein_analysis.R")
