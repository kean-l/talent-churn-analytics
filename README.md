# Top-Talent Churn — HR Analytics

Predicting which high-performing employees are at risk of leaving an IT company,
and turning that into an action plan management can actually use.

## Overview
Team case study for UvA Business Analytics, built on a provided IT-company
scenario dataset (small, synthetic — so the focus is on method, not headline
accuracy). The goal: identify "top talent" likely to churn early enough to
intervene.

## Tech
Python · scikit-learn · SHAP · pandas

## What I did
- Defined "top talent" from performance data using a threshold backed by the
  Pareto principle and a natural break in the distribution.
- Optimised the models for **recall** rather than accuracy, on the reasoning
  that missing a genuine flight risk is the most expensive error for the
  business (far costlier than a false alarm).
- Compared logistic regression, random forest, and gradient boosting; chose
  logistic regression after the tree models overfit the small dataset.
- Used **SHAP** to explain individual predictions and surface the drivers of
  turnover, keeping the model transparent for non-technical stakeholders.
- Built an executive dashboard with a "talent value at risk" figure and a
  watchlist of the highest-risk top performers, translated into concrete
  retention recommendations.

## Notes
With a small, synthetic dataset the priority was sound methodology — honest
validation, explainability, and a clear business translation — rather than
chasing an impressive-looking score on data that wouldn't support it.
