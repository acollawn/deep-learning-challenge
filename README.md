# deep-learning-challenge
Module 21 Challenge - Deep Learning

## Report

### Overview of the analysis: 
Alphabet Soup is a nonprofit foundation that provides funding to a wide range of organizations. Using features in the dataset provided by Alphabet Soup, we created a binary classifier that predicts the success of applicants. The purpose of this model is to help Alphabet Soup predict whether or not applicants will be successful.


### Results:

Data Preprocessing

1. What variable(s) are the target(s) for your model?
    * the target for our model is 'IS_SUCCESSFUL'
2. What variable(s) are the features for your model?
    * the features of our model are:
        * APPLICATION_TYPE
        * AFFILIATION
        * CLASSIFICATION
        * USE_CASE
        * ORGANIZATION
        * STATUS
        * INCOME_AMT
        * SPECIAL_CONSIDERATIONS
        * ASK_AMT
   
3. What variable(s) should be removed from the input data because they are neither targets nor features?
    * 'EIN' and 'NAME' are  the identification columns that we remove because they are neither targets nor features

Compiling, Training, and Evaluating the Model

4. How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * I chose to add a third hidden layer with a different activation function in my model, in an attempt to increase the accuracy. The layer included 15 as the unit value and tanh as the activation function. Tanh functions are primarily used for classifying data into 1 of 2 classes, and the goal is for this funtion to help classify data points into the 'successful' or 'not successful' classes. 
5. Were you able to achieve the target model performance?
    * I was not anel to achieve the target model performance. 
6. What steps did you take in your attempts to increase model performance?
    * In an attempt to increase the model performance I...
        * dropped an additional column (3 total) - I attempted to add columns back initially, but when I would run the model, it would crash and would not finish, so I was forced to drop the colums we initially dropped and then more
        * added a bin for ASK_AMT due to the large number of unique values equalling 1.
        * added a third hidden layer that included the tanh activation function with units equal to 15
        * increased the number of epochs to 200, which did seemingly help each epochs accuracy

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

This deep learning model was made to predict if organizations that apply for funding from Alphabet Soup will be successful or unsuccessful. The model I created achieved an accuracy score of 73% (.7314). Despite my best efforts, I was unable to reach a score of 75%. When thinking about other models to use for an improved model, I think using a random forest model could potentially improve the accuracy. Using a model with branches as the way of organized learning, has a chance to learn the trends in this data at a high level. By making sure the n_estimators value is set to a large number, we ensure there are enough trees to properly train our model, with the goal of increasing the accuracy.

