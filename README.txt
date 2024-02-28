
Using different learning algorithms to test if a players success in the NBA Draft Combine can give us a hint on his future playing
performance using NBA draft combine data from 2012-2020




--==--==-- Contains :

Main.ipynb   //// All algorithms inside this code\\\
PER-MergeScript.ipynb  //// Excel refurbishment / PER calculator

--==--==--











--==--==--
1. Result using StandartScaler()
2. Result using MinMaxScaler()
3. Resutlt SVR using RBF , Linear , Sigmoid
4. Result changing MLP parameters
5. Result RandomForest different number of estimators
--==--==--






1


/////Using Standart Scaler instead of MinMaxScaler\\\\\\\\\\


Classification Report for SVR:
              precision    recall  f1-score   support

        High       1.00      0.00      0.00        28
         Low       0.39      0.90      0.55        92
    Moderate       0.50      0.23      0.31        61
    Very Low       1.00      0.00      0.00        58

    accuracy                           0.41       239
   macro avg       0.72      0.28      0.22       239
weighted avg       0.64      0.41      0.29       239

Classification Report for Random Forest:
              precision    recall  f1-score   support

        High       1.00      0.07      0.13        28
         Low       0.44      0.87      0.59        92
    Moderate       0.49      0.31      0.38        61
    Very Low       0.76      0.22      0.35        58

    accuracy                           0.48       239
   macro avg       0.67      0.37      0.36       239
weighted avg       0.60      0.48      0.42       239

Classification Report for Linear Regression:
              precision    recall  f1-score   support

        High       0.41      0.32      0.36        28
         Low       0.52      0.65      0.58        92
    Moderate       0.69      0.33      0.44        61
    Very Low       0.52      0.66      0.58        58

    accuracy                           0.53       239
   macro avg       0.54      0.49      0.49       239
weighted avg       0.55      0.53      0.52       239

Classification Report for MLP:
              precision    recall  f1-score   support

        High       0.19      0.18      0.18        28
         Low       0.36      0.34      0.35        92
    Moderate       0.26      0.18      0.21        61
    Very Low       0.25      0.36      0.30        58

    accuracy                           0.28       239
   macro avg       0.26      0.26      0.26       239
weighted avg       0.29      0.28      0.28       239


/////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\





2





/////////// Using MinMaxScaler \\\\\\\\\\

Classification Report for SVR:
              precision    recall  f1-score   support

        High       1.00      0.00      0.00        28
         Low       0.39      1.00      0.56        92
    Moderate       1.00      0.03      0.06        61
    Very Low       1.00      0.00      0.00        58

    accuracy                           0.39       239
   macro avg       0.85      0.26      0.16       239
weighted avg       0.76      0.39      0.23       239

Classification Report for Random Forest:
              precision    recall  f1-score   support

        High       1.00      0.07      0.13        28
         Low       0.45      0.87      0.59        92
    Moderate       0.50      0.33      0.40        61
    Very Low       0.78      0.24      0.37        58

    accuracy                           0.49       239
   macro avg       0.68      0.38      0.37       239
weighted avg       0.61      0.49      0.43       239

Classification Report for Linear Regression:
              precision    recall  f1-score   support

        High       0.41      0.32      0.36        28
         Low       0.52      0.65      0.58        92
    Moderate       0.69      0.33      0.44        61
    Very Low       0.52      0.66      0.58        58

    accuracy                           0.53       239
   macro avg       0.54      0.49      0.49       239
weighted avg       0.55      0.53      0.52       239

Classification Report for MLP:
              precision    recall  f1-score   support

        High       1.00      0.00      0.00        28
         Low       1.00      0.00      0.00        92
    Moderate       1.00      0.00      0.00        61
    Very Low       0.24      1.00      0.39        58

    accuracy                           0.24       239
   macro avg       0.81      0.25      0.10       239
weighted avg       0.82      0.24      0.09       239

///////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\




3


//////////// SVR: Sigmoid\\\\\\\\\\\\\\\\
Classification Report for SVR:
              precision    recall  f1-score   support

        High       1.00      0.00      0.00        28
         Low       0.39      0.90      0.55        92
    Moderate       0.50      0.23      0.31        61
    Very Low       1.00      0.00      0.00        58

    accuracy                           0.41       239
   macro avg       0.72      0.28      0.22       239
weighted avg       0.64      0.41      0.29       239
///////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\



//////////// SVR: rbf\\\\\\\\\\\\
Classification Report for SVR:
              precision    recall  f1-score   support

        High       1.00      0.00      0.00        28
         Low       0.39      0.97      0.55        92
    Moderate       0.50      0.07      0.12        61
    Very Low       1.00      0.00      0.00        58

    accuracy                           0.39       239
   macro avg       0.72      0.26      0.17       239
weighted avg       0.64      0.39      0.24       239
///////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\


//////////// SVR: Linear\\\\\\\\\\\\\\\\\\

Classification Report for SVR:
              precision    recall  f1-score   support

        High       0.83      0.18      0.29        28
         Low       0.46      0.98      0.63        92
    Moderate       0.78      0.41      0.54        61
    Very Low       1.00      0.10      0.19        58

    accuracy                           0.53       239
   macro avg       0.77      0.42      0.41       239
weighted avg       0.72      0.53      0.46       239



================= Heighest: Linear ====================




4



/////////////// MLP: activation='logistic',hidden_layer_sizes=(16, 17, 1), max_iter=100  \\\\\\\\\\\\\\\\\\\\\\\\\

Classification Report for MLP:
              precision    recall  f1-score   support

        High       1.00      0.00      0.00        28
         Low       1.00      0.00      0.00        92
    Moderate       1.00      0.00      0.00        61
    Very Low       0.24      1.00      0.39        58

    accuracy                           0.24       239
   macro avg       0.81      0.25      0.10       239
weighted avg       0.82      0.24      0.09       239

=== Perfect number of iteration among hyperparameter tuning found to be 250 ===

//////////// MLP: mlp_regressor = MLPRegressor(activation='Logistic',hidden_layer_sizes=(16, 17, 1), max_iter=250, random_state=42) \\\\\\\\\\\\


Classification Report for MLP:
              precision    recall  f1-score   support

        High       0.23      0.25      0.24        28
         Low       0.31      0.25      0.28        92
    Moderate       0.22      0.16      0.19        61
    Very Low       0.18      0.28      0.22        58

    accuracy                           0.23       239
   macro avg       0.23      0.23      0.23       239
weighted avg       0.25      0.23      0.24       239


=== Highest performing activation function was Sigmoid ('Logistic') , among  Rectified Linear Unit (ReLU) , Hyperbolic tangent ('teuh') ===




5


/////////////// RandomForest: NumberOfEstimators= 100 \\\\\\\\\\\\\\\\\\

Classification Report for Random Forest:
              precision    recall  f1-score   support

        High       1.00      0.07      0.13        28
         Low       0.44      0.87      0.59        92
    Moderate       0.49      0.31      0.38        61
    Very Low       0.76      0.22      0.35        58

    accuracy                           0.48       239
   macro avg       0.67      0.37      0.36       239
weighted avg       0.60      0.48      0.42       239

=== Number of Estimators does not change the accuracy among 100,200,300,500,1000===



Conclusion:
Highest accuracy recorded was svr and Linear Regression providing max parameter tuning












