# Data-mining

Data mining project to understand what contributes to a high rated dark chocolate bar.
Where are the best cocoa beans grown based on the highest-rated chocolate bars? Which countries produce the highest-rated or lowest-rated bars? Is there a connection between cocoa solids percentage and bar rating? We aim to answer these questions using the Over 2,300 Plain Dark Chocolate Bars Rated! database that provides chocolate manufacturer, company location, bean origin, ingredients, characteristics, and rating. We also can answer which countries have the highest-rated chocolate on average.

Data: 
10 columns, 2362 rows; Bategorical and continuous types of data. 
Mean Rating is found to be 3.19
Mean Cocoa Percentage is found to be 71.62%
Mean number of ingredients was not produced as there are missing values. Preprocessing will be done on the data to impute the missing values. 
Missing values: We will be using the mean strategy to impute the missing values in the NumberOfIngredients column. 
Type conversions: The Cocoa percentage is converted to Float from percentage value in order to do descriptive analysis on it. 
![image](https://user-images.githubusercontent.com/22393419/147868307-be0f3e5a-d1cb-45be-99a7-1dd64a8a3423.png)
Fig 1 - Histogram of Ratings
Plotting a histogram of the chocolate bar ratings reveals a left-skewed or negatively skewed curve. 

![image](https://user-images.githubusercontent.com/22393419/147868348-64e14720-ab47-463a-b289-059eed1801a8.png)
Fig 2 - Cocoa% vs Rating Scatter Plot

![image](https://user-images.githubusercontent.com/22393419/147868355-dd7aef0a-6e95-4ed5-a285-f5ba58f57f18.png)
Fig 3 - Ingredients vs Ratings Scatter Plot
Creating a scatter plot of different variables of the chocolate bar data does not yield a linear relationship between points. 

Handling Missing Values: 
There are 2 columns with missing values: NumberofIngredients and Ingredients. 
We imputed the missing value in Number of ingredients with the round value of the mean of the number of ingredients.
For Ingredients, which is a string value, we applied the Apriori algorithm on that column separately to find the most frequent itemset of minimum length equal to the round value of the mean of the number of ingredients. Doing this we found that the most frequent ingredients occurring together are: [' B,S,C']. Therefore, we impute the Ingredients missing data with this value. 

# Methodology:
In this project, we utilized data cleaning and preparation in order to remove any outliers or missing information that could skew our results using data modeling and aggregation in some cases to provide a specific result. Outlier detection, including modeling the data using histograms and charting to communicate results of patterns in the data was also used to find anomalies. Anomalies in this data set would not be used to optimize the data, but would rather be considered mistakes when encoding the data. Any anomalies were thus removed rather than explored.
Text mining using Knime was used to find patterns in the data. Charting the largest occurrence of ingredient combinations in the chocolate bars ranked between 3.0 and 5.0 yielded informational results and revealed unknown patterns in the data. Chocolatiers and other people interested in this data could thus use this information to make inferences and other insights into how they produce and work with chocolate, for instance. 
Association analysis and cluster analysis has been used with python to find patterns in the data set. Association analysis has been used to find the most frequently occurring combination of ingredients and its association with the rating of that chocolate bar. For this task we have used the Apriori algorithm to do association analysis. A minimum support of 30% and length of 3 has been used.
We have used clustering to find a pattern between Cocoa percentage and rating. We have used the KMeans algorithm using the library scipy.cluster.vq to do clustering, with a K value of 3. The value of 3 was decided by doing the elbow method to find the optimal K-value for K-means clustering. 

Softwares used: Python and Knime
