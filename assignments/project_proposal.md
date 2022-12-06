# Project Proposal

## Group Members

- Li Shandross
- Scott Hebert

## Summary Description

Predict survival of patients with heart failure and compare our Bayesian model(s) against the paper's machine learning methods (best-performing models)

Outcome of interest: survival rate of patients with heart failure

The original authors applied machine learning classification to build initial prediction models, identify the most important risk factors of survival for patients with heart failure, and use the top two risk factors to create three new prediction models. They also performed further analysis by creating a categorical follow-up time variable in which they used stratified logistic regression, both for models with all predictors and models with only the two most important risk factors.
This project will center around building a hierarchical, logistic regression Bayesian model using serum creatinine and ejection fraction as predictors, using follow-up time as groups. We will compare this against the authors' models, and if time allows, we will also build several other models for comparison, which may include: a (non-hierarchical) Bayesian logistic regression model without predictors, a hierarchical Bayesian logistic regression model with all predictors, a non-hierarchical Bayesian logistic regression model with all predictors, a non-hierarchical Bayesian logistic regression model with the top two predictors.

## Dataset

A dataset that contains the medical records of 299 patients who had heart failure, collected during their follow-up period, where each patient profile has 13 clinical features. [https://archive.ics.uci.edu/ml/datasets/Heart+failure+clinical+records]

## Reference paper

Chicco, D., Jurman, G. Machine learning can predict survival of patients with heart failure from serum creatinine and ejection fraction alone. BMC Med Inform Decis Mak 20, 16 (2020). https://doi.org/10.1186/s12911-020-1023-5

## Action Plan

- Use dplyr package to create follow-up time variable (as described in the paper) and otherwise manipulate the data to prepare it for analysis
- Replicate simple logistic regression used in the study (not including the machine learning methods) as a quality check
- Determine model equations for the main Bayesian model (Bayesian hierarchical logistic regression model with predictors of serum creatinine level and ejection fraction)
- Implement the model in rstan
- Compare Bayesian hierarchical logistic regression model to the machine learning methods described in the reference paper, creating a train/test split if necessary
- Implement and test other Bayesian models described above where time allows
