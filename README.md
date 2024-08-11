# Hyperparameter Tuning with DecisionTreeClassifier

This repository contains code for performing hyperparameter tuning on a `DecisionTreeClassifier` using different search strategies available in scikit-learn, including `GridSearchCV`, `RandomizedSearchCV`, `HalvingGridSearchCV`, and `HalvingRandomSearchCV`. The goal is to compare these methods in terms of time taken and the accuracy of the resulting models.

## Overview
This project demonstrates how to use different hyperparameter search strategies to tune a `DecisionTreeClassifier`. The methods are compared based on the time they take to run and the accuracy (best score) they achieve. The code also visualizes the results to highlight the trade-offs between these methods.

## Dependencies
- Python 3.x
- pandas
- scikit-learn
- matplotlib

## Methods

The code compares the following hyperparameter tuning methods:

- **GridSearchCV**: An exhaustive search over the parameter grid, testing every possible combination.
- **RandomizedSearchCV**: A random search over a subset of the parameter grid, trading thoroughness for speed.
- **HalvingGridSearchCV**: An iterative version of GridSearchCV that progressively reduces the number of candidates, focusing resources on the most promising options.
- **HalvingRandomSearchCV**: Similar to HalvingGridSearchCV, but with random sampling of the parameter space, further improving speed.

## Results
After running the script, you will see two visualizations:

-  Time Taken by Each Search Method: A bar chart showing the time each method took to complete the search.
-  Best Scores Achieved by Each Search Method: A bar chart comparing the best accuracy scores found by each method.

These results help you understand the trade-offs between exhaustive searches and faster, less thorough methods.

## Conclusion

The results demonstrate that while GridSearchCV generally finds the most accurate model, it is the most time-consuming. On the other hand, HalvingRandomSearchCV is the fastest but may not always achieve the best score. The choice of method should depend on the available computational resources and the need for accuracy versus speed.
