# Credit Risk Analysis Report

## Overview of the Analysis

For the analysis of the machine learning models, we:

1) Conducted this analysis in order compare two data sets, an original and overampled set, to determine model accuracy, percision, and recall.
2) The data analyzed included loan size, interest rate, borrower income, debt to income, number of accounts, derogatory marks, total debt, and loan status of potential borrowers. Using historical lending activity, we are creating a model to determine the creditworthiness for borrowers based on the above-mentioned data.
3) To complete our analysis, we must predict variables including y_counts (target value balance), logistic_regression_model (obtained from first instantiating and fitting), balance_accuracy_score, confusion_matrix, and classification_report_imbalanced..
4) The machine learning process went through the following basic steps: obtaining the data then splitting it into training and testing sets; creating first a logistic regression model using the original data and determining the balanced accuracy score, confusion matrix, and imbalanced classification report; use the oversampler module to resample the data; create a new logisitc regression model with the resampled data; lastly, determine the new scores from the new model and compare it to the orignial data model.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1 (Original Data):
  * Accuracy:
  0.9520479254722232
  
  * Precision:
  [[18663,   102],
       [   56,   563]]
       
  * Recall:
  
           pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.91      1.00      0.95      0.91     18765
          1       0.85      0.91      0.99      0.88      0.95      0.90       619

avg / total       0.99      0.99      0.91      0.99      0.95      0.91     19384

* Machine Learning Model 2 (Rebalanced Data):
  * Accuracy:
  0.9936781215845847
  
  * Precision:
  [[18649   116]
 [    4   615]]
  
  * Recall:
  
        pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

* As shown above, the data from the original model is less accurate, less precise, and has lower recall values than the resampled model. 

## Summary

From the machine learning models, the following conclusions can be drawn:

1) The resampled model preforms better in this case. As mentioned above, the resampled data has a 99% accuracy as opposed to 95%, the resampled data has more accurate and fuller clusters, and has higher recall values, making it the better model to utilize. 
2) Does performance depend on the problem we are trying to solve? As indicated by the results of the resampled model, for a better performance, the number of '1s' being predicted increased substantially as opposed to the original data model. 


