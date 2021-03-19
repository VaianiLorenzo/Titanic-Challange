# Titanic-Challange
### Kaggle challange: Titanic - Machine Learning from Disaster (https://www.kaggle.com/c/titanic/overview)
The competition is simple: use machine learning to create a model that predicts which passengers survived the Titanic shipwreck.

The data is located in the "/datasets" folder and has been split into two groups:
  - training set (train.csv)
  - test set (test.csv)
Note that the test set does not have labels: the prediction must be evaluated uploding them on the Kaggle website. 

The "/scripts" folder contains the scripts, one for each new version of the code. 

The "/outputs" folder contains the predictions obtained for each version of the main script. 

### Version 1
All the categorical features are processed with the one-hot encoding and the missing values are managed. 
Four different binary classifier are tested and the best one is selected to predict th test labels. 
Results are not very good: accuracy of ~83% on training set (obtained with random forest) ~63% on test set(assigned by kaggle).

### Version 2 (Starting from version 1)
Family member counter features are replaced by a unique global counter and an "is alone" flag feature. Moreover the lenght of name feature is added.
Results are worse: accuracy of ~83% on training set (obtained with random forest) ~56% on test set (assigned by kaggle).

### Version 3 (Starting from version 2)
Each subset of feature obtained with a one-hot representation is replaced with a single categorical feature (from 0 to N) in order to reduce the dimensionality. 
Results are now good: accuracy of ~83% on training set (obtained with random forest) ~77% on test set (assigned by kaggle).
