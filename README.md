## Table of Contents

1. [Overview](#overview)
2. [Dataset Description](#dataset-description)
3. [Requirements](#requirements)
4. [Setup](#setup)
5. [Key Features](#key-features)
6. [Methodologies](#methodologies)
7. [Usage Instructions](#usage-instructions)
8. [Output and Results](#output-and-results)

## Overview

Water quality management is vital for ecosystems and human health. This project addresses the limitations of traditional monitoring by leveraging multivariate time series forecasting. It employs advanced models like LSTM, TCN, TFT, and ARIMA to predict key water quality parameters, including:
- **Dissolved Oxygen**
- **Temperature**
- **Salinity**
- **pH**
- **Turbidity**

The notebook includes data preprocessing, feature engineering, exploratory analysis, seasonality visualization, and multi-horizon forecasting.

## Dataset Description

The dataset contains **30,894 records** collected at **30-minute intervals** from the Brisbane River. Key variables include:
- **Temperature**: Affects chemical and biological processes.
- **Dissolved Oxygen**: Essential for aquatic life.
- **Chlorophyll**: Indicates algae concentration.
- **Turbidity**: Reflects water clarity.
- **Salinity**: Influences aquatic habitats.
- **pH**: Measures water's acidity/alkalinity.

Missing values and multivariate dependencies are handled through preprocessing, correlation analysis, and temporal feature engineering.

## Requirements

### Software
- **Python 3.8+**

### Python Libraries
- `pandas`
- `numpy`
- `matplotlib`
- `scipy`
- `scikit-learn`
- `tensorflow`
- `torch`
- `ray`
- `statsforecast`

## Setup

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/downshift/water-quality-monitoring-dataset).
2. Update the file path in the notebook:
   ```python
   file_path = '/path/to/brisbane_water_quality.csv'
   
## Key Features

- **Data Preprocessing**:
  - Handles missing values, outliers, and irregular time steps.
  - Adds moving averages, lagged features, and time-based features.
- **Exploratory Analysis**:
  - Seasonality trends and correlations visualized with plots.
  - Fourier Transform for frequency analysis.
- **Forecasting Models**:
  - LSTM and TCN for deep learning.
  - Temporal Fusion Transformer (TFT) for interpretability.
  - AutoARIMA for statistical benchmarking.
- **Hyperparameter Tuning**:
  - Efficient optimization using Ray Tune.
   
## Methodologies

1. **Preprocessing**:
   - Missing value interpolation.
   - Min-Max scaling for normalization.
   - Time-based and lagged feature engineering.
2. **Exploratory Analysis**:
   - Visualizing time series trends and correlations.
   - Seasonal patterns analysis (daily, weekly).
3. **Modeling**:
   - Deep learning models: LSTM, TCN, TFT.
   - Statistical model: AutoARIMA.
   - Incremental ARIMA training for robust predictions.
4. **Evaluation**:
   - Metrics: MSE, MAE, RMSE, and R².
   - Visual comparison of predictions vs. actuals.

## Usage Instructions

1. Run the notebook sequentially.
2. Adjust parameters, such as forecast horizon:
   ```python
   forecast_horizon = 36  # Predict 6 hours into the future

## Output and Results

- **Visualizations**:
  - Seasonal trends, correlations, and predictions.
  - Training and validation loss curves.
- **Metrics**:
  - Quantitative evaluation for all models.
  - Multi-horizon forecast accuracy.
- **Predictions**:
  - Forecasted values for water quality parameters.

