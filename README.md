# active-learnig-ML
in this project, we will make a comparison between 3 active learning strategies and a random strategy using two datasets iris and digits from sklearn balance data
and unbalanced dataset  churn dataset 
Introduction
i worked on there datasets :
(1)   Load digits :
This classification contains data points, where each data point is an 8X8 image of a single digit.
(2) iris dataset :
The Iris Dataset contains four features (length and width of sepals and petals) of 50 samples of three species of Iris (Iris setosa, Iris virginica, and Iris varicolored). These measures were used to create a linear discriminant model to classify the species.
i worked on a churn dataset 
(3)Churn: is a data set of information about a customer that we feed the machine so it can tell us if he/she is going to leave or stay
the Data set consists of 14 columns with 10 features and one target, in the following we will demo each feature
1 - Credit Score: it represents the creditworthiness of the customer
2 - Geography : is the country where the customer is currently living
3 - Gender : this is obviously the customer’s gender (female or male) 
4 - Age : the customer’s age
5 - tenure: period or duration for which the loan amount is sanctioned
6 - Balance: how much money the customer has
7 - NumOfProducts : is the number of bank retail products the customer uses
8 - HasCrCard: tells whether the customer has a credit card or no
9 - IsActiveMember: the state of activation of the customer
10	- EstimatedSalary: the annual salary of the customer

We applied three strategies of active learning on the two datasets from ModAi Library and compared the results between the three strategies
Active Learning Strategies 
(1) Uncertainty sampling strategy
It is a strategy used in machine learning for selecting the most informative data points to be labeled by an expert or a human annotator.The uncertainty sampling strategy works by first training a model on a subset of labeled data, then using the model to predict the labels of the remaining unlabeled data.The samples with the highest uncertainty score are then selected for labeling
(2) Margin sampling strategy
The margin sampling strategy works by first training a model on a subset of labeled data, then using the model to predict the labels of the remaining unlabeled data. For each example, the difference between the two highest predicted probabilities is calculated, and the examples with the smallest margin are selected for labeling.
(3) Entropy  sampling strategy
The entropy sampling strategy works by first training a model on a subset of labeled data, then using the model to predict the labels of the remaining unlabeled data. For each example, the entropy of the predicted probabilities is calculated, and the examples with the highest entropy are selected for labeling.








Experiments 
Results on   load_digit dataset 
Uncertainty sample
Testing accuracy   : 96.89695550351288 %
MSE [TEST]          : 0.6381733021077284
Training accuracy  : 100.0 %
MSE [TRAIN]         : 0.0
precision :  0.9689695550351288
recall    :  0.9689695550351288
f1_score  :  0.9689695550351288
 
 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        18
           1       1.00      1.00      1.00         8
           2       1.00      1.00      1.00        10
           3       1.00      1.00      1.00         9
           4       1.00      1.00      1.00        13
           5       1.00      1.00      1.00         6
           6       1.00      1.00      1.00         7
           7       1.00      1.00      1.00         4
           8       1.00      1.00      1.00        11
           9       1.00      1.00      1.00         3

    accuracy                           1.00        89
   macro avg       1.00      1.00      1.00        89
weighted avg       1.00      1.00      1.00        89

              precision    recall  f1-score   support

           0       0.99      0.99      0.99       160
           1       0.95      0.95      0.95       174
           2       1.00      0.98      0.99       167
           3       0.97      0.98      0.97       174
           4       0.99      0.98      0.99       168
           5       0.98      0.94      0.96       176
         6       1.00      0.99      0.99       174
           7       0.99      0.99      0.99       175
         8       0.91      0.95      0.93       163
           9       0.92      0.93      0.92       177

    accuracy                           0.97      1708
   macro avg       0.97      0.97      0.97      1708
weighted avg       0.97      0.97      0.97      1708

 Margin sampling 
Testing accuracy   : 96.13583138173301 %
MSE [TEST]          : 0.7540983606557377
Training accuracy  : 100.0 %
MSE [TRAIN]         : 0.0
precision :  0.9613583138173302
recall    :  0.9613583138173302
f1_score  :  0.9613583138173302
 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        18
           1       1.00      1.00      1.00         8
           2       1.00      1.00      1.00        10
           3       1.00      1.00      1.00         9
           4       1.00      1.00      1.00        13
           5       1.00      1.00      1.00         6
           6       1.00      1.00      1.00         7
           7       1.00      1.00      1.00         4
           8       1.00      1.00      1.00        11
           9       1.00      1.00      1.00         3

    accuracy                           1.00        89
   macro avg       1.00      1.00      1.00        89
weighted avg       1.00      1.00      1.00        89

              precision    recall  f1-score   support

           0       0.99      0.99      0.99       160
           1       0.91      0.98      0.94       174
           2       0.98      0.99      0.98       167
           3       0.98      0.93      0.96       174
           4       0.98      0.98      0.98       168
           5       0.93      0.96      0.95       176
           6       1.00      0.95      0.98       174
           7       0.97      0.97      0.97       175
           8       0.90      0.90      0.90       163
           9       0.97      0.95      0.96       177

    accuracy                           0.96      1708
   macro avg       0.96      0.96      0.96      1708
weighted avg       0.96      0.96      0.96      1708

 Entropy sampling 
Testing accuracy   : 96.25292740046838 %
MSE [TEST]          : 0.7107728337236534
Training accuracy  : 100.0 %
MSE [TRAIN]         : 0.0
precision :  0.9625292740046838
recall    :  0.9625292740046838
f1_score  :  0.9625292740046838
 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        18
           1       1.00      1.00      1.00         8
           2       1.00      1.00      1.00        10
           3       1.00      1.00      1.00         9
           4       1.00      1.00      1.00        13
           5       1.00      1.00      1.00         6
           6       1.00      1.00      1.00         7
           7       1.00      1.00      1.00         4
           8       1.00      1.00      1.00        11
           9       1.00      1.00      1.00         3

    accuracy                           1.00        89
   macro avg       1.00      1.00      1.00        89
weighted avg       1.00      1.00      1.00        89

              precision    recall  f1-score   support

         0       1.00      0.97      0.99       160
           1       0.95      0.94      0.95       174
           2       0.99      0.96      0.97       167
           3       0.98      0.97      0.98       174
           4       0.99      0.95      0.97       168
           5       0.98      0.97      0.98       176
           6       0.99      0.99      0.99       174
           7       0.98      0.98      0.98       175
           8       0.85      0.98      0.91       163
           9       0.93      0.91      0.92       177

    accuracy                           0.96      1708
   macro avg       0.96      0.96      0.96      1708
weighted avg       0.96      0.96      0.96      1708
Random Sampling    
Testing accuracy   : 91.72885572139303 %
MSE [TEST]          : 1.5199004975124377
Training accuracy  : 100.0 %
MSE [TRAIN]         : 0.0
precision :  0.9172885572139303
recall    :  0.9172885572139303
f1_score  :  0.9172885572139303
 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        26
           1       1.00      1.00      1.00        21
           2       1.00      1.00      1.00        18
           3       1.00      1.00      1.00        17
           4       1.00      1.00      1.00        20
           5       1.00      1.00      1.00        22
           6       1.00      1.00      1.00        14
           7       1.00      1.00      1.00        13
           8       1.00      1.00      1.00        24
           9       1.00      1.00      1.00        14

    accuracy                           1.00       189
   macro avg       1.00      1.00      1.00       189
weighted avg       1.00      1.00      1.00       189

              precision    recall  f1-score   support

           0       0.96      0.98      0.97       152
           1       0.85      0.88      0.86       161
           2       0.88      0.99      0.93       159
           3       0.99      0.83      0.90       166
           4       0.96      0.94      0.95       161
           5       0.89      0.94      0.92       160
           6       0.98      0.98      0.98       167
           7       0.89      0.95      0.92       166
           8       0.90      0.79      0.84       150
           9       0.90      0.89      0.89       166

    accuracy                           0.92      1608
   macro avg       0.92      0.92     0.92      1608
weighted avg       0.92      0.92      0.92      1608


The best result we got it using Uncertainty Sampling 
Results on   iris dataset  
Entropy  sampling
Testing accuracy   : 97.5 %
MSE [TEST]          : 0.025
Training accuracy  : 96.66666666666667 %
MSE [TRAIN]         : 0.03333333333333333
precision :  0.975
recall    :  0.975
f1_score  :  0.975
 
        precision    recall   f1-score    support

           0       1.00      1.00      1.00                7
           1       0.92      1.00      0.96              11
           2       1.00      0.92      0.96             12

    accuracy                                        0.97     30
   macro avg          0.97      0.97      0.97      30
weighted avg       0.97      0.97      0.97      30

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        43
           1       1.00      0.92      0.96        39
           2       0.93      1.00      0.96        38

    accuracy                           0.97         120


Margin sampling
Testing accuracy   : 98.33333333333333 %
MSE [TEST]          : 0.016666666666666666
Training accuracy  : 100.0 %
MSE [TRAIN]         : 0.0
precision :  0.9833333333333333
recall    :  0.9833333333333333
f1_score  :  0.9833333333333333
 
        precision    recall  f1-score   support

           0       1.00      1.00      1.00         7
           1       1.00      1.00      1.00        11
           2       1.00      1.00      1.00        12

 accuracy                           1.00        30
 macro avg           1.00      1.00      1.00        30
weighted avg       1.00      1.00      1.00        30

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        43
           1       1.00      0.95      0.97        39
           2       0.95      1.00      0.97        38

    accuracy                           0.98       120
   macro avg       0.98      0.98      0.98       120
weighted avg       0.98      0.98      0.98       120


Uncertainty sampling 
Testing accuracy   : 98.33333333333333 %
MSE [TEST]          : 0.016666666666666666
Training accuracy  : 100.0 %
MSE [TRAIN]         : 0.0
precision :  0.9833333333333333
recall    :  0.9833333333333333
f1_score  :  0.9833333333333333
 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00         7
           1       1.00      1.00      1.00        11
           2       1.00      1.00      1.00        12

    accuracy                                1.00        30
   macro avg       1.00      1.00      1.00        30
weighted avg       1.00      1.00      1.00        30

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        43
           1       1.00      0.95      0.97        39
           2       0.95      1.00      0.97        38

    accuracy                               0.98       120
   macro avg       0.98      0.98      0.98       120
weighted avg       0.98      0.98      0.98       120
Random Sampling 
Testing accuracy   : 93.33333333333333 %
MSE [TEST]          : 0.06666666666666667
Training accuracy  : 98.33333333333333 %
MSE [TRAIN]         : 0.016666666666666666
precision :  0.9333333333333333
recall    :  0.9333333333333333
f1_score  :  0.9333333333333333
 
              precision    recall  f1-score   support

           0       1.00      1.00      1.00        43
           1       1.00      0.95      0.97        39
           2       0.95      1.00      0.97        38

    accuracy                               0.98       120
   macro avg       0.98      0.98      0.98       120
weighted avg       0.98      0.98      0.98       120

              precision    recall  f1-score   support

           0       1.00      1.00      1.00         7
           1       0.91      0.91      0.91        11
           2       0.92      0.92      0.92        12

    accuracy                            0.93        30
   macro avg       0.94      0.94      0.94        30
weighted avg       0.93      0.93      0.93        30

The best results we got it using Uncertainty Sampling and Margin Sampling 

Bonus
We have 2 classes 
Class number 1 count 2037
Class number 2 count 7963
 
Results 










Uncertainty Sampling
Testing accuracy   : 78.96875 %
MSE [TEST]          : 0.2103125
Training accuracy  : 79.75 %
MSE [TRAIN]         : 0.2025
precision :  0.7896875
recall    :  0.7896875
f1_score  :  0.7896875
 
              precision    recall  f1-score   support

           0       0.81      0.98      0.88       316
           1       0.60      0.11      0.18        84

    accuracy                           0.80       400
   macro avg       0.70      0.54      0.53       400
weighted avg       0.76      0.80      0.74       400

              precision    recall  f1-score   support

           0       0.80      0.97      0.88      7647
           1       0.41      0.08      0.13      1953

    accuracy                           0.79      9600
   macro avg       0.61      0.52      0.51      9600
weighted avg       0.72      0.79      0.73      9600



margin sampling
Testing accuracy   : 78.96875 %
MSE [TEST]          : 0.2103125
Training accuracy  : 79.75 %
MSE [TRAIN]         : 0.2025
precision :  0.7896875
recall    :  0.7896875
f1_score  :  0.7896875
 
              precision    recall  f1-score   support

           0       0.81      0.98      0.88       316
           1       0.60      0.11      0.18        84

    accuracy                           0.80       400
   macro avg       0.70      0.54      0.53       400
weighted avg       0.76      0.80      0.74       400

              precision    recall  f1-score   support

           0       0.80      0.97      0.88      7647
           1       0.41      0.08      0.13      1953

    accuracy                           0.79      9600
   macro avg       0.61      0.52      0.51      9600
weighted avg       0.72      0.79      0.73      9600




entropy sampling
Testing accuracy   : 78.96875 %
MSE [TEST]          : 0.2103125
Training accuracy  : 79.75 %
MSE [TRAIN]         : 0.2025
precision :  0.7896875
recall    :  0.7896875
f1_score  :  0.7896875
 
              precision    recall  f1-score   support

           0       0.81      0.98      0.88       316
           1       0.60      0.11      0.18        84

    accuracy                           0.80       400
   macro avg       0.70      0.54      0.53       400
weighted avg       0.76      0.80      0.74       400

              precision    recall  f1-score   support

           0       0.80      0.97      0.88      7647
           1       0.41      0.08      0.13      1953

    accuracy                           0.79      9600
   macro avg       0.61      0.52      0.51      9600
weighted avg       0.72      0.79      0.73      9600


random sampling 
Testing accuracy   : 78.84210526315789 %
MSE [TEST]          : 0.21157894736842106
Training accuracy  : 79.80000000000001 %
MSE [TRAIN]         : 0.202
precision :  0.7884210526315789
recall    :  0.7884210526315789
f1_score  :  0.7884210526315789
 
              precision    recall  f1-score   support

           0       0.81      0.97      0.88       396
           1       0.56      0.14      0.23       104

    accuracy                           0.80       500
   macro avg       0.68      0.56      0.56       500
weighted avg       0.76      0.80      0.75       500

              precision    recall  f1-score   support

           0       0.81      0.96      0.88      7567
           1       0.43      0.13      0.20      1933

    accuracy                           0.79      9500
   macro avg       0.62      0.54      0.54      9500
weighted avg       0.73      0.79      0.74      9500



