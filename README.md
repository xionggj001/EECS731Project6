# EECS731Project6
Anomaly Detection

The data from real world contains lots of outliers (bad data). Anomaly detection is the task that detects the outliers and clean the data for further usage. In this project, we apply the anomaly detection techniques to the data set from NAB. 

The dataset we use is the tweets volumn for UPS, which can be found in this link: https://github.com/numenta/NAB/tree/master/data/realTweets

# Part 1: Data Exploration

In this part, we analyze the data, visualize the distribution of tweet volumn, convert it into time series dataframe, and show the tweet volumn accross time.

# Part 2: Anomaly Detection

In this part, we adopt two different models to do this task.

Model 1: Isolation Forest

The IsolationForest ‘isolates’ observations by randomly selecting a feature and then randomly selecting a split value between the maximum and minimum values of the selected feature.

It can be represented by a tree structure, and the number of splittings required to isolate a sample is equivalent to the path length from the root node to the terminating node.

When a forest of random trees collectively produce shorter path lengths for particular samples, they are highly likely to be anomalies.

Model 2: One-class SVM

A One-Class Support Vector Machine is an unsupervised learning algorithm that is trained only on the 'normal' data. It learns the boundaries of these points and is therefore able to classify any points that lie outside the boundary as, you guessed it, outliers.

According to our experiment, one-class SVM detects more outliers than Isolation Forrest.
