# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Mathea Myhrvold

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I did not have any difficulties submitting the initial training. 

### What was the top ranked model that performed?
The last model with the tuned hyperparameters.

Using the fit_summary and leaderboard:
The best model for the training run was KNeighborsDist
For the additional feature, the best model was WeightedEnsemble_L2
For the hyperparameter optimization, the best model was WeightedEnsemble_L2

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Splitting up the datetime column significantly improved results, most likely due to the trend that bike sharing changes the most as the hour changes and less on day of the week or month. I added additional features by splitting the datetime column into day of week and hour.

### How much better did your model preform after adding additional features and why do you think that is?
Model score went from -92.442085 to -32.443595. Most likely due to the trend that bike sharing changes the most as the hour changes and less on day of the week or month

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The model perfromed roughly the same after hyper parameter tuning. Model score: -32.443595 to -36.902817. This is due to my inability to tune more than the 'GBM' hyperparameters. 

### If you were given more time with this dataset, where do you think you would spend more time?
I would like to get more hyperparamters tuned. This would likely improve my model even more.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|   | model        | hpo1 | hpo2 | hpo3 | score   |   |
|---|--------------|------|------|------|---------|---|
| 0 | initial      | NA   | NA   | NA   | 1.86412 |   |
| 1 | add_features | NA   | NA   | NA   | 0.52719 |   |
| 2 | hpo          | GBM  | GBM  | GBM  | 0.52476 |   |

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
Tuning of the model hyperparameters and adjusting the data columns greatly improves model performance, and should be explored when training models to best predict unseen data. 
