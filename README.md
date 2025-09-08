# Store Sales Forecasting

A machine learning project for forecasting store sales using time series analysis and external factors.

## Dataset

This project uses the [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) dataset from Kaggle
Data which was used:

- **train.csv** - Training data with sales information for a period up until 15 August 2017
- **test.csv** - Test data which includes the dates which need to be predicted (16 August 2017 - 31 August 2017)
- **oil.csv** - Daily oil price data (external factor)
- **sample_submission.csv** - Example submission format



## Instructions to download the data set using your Kaggle API credentials. 
Based on the recommended way to create the repository by ChatGPT i worked on the data i downloaded the dataset using my Kaggle credentials.
  
1.) Install the Kaggle API using pip install kaggle

2.) Download your Kaggle API ( Click on profile picture → Account → scroll down to API). A file named kaggle.json will be downloaded. 

3.) Place the Kaggle API in your systems default location ( This was done automatically by opening it if using Cursor)

4.) Open a terminal and run - kaggle competitions download -c store-sales-time-series-forecasting -p data/

6.) Unzip the files 

7.) Load the data into your project
  
## Project Approach

1.) I started by ensuring the data was set up correctly and all recommended packages were installed. 

2.) Explored the data in the notebooks
- I then explored the data, to see if there was any direct correlation between the oil price and sales as well as correlation between promotions on sales. (Refer to Data Exploration folder) 
- Whilst there was some correlation these did not seem to have a significant impact and for the purpose of this submission i chose to ignore this data. ( I plan on incorporating this at a later stage)
  
3.) Used rolling avergages to create predictions - Used a 28 rolling average
   
4.) Generated predictions for holdout data (Period 1 August 2017 - 15 August 2017) to test the model.
   
5.) Created prediction for test set (Period 16 August 2017 - 31 August 2017)

6.) Submitted project on Kaggle

## Project Structure

```
├── data/                   # Dataset files
├── notebooks/              # Jupyter notebooks for analysis
├── src/                    # Source code
├── models/                 # Trained models
├── requirements.txt        # Python dependencies
└── README.md              # This file
```
