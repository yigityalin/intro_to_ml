For questions 2.2 and 2.3, the NaiveBayesClassifier class is implemented. Since the most of the code is identical for these two questions, there is only one class. This class has two parameters: estimator and alpha. When an instance of this class is created with parameter estimator = 'mle', the alpha value is ignored and the classifier uses the MLE, which is what Question 2.2 asks. When an instance of this created with parameter estimator = 'map', the classifier uses the MAP estimator, which is what Question 2.3 asks. For MAP estimator, the alpha parameter is not ignored. It determines the alpha term in the additive smoothing. Note that this is the same alpha as in the description of question 2.3 in the homework pdf. By setting alpha = 1, we obtain the answer for question 2.3.

The explanation of the methods:

fit: calculates the priors and likelihoods and stores it in the model.
get_scores: calculates the log probability (not exactly the probability but a scaled version) of the sample being in each class (only for fitted model)
predict: calls the get_scores method and returns the class with the highest score (only for fitted model)
evaluate: calculates the accuracy of the classifier on a given dataset (only for fitted model)
confusion_matrix: constructs the confusion matrix for a given dataset (only for fitted model)

Further explanation and example usage can be found in the .ipynb file.