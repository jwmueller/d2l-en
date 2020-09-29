# Introduction to AutoML
:label:`sec_intro_automl`

Machine Learning (ML) has advanced significantly in recent years. Nowadays, a successful ML pipeline requires cumbersome administration of numerous techniques for data preprocessing/splitting, feature engineering, model selection, hyperparameter tuning, model ensembling, and transfer learning. As the state-of-the-art progresses in each of these areas, it is difficult even for a ML expert to incorporate all of the recent best practices into their modeling.

Automated machine learning offers an enticing alternative. For the novice, AutoML removes many of the barriers of deploying high performance ML. This is crucial to democratize deep learning techniques, which can only be successfully utilized after many opaque decisions have been properly addressed. For the expert, AutoML offers the potential of implementing best practices for each aspect of the ML pipeline only once, and then being able to repeatedly deploy them. The AutoML system will automatically identify which practices are most appropriate for a given dataset and apply them without human oversight. Rather than manually managing/implementing the modeling pipeline, experts can instead spend their valuable time on domain-specific aspects of their data driven problems such as how to translate ML predictions into business decisions or which additional data to collect.




* Why do we care about AutoML: accessibility, reliability, maintainability, quickest path from raw data to high-quality deployed model. Also laziness.

* Use-case anecdotes (e.g. models that need to be retrained every night, applications with separate models per user or geographic locale, complexity of maintaining best-practices across a full ML pipeline with many steps).

* Short list + two-sentence description of popular existing AutoML tools like AutoWEKA, TPOT, auto-sklearn, H2O, AutoKeras, Auto-Pytorch

* Short overview of AutoGluon and why it is tool-of-choice in this AutoML Chapter (easiest-to-use, most accurate, broadest set of ML capabilities).

* Key considerations for AutoML:
    * Data splitting. For AutoML, accurate estimates of performance on held-out data are absolutely critical to guide design-decisions, so use of multiple training/validation folds is preferable.
    * Evaluation metrics. Evaluation metric can be used to select hyperparameter-values, early-stop iterative training, construct ensembles that combine model-predictions in the way that’s best under the evaluation metric.
    * Training time-limits. Imposition of time-limits on the training process is crucial to ensure good user-experience but may change ML intuition about what is best.
        * For example, if 6-layer neural network is the best model if trained long enough, but 3-layer network can achieve 99.9% of the accuracy in 1/4 of the training-time, one probably achieves superior accuracy under same time-limit by ensembling 4 different 3-layer networks.
        * Ideal AutoML system should monotonically improve with more training time, however, overfitting becomes increasingly dangerous. Example: HPO with fixed validation dataset and many hyperparameters that can be tuned is particularly prone to overfitting if run for long time.
        * Also - Algorithm failure. Fault tolerant ML design
    * Key user-inputs for AutoML: Evaluation Metric, Training time-limits, Feature Engineering based on Domain Knowledge, Deployment considerations (e.g. is reducing accuracy to achieve superior latency desirable).


## AutoGluon

Our code examples rely on AutoGluon, an easy-to-use AutoML framework that focuses on deep learning and real-world applications spanning image, text, or tabular data (github.com/awslabs/autogluon/). With hardly any code, AutoGluon can produce accurate ML models that empirically outperform other AutoML solutions as well as many data scientists. AutoGluon provides best in-class models from various sources including GluonCV/GluonNLP, CatBoost, and scikit-learn. AutoGluon can additionally be used by data scientists to tune their existing bespoke models implemented in frameworks like MXNet or PyTorch, and improve how these models are being utilized.


## Summary


## Exercises

