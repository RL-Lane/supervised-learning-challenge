# supervised-learning-challenge

### Robert Lane

This project analyses borrower data from [Lending Club](https://www.lendingclub.com/) to predict whether or not future borrowers would be considered high risk for loan repayment.

Further exploration of methods and coding can be found in the Jupyter Notebook included within this repository.

### Conclusions  

To interpret the data correctly, please note that a positive result indicates that the potential borrower is considered to be high risk.  For lenders, false negatives may be dangerous because that could mean the lender takes on too much risk, or at least takes on risks without associated interest rates to account for that.  False positives are also a problem, because offering rates that are too high can lead to a loss of customers who shop for better rates elsewhere.

* Unscaled:  
  *   Logistic Regression:
    *     This has far too many false positives, so true predictions are almost random.

  *   Random Forest Classifier:
    *     Overall, it's better than Logistic Regression here, but it has too many false negatives - in fact, it has more false negatives than true positives

* Scaled:  
  *   Logistic Regression:
    * Reasonable fits in all categories listed: accuracy, precision, sensitivity, and specificity.  It would be nice to have measurement scores above 90%, but given some of the poor performance the other models demonstrated in the confusion matrix, this one seems to be the best overall in most cases.

  * Random Forest Classifier:  
    * In this case, the Random Forest Classifier has an awful sensitivity score because there are several times as many false negatives as true positives.


Overall, I would have to rate the Scaled Logistic Regression as the best overall model used in this analysis.

One final thing to note is that since the test data isn't a random sample of the same dataset as the training set, it can be affected by external changes.  The big one would be the introduction of Covid-19, which wouldn't have been affecting any data prior to 2020.
