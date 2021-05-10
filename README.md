# Risky Business

### Background
In order to mitigate risk, I used machine learning techniques to predict credit risk.
I built and evaluated several machine-learning models to predict credit risk using free data from LendingClub. I employed different techniques for training and evaluating models with imbalanced classes and used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

- Resampling
- Ensemble Learning


### Resampling
I used the imbalanced learn library to resample the LendingClub data and built and evaluated logistic regression classifiers using the resampled data. I loaded the Lending Club data, split the data into training and testing sets, and scaled the features data. In order to oversample the data, I used the Naive Random Oversampler and SMOTE algorithms. I undersampled the data using the Cluster Centroids algorithm and Over- and under-sample using a combination SMOTEENN algorithm.

I needed to:

- Train a logistic regression classifier from sklearn.linear_model using the resampled data.
- Calculate the balanced accuracy score from sklearn.metrics.
- Calculate the confusion matrix from sklearn.metrics.
- Print the imbalanced classification report from imblearn.metrics.

#### Results 
SMOTE Oversampling had the best balanced accuracy score with a score of 64.48%.

Naive Random Oversampling had the best recall score with 67% average.

SMOTE Oversampling had the best geometric mean score with 65%.


### Ensemble Learning
In this section, I trained and compared two different ensemble classifiers to predict loan risk and evaluated each model. I used the Balanced Random Forest Classifier and the Easy Ensemble Classifier. I completed the following steps for each model:

- Load the Lending Club data, split the data into training and testing sets, and scale the features data.
- Train the model using the quarterly data from LendingClub provided in the Resource folder.
- Calculate the balanced accuracy score from sklearn.metrics.
- Print the confusion matrix from sklearn.metrics.
- Generate a classification report using the imbalanced_classification_report from imbalanced learn.
- For the balanced random forest classifier only, print the feature importance sorted in descending order (most important feature to least important) along with the feature score.

#### Results

Easy Ensemble Classifier had the best balanced accuracy score with 92.6%

Easy Ensemble Classifier had the best recall score with 94%

Easy Ensemble Classifier had the best geometric mean score with 93%

The top three features are:
(0.06502785730329358, total_rec_prncp'),
(0.06480222129516051, 'total_rec_int'),
(0.06256804840515041, 'total_pymnt_inv')