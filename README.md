# Solar Home Electricity Forecasting

## Contributors
- Thrushwanth Kakuturu (My self)
- Gnanambal Kamakshi Renganathan
- Sireesha Pulipati(Team Lead)

## Overview
Ausgrid is a major electricity distributor in Australia, responsible for managing and distributing electricity to residential, commercial, and industrial consumers. Recently, Ausgrid has focused on integrating renewable energy sources into its grid infrastructure to reduce carbon emissions and promote sustainability.

Solar electricity generation is a key component of this renewable energy transition. However, photovoltaic energy is volatile as it depends on weather conditions, making it challenging for network operators to integrate and manage. Renewable energy forecasting is a crucial solution to effectively manage this volatility within the power system.

This project aims to develop a robust forecasting model to predict energy consumption, ensuring optimal energy management and proper control of energy supplied to users.

## Data Source
The data for this project is sourced from Ausgrid's Solar Home Electricity Data, available at [Ausgrid Data to Share](https://www.ausgrid.com.au/Industry/Our-Research/Data-to-share/Solar-home-electricity-data).

## Datasets
- **Monthly Data**: This dataset includes information from 2,657 solar homes and 4,064 non-solar homes, providing a comprehensive view of energy consumption patterns. It covers a period of 8 years (2007-2014), allowing for the identification of seasonal trends.
- **Total Household Energy Needs**: This metric accounts for the total electricity used by households, considering both solar generation and grid consumption. It can be estimated by:
  \[
  \text{Net Household Consumption} = \text{Total Grid Consumption} - \text{Solar Power Output}
  \]

## Forecasting Models
### SARIMA
A statistical model for time series forecasting that can capture seasonality, trend, and noise in the data.

### XGBoost
A scalable machine learning system for tree boosting, particularly suited for large datasets and high-dimensional features.

## Development and Deployment

### Development
- **Environment**: Vertex AI Workbench / Colab
- **Models Developed**: SARIMA and XGBoost

### Deployment (XGBoost)
1. **Generate Model Artifacts**: Train the XGBoost model and save it as a model artifact.
2. **Upload to Google Cloud Storage (GCS)**: Upload the model artifact to a designated GCS bucket.
3. **Import the Model into Vertex AI**: Import the model into Vertex AI for deployment.
4. **Deploy to Vertex Endpoint**: Deploy the model to a Vertex endpoint for serving next month predictions for every customer.

## Technologies Used
- **Programming Languages**: Python
- **Libraries**: XGBoost, Pandas, NumPy, Scikit-learn, Matplotlib, statsmodels
- **Platform**: Google Cloud (Vertex AI, Google Cloud Storage)

## Conclusion
This project successfully developed and deployed an XGBoost model to forecast solar home electricity consumption. The development of XGBoost modelf, combined with deployment on Google Cloud's Vertex AI, provides a robust solution for managing renewable energy in the power system. The forecasting model aids in optimal energy management, contributing to Ausgrid's sustainability goals.




