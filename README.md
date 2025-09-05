# Store Sales Forecasting

A machine learning project for forecasting store sales using time series analysis and external factors.

## Dataset

This project uses the [Store Sales - Time Series Forecasting](https://www.kaggle.com/competitions/store-sales-time-series-forecasting) dataset from Kaggle, which includes:

- **train.csv** - Training data with sales information
- **test.csv** - Test data for predictions
- **stores.csv** - Store information and metadata
- **oil.csv** - Daily oil price data (external factor)
- **holidays_events.csv** - Holiday and event information
- **transactions.csv** - Transaction data per store
- **sample_submission.csv** - Example submission format

## Setup

1. Install required packages:
```bash
pip install -r requirements.txt
```

2. Set up Kaggle API credentials:
   - Download your `kaggle.json` file from Kaggle
   - Place it in `~/.kaggle/` directory
   - Run the download script to get the dataset

## Project Structure

```
├── data/                   # Dataset files
├── notebooks/              # Jupyter notebooks for analysis
├── src/                    # Source code
├── models/                 # Trained models
├── requirements.txt        # Python dependencies
└── README.md              # This file
```

## Getting Started

1. Download the dataset using your Kaggle credentials
2. Explore the data in the notebooks
3. Build and train forecasting models
4. Generate predictions for the test set

## Features

- Time series forecasting with external factors
- Store-specific sales patterns
- Holiday and event impact analysis
- Oil price correlation analysis