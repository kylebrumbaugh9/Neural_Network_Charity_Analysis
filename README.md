# Neural_Network_Charity_Analysis

## Overview

### Purpsose
The purpose of this analysis was to apply machine learning to determine whether applicants will be successful if they are funded by Alphabet Soup. I took a .csv file holding 34000+ organizations that received funding and I applied machine learning to determine if I could find which factors pointed to success

## Results

### Data Preprocessings
- The target variable for the model was the IS_SUCCESSFUL field in the .csv/dataframe
- The features for the model were every other field, initially. APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT
- I also removed a few variables from the dataset as well because they were neither targets, nor features: EIN, NAME, and eventually STATUS and SPECIAL_CONSIDERATIONS

### Compiling, Training, and Evaluating the Model

First go around, I selected 110 total neurons, 2 hidden layers, and relu activation functions within those layers to match the suggestions laid out in the starter code. Later, to attempt to hit 75% accuracy, I added an additional hidden layer and increased the number of neurons to 150. 

I was not able to achieve 75% accuracy, but I tried numerous updates to get there.

- I removed more columns that I deemed "excessive": STATUS and SPECIAL_CONSIDERATIONS because I reviewed the .csv and saw how few loans there were with a STATUS of 0 and how few SPECIAL_CONSIDERATIONS were Y (see image below). In this step, I also increased the number of neurons from 80 -> 100 and 30 -> 50 
 
![image](https://user-images.githubusercontent.com/114685724/225485556-4e203c9c-a530-4ac4-8f71-84e18783e584.png)

![image](https://user-images.githubusercontent.com/114685724/225485869-e1b7ffe6-dccb-4ec3-a595-8c1169095565.png)


- I also added an additional hidden layer with 25 neurons to see if that would increase the accuracy

![image](https://user-images.githubusercontent.com/114685724/225485900-69680ca9-0d51-4a28-b95e-938877466b9b.png)


- Finally, I added updated the activation function from relu to tanh to see if that increased the accuracy

![image](https://user-images.githubusercontent.com/114685724/225485929-4470146b-409b-4449-9f2e-a62ea204e89a.png)


## Summary

Overall, I wsa able to increase accuracy slightly with each change. On the 4 attempts I made, accuracy went from 0.7255 to 0.7256 to 0.7263 to 0.7254. 

The Tanh activation function appears to have actually hurt the accuracy, but overall the model was getting sligthly better each time. I would recommend trying the other activation functions and increasing the hidden layers and neurons even further to see what we can do to optimize the model and predict at an accuracy greater than 75%. 
