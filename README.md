# Taxi_duration_model_Mexico_City

A brief description of the idea behind this project

## Table of Contents

-[Motivation](#Motivation)
-[Methodology](#Methodology)
-[Key Findings](#Key_Findings)
-[Model Performance](#Model_Performance)

## Motivation

I wanted to select a dataset that was not something familiar to me but also somehting I could complete in the 24 hours i had. So I chose to do something about my country, Mexico. I found taxi trip data in Kaggle (https://www.kaggle.com/datasets/mnavas/taxi-routes-for-mexico-city-and-quito/code) which sounded like a great opportunity. I had to think about a specific problem to solve. I understood that there have been multiple models that estimate the time duration of taxi trips so I wanted to give my own twist at the end. I would use it to predict if you should move closer to your place of work depending on the rent, and the time and money expended in the trips.

## Methodology

The first hurdle I was present was the fact that I had only 24 hours to complete the assignment, so I decided to only create a model to estimate the time a taxi takes from different starting points and ending points in Mexico City. This left the estimation of the rent to variables the user has to decide. 

The first step in the process was to clean the database since it had multiple datapoints that were outliers. For example, a trip taht apparently took 139 years to complete, and one which average speed was 1900 Km/h, ¡Ridiculous! 

Once the data was cleaned, analysis on the different columns was made to understand which ones would be most useful during the creation of features and the training of the models. Some data like the 'vendor_id' was limited to only some specific values since it had some very low frequency categorical values that could skew results. 

In feature engineering there were 4 variables that were created and used in the final models. The first was a variable called 'traffic_day' which aims to represent if that specific day of the week has in average more traffic than others. The next one was the manhattan distance which is a variable widely used in taxi trip models because it takes a normal distance and measures it as if it was a gridlike pattern. Lastly there were two variables which aim was to create different groupings of locations on the map these were called 'pickup_zone' and 'dropoff_zone' depending on if they were starting points or end points.

Once the variables that would be used for the model were selected, the categorical variables were one hot encoded and the numerical ones were scaled. These were used to train the 5 following models:  Ridge regression, Lasso Regression, Random Forest, XGBoosted Regressor and a neural network. From the five the one with the best RMSE and good behaviour was selected.

## Key_Findings
  

