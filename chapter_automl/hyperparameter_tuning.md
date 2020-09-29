# Hyperparameter Tuning
:label:`sec_hyperparameter_tuning`

Hyperparameter Optimization (HPO)

## Hyperparameter Search Space

Examples of Hyperparameter search spaces (e.g. searching on log-scale vs linear-scale).

Appropriately-sizing search space (need to consider runtime).

Start with good initial default hyperparameter values to ensure reasonable anytime performance.

### AutoGluon Example


## Hyperparameter Optimization Algorithms

###  Random Search

Why Random search > grid search for larger spaces

Random search can be used for HPO in AutoGluon as follows...

### Bayesian optimization

Basic overview

Batch BayesOpt rather than fully sequential

Bayesian optimization can be used for HPO in AutoGluon as follows...


### Hyperband

Briefly mention asynchronous variants like ASHA

BOHB, A-BOHB

Multifidelity HPO can be used in AutoGluon as follows...


## Implementation Issues

Difference between objective function for model-training and evaluation metric for HPO

Overfitting with extensive HPO, and how cross-validation can mitigate it.

Importance of good default HP values to ensure reasonable anytime-performance.

Refitting models to full training+validation data post-HPO.

Overfitting validation set.


## Summary


## Exercises

