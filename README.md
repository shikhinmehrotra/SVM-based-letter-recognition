# SVM-based-letter-recognition
This project builds a linear SVM model to predict which letter of the alphabet is present in a image.

# Data set
The data set consists of various attributes such as the height of the box containing the letters, width of the box and various other dimensions related to the letter.

# Data visualisation and data preparation
Barplot is built to visualise the value of one of the attributes for each of the letters. Further, a heat map is built to visualise the correlation amongst different attributes. This is followed by scaling of data and splitting it in test and training data.

# Model building
Two models are built simultaneously. One model is a linear Support Vector Classifier while the other model is a non-linear model that uses a RBF kernel. The preliminary linear model gives an accuracy of ~85% while the non-linear model gives an accuracy of ~93%.

# Hyperparameter tuning
GridSearchCV class of SkLearn is used to find the optimal hyperparameters, gamma and C, which control the non-linearity and softness of the classifier, respectively. For various values of these hyperparameters, plots of train and test accuracy are drawn. The plots depict the following key insights:
1) Non-linear models (high gamma) perform much better than the linear ones
2) At any value of gamma, a high value of C leads to better performance
3) None of the models tend to overfit (even the complex ones), since the training and test accuracies closely follow each other

This suggests that the problem and the data is inherently non-linear in nature, and a complex model will outperform simple, linear models in this case.

# Final model with optimal hyperparameters
A final support vector machine model is built using the optimal parameters found out through hyperparameter tuning. Accuracy is found to be 95.96%.
