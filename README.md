# Neural_Network_Charity_Analysis

## Overview of the analysis:

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

Dataset includes investments in more than 34,000 organizations, including a binary column stating whether or not the money was used effectively. After cleaning the dataset and using sklearn's OneHotEncoder() to standardize the dataset, we're setting the outcome column as the target, with the remaining columns set as features to split the data into train and testing data. We then use sklearn's StandardScaler() and TensorFlow to determine accuracy using different nodes and activation functions.



## Data Preprocessing

**Variables considered for our target model**
- IS_SUCCESFUL


**Variable(s) considered to be the features model**

- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE

**Removed:**

- EIN
- NAME

## Compiling, Training, and Evaluating the Model:

**Main:**

- number_input_features = 37
- hidden_nodes-layer1 = 80
- hidden_nodes_layer2 = 30

![base](https://user-images.githubusercontent.com/49954261/157192277-8c9f6435-9b09-4748-9c4d-443cf6f4b262.png)

![base_acc](https://user-images.githubusercontent.com/49954261/157192178-0e55bd76-6f3c-45cb-8fe3-ccd9e0fd0799.png)


**1st attempt**

![Atempt1](https://user-images.githubusercontent.com/49954261/157184330-cae0e118-c35a-49f7-beff-5807fc0ba4b3.png)

**Also tried dropping the AFFILIATION column:**

![dropxcol](https://user-images.githubusercontent.com/49954261/157184464-26b6b6b0-e862-4183-865d-c71d848d3180.png)

**Another attempt - Adding a third layer w different activations "softmax"** 

![3rd_layer](https://user-images.githubusercontent.com/49954261/157186115-69fe0e63-dcd9-49cf-9e9e-ec5b44712304.png)



## Summary: 

![68%](https://user-images.githubusercontent.com/49954261/157193081-a7ed66cb-2108-4272-a9fe-fe63fab6ff30.png)

**Our main model performed at almost 70%. After multiple attempts- using different cut off points- ex: <200 or <580, various random states, removing an extra column, experimenting with 2 layers or 3 layers(neither improved but decreased the score)- various activations; relu, sigmoid, softmax, random-states=1-42- we were unable to make any significant improvements!**
