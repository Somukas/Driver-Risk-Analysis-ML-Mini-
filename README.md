This is a python code that tries to analys risk by the methodology given by Ding et al.
Result
XGBoost gave an accuracy of 82% which is acceptable but not as good as the original implementation. The problem here is the roc_auc score. A low score indicates that the model is unable to differentiate between positive and negative classes. This occurs due to imbalanced data, something that should have been dealt with when SMOTE was used. In fact, not using SMOTE gives a higher accuracy while the score remains unchanged. 

ROC AUC Score: 0.5416781097931809
Accuracy: 82.06%


Logistic Regression gave an accuracy of 84% which is again acceptable. It behaved similarly with the score and gave the same results that XGBoost gave. This signifies that either the dataset has some problem or the algorithms used do not fit it which should not be happening as the features used are similar to that used in the base paper. Another problem may be that the dataset is not as big as the base paper’s but holds more diversity i.e. the base paper only worked with bus drivers.     

Conclusion
This low score, and the extremely low values of importance indicate that the risk we will assign to the drivers have a high chance of being incorrect as the models are unable to actually understand and identify the patterns found in the dataset. Again, as the dataset was not obtained from any institution but was found online it may be due to a problematic dataset. 

Future Scope
Try using a different dataset with more rows or change the algorithms being used and try finding the importance and odds ratio manually instead. 
