# Linear Regression Model - Bike Sharing Assignment
## Problem Statement
* A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.
_______________________________________________________________________________________________________________________________
* A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 
* In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits


* They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:-

    * Which variables are significant in predicting the demand for shared bikes.
    * How well those variables describe the bike demands
    
    
* Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors. 

## Business Goal:
* We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market. 

### Steps for Model Building
1.Reading and Understanding Data  
2.Visualising the Data  
3.Data Preparation  
4.Splitting the Data into Training and Testing Sets  
5.Feature Scaling  
6.Building the Model  
7.Residual Analysis of the train data  
8.Making predictions using final model  
9.Model Evaluation


#### The equation of our best fitted line is:

𝑐𝑜𝑢𝑛𝑡=0.0901+0.4918×𝑡𝑒𝑚𝑝+0.0915×𝑆𝑒𝑝𝑡𝑒𝑚𝑏𝑒𝑟+0.0647×𝑆𝑎𝑡𝑢𝑟𝑑𝑎𝑦+0.0516×𝑠𝑢𝑚𝑚𝑒𝑟+0.0984×𝑤𝑖𝑛𝑡𝑒𝑟+0.2333×𝑌𝑒𝑎𝑟+0.0568×𝑤𝑜𝑟𝑘𝑖𝑛𝑔𝑑𝑎𝑦−0.03051×𝑙𝑖𝑔ℎ𝑡𝑠𝑛𝑜𝑤−0.0800×𝑚𝑖𝑠𝑡𝑐𝑙𝑜𝑢𝑑𝑦−0.0647×𝑠𝑝𝑟𝑖𝑛𝑔


From the regression model above , we have the following variables and their coefficients which are significant in predicting the demand for shared bikes:

const         = 0.0901      
Year          = 0.2333    
workingday    = 0.0568    
temp          = 0.4918      
Sep           = 0.0915      
Sat           = 0.0647      
Light Snow    = -0.3051      
Mist + Cloudy = -0.0800      
spring        = -0.0647      
summer        = 0.0516      
winter        = 0.0984

## We can see the demand for bikes depends mainly on below variables:

##### year, working day, temp, month, day, Weather situation, season
##### Demands increases in the month of  septembe  and also 2019 year have more rental count than 2018
##### Demand decreases if it is holiday , Spring, Light rain_Light snow_Thunderstorm, Mist_cloudy


#### The Mean Squared Error , Root Mean Squared Error and Mean Absolute error
- MAE: 0.07307280864355646
- MSE: 0.008972150111724591
- RMSE: 0.0947214342782276

* Assumptions of Linear Regression:
    - The error terms are normally distributed.
    - The training and testing accuracy are nearly equal hence there is no Overfit/Underfit situation.
    - The predicted values have linear relationship with the actual values.**

#### Comparison between the results on Train and Test datasets:
- R-squared Value:

    - Train set : 82.6%
    - Test set : 81.1%

- Adj R-squared Value:

    - Train set : 82.3%
    - Test set : 80.1%

* As we can see that the difference between the R-squared value for the train and test dataset is not more than 5% , therefore we can say that this is a good model .

* As we can see that the difference between the Adj R-squared value for the train and test dataset is not more than 5% , therefore we can say that this is a good model .

#### Important outcome of analysis:-
- We can see that temperature variable is having the highest coefficient 0.4918, which means if the temperature increases by one unit the number of bike rentals increases by 0.4914 units.
- We also see there are some variables with negative coefficients. A negative coefficient suggests that as the independent variable increases, the dependent variable tends to decrease.
- We have spring, mist cloudy , light snow variables with negative coefficient. The coefficient value signifies how much of the dependent variable changes given a one-unit shift in the independent variable while holding other variables in the model constant.

#### Predictions:
- Temperature could be a prime factor for making decision for the comapany.
- We can see demand for bikes was more in 2019 than 2018 so year is also important variable.
- Working days as they have good influence on bike rentals. So it would be great to provide offers to the working individuals.
* The top features contributing significantly towards explaining the demand of the shared bikes are :-
    - temperature
    - year
    - winter
    - workingday
