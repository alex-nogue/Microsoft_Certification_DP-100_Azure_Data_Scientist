
## Modules and methods used in Azure Machine Learning Studio

This notebook contains some modules from Azure Machine Learning Studio that might possibly be asked in the DP-100 exam.

### Clean and Preprocessing Data

#### MICE 
For each missing value, this option assigns a new value, which is calculated by using a method described in the statistical literature as "Multivariate Imputation using Chained Equations. With a multiple imputation method, each variable with missing data is modeled conditionally using the other variables in the data before filling in the missing values. In contrast, in a single imputation method (such as replacing a missing value with a column mean) a single pass is made over the data to determine the fill value. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/clean-missing-data


#### Edit Metadata
Edits metadata associated with columns in a dataset. The values and the data types in the dataset are not actually altered; what changes is the metadata inside Azure Machine Learning that tells downstream components how to use the column. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/edit-metadata


#### Split Data
Partitions the rows of a dataset into two distinct sets. This module is particularly useful when you need to separate data into training and testing sets. You can customize the way that data is divided as well. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/split-data

#### Partition and Sample
Creates multiple partitions of a dataset based on sampling. This module supports several related tasks that are important in machine learning:

- Dividing your data into multiple subsections of the same size. You might use the partitions for cross-validation for instance.
- Separating data into groups and then working with data from a specific group.
- Sampling. Sampling is an important tool in machine learning because it lets you reduce the size of a dataset while maintaining the same ratio of values.
- Creating a smaller dataset for testing.

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/partition-and-sample


### Modelling and feature engineering
#### Evaluate Model
Evaluates the results of a classification or regression model with standard metrics. The metrics returned by Evaluate Model depend on the type of model that you are evaluating: Classification, Regression or Clustering Models. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/evaluate-model

#### Score Model
Scores predictions for a trained classification or regression model. <br>
Score Model comes after training and takes as inputs the trained model and the test data. It then generates predictions for every data point. Then, one could use Evaluate Model module to produce evaluation metrics on that predictions. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/score-model

#### Score Matchbox recommender
Predictions based on a trained recommendation model, based on the Matchbox algorithm from Microsoft Research. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/score-matchbox-recommender

#### SMOTE
Stands for Synthetic Minority Oversampling Technique and aims at increasing the number of low incidence examples in a dataset using synthetic minority oversampling. Used when we have an unbalanced feature we want to predict. SMOTE is a better way of increasing the number of rare cases than simply duplicating existing cases. However, SMOTE does not change the number of majority cases. <br>
The algorithm takes samples of the feature space for each target class and its nearest neighbors, and generates new examples that combine features of the target case with features of its neighbors. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/smote

#### Sweep Clustering
Performs a parameter sweep to determine the optimum settings for a clustering model. A parameter sweep is a way of finding the best hyperparameters for a model, given a set of data. The Sweep Clustering module is designed specifically for clustering models. You provide a clustering model as input, together with a dataset. The module iterates over a set of parameters you specify, building and testing models with different parameters, until it finds the model with the best set of clusters. It automatically computes the best configuration, and then trains a model using that configuration. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/sweep-clustering

#### Cross-Validate Model
Cross-validates parameter estimates for classification or regression models by partitioning the data. <br>
Cross-validation is an important technique often used in machine learning to assess both the variability of a dataset and the reliability of any model trained using that data. <br>
The Cross-Validate Model module takes as input a labeled dataset, together with an untrained classification or regression model. It divides the dataset into some number of subsets (folds), builds a model on each fold, and then returns a set of accuracy statistics for each fold. By comparing the accuracy statistics for all the folds, you can interpret the quality of the data set and understand whether the model is susceptible to variations in the data. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/cross-validate-model

#### Normalize Data
Rescales numeric data to constrain dataset values to a standard range. Normalization is a technique often applied as part of data preparation for machine learning. The goal of normalization is to change the values of numeric columns in the dataset to use a common scale, without distorting differences in the ranges of values or losing information. <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/normalize-data

#### Principal Component Analysis
Computes a set of features with reduced dimensionality for more efficient learning. The module analyzes your data and creates a reduced feature set that captures _all_ the information contained in the dataset, but in a smaller number of features. (Alex's note: disagree with the term "all" as you capture only a fraction of the information - we select the number of components such that this fraction is kept high - close to 1). <br>

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/principal-component-analysis

#### Group data into bins
Puts numerical data into bins to group numbers or change the distribution of continuous data. <br>
The Group Data into Bins module supports multiple options for binning data. You can customize how the bin edges are set and how values are apportioned into the bins. For example, you can:

- Manually type a series of values to serve as the bin boundaries.
- Calculate entropy scores to determine an information values for each range, to optimize the bins in the predictive model. + Assign values to bins by using quantiles, or percentile ranks.
- Control the number of values in each bin can also be controlled.
- Force an even distribution of values into the bins.

There are different binning modes:

- __Entropy MDL__: It then makes a pass over the data and attempts to determine the number of bins that minimizes the entropy. In other words, it chooses a number of bins that allows the data column to best predict the target column.
- __Quantiles__: The quantile method assigns values to bins based on percentile ranks. 
- __Equal Width__: With this option, you must specify the total number of bins. The values from the data column are placed in the bins such that each bin has the same interval between starting and end values. As a result, some bins might have more values if data is clumped around a certain point.
- __Custom Edges__: You can specify the values that begin each bin.
- __Equal Width with Custom Start and Stop__: This method is like the Equal Width option, but you can specify both lower and upper bin boundaries.

More here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/group-data-into-bins

### Feature Selection Modules
There are three modules on Machine Learning Studio for feature selection: Filter Based Feature Selection, Fisher Linear Discriminant Analysis and Permutation Feature Importance. <br>

You can find them here: https://docs.microsoft.com/en-us/azure/machine-learning/studio-module-reference/feature-selection-modules
####  Filter Based Feature Selection
Identifies the features in a dataset with the greatest predictive power. <br>
When you use the Filter Based Feature Selection module, you can choose from among well-known feature selection methods. The module outputs both the feature selection statistics and the filtered dataset. <br>
In general, feature selection refers to the process of applying statistical tests to inputs, given a specified output, to determine which columns are more predictive of the output. <br>
This module for feature selection is called "filter-based" because you use the selected metric to identify irrelevant attributes, and filter out redundant columns from your model. You choose a single statistical measure that suits your data, and the module calculates a score for each feature column. The columns are returned ranked by their feature scores.<br>
These are the feature selection metrics included in the module:

- __Pearson Correlation__:<br>
For any two variables, it returns a value that indicates the strength of the correlation. Pearson's correlation coefficient is computed by taking the covariance of two variables and dividing by the product of their standard deviations. The coefficient is not affected by changes of scale in the two variables.
- __Mutual information__: <br>
The mutual information score measures the contribution of a variable towards reducing uncertainty about the value of another variable: namely, the label. The mutual information score is particularly useful in feature selection because it maximizes the mutual information between the joint distribution and target variables in datasets with many dimensions.
- __Kendall Correlation__: <br>
Kendall's rank correlation is one of several statistics that measure the relationship between rankings of different ordinal variables or different rankings of the same variable. In other words, it measures the similarity of orderings when ranked by the quantities. Both this coefficient and Spearman’s correlation coefficient are designed for use with non-parametric and non-normally distributed data.
- __Spearman Correlation__: <br>
Spearman's coefficient is a nonparametric measure of statistical dependence between two variables.

####  Fisher Linear Discriminant Analysis
Identifies the linear combination of feature variables that can best group data into separate classes. This method is often used for dimensionality reduction, because it projects a set of features onto a smaller feature space while preserving the information that discriminates between classes. <br>
Linear discriminant analysis is similar to analysis of variance (ANOVA) in that it works by comparing the means of the variables.

####  Permutation Feature Importance
Computes the permutation feature importance scores of feature variables given a trained model and a test dataset. Computes a set of feature importance scores for your dataset. You use these scores to help you determine the best features to use in a model.

### Microsoft Cognitive Toolkit
https://docs.microsoft.com/en-us/cognitive-toolkit/<br>

The Microsoft Cognitive Toolkit (CNTK) is an open-source toolkit for commercial-grade distributed deep learning. It describes neural networks as a series of computational steps via a directed graph. CNTK allows the user to easily realize and combine popular model types such as feed-forward DNNs, convolutional neural networks (CNNs) and recurrent neural networks (RNNs/LSTMs). CNTK implements stochastic gradient descent (SGD, error backpropagation) learning with automatic differentiation and parallelization across multiple GPUs and servers. <br>

#### Post Batch Normalization Statistics
Post batch normalization statistics (PBN) is the CNTK version of how to evaluate the population mean and variance of Batch Normalization. <br>
Since the parameters keep updating while training, the accuracy of mean and variance, using running statistics, will be impacted as well. PBN keeps updating the evaluation as the data updates. <br>

More here: https://docs.microsoft.com/en-us/cognitive-toolkit/post-batch-normalization-statistics

### Other
Python melt() <br>
https://www.geeksforgeeks.org/python-pandas-melt/
