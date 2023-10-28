# ML2_Final_Project
This project can be viewed as a continued project of the DTSA 5509 final project "Predicting Sleep Quality with Supervised Machine Learning Methods: A Case Study." It predicted whether the subject slept well or not, i.e., simplified the multi-level sleep quality level prediction problem to a binary class classification problem, using purely supervised machine learning approaches - logistic regression (LR), decision tree (DT), adaboost (AdaB), random forest (RF), and support vector machine (SVM) models. It was concluded that the SVM model performed the best, with an AUC of 0.72, an accuracy of 0.62, and an F1-score of 0.62. In this project, I want to cope with the multi-level sleep quality level prediction problem as a multi-class classification problem, as well as compare the purely supervised SVM model with hybrids of unsupervised clustering approaches and a supervised SVM classifier. In addition, I want to improve the data cleaning process by doing feature scaling and categorical variable encoding if applicable. I will also look into the possibility of overfitting in more detail.

Here are the models I will build in this project:
1. the SVM model: a purely supervised model
2. the KMeans_SVM model: a hybrid model of an unsupervised k-means clustering and a supervised SVM classifier, with hyperparameters to be tuned together
3. the Agg_SVM model: a hybrid model of an unsupervised agglomerative hierarchical clustering and a supervised SVM classifier, with hyperparameters to be tuned together

Unfortunately, since the dataset is small and imbalanced (when treated as a multi-class classification problem), all the models overfit. I tried to fix this issue by applying feature scaling to X_train and X_test to tackle the models' sensitivity on distance metrics, and running 5-fold cross validations to find the best suited hyperparameters. In addition, I  manually set the hyperparameter 'class_weight' in SVM as'balanced' to balance the classes. However, the models still overfit. I also tried but failed to split the data using stratificated sampling, because y_test does not contain all the class labels. More advanced resampling technique like SMOTE also turned out to be not applicable here, since a few minority classes has only 1 instance each. Random oversampling and other resampling techniques will introduce higher risk of overfitting. Thus, gathering more real-world samples is likely the only solution to this issue. <br>

If I were to conduct this multi-class classification project again, I will ask the subject to record at least 3 months of his sleep instances in order to get a larger, more balanced dataset. I believe this will fix the issue of model overfitting, and will result in models with good performances. 

Nevertheless, your suggestions for techniques to mitigate the impact of such an imbalanced, small dataset are very welcomed!

Please do not use my code or text without proper citation, thank you!
