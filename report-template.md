# Alphabet Soup Charity Report

## Overview of the Analysis

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special considerations for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively


The following steps were performed in order to build our neural network model:

1. Import our main 3 dependencies: sklearn, Pandas, and tensorflow.
2. Import our dataset 'charity_data.csv' and store it into a dataframe.
3. From our complete dataframe, we drop two columns we don't need: 'EIN' and 'NAME'.
4. Created cutoff point to bin "rare" categorical variables together in a new value, Other for both CLASSIFICATION and APPLICATION_TYPE
5. Converted categorical data to numeric with pd.get_dummies.
6. split the preprocessed data into features and target arrays.
7. Lastly split into training and tesing datasets.
8. Compile, train, and evaluate the model.
9. Optimize the model using the keras-tuner library.

Our target variable:

* IS_SUCCESSFUL

Our feature variables:

* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS—Active
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT
* IS_SUCCESSFUL


## Results

### Neural network attempt 1:

activation: "relu", "relu", "relu"

hidden_nodes_layer1 = 9
hidden_nodes_layer2 = 18

accuracy = 0.73
loss = 0.55


### Neural network attempt 2:

activation: "relu", "relu", "relu"

hidden_nodes_layer1 = 9
hidden_nodes_layer2 = 18
hidden_nodes_layer3 = 27

accuracy = 0.73
loss = 0.56


### Neural network attempt 3:

activation: "relu", "tanh", "tanh"

hidden_nodes_layer1 = 9
hidden_nodes_layer2 = 18
hidden_nodes_layer3 = 27

accuracy = 0.73
loss = 0.55


## Summary

even though different layers were used with different activation functions, we weren't able to reach 75% accuracy on our model.


