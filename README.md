# Store Sales Forecasting

Project for forecasting store sales using time series analysis and external factors.
The purpose of the project is to predict the sales for the period 16 August 2017 - 31 August 2017

## Dataset

This project uses the [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) dataset from Kaggle
Data which was used:

- **train.csv** - Training data with sales information for a period up until 15 August 2017
- **test.csv** - Test data which includes the dates which need to be predicted (16 August 2017 - 31 August 2017)
- **oil.csv** - Daily oil price data (external factor)
- **sample_submission.csv** - Example submission format



## Instructions to download the data set using your Kaggle API credentials. 
Based on the recommended way to create the repository by ChatGPT i downloaded the dataset using my Kaggle credentials as the files were too large to upload into GitHub
  
1.) Install the Kaggle API using pip install kaggle

2.) Download your Kaggle API ( Click on profile picture → Account → scroll down to API). A file named kaggle.json will be downloaded. 

3.) Place the Kaggle API in your systems default location ( This was done automatically by opening it if using Cursor)

4.) Open a terminal and run - kaggle competitions download -c store-sales-time-series-forecasting -p data/

6.) Unzip the files 

7.) Load the data into your project
  
## Project Approach and updates

1.) I started by ensuring the data was set up correctly in the correct format and all recommended packages were installed in my notebook.

2.) Exploration of data
- I then explored the data, to see if there was any direct correlation between the oil price and sales as well as correlation between promotions on sales. (Refer to Data Exploration folder in notebook) 
- Whilst there was some correlation these did not seem to have a significant impact and for the purpose of this submission i chose to ignore this data. ( I plan on incorporating this at a later stage)
  
3.) Used rolling averages to create predictions - Used a 28 rolling average i created the predicted sales.
   
4.) Tested the model by generating predictions for holdout data and comparing against the actual data in training data (Holdout Period = 1 August 2017 - 15 August 2017). Used the Kaggle evaluation metric and got a Validation RMSLE: 0.5151455759803385 
   
5.) Created prediction for test set (Period 16 August 2017 - 31 August 2017) 

6.) Submitted 1st version of project on Kaggle (1st submission had a RMSLE of 1.16668). The higher RMSLE was as a result of the 31 August 2017 not having any data in my 1st submission. 

7.) Updated code and submitted 2nd version on Kaggle with a RMSLE of 0.46618. Ranked 89 on the leaderboard. 

## Next Steps/Improving the forecast

1.) Incorporate Additional Features

Oil prices – Sales may be influenced by changes in fuel cost and transportation.

Holiday and special events – Certain holidays or promotions can significantly impact sales.

Store-level promotions – Items on promotion often see increased sales.

2.) Advanced Time Series Models

Using ARIMA Models that capture trends, seasonality, and autocorrelation in the sales data.
