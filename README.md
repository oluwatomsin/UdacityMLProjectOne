# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Useful Resources
- [ScriptRunConfig Class](https://docs.microsoft.com/en-us/python/api/azureml-core/azureml.core.scriptrunconfig?view=azure-ml-py)
- [Configure and submit training runs](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-set-up-training-targets)
- [HyperDriveConfig Class](https://docs.microsoft.com/en-us/python/api/azureml-train-core/azureml.train.hyperdrive.hyperdriveconfig?view=azure-ml-py)
- [How to tune hyperparamters](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters)


## Summary
**The dataset contains information about a marketing campaign from a banking network. Information included age, marital status, default, loan information, and education. The bank is looking to predict the probability of a successful engagement with clients.

"**

**The best performing model was a voting ensemble model generated using AutoML with an accuracy of 0.9180.
"**

## Scikit-learn Pipeline
**logistic regression model was used initially with our hyperdrive configuration. The hyperparameters 'Max iterations' and 'C', were tuned for our logistic regression.so the logic behind this experiment it to choose the hyperparameter that gives the best accuracy. **

**Randomparameter sampler is much faster that other parameter samplers**

**The bandit policy helps stop the run after a specified number of run with no significant increase it accuracy. It imporves run time and prevents wastage of resources.**

## AutoML
**The best performing model was Voting ensemble model. Other models include 'XGBoostClassifier', 'LogisticRegression', 'SGD', 'LightGBM', 'XGBoostClassifier', 'XGBoostClassifier', 'XGBoostClassifier'.**

## Pipeline comparison
**In both cases, we recorded quite a high accuracy of 92% in AutoML and 91% in hyperdrive. Although it will be recommended that in cases where resources are limited, hyperdrive is a better option becuase it runs faster and doesn't consume much resources unlike AutoML which takes time and consumes resources, Although my produce better models accuracy.**

## Future work
**There is class imbalance, we could get more data to improve the model.**