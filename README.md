# deep-learning-challenge
## Background
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

## Report

### Overview
The purpose of this analysis is to create a model that can predict wether an applicant will be successful or not after recieving a funding from Alphabet Soup based on data from the 34,000 organizations Alphabet has previouslt funded. 
### Results
* **Target Variable**:
  * IS_SUCCESSFUL
* **Features**:
  * AFFILIATION
  * CLASSIFICATION
  * USE_CASE
  * ORGANIZATION
  * STATUS
  * INCOME_AMT
  * ASK_AMT
* **Removed Features**:
  * EIN & NAME - Both of these columns are ID columns that are unique to each organization

#### Model
* Input Layer:
  * 128 neurons
  * Activation function: ReLU
* Hidden Layer 1:
  * 64 neurons
  * Activation function: ReLU
* Hidden Layer 2:
  * 32 neurons
  * Activation function: ReLU
* Hidden Layer 3:
  * 16 neurons
  * Activation function: ReLU
* Output Layer:
  * 1 neurons
  * Activation function: Sigmoid

#### Optimization
Several changes were made in attempt to increase the accuracy of the model.
1. Number of epochs was increase from 50 to 100
2. Train test split was altered decreasing the test size from 25% to 20%
3. Two hidden layers were added 
4. Increase number of neurons in each layer form 16,8,1 to 128,64,32,16,1
The accuracy reached 72.46%
### Summary

#### Suggestion
A different model that could be used to solve this problem would be random forest. I believe a random forest model can provide a deeper insight into the relative influence of each feature on the success of an organization. 
