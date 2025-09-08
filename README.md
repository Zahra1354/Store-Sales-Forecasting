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



## Instructions to download the data set. 
Based on the recommended way to create the repository by ChatGPT i downloaded the dataset into Cursor using my Kaggle credentials as the files were too large to upload into GitHub. ChatGPT is able to provide a detailed step-by-step guide on how to download using your Kaggle API credentials.

The files can also be downloaded directly from Kaggle and place the files inside a /data folder in the repository.

https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data
  
## Project Approach and updates

1.) I started by ensuring the data was set up correctly in the correct format and all recommended packages were installed in my notebook.

2.) Exploration of data
- I then explored the data, to see if there was any direct correlation between the oil price and sales as well as correlation between promotions on sales. (Refer to Data Exploration folder in notebook) 
- Whilst there was some correlation these did not seem to have a significant impact and for the purpose of this submission i chose to ignore this data. ( I plan on incorporating this at a later stage)
  
3.) Used rolling averages to create predictions - Used a 28 rolling average to create the predicted sales in the sales_pred column.
   
4.) Tested the model by generating predictions for holdout data and comparing against the actual data in training data (Holdout Period = 1 August 2017 - 15 August 2017). Used the Kaggle evaluation metric and got a Validation RMSLE: 0.5151455759803385 
   
5.) Created prediction for test set which is the data for which the sales need to be predicted (Period 16 August 2017 - 31 August 2017) and created a CSV file in the competition submission format. 

6.) Submitted 1st version of project on Kaggle (1st submission had a RMSLE of 1.16668). Through investigation i determined that the higher RMSLE was as a result of the 31 August 2017 not having any data in my 1st submission. 

7.) Updated code to include data for 31 August 2017 and submitted 2nd version on Kaggle with a RMSLE of 0.46618. Ranked 89 on the leaderboard. 

<img width="697" height="118" alt="image" src="https://github.com/user-attachments/assets/915403b2-ab5d-4168-bc03-cc359df96a19" />


## Next Steps/Improving the forecast

1.) Incorporate Additional Features

Oil prices – Sales may be influenced by changes in fuel cost and transportation.

Holiday and special events – Certain holidays or promotions can significantly impact sales.

Store-level promotions – Items on promotion often see increased sales.

2.) Advanced Time Series Models

Using ARIMA Models that capture trends, seasonality, and autocorrelation in the sales data.
