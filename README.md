# Neural Network Model Report

## Overview

This model was designed to help the nonprofit foundation Alphabet Soup select applications for funding that have the best chance of success. The model was fit and tested using historical data of over 34,000 organizations that have recived funding along with their success outcomes. This is a binary model designed to classify organizations as successful or not successful.

## Results

* Data Preprocessing: 
    * The model used the following feature set to classify success: 
        * APPLICATION_TYPE
        * AFFILIATION
        * CLASSIFICATION
        * USE_CASE
        * ORGANIZATION
        * STATUS
        * INCOME_AMT
        * SPECIAL_CONSIDERATIONS
        * ASK_AMT
    * The target variable of the model is : IS_SUCCESSFUL
    * Removed from the data set prior to training and testing were the NAME and EIN identification columns

* Compiling, training, and evaluating the model
    * This sequential model is comprised of:
        * Input layer with 44 neurons - selected based on number of feature items (after dummie separation)
        * Hidden layer 1 has 12 neurons and rectified linear unit (relu) activation function 
        * Hidden layer 2 has 6 neurons and a relu activation function
        * Output layer has 1 neuron and a sigmoid activation function - sigmoid function selected for classification use (same function as is used for logistic regression classification)
        * This model has a total of 625 parameters
    * With some luck, the model was able to achieve target performance on the first try. 
        * Model accuracy: 1.000
        * Model loss: 1.363x10^-08
        * An alternate model can be seen with the jupyter notebook file under "Optimize the Model"
            * This model includes less neurons, more layers, and was trained with 150 epochs as opposed to the previous 100. 
            * Results for this model:
                * Accuracy: .9998
                * Loss: .0020

## Summary

This model was able to achieve target performance with the aformentioned structure. The model showed 100% accuracy with loss less than .000001. While this model can accurately classify applicants, there is potential for further optimization testing. It is possbile that the same or similar result can be found using less neurons and trained with varying epochs. By decreasing the number of overall neuron in the neural network it can help to reduce the reliance on specific neurons or features. By reducing the network's relicance on specific neurons, the model is able to become more robust and will be less susceptible to overfitting. One method for implementing this would be through dropout regularization. 


## Resources

Data for this project was provided by Edx. 

This project was completed individually with code guided by class examples and aided in debugging by the Xpert Learning Assistant. 

More information on the types of activation functions and use cases see https://machinelearningmastery.com/choose-an-activation-function-for-deep-learning/ 

More information on dropout regularization can be found at https://medium.com/@abhishekjainindore24/all-about-anns-and-dropout-39099dbc9f7e#:~:text=Dropout%20regularization%20is%20a%20technique,and%20less%20susceptible%20to%20overfitting. 