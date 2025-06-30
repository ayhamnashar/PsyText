# Baseline Model

## Overview

This folder contains the implementation and evaluation of several baseline models for the project. Baseline models are simple models that serve as reference points for evaluating the performance of more complex models developed later.

## Model Choice

I implemented and compared several baseline models:
- **DummyClassifier:** Predicts the most frequent class and serves as a naive reference.
- **Logistic Regression:** A simple, interpretable linear model using Bag-of-Words and TF-IDF features.
- **Naive Bayes:** A probabilistic model commonly used for text classification.

These models were chosen because they are fast to train, easy to interpret, and provide a meaningful lower bound for model performance.

## Feature Selection

Only the tweet text was used as input feature, transformed using Bag-of-Words (CountVectorizer) and TF-IDF. This ensures a fair and simple baseline without engineered features.

## Implementation

All models were trained and evaluated using the same train/test split. The code includes:
- Data exploration (class and text length distribution)
- Model training and prediction
- Calculation of multiple metrics (accuracy, precision, recall, F1-score)
- Visualization of results (performance comparison and confusion matrix)

## Evaluation

The following metrics were used to evaluate the models:
- **Accuracy:** Overall correctness of the model.
- **Precision, Recall, F1-score:** To account for class imbalance and provide a more detailed performance view.

The results are summarized in a comparison table and visualized in bar charts and confusion matrices.

## Submission

Completed [baseline_model.ipynb](baseline_model.ipynb) notebook as part of the project.

## Notes

- The best baseline accuracy is saved for comparison with advanced models.
- All results and visualizations are documented in the notebook.