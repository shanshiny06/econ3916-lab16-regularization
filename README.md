# econ3916-lab16-regularization
# Regularization: Buying Bias to Sell Variance

## Objective

I tested how LASSO and Ridge trade a small amount of bias for lower variance compared to OLS, on a problem with many more predictors than real signals.

## Methodology

- I built a simulated dataset with 200 predictors, of which only 5 had a real effect on the outcome, and used 105 rows for training.
- I fitted OLS, Ridge, and LASSO to the training data and compared their mean squared error on a held-out test set.
- I traced the LASSO path as the penalty decreased, recording the step at which all five true predictors had entered and the step at which the first noise variable entered.
- I chose the LASSO penalty by 5-fold cross-validation, fitting the scaler inside each fold so that no information from the validation fold leaked into training.
- I scored LASSO's selected variables against the known truth, counting how many of the 5 true predictors it found and how many noise variables it wrongly kept.
- I gave LASSO and Ridge two near-duplicate predictors to see how each method handles correlated inputs.
- I wrote my own prompt asking an AI to produce the cross-validation loop, refined it over several rounds, and checked its chosen lambda and CV MSE against my own results.

## Key Findings

- **Test MSE:** OLS scored [YOUR VALUE], Ridge scored [YOUR VALUE], and LASSO scored [YOUR VALUE].
- **LASSO path:** All five true predictors were in the model from step [YOUR VALUE], and the first noise variable entered at step [YOUR VALUE].
- **Cross-validation:** 5-fold CV chose lambda = [YOUR VALUE], with a CV MSE of [YOUR VALUE].
- **Variable selection:** LASSO found [YOUR VALUE] of the 5 true predictors and kept [YOUR VALUE] false positives.
- **Near-duplicate predictors:** LASSO put [YOUR VALUE] on one predictor and zero on the other. Ridge split the weight between them, giving [YOUR VALUE] and [YOUR VALUE].
- **AI-assisted CV loop:** I went [YOUR VALUE] rounds with the AI before I was satisfied with the code. When I compared its lambda and CV MSE with mine, I found [YOUR RESULT].
