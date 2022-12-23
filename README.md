# IMDB_Movie_Review_Classification
Tags: NLP, Sentiment Analysis, Supervised Machine Learning, Neural Network

### Overview:
In this project, I constructed 3 different models for IMDB movie review classification using **SVM**, **XG-Boost** and **BERT**. Details about model parameters can be found in the "Parameters.txt" file. Some metrics, including accuracy, precision, recall and f1-score, were used to evaluate the reliability of our models when making prediction based on testing data. In addition to modeling, some simple visualizations were also done to investigate the pattern of word usages in positive and negative reviews. In this README.txt, I will mainly focus on the models I built and their results. More plots can be found in "text_classification.ipynb".

### Terminology:

**TP, FP, TN, FN**: True Positive (TP) is defined as the number of positive predictions made by the model that are correct; False Positive (FP) is defined as the number of positive predictions made by the model that are incorrect (i.e. the true labels are negative). True Negative (TN) and False Negative (FN) are defined in a similar way.

**Accuracy**: It gives the overall reliability of the model in classifying for both positive and negative cases. It is calculated using the formula (TP+TN)/N, where N is the total predictions made.

**Precision**: It reflects the model's success probability in making positive predictions. It is calculated using the formua TP/(TP+FP).

**Recall**: It tells us how goot the model is at identifying the true positive cases. It is calculated using the formula TP/(TP+FN).

### Results:

<div align="center">
<img src="https://user-images.githubusercontent.com/59629686/209265761-49d890e4-8757-41af-a8b9-fb80f6bb0aee.png" width=300 height=200>
</div>
                         


**SVM**
                                                                                                     
Support Vector Machine is a commonly used supervised learning technique in classification problems. It classifies data into different clusters by finding a hyperplane that best divides the points that belong to different classes (i.e. maximizes the total distance between two classes).

Using SVM, the model achieved an accuracy of 0.89. The precision and recall for positive reviews are 0.88 and 0.90, respectively. For negative reviews, precision and recall are 0.9 and 0.88. The f1-scores for both classes are 0.89.
```
              precision    recall  f1-score   support

    negative       0.90      0.88      0.89      2495
    positive       0.88      0.90      0.89      2505

    accuracy                           0.89      5000
```


<div align="center">
<img src="https://user-images.githubusercontent.com/59629686/209266265-f8680243-2ebc-4944-8141-cfa29400fc1f.png" width=400>
</div>


**XG-Boost**

XG-Boost is a popular ensembling method, which combines a series of gradient-boosted decision trees and apply majority voting principle to find the most likely label for the input data. It has been a very popular algorithm in solving regression and classification problems in the real world.

After adjusting for the parameters using grid search, the 'best' XG-Boost model is able to achieve an accuracy of 0.87. For positive reviews, it yields a precision of 0.86 and recall of 0.88. For negative reviews, it yields a precision of 0.88 and 0.86. The f1-score is 0.87.

```
              precision    recall  f1-score   support

    negative       0.88      0.86      0.87      2495
    positive       0.86      0.88      0.87      2505

    accuracy                           0.87      5000
```





<div align="center">
<img src="https://user-images.githubusercontent.com/59629686/209266433-c8fb9302-76c9-468f-8863-15b57fbbb232.png" width=400>
</div>

**BERT**

BERT, or Bidirectional Encoder Representations from Transformers, is a transformer-based 

