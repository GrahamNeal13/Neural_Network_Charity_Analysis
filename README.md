# Neural_Network_Charity_Analysis
Module 19

## Overview of analysis:

### Background:
"Beks has come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

    - EIN and NAME—Identification columns
    - APPLICATION_TYPE—Alphabet Soup application type
    - AFFILIATION—Affiliated sector of industry
    - CLASSIFICATION—Government organization classification
    - USE_CASE—Use case for funding
    - ORGANIZATION—Organization type
    - STATUS—Active status
    - INCOME_AMT—Income classification
    - SPECIAL_CONSIDERATIONS—Special consideration for application
    - ASK_AMT—Funding amount requested
    - IS_SUCCESSFUL—Was the money used effectively"

## Results:

  + Data Preprocessing -
    - What variable(s) are considered the target(s) for your model?
        The target for the model is the "IS_Successful" column.
    - What variable(s) are considered to be the features for your model?
        The features of the model are 
    - What variable(s) are neither targets nor features, and should be removed from the input data?
        The 'EIN' and 'NAME' are both non-beneficial columns and are dropped from the dataframe.  

