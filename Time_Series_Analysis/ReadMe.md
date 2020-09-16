Time series analysis is done with a purpose of identifying trends, cycles and seasonal variances to aid in the forecasting of the future events based on previously observed values. In this project, we build a model to predict the stock of products in future.

#### Data Preprocessing:
We encountered certain irregularities in the dataset and
resolved them as below:
* Header rows and Date feature were treated the same way as done for MBA in section [A].
* Converted ’Net Sales Units’ feature to numeric value.
* Label encoding for categorical features like ’Store #’ and ’Item Number’.
* Removed the records with ’Item Type’ as ’Defective’ and ’Return’. This is because the stock prediction should only be done based on the actual sales of items.

#### Model:
Features used: ’Date’, ’Store #’, ’Item Number’, ’Net Sales Units’.

#####Description:
* We grouped the data based on Date, Store #, Item number features and did summation of Net Sales Units for the combination. 

Then, we performed some analysis:
* We analysed weekly Store Sales which for each store over the course of a few months. Here we wanted to see if there are any seasonality trends in the total store sales.

We visualised our data using time series decomposition that broke down the time series into trend, seasonality, and noise. Refer figure 5 for this. The trend of sale is varied and there is a pattern in seasonality wherein the sale increases from the month of May to June as well as in December every year.

* There’s definitely a seasonality in the store’s sales across the year.
* Day of week plays a role in sales. However, all the stores have similar distributions i.e. it follows a general weekly trend.

Model building:
- Date being a non-numeric field, we have engineered the dataframe by adding features such as Day of Year, Day of week, Month and whether it is a weekday/weekend.
- We have also added prior year sales.
- We have split the dataset into train and test where test data consists of last 5 months.
- We have used XGBoost model to predict the sales units and gauge the accuracy of the model using RMSE.

![Seasonality Trends](https://github.com/Kaustubh-Sable/Retail-Data-Analysis/blob/master/Time_Series_Analysis/Images/Seasonality_Trends.png)

####  Results:
We tested our model against the test dataset and got the root mean square error (RMSE) value as 1.06006. From this, we can deduce that our model has performed quite well. Hence, the predicted values by our model could be helpful for item-wise demand prediction for various stores.

#### References
* Soheila Mehrmolaei ; Mohammad Reza Keyvanpour (2016). Time series forecasting using improved ARIMA.
* http://airccse.org/journal/ijcsea/papers/4214ijcsea02.pdf
* https://www.kaggle.com/enolac5/time-series-arima-dnn-xgboost-comparison
* Frequent Itemsets via Apriori Algorithm: http://rasbt.github.io/mlxtend/user guide/frequent patterns/apriori
* Andrej Trnka (2010). Market Basket Analysis with Data Mining methods.
