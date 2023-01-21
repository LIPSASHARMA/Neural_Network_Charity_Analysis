# Neural_Network_Charity_Analysis
UoT module on Neural Networks

## Overview of the analysis: Explain the purpose of this analysis

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

## Results: 

### Data Preprocessing
What variable(s) are considered the target(s) for your model?
Checking to see if the target is marked as successful in the DataFrame, indicating that it has been successfully funded by AlphabetSoup.

What variable(s) are considered to be the features for your model?
The IS_SUCCESSFUL column is the feature chosen for this dataset.

What variable(s) are neither targets nor features, and should be removed from the input data?
The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency.

### Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the optimized model, layer 1 started with 120 neurons with a relu activation. For layer 2, it dropped to 80 neurons and continued with the relu activation. From there, the sigmoid activation seemed to be the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).

Were you able to achieve the target model performance?
The target for the model was 75%, but the best the model could produce was 72.7%.

What steps did you take to try and increase model performance?
Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy. The linear activation produced the worst accuracy, around 28%. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.



## Summary: 
The model ended up with the accuracy score of 72% after optimization. Furthermore, we could further also optimize our neural network by removing more features or simply adding more data to the dataset to increase accuracy. We could have used the Random Forest because it will provide more accuracy, performs faster and avoids overfitting. 
