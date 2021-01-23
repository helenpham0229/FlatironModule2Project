## Introduction
This project involes an iterative approach to building a multiple linear regression model to predict sale prices for houses in King County, WA by utilizing data of houses sold in 2014 and 2015. The dataset also includes several variables such as number of bedrooms, number of times the house was viewed before being bought, square footage of the home, the zipcode that the house is located in, and many more.

In this project, I followed the OSEMN (Obtain, Scrub, Explore, Model, and Interpret) framework to find out which independent variables have the most influence in determining the sale price of a house.

## Obtain
King County House Prices dataset is provided in a CSV file ("kc_house_data.csv"). The dataset contains over 21000 entries with 21 columns which include information about properties within King County, Washington.

## Scrub & Explore
The main portion of this project is to clean the dataset and explore the relationships between each independent variable to the dependent variable. We will find missing/null values, change data types, eliminate outliers, use heatmap to find multicollinearity.

## Model
After comparing and testing different regression with different features, the final model has
* R-squared:  0.580
* Training Score:  0.580
* Test Score: 0.573
* P-values: all are less than 0.05

We also want to make sure that our model met all 4 of linear regression assumptions
* Linear relationship: We check this assumption by exploring the regression plots between each independent variable vs. dependent variable (price)
* Independence: This is satisfied when we check the heatmap
* Homoscedasticity: This is checked by the residuals vs. fitted values plot. We can also use significance test like Goldfeld-Quandt to detect homoscedasticity. Since this test gives us a p-value > 0.05, the null hypothesis cannot be rejected, and we can assume the data is homoscedastic.
* Normality: We use a Normal Q-Q plot and check to see the overall shape of our data against the required distribution to test the normality assumption. Our distribution is fairly normal and we can see how the quantiles of normal data appear as a straight line along the diagonal when plotted against a standard normal distribution's quantiles.

## Interpret

* Multiple regression analysis was used to test if certain variables significantly predicted the sale price of homes in King County, Washington. 
* The results of the regression indicated that 12 predictors can be explained 58% of the variance. 
* All of the independent variables used in the model were significant predictors of sale price with p-values less than 0.05. 
* All 4 assumptions of linear regression are met
* Looking at coefficients and predictors, we can conclude from our model that:

>Houses that are renovated or built in the last 10 years increase the sale price of a home by 4833.19 dollars

>One unit increase in square footage of internal living space increases the sale price by 147.61 dollars

>One additional bathroom increases the sale price by 9172.90 dollars

## Future Work
* Instead of using longitude and latitude as location indicator, we can use zipcode or cities as location point of interest based on population
* Do more research on school district as it could be an important variable in choosing a house
* Build a regression model to predict prices of homes over 1 million for high income families
