# Time Series Forecasting Using Deep Learning on the Jena Climate Dataset

## Project Goals

This project leverages the Jena Climate Dataset to explore and predict key climate variables, particularly temperature, using a range of machine learning and deep learning models.

### Objectives:
- **Feature Analysis**: Analyze features such as time, atmospheric pressure, and other climate-related variables.
- **Model Development**: Develop robust predictive models to forecast climate metrics. Techniques include linear regression, random forests, and advanced deep learning models such as Long Short-Term Memory (LSTM) networks.
- **Model Evaluation**: Evaluate each model’s performance and compare results to determine the most effective approach for climate prediction.

This project aims to demonstrate the application of data science to real-world climate data, highlighting how predictive modeling can contribute to understanding climate dynamics and aiding in environmental decision-making.

## Dataset Information

### Context
The Jena Climate Dataset consists of weather time series data recorded at the Weather Station of the Max Planck Institute for Biogeochemistry in Jena, Germany.

### Content
The dataset includes 14 different quantities recorded every 10 minutes from January 1st, 2009 to December 31st, 2016. Key variables include:

| Variable   | Description |
|------------|-------------|
| Date Time  | Date-time reference |
| p (mbar)   | Atmospheric pressure in millibars |
| T (degC)   | Temperature in Celsius |
| Tpot (K)   | Temperature in Kelvin |
| Tdew (degC) | Dew Point temperature in Celsius |
| rh (%)     | Relative Humidity (%) |
| VPmax (mbar) | Saturation vapor pressure |
| VPact (mbar) | Actual vapor pressure |
| VPdef (mbar) | Vapor pressure deficit |
| sh (g/kg)  | Specific humidity |
| H2OC (mmol/mol) | Water vapor concentration |
| rho (g/m³) | Air density |
| wv (m/s)   | Wind speed |
| max. wv (m/s) | Maximum wind speed |
| wd (deg)   | Wind direction in degrees |

## Model Performance

The project employed various machine learning models, with a focus on LSTM networks. Below are the final results:

| Model | Dataset   | MSE     | RMSE    | MAE     | R²      | Adj_R²  |
|-------|-----------|---------|---------|---------|---------|---------|
| LSTM5 | Training  | 0.499458 | 0.706723 | 0.483696 | 0.993098 | 0.993097 |
| LSTM5 | Validation| 0.396326 | 0.629544 | 0.441240 | 0.988936 | 0.988920 |
| LSTM5 | Testing   | 0.462252 | 0.679891 | 0.469571 | 0.993363 | 0.993354 |

### Metrics:
- **MSE (Mean Squared Error)**: Measures the average squared difference between predicted and actual values.
- **RMSE (Root Mean Squared Error)**: Measures the square root of the average squared differences; gives an idea of the magnitude of error.
- **MAE (Mean Absolute Error)**: Measures the average absolute differences between predictions and actual values.
- **R² (R-squared)**: Indicates how well the model explains the variance in the target variable.
- **Adjusted R²**: Adjusted R² accounts for the number of predictors in the model, providing a more accurate measure of model performance.

## Technologies Used
- **Data Processing**: Pandas, NumPy
- **Modeling**: TensorFlow/Keras for LSTM networks
- **Visualization**: Matplotlib, Seaborn

## Conclusion
The LSTM model demonstrated strong performance in predicting temperature, with high R² values indicating a robust fit to the data. The project showcases the effectiveness of deep learning techniques in time series forecasting and highlights the potential for these models in climate prediction.

## Future Work
- **Model Enhancement**: Experiment with additional deep learning architectures and hyperparameters.
- **Feature Engineering**: Explore additional features or external data sources to improve model performance.
- **Deployment**: Consider deploying the model for real-time climate forecasting applications.

