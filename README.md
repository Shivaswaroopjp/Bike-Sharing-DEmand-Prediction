# Bike-Sharing-Demand-Prediction

## Description: 

Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern.
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

### Dataset : 
https://www.kaggle.com/c/bike-sharing-demand

## Execution: 

For the First step, the data is imported from a csv file and converted to a  panda’s DataFrame . Pandas is inbuilt library in python that is used in handling and manipulating Dataframes. Dataframe is basically collection of Rows and Columns. 
Once the data is clean, we check for the statistics of the cleaned data. The statistics of the data tells us the mean, median and the distribution of the data and some more info. 

## Data Visualizations:

After the data is cleaned, Visualizations can be done on the data and inferences can be noted. 
One such visualization is to find the correlation between the variables and found out that Temperature and Dew point Temperature are highly correlated and dew point has to be deleted from the DataFrame.
Another such visualizations is to find out what are the months in which the people in seoul like to drive the rented bicycles. Plotting that we found that people like driving more in summers than in any other weather.
Similarly, we can plot the frequency of bikes rented to the hour of the day and found out that there is a significant increase in the number of rents at 08:00 in the morning and 18:00 in the evening. So, we can infer that people using the rented bikes are mostly office going people. 
Also, we plotted the number of rented bikes according to the weekday and find out that most of the traffic is on weekdays and least on Sunday.
Similarly, by plotting the temperatures in which people like to ride the bikes to find out that the sweet spot of temperature for riding is around 25 degrees Celsius.
Also, by plotting the time of day (day or night) in which the riders prefer riding, to find out that more than 75% rides happen in daytime and the rest in night time.

Another such Visualization is plotting amount of rainfall and snowfall in which riders are found renting the bikes most and found out that people are found riding in very less to nil rainfall and snowfalls.

## data modelling: 

Coming to the second part, which is Data Modelling in which we try out different Supervised Machine Learning Regressor algorithms fits the best to our dataset and gives us the best accuracy (R2 scores).
Starting with a primitive Regressor Algorithm as Multiple Linear regression and fitting it to our dataset to find out that, this algorithm doesn’t give us satisfactory results as the R2 score for testing and training datasets is around 47%. So, we end up discarding this model and look onto new models.
Next, we take on lasso and Ridge Regression Algorithms. The main idea behind Ridge Regression is to find a new line that doesn’t fit the training data. Fitting this on our dataset to found that the accuracy results were not so pleasing with R2 score around 48%. Same is the case with Lasso Regression.
Let’s look onto next Algorithm “Decision Tree Regression”. Decision Tree Regressor is fairly complex algorithm when compared to Linear Regression models. Coming to the R2 scores, fairly appealing with R2 scores around 67% on training and testing datasets.

Last but not the least, Random Forest Regressor which is a tad more complex than Decision Tree and hence, we could expect more accurate results. Confirming on our Expectation the accuracy results are slightly better than Decision tree Regressor, with training R2 scores of 79% and testing scores of 75%.

Coming to our last regressor, Extra trees regressor. As it is the most complex of all our previous models and hence has the best results in the lot. The R2 scores for Training dataset are 80% and the score for testing dataset is 76%, Which is the best performance we saw in all of our regressor algorithms. 

## Conclusion:

Concluding, We choose to go ahead with Extra Tree Regressor as it had the best performance and R2 scores.


### References: 
  1. https://anindya-saha.github.io/blog/machine-learning-with-python/kaggle-bike-sharing-demand/kaggle-bike-sharing-demand.html
  2. https://towardsdatascience.com/end-to-end-case-study-bike-sharing-demand-dataset-53201926c8db
