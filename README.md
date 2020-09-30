# London Housing Price Analysis 
Project Goal: To find the best group to predictors of housing prices of Greater London using R 

# Introduction
The objective of this project was to analyze the price of a house across the Boroughs of London. The analysis involves using visualization to understand the effect of different features on the price of a house and creating an optimal model to predict the price of a house. 

As per the data, houses can be as old as 106+ years (preworld war 1) and ranging from price as low as 8500 to as high as 850000 pounds. The houses are categorized as leased or freehold. It can have two to five bedrooms with one or more bathroom. Further, there are houses with or without a central heating system and different types of garage space. All these feature can have impact on the pricing of a house along with its location or which borough it is in. 

# EDA

![](/images/eda_1.png)

![](/images/EDA2.png)

# Data Modeling
After analyzing the data through visualization, few of the features like floor area, number of bedrooms, age of a house, type of house, a house with a central system, garage space showed some impact on the price of the house while others didn’t. Some models was created using these features.

But before creating the model, the dataset was split into a training set and test set to test the performance of the model on test data. The split ratio was 70-30, i.e using 70% of the data for training the model and 30% of the data for testing.

## Random Forest
Random forest is an ensemble learning model, one of the most used models for these kinds of predictions.
The default value for the number of trees in the random forest is 500 and the node size is 1. Location-based details are removed from the dataset before creating a random forest model as it has no major effect on the price of houses. The five most significant features as per this model are floor area,houses with central heating, number of bedrooms, age & type of house.

![image4](/images/EDA4.png)

## Parameter tuning
The random forest model can be further tunned to produce an optimal model. After comparing different models with different combination of number of trees and node size, number of tree equals to 1000 and node size equals to 20 gives the best RMSE of 25942.

![image5](/images/EDA5.png)

# Conclusion
Floor Area certainly is a major feature to impact the price. More the floor area higher the price. The number of bedrooms, when it is 4 or 5 have a higher impact on price. New houses have higher prices except for some historical buildings like houses from before world war 1. Location wise, house with all price range is spread across the borough of London, also the median price for all the boroughs is almost the same. 

The detached house is more expensive as compared to other types and Bangalow is least expensive irrespective of age except for house before the world was 1. Having central heating and garage space does add on the price of the house but garage space doesn’t have any major impact. Freehold houses especially old property have higher prices as compare to leased ones. The proportion of skill type or employment status in a house doesn’t affect the price of the house much.

