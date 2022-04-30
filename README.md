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
    
        The features of the model are listed in the cell block for the "Generate our categorical variable lists," which are the following: "Application_Type", "Affiliation", "Use_Case", "Oranization", "Income_Amt", "Special_Considerations"
        
    - What variable(s) are neither targets nor features, and should be removed from the input data?
    
        The 'EIN' and 'NAME' are both non-beneficial columns and are dropped from the dataframe.  
        
    + Compiling, Training, and Evaluating the Model - 
    
    - Using the provide code sample I was able to set a base of two hidden layers with 80 neurons in the first layer and 30 in the second layer.  However I chose to increase the second layer by 10 to improve the model accuracy for the first attempt in the "AlphabetSoupCharity.IPYNB" file.  Then I used the "ReLU" activation funcition in the two hidden layers and "Sigmoid" for the output activation function.  This gave me the following Loss/Accuracy return:
        
        Loss: 0.5574895739555359, Accuracy: 0.7240816354751587
 
 ## Summary: 
 
   ### Optimizing the model
 
   Now this is a good start to begin experimenting with activation functions and hidden layers.  In the first attempt I used the frame work of the previous trial model.  Instead of using 80/40 I increase the second layer yet again to 50, but still used the ReLU/Sigmoid combination to see if this would increase performance.  
    
![attempt_opt1.png](https://github.com/GrahamNeal13/Neural_Network_Charity_Analysis/blob/main/Images/attempt_opt1.png)

   But we can see from the image above that the accuracy and loss do not really improve.  This enboldened me to really change the activation functions but still use the 80/40 neuron count in the hidden layers.  So I changed the activation funcitions to "Tanh" for both hidden layers and the output layer.  Thinking this would help to find the clusters if the data may be spiraled.  
   
![attempt_opt2.png](https://github.com/GrahamNeal13/Neural_Network_Charity_Analysis/blob/main/Images/attempt_opt2.png)

   Yet again this did not show any real improvement which lead me to remember that ReLU had a similiar activation function "Leaky ReLU" whereby negative input values will return very small negative values.  I came to the conclusion that combining the two of these functions might result in a higher performing model.  So my third attempt was to use the neuron count 80/40 on the hidden layers with Leaky ReLU activation functions applied.  In the output layer I used the ReLU activation function and got these results:
   
![attempt_opt3.png](https://github.com/GrahamNeal13/Neural_Network_Charity_Analysis/blob/main/Images/attempt_opt3.png)

   Unfortunately, I was not able to increase accuracy beyond 72-73% and loss below 0.55.  Now some improvements that I would recommend for future models would be to increase the number of hidden layers using the activation function "ReLU" as this performed in categoriig the data better than the "Tanh" attempt.  I would also suggest the neuron count be 80 in the first layer, 40 neurons in the second layer, and 10 to 20 neurons in the third layer.  This should result in a accuracy score that achieve the target model performance of 75%.  This will filter and categorize the data quickly and should result in a more accurate overall model without overfitting.  
   I would also recommend using a Random Forest model as an alternative.  Random forest classifiers are a type of ensemble learning model that combines multiple smaller models into a more robust and accurate model. Random forest models use a number of weak learner algorithms (decision trees) and combine their output to make a final classification (or regression) decision. Structurally speaking, random forest models are very similar to their neural network counterparts.  Since both output and feature selection of random forest models are easy to interpret, and they can easily handle outliers and nonlinear data.  Which would be a better fit for the dataset.
   

        







