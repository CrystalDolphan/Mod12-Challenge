# Module 12 Report

## Overview of the Analysis

* The purpose of the analysis is to test and experiment which model is the best for predicting both healthy loans and risky loans, with imbalanced datasets.
* By using different predictions models, we are aiming to forecast the default probabilities of different loans. A higher score in predictions indicates a higher precision.
* The original variable y (i.e. "loan status") indicates that there are 75036 healthy loans and 2500 risky laons in the dataset.
* The machine learning stages I went through are in the following order: firstly, the train_test_split function was used to split the testing data and training data; secondly, data was fit into the logistic regression model with random state equal to 1; then, to evaluate the model's performance, I calculated the accuracy score and generated the classification report. After that I resampled the data and repeated the above process with the resampled data.
* The main methods I used is logistic regression and random over sampling.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:

  * Description of Model 1 Accuracy, Precision, and Recall scores.
                  pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.91      1.00      0.95      0.91     18765
          1       0.85      0.91      0.99      0.88      0.95      0.90       619

avg / total       0.99      0.99      0.91      0.99      0.95      0.91     19384


* Machine Learning Model 2:

  * Description of Model 2 Accuracy, Precision, and Recall scores.
  
                 pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* As we can see from the results above, machine learning model 2 performs better since it has higher scores than machine learning model 1.
* I think performance depend on the problem we are trying to solve. In this case, it is obvious that risky loans ('1''s) have higher probabilities of default, however, the model performs more poorly when making predictions for risky loans. Hence, even though machine learning model 2 wins over the other one, it still has some flaws we need to improve on. 