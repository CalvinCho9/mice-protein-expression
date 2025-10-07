# mice-protein-expression
Overview

This project analyzes the Mice Protein Expression dataset from the UCI Machine Learning Repository using statistical and machine learning techniques to identify proteins that distinguish control and trisomic (Down syndrome model) mice. The analysis demonstrates a complete workflow for biological data exploration and modeling in R.

Dataset

Source: UCI Machine Learning Repository

Samples: 1,080 protein expression measurements from 72 mice

Features: 77 protein variables from cerebral cortex tissue

Labels: 8 experimental classes based on genotype, treatment, and behavior

The dataset provides measurements of protein expression in the cerebral cortex for control and trisomic mice under different drug and behavioral conditions.

Methods

Data Preprocessing

Imported the dataset directly from the UCI repository

Cleaned missing values and standardized column names

Encoded categorical variables for modeling

Exploratory Data Analysis

Examined protein expression distributions by genotype

Visualized feature correlations and class balance

Modeling

Logistic Regression: Built an interpretable baseline model to classify genotype

Bayesian Logistic Regression: Quantified uncertainty using posterior distributions via rstanarm

Random Forest: Applied an ensemble method to classify genotype and identify the most predictive proteins

Evaluation

Compared model performance on training and test sets

Used accuracy, confusion matrices, and feature importance rankings

Results

All three models achieved strong classification performance, with logistic and Bayesian regression identifying DYRK1A, ITSN1, and SOD1 as significant predictors, and random forest confirming their importance. These results align with known biological patterns in trisomic mice, where chromosome 21 genes are overexpressed.
