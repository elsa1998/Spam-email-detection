# Spam-email-detection
Build deep learning model to determine whether an email is spam or not. Within different methods (Decision tree, Logistic Regression, KNN, SVM, LightGBM, and Neutral Network), LightGBM has the best performance in cost-sensitivie and accurate model.

## Goal
Determine whether a given email is spam or not

## Data Exploration
- Correlation
- Normalization

## Modeling(i): best accuracy
- Cross validation for inner and outer loops
- Tuning hyper parameters
- GridSearchCV based on accuracy
- Compare accuarcy between 6 models (best model accuracy = 95.2%)

## Modeling(ii) : best cost-sensitive
Use 10:1 cost ratio for different misclassification errors. FPR (classify non-spam as spam):10, FNR(classify spam as non-spam):1
- Cross validation for inner and outer loops
- Tuning Hyperparameter
- GridSearchCV based on cost-sensitive score
- Compare cost between 6 models (the lowest cost = 296.25)

## Best model: LightGBM
- Train-Test Split
- Normalization
- Fitting model
- Evaluation: classification_report, ROC, lift curve

## Result
- Accuracy: {'Decision Tree': 0.922, 'Logistic Regression': 0.926, 'KNN': 0.895, 'SVM': 0.936, 'LightGBM': 0.952, 'Neural Network': 0.936}
- Cost: {'Decision Tree': 377.25, 'Logistic Regression': 391.75, 'KNN': 415.0, 'SVM': 345.5, 'LightGBM': 296.25, 'Neural Network': 409.25}
