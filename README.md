# Kings County Housing Bake-off

<image>

## Overview

This project utilizes linear regression analysis to predict housing prices in Kings County, Seattle, WA. The training data for this will be cleaned and then explored for feature engineering. The packages used in this project are from the Scikit python library.

## Business Problem

A Seattle real estate company is trying to accurately predict housing prices in Kings County. Being able to accurately predict prices of homes based on their relative features will aide in maximizing profits. Our job is to use our Python and more specifically linear regression knowledge, to help them in becoming a more sophisticated business.

## Approach

    1. Check and clean the data for impurities
    2. Perform EDA and statistical analysis to grasp a better undertanding of the data
    3. Get a baseline model with few changes to the dataset
    4. Engineer new features based on findings
    5. Model several linear regression models and choose the one with the lowest RMSE
    6. Apply the model to the holdout dataset
    
## Methods

No data cleaning was used apart from the few observations that had been determined to have false records when they were cross referenced with Zillow.

The data was standardized using sklearn's standard scalar. 

I used independent T tests to decide which features were key in determining price. Then I created interaction columns and polynomial columns for all of my features. In addition, I used geospatial data for Pikes Place, a market in the center of city to determine roughly how far each home was from the heart of Seattle. The zipcodes were also dummied and added to the data set.

When creating my model I used a train test split on the data trying to get the lowest possible RMSE. My second model used my zipcode dummies along with my new features that I created to get me an RMSE of 125K. I only used my top 54 features in the model.

## Results

### Does a house on the waterfront impact its price?

(IMAGE)

From our analysis we got a p-value of 3.47e-23 which is lower than our alpha of 0.05. With this we can conclude that a house on the waterfront does impact its average price

### Is the number of bedrooms directly correlated with price?

(IMAGE) 

As we see homes that have more than 2 bedrooms we can see the price of the home drastically increase.

### Does location (based on zipcode) impact price?

(IMAGE)

We got very low p-values for all the zipcodes that we dummied. Meaning taht we can reject the null hypothesis and conclude that zipcode does have an effect on the price of the home.


## Modelling

Using the Scikit-learn package I developed 4 models.
  
  1. Linear Regression
  2. Linear Regression Using Recursive Feature Elimination
  3. Linear Regression Using K-best
  
## Summary

I was able to reduce my RMSE by almost 70k since my first model. Creating new features for basement and renovation, as well as coding the zipcode into dummy varaibles turned out to be extremely helpful. Hopefully the firm can use my findings to help them better predict housing prices. 

## Future Work

Future work involved create additional features, as getting houses within the distinct top 5 neighborhoods and figuring out just how big of an impact those homes are making. As well as, maybe trying to see the month in which sales are the highest. Overall, there is a lot to be done, but this is a step into the right direction.

