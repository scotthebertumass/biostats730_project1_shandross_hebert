# Project Proposal

## Goal

Predict survival of patients with heart failure and compare our bayesian model against the paper's machine learning methods (best-performing models)

## Reference Paper's Approach

Apply machine learning classifiers to build initial prediction model and identify most important risk factors, then use those top 2 only to build another machine learning prediction model -> they discovered the 2-predictor model to be better than the one that use all predictors

- Initial predictor model
- One linear statistical method (Linear Regression),
- Three tree-based methods (Random Forests, One Rule, Decision Tree),
- One Artificial Neural Network (perceptron),
- Two Support Vector Machines (linear, and with Gaussian radial kernel),
- One instance-based learning model (k-Nearest Neighbors),
- One probabilistic classifier (Naïve Bayes), andan ensemble boosting method (Gradient Boosting)

Ranking of risk factors

- Statistical: common univariate tests such as Mann–Whitney U test [85], Pearson correlation coefficient [86], and chi square test [87] to compare the distribution of each feature between the two groups (survived individuals and dead patients), plus the Shapiro–Wilk test [88] to check the distribution of each feature
- Machine learning: random forests only

Final predictor models

- Tried bunch of machine learning methods, selected models were random forests (top performing on all features), gradient boosting and svm with radial gaussian kernel (shown efficient performance for medical informatics data)

Also stratified logistic regression using follow up time for a second analysis (this out performed the other model without follow up time)

## Approach

- Using a (non-hierarchical) Bayesian model with serum creatinine and ejection fraction as predictors to create a logistic regression model
- For comparison, create a Bayesian logistic regression model without predictors
- Create another Bayesian logistic regression model using follow-up time, if possible
