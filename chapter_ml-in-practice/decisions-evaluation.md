# From Prediction to Making Decisions
:label:`sec_decisions_evaluation`

### Decisions, Risk, and Estimates

Checklist to ensure standard supervised learning is appropriate, including:
    1. examples must be statistically independent
    2. future test data should follow the same distribution as present dataset (is there selection bias?)
    3. caution about datasets containing time (temporal drift)
    4. caution about feedback loops (where predictions influence future behavior/data)
    5. caution about role of rarely-occurring classes in datasets for multiclass classification
    6. caution about whether or not extrapolation is desired for regression and how to facilitate this (eg. linear-models/neural-networks/gradient-boosted-trees may extrapolate, RF/KNN models will not extrapolate, can transform data to encourage extrapolation or discourage).

### Evaluation Metrics

Accuracy vs Calibration/confidence.

AUC, class-imbalance, calibration, confusion matrix.

Strategies for balancing training data (SMOTE, per mini-batch class balancing)

Fairness

### Expected Risk Minimization

Which training objectives to adopt for which evaluation metrics

Miscellaneous practical tips:

For classification metric like log-loss, need to ensure AutoML system never outputs predicted-probabilities = 0.

For regression metric like Root Mean Squared Logarithmic Error (e.g. often used if predicting non-negative values like delivery-time where underestimation may make customers unhappy), can transform Y-values via log(x + 1), and transform model-predictions via the inverse: exp(y) - 1, adopting the MSE metric for training.

For AUROC evaluation metric, it’s often actually better to early-stop based on log-likelihood metric for certain iteratively-trained models like gradient-boosted trees.

### Variance Penalties

Markowitz and beyond, Gorillas


## Summary


## Exercises

