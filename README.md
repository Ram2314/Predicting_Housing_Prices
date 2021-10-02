 ## **Problem Statment**: 

With many new home buyers, many times it can be very confusing experience. Especially if they do not know what kind of house their budget could potentially buy. For many, certain feature of home are more important than others. As a example, someone may want a pool in the house more than they want a 3 car garage. Adding and eliminating features changes the price of housing and therefore will determine if a buyer could potentially buy the home.Therefore will look at Ames Housing Data and select features & model regressions to produce the most accurate model to predict the ‘Sale Price’ of a house based on different features of the house. In this way we can help a new home buyer select features by priority to find them a house that they can afford while still letting them have the house they always wanted. 

We will be looking about 81 features:
1. Qualitative: Stuff like Garage Area, 2 or 3 car Garages, Pool Quality ect.
2. Quantitative:  Garage Area, Total Basement surface area ect.. 

These features will let us know 
1. Given some list of features a client is looking for in a house, what kind of housing price could they expect?
2. What model would be best to use?

## **Data Cleaning and EDA**
We first do a corrolation heatmap to idenity the most correlated numaric variables in the data set.
![](images/Screen%20Shot%202021-07-24%20at%201.42.07%20AM.png)
From here we pick the top 6 variables to use in our model. Future work will include more variables without sacrificing to many features. 
![](images/Screen%20Shot%202021-07-24%20at%201.42.13%20AM.png)
Next we normalize our target variable (Sale Price) using a log transform.
![](images/Screen%20Shot%202021-07-24%20at%201.56.24%20AM.png)
And get rid of outliers and wierd 0's showing up in our data.
![](images/Screen%20Shot%202021-07-24%20at%201.56.54%20AM.png)
## **Modeling**
We look at the peroformace of 3 regression models (Linear, L.A.S.S.O and Rigid). We used a 20/80 train_test_split. All three models performed very well, but the once with the most accuracy was the Rigid model. 
![](images/Screen%20Shot%202021-07-24%20at%202.05.10%20AM.png)
## **Recomendation/Future Work**
Given the metrics, the Rigid Model would be the most accurate. However, we had to sacrifice some features from the model and therefore clients cannot use some features to predict a housing price. Improvements in feature engineering and better dummifying features will lead to a accurate model without having to sacrifice to many features.
