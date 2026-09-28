# MSCS 634 Lab 2: Classification Using KNN and RNN Algorithms

## Purpose
The purpose of this lab is to compare the performance of K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classifiers using the Wine dataset from the sklearn library.

The dataset contains 178 samples, 13 features, and 3 wine classes. The data was divided into 80% training data and 20% testing data.

## KNN Results
The KNN classifier was tested using k values of 1, 5, 11, 15, and 21.

- k = 1: Accuracy = 77.78%
- k = 5: Accuracy = 80.56%
- k = 11: Accuracy = 80.56%
- k = 15: Accuracy = 80.56%
- k = 21: Accuracy = 80.56%

The highest KNN accuracy was approximately 80.56%.

## RNN Results
The Radius Neighbors classifier was tested using radius values of 350, 400, 450, 500, 550, and 600.

- Radius = 350: Accuracy = 72.22%
- Radius = 400: Accuracy = 69.44%
- Radius = 450: Accuracy = 69.44%
- Radius = 500: Accuracy = 69.44%
- Radius = 550: Accuracy = 66.67%
- Radius = 600: Accuracy = 66.67%

The highest RNN accuracy was approximately 72.22% with a radius of 350.

## Key Insights
KNN performed better than RNN for the tested parameter values. KNN achieved its highest accuracy with k values of 5, 11, 15, and 21.

For RNN, accuracy generally decreased as the radius increased. This suggests that a larger radius included more observations from different wine classes, which reduced classification performance.

## Challenges and Decisions
One important decision was selecting an appropriate method for handling observations that did not have neighbors within the specified radius. The `outlier_label='most_frequent'` option was used in the Radius Neighbors classifier to prevent prediction errors.

A random state of 42 was used for reproducibility, and stratification was used during the train-test split to maintain the class distribution.

## Conclusion
Based on the results, KNN performed better than RNN for this Wine dataset and the tested parameter values.
