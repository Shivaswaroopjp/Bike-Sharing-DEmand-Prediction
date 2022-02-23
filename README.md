# Bike-Sharing-Demand-Prediction


## Description:

Prediction of bankruptcy is a phenomenon of increasing interest to firms who stand to lose money because on unpaid debts. Since computers can store huge dataset pertaining to bankruptcy making accurate predictions from them before hand is becoming important.
The data were collected from the Taiwan Economic Journal for the years 1999 to 2009. Company bankruptcy was defined based on the business regulations of the Taiwan Stock Exchange.
In this project, we have used various classification algorithms varying from Logistic Regression till CATBoost, and their accuracy metrics have been plotted simultaneously.

## Execution:

### Dataset: 
https://www.kaggle.com/c/bike-sharing-demand

### Data cleaning:

For the First step, the data is imported from a csv file and converted to a panda’s DataFrame. Pandas is inbuilt library in python that is used in handling and manipulating Dataframes. Dataframe is basically collection of Rows and Columns. 
Once the data is clean, we check for the statistics of the cleaned data. The statistics of the data tells us the mean, median and the distribution of the data and some more info. Also, we checked for any null values and duplicate values in the whole dataset and for our surprise, we didn’t find neither any null nor duplicate values.
After the data is cleaned, Visualizations can be done on the data and inferences can be noted. 

### Visualizations:

One such visualization is to find the correlation between the variables. Plotting the correlation between variables is not visually appealing as there are 65 different variables. But we see some red squared in between that says they are highly correlated. 
As the target variable is categorical i.e., Bankrupt or not, plotting this variable we find out that around 97% of the data present is of financially stable and the rest is financially unstable.
Similarly, we can plot the Boxplot of Correlations between the variables and also feature distributions for close to bankruptcy companies.
After all this, we remove the outliers. Outlier is a data point that is present very far away from the mean of the distribution of the data. There is a set procedure to remove the outliers. And once the outliers are scaped of, The Boxplot distribution is plotted once again to find out that most of the outliers are removed.
Then, we perform a Log (Logarithmic) transformation on the data, the log transformation is performed in the data to remove any skewness present in the data and produce an approximate log-normal distribution. After the log transformation has been performed, we see a approximation of normal distributions in our dataset.

### Data modelling:

Coming to the second part, which is Data Modelling in which we try out different Supervised Machine Learning Classification algorithms fits the best to our dataset and gives us the best accuracy scores like precision, Recall, AOC-ROC curve, Accuracy and so on
Starting with a primitive Logistic Regression, Logistic regression is a statistical model that in its basic form uses a logistic Function to model a binary dependent variable, although many more complex extensions exist. After we apply Logistic regression to our model, the overall accuracy scores were 0.89 and f1-scores of 0.94 and the AOC-ROC score of 0.83
Next, we take on Random Forest Classifier algorithm. Random Forest being a much more complex algorithm produces better results. Providing an overall accuracy of 0.95, f1-score of 0.97 and finally AOC-ROC score of 0.70
Let’s look onto next Algorithm XGBOOST. XGBoost is an implementation of gradient boosted decision trees designed for speed and performance. XGBoost is a decision-tree-based ensemble Machine Learning algorithm that uses a gradient boosting framework. Coming to its accuracy scores, overall accuracy score of 0.95, and a f1-score of 0.97 and AOC score of 0.66

Last on our list is the CATBoost, CATBoost is a member of the family of GBDT (Gradient Boosted Decision Tree) machine learning ensemble techniques. Moving on to its accuracy metrics, total average accuracy comes up to 

Coming to our last regressor, Extra trees regressor. As it is the most complex of all our previous models and hence has the best results in the lot. The R2 scores for Training dataset are 80% and the score for testing dataset is 76%, Which is the best performance we saw in all of our regressor algorithms. 0.93, f1-score of 0.97 and ROC score of 0.76

### Conclusion: 

Concluding, according to the f1-scores and the Accuracy metrics, CATBoosT is the best metric to choose for further predictions. According to AOC-ROC, Logistic Regression stands first with a score of 0.86 Nevertheless, in this case, the best decision is to use Logistic regression because it can better recognize the minority class even misclassifying some not close to bankruptcy companies as close to bankruptcy.Also, the parameters that contribute to bankruptcy of a company are also external such as decisions taken by the CEO of the company and dwindling workforce and so on, which can neither be calculated nor predicted.


## Credits and References:
  1. https://towardsdatascience.com/end-to-end-case-study-bike-sharing-demand-dataset-53201926c8db
  2. https://anindya-saha.github.io/blog/machine-learning-with-python/kaggle-bike-sharing-demand/kaggle-bike-sharing-demand.html

