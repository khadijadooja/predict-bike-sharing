# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### khadija gouraguine


## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
I realize that the predictions can be directly used to add to the submission file.just affect the output of predictions to file submit 
and for changes we need to specify the column count 
### What was the top ranked model that performed?
the top ranked model is WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
the exploratory analysis help to analyse our data and see importance of each features,
i extracted column day from original column datetime with function "to_datetime.dt.day" 

### How much better did your model preform after adding additional features and why do you think that is?
for first time i added just one feautre 'day', the model prefromed a little more better than the original 
but the second time when i added more features, the model preformed lot better, i think that explain the importance of features for fitting our model. so more features = increase score

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
after using more features and diffferent HyperParameters the model much better specially when i augment numbre of trials 
but the training take more time to build the model 
-so for building strong model for resolving our problem ,we must choose right hyperParameters 
### If you were given more time with this dataset, where do you think you would spend more time?
I think if i have more time with the dataset, i would spend time to try more hyperparameters and different models for building the right model that will perform much better whith our data

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
	model	num_bag_folds	num_trials	max_stack_level	score
0	initial	8	1	3	1.81114
1	add_features	8	1	3	1.78080
2	hpo	8	5	3	1.80389
3	features_hpo	8	8	3	0.62597

### Create a line plot showing the top model score for the three (or more) training runs during the project.


![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.


![model_test_score.png](img/model_test_score.png)

## Summary
in this project we lean :
how to analyse and extract data for training our model 
the importance of type and adding features to best fitting
use different hyperParameters for augment performance score 

