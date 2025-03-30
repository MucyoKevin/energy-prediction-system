# Energy Consumption Forecasting 

## Project Overview

This project forecasts Romania's electricity consumption using historical data from January 2019 to March 2024. We compare three time-series forecasting approaches:
- **ARIMA (AutoRegressive Integrated Moving Average)**
- **SARIMA (Seasonal ARIMA)**
- **LSTM (Long Short-Term Memory neural networks)**
The goal is to determine the most accurate method for predicting energy consumption patterns to support grid management and resource planning.

## Dataset

The dataset contains hourly electricity consumption and production data from Romania, aggregated to monthly sums for analysis.

- **Time Period:**:January 2019 - March 2024
- **Measurements**: Consumption in megawatt-hours (MWh)
- **Additional Data**:  Includes production by source (Nuclear, Wind, Hydroelectric, etc.)
- **Source**: https://www.kaggle.com/datasets/stefancomanita/hourly-electricity-consumption-and-production/data


## Methodology

*Data Preparation*
  1. Loaded and aggregated hourly data to monthly sums

  2. Performed exploratory analysis to identify trends and seasonality

  3. Checked stationarity using Augmented Dickey-Fuller test

  4. Applied differencing to make data stationary

*Models Implemented*

1. *ARIMA Model*
Parameters: (1,2,1)

Differencing: Second-order to achieve stationarity

2. *SARIMA Model*
Parameters: (0,1,0)(1,1,1,12)

Handles both trend and seasonality

3. *LSTM Model*
Architecture: 50-unit LSTM layer

Training: 50 epochs with batch size 32

Sequence length: 12 months

## Key Findings:

-SARIMA performed best, effectively capturing seasonal patterns

-LSTM showed promise but would benefit from more training data

-ARIMA underperformed due to inability to model seasonality

## Future Work

Potential improvements:

-Incorporate exogenous variables (weather, holidays)

-Experiment with hybrid models

-Extend forecasting horizon

-Deploy as real-time forecasting system

## Usage

1. **Clone the repository**:
   ```
   git clone <repository-url>
   cd Energy_prediction_system
   ```

2. **open the notebook and follow the steps**
   

## License

[MIT License](LICENSE)

## Contributors

- Mucyo Kevin - Initial work 