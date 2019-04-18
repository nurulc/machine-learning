## Confusion Matrix

The tabulation of actual to predicted, where the rows are the actual labels, and the columns are the predicted values.

![](http://rasbt.github.io/mlxtend/user_guide/evaluate/confusion_matrix_files/confusion_matrix_1.png)


### Sensitivity

True Positive / (True Positive + False Negitive)   

If _C_ is the confusion matrix    *_Sensitivity_* = _C[0,0]/Sum(C[\-,0])_

### Specificity

True Negetive / (False Positive + True Negitive)   

If _C_ is the confusion matrix    *Specificity* = _C[1,1]/Sum(C[\-,1])_
