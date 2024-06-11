# project-2-group-3 : Retail Paint Store Sales Prediction

# Summary
The project successfully identified the most suitable forecasting model (SARIMA) for paint sales across multiple stores. While initial models like linear regression and ARIMA had limitations, the SARIMA model effectively captured seasonality and provided accurate forecasts. The use of Prophet as an alternative model further validated these findings. Despite facing data and technical challenges, the project laid a strong foundation for future enhancements, including the integration of external data and real-time forecasting capabilities. By addressing these areas, the forecasting system can become a valuable tool for inventory management, sales optimization, and demand anticipation. Should be noted that there was a clear observation related to Covid in the stores data that were open before and after this global pandemic. Overall all stores do show they are profitable and will continue to produce for the business, but with this data they can now focus advertising efforts on the stores that have not been producing as well as others. 

# Background:
Team objective was to analyze retail paint store sales data to create models that would predict future possibilities for sales. We were able to gather data from the retail store and transformed into a usable format to process with several data models. The information produced can potentially be used by the store owners to create plans to generate sales. 

# Requirements: 
In order to properly run these steps in the workbooks you will need to have the following dependencies installed. Once installed you will need to pull the required libraries into your workbook. 

Installs: 
- pip install pandas
- pip install numpy
- pip install pathlib
- pip install matplotlib
- pip install datetime
- pip install bokeh
- pip install sklearn
- pip install prophet
- pip install statsmodels
- pip install arch

Pandas support: 
- import pandas as pd
- from pandas.plotting import lag_plot
- import numpy as np
- from pathlib import Path
- import matplotlib.pyplot as plt

Datetime support: 
- from datetime import datetime, timedelta

Bokeh support:
- import bokeh as bokeh
- from bokeh.plotting import figure, show
- from bokeh.io import output_notebook
- from bokeh.models import ColumnDataSource
- from bokeh.models import NumeralTickFormatter

SkLearn Support: 
- from sklearn.preprocessing import StandardScaler
- from sklearn.linear_model import LinearRegression

Prediction Models: 
- from prophet import Prophet
- from arch import arch_model
- from statsmodels.tsa.stattools import adfuller
- from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
- from statsmodels.tsa.arima.model import ARIMA
- from statsmodels.tsa.statespace.sarimax import SARIMAX

# Data Elements
This project was specifically utlizing time series data that was extracted from a financial system for retail sales. Common fields used were Year, Sales(in dollars), Gallons, Month, week of year. For use of standardization we transformed the year/month/week of year into a single date time column and extracted just the specific columns needed. We utilized datetime/sales/gallons in our models to permit trending and proper plotting visually over time. 
All data files utlized for this project are in the /data directory within the project. 
- original data file extracted from client system (allstores_2007topresent_final)
- processed data files store*_data created from cleaning steps and made available to run models and plotting
- several test files were utilized to work through data processing steps with smaller sets of data, also used for some initial model/plotting steps
- Data dates varied due to length of store being in operation *2007 - May 2024
    - Store 1 had data points going back to 2021
    - Store 2 had data points going back to 2017
    - Store 3 had the most data points going back to 2007
    - Store 4 had data points going back to 2022
    - Store 5 had data points going back to 2014

# Future Enhancements
If our team was to continue with this effort we have agreed the following would be a benefit to the data and information produced: 
- Data Enhancement:
    - Integrate more detailed external data (e.g., economic forecasts, advanced weather data).
    - Collect and include data on customer demographics and buying behaviors.
- Model Improvement:
    - Experiment with additional machine learning models
    - Explore ensemble methods for improved prediction accuracy.
- System Deployment:
    - Develop a real-time forecasting system that updates predictions based on new sales data.
    - Implement a user-friendly interface for store managers to access forecast and insights.
- Evaluation and Feedback:
    - Continuously evaluate model performance with new data.
    - Gather feedback from stakeholders to refine the model and improve its usefulness.


# Supporting Information
- file share location for data sharing: 
https://drive.google.com/drive/folders/1ikmymqF7VuWBbDtaPKaG0Hb8fGMo3vbP

- github repo for all code and results: 
https://github.com/galedione/project-2-group-3.git

- pandas date time documentation: 
https://docs.python.org/3/library/datetime.html

- Bokeh visualization library: 
https://bokeh.org/

- Model documentation: 
    - https://machinelearningmastery.com/develop-arch-and-garch-models-for-time-series-forecasting-in-python/
    - https://arch.readthedocs.io/en/latest/univariate/introduction.html
    - https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html
