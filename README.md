# housing-data-london
# Introduction
The objective of this project was to analyze the price of a house across the Boroughs of London. The analysis
involves using visualization to understand the effect of different features on the price of a house and creating
an optimal model to predict the price of a house. As per the data, houses can be as old as 106+ years (preworld
war 1) and ranging from price as low as 8500 to as high as 850000 pounds. The houses are categorized
as leased or freehold. It can have two to five bedrooms with one or more bathroom. Further, there are houses
with or without a central heating system and different types of garage space. All these feature can have impact
on the pricing of a house along with its location or which borough it is in. 

# EDA
![](https://github.com/rchadha96/housing-data-london/blob/master/images/EDA%20(1).png  | width=100)
![](https://github.com/rchadha96/housing-data-london/blob/master/images/EDA%20(2).png)

# Data Modeling
After analyzing the data through visualization, few of the features like floor area, number of bedrooms, age of a
house, type of house, a house with a central system, garage space showed some impact on the price of the
house while others didn’t. Some models was created using these features. But before creating the model, the
dataset was split into a training set and test set to test the performance of the model on test data. The split
ratio was 70-30, i.e using 70% of the data for training the model and 30% of the data for testing.

## Random Forest
Random forest is an ensemble learning model, one of the most used models for these kinds of predictions.
The default value for the number of trees in the random forest is 500 and the node size is 1. Location-based
details are removed from the dataset before creating a random forest model as it has no major effect on the
price of houses. The five most significant features as per this model are floor area,houses with central heating, number of bedrooms, age & type of house.
![](https://github.com/rchadha96/housing-data-london/blob/master/images/EDA%20(4).png)

## Parameter tuning
The random forest model can be further tunned to produce an optimal model. After comparing different models
with different combination of number of trees and node size, number of tree equals to 1000 and node size
equals to 20 gives the best RMSE of 25942.
![](https://github.com/rchadha96/housing-data-london/blob/master/images/EDA%20(5).png)



