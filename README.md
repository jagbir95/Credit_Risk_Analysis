# Credit_Risk_Analysis
# Overview of the Analysis
The main purpose of this analysis is to apply machine learning algorithms to determine weather a loan application is a high risk or a low risk based on different factors. In this challenge we will be using six different machine learning models to resample the data and predict risky loans. Also we will be comparing each model's accuracy score to evaluate the performance.
# Results
### Oversampling
- [RandomOverSampler Model](https://drive.google.com/file/d/1CgEwsATfCtBvjlsLkORu1lvUm8pS2dIz/view?usp=sharing): randomly selects the minority class data and makes it equal to the majority class data to predict the results.
The accuracy score of this model is 59% and High Risk precision rate is 1% with recall at 62% and f1 score of 2%. The Low Risk precision rate is 100% with recall at 56%.
- [SMOTE Model](https://drive.google.com/file/d/1qt8z30dp_3LpgrjTXp_Na34tlrMl7g2n/view?usp=sharing): also known as Synthetic Minority Oversampling Technique increases the size of  minority class data based on closest neighbor values instead of random selection.
The accuracy score of this model is 62% and High Risk precision rate is 1% with recall at 64% and f1 score of 2%. The Low Risk precision rate is 100% with recall at 60%.
### Undersampling
- [ClusterCentroids Model](https://drive.google.com/file/d/1LKGF6XCQmj6dmqFwd8pHOqZoLQlEazft/view?usp=sharing): under samples the majority class by replacing a cluster of majority samples by the cluster centroid of a KMeans algorithm.
The accuracy score of this model is 55% and High Risk precision rate is 1% with recall at 68% and f1 score of 1%. The Low Risk precision rate is 100% with recall at 42%.
### Combination Sampling
- [SMOTEENN Model](https://drive.google.com/file/d/1Kis_2PxJUYpCNQ20iS40qXYvG-jlaLib/view?usp=sharing): combine over- and under-sampling using SMOTE and edited nearest neighbors.
The accuracy score of this model is 68% and High Risk precision rate is 1% with recall at 77% and f1 score of 2%. The Low Risk precision rate is 100% with recall at 59%.
### Ensemble Classifiers
- [BalancedRandomForestClassifier Model](https://drive.google.com/file/d/1bxWoyIdxCtHTco7lV6ePWnKBrg1WeIv5/view?usp=sharing): randomly under-samples each bootstrap sample to balance it.
The accuracy score of this model is 78% and High Risk precision rate is 4% with recall at 67% and f1 score of 7%. The Low Risk precision rate is 100% with recall at 90%.
- [EasyEnsembleClassifier Model](https://drive.google.com/file/d/1SZXASGiFDKDzIb6mFUnt4Td95XvdLoZI/view?usp=sharing): is an ensemble of AdaBoost learners trained on different balanced bootstrap samples. The balancing is achieved by random under-sampling.
The accuracy score of this model is 93% and High Risk precision rate is 9% with recall at 92% and f1 score of 16%. The Low Risk precision rate is 100% with recall at 94%.

# Summary
- According to the results, out of six models the EasyEnsembleClassifier model has the highest accuracy score of 93%. However, all the models are weak in predicting the precision of high-risk credit. Therefore, I do not recommend using any of the above models. 