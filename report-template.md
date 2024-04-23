# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Nicole Dcosta

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
 I realized that the output format of the predictor needed to be compatible with the submission requirements.

### What was the top ranked model that performed?
 WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
we found the different types of  data changed the int to categorical split `datetime` to 3 different features and also added peak_hour as the additional feature 

### How much better did your model perform after adding additional features and why do you think that is?
a lot better from 1.79973 to 0.46327
increased feature relevance and better representation

## Hyperparameter tuning
### How much better did your model preform after trying different hyper parameters?
compared to the first model 1.79973 to 0.51326 
compared to the second model 0.46327 to 0.51326 

### If you were given more time with this dataset, where do you think you would spend more time?
finding better relation between the features,tunning more parameters


### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.


| Model         | hpo1         | hpo2          | hpo3           | Score   |
|---------------|--------------|---------------|----------------|---------|
| initial       | mentionted   | mentioned     | mentioned      | 1.79973 |
| add_features  | mentioned    | mentioned     | mentioned      | 0.46327 |
| hpo           | GBM,NN       | GBM,KNN,NN    | GBM,KNN,NN,XGB | 0.51326 |


### Create a line plot showing the top model score for the three (or more) training runs during the project.

![image](https://github.com/Nicole09999/bike_rentals_prediction/assets/106644205/93598bbd-f5bb-4196-8936-2337c0ad396d)


### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.
![image](https://github.com/Nicole09999/bike_rentals_prediction/assets/106644205/b4cbc766-e1ef-4338-98ed-110dda2cb3a8)


## Summary
Initial Model: This is the baseline model without any hyperparameter optimization or additional features. It achieved a score of 1.79973.
Add Features Model: After adding additional features and maintaining the same hyperparameter optimization settings as the initial model, the score significantly improved to 0.46327. This suggests that the added features contributed positively to the model's performance.
HPO Model: This model underwent hyperparameter optimization with various configurations, including different combinations of models (GBM, KNN, NN, XGB). Despite the hyperparameter tuning, the score slightly increased to 0.51326 compared to the model with added features. This indicates that while hyperparameter optimization helped, the added features had a more significant impact on improving model performance.
In summary, adding additional features had a substantial positive effect on the model's performance, while hyperparameter optimization provided further but relatively minor improvements.
