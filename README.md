# Multivariate Timeseries Forecasting of Gold Prices in lieu of COVID-19

This repository contains a jupyter notebook that focuses on analyzing gold prices in relation to COVID-19 cases and vaccination efforts.

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Analysis](#analysis)
- [Models](#models)
- [Results](#results)
- [Credits](#credits)

## Introduction

In this project, I aim to investigate the relationship between gold prices and COVID-19 by analyzing global COVID-19 cases, vaccination data, and gold prices. The goal is to predict gold prices based on COVID-19 data and evaluate the accuracy of the predictions for more than a **6 month period**.

## Data

The project utilizes two main datasets:

- COVID-19 Data: The COVID-19 data is sourced from [Our World in Data](https://github.com/owid/covid-19-data) and includes weekly global new cases and new vaccinations data.
- Gold Price Data: The gold price data is sourced from the [World Gold Council](https://www.gold.org/goldhub/data/gold-prices) and includes weekly gold prices from February 2012 to January 2022.

## Analysis

The project involves the following steps:

1. Data preprocessing: The COVID-19 and gold price datasets are loaded and preprocessed. The data is cleaned, transformed, and aggregated as necessary.
2. Exploratory data analysis: Various visualizations are created to explore the relationships between COVID-19 cases, vaccinations, and gold prices over time.
3. Model training: Four different models (LSTM, XGB, TCN and TFT) are trained to predict gold prices based on COVID-19 data. Each model is hyperparameter opitimized using [Optuna](https://optuna.org).
4. Model evaluation: The trained models are evaluated using the mean absolute percentage error (MAPE) metric to assess their accuracy in predicting gold prices.
5. Results visualization: The predictions and actual gold prices are plotted to visualize the performance of each model.

## Models

The project utilizes the following models for gold price prediction:

1. LSTM Model: This model is based on the LSTM architecture.
2. XGB Model: This model utilizes the XGBoost algorithm and incorporates static covariates.
3. TFT Model: This model is based on the Transformer architecture and uses quantile regression for likelihood modeling.
4. TCN Model: This model utilizes Temporal Convolutional Neural Networks, neural network architecture adopted for better Time Series Foreacasting

## Results

The performance of each model is evaluated using the MAPE metric. The results are as follows:

- LSTM Model: MAPE = 3.06
- XGB Model: MAPE = 2.82
- TFT Model: MAPE = 2.31
- TCN Model: MAPE = 2.60


Based on these results, the use of various machine learning techniques in conjunction with appropriate covariate data can help us reasonably forecast gold prices while also providing evidence of a fundamental link between the demand for gold and the global economic and geopolitical situations allowing for better investment decisions.

## Credits

The following resources were used in the making of this project:
- [Darts](https://unit8.com/resources/darts-time-series-made-easy-in-python/)
- [SKLear](https://scikit-learn.org/stable/)
- [Pandas](https://pandas.pydata.org)
- [Numpy](https://numpy.org)
- [Matplotlib](https://matplotlib.org)
- [Seaborn](https://seaborn.pydata.org)

Also, I'd like to thank the authors of the following research papers for inspiring and guiding this research:
- Ibrahim Yousef, Esam Shehadeh (2020). The Impact of COVID-19 on Gold Price Volatility, International Journal of Economics and Business Administration Volume VIII Issue 4, 353-364
- Roshan Gautam, Yoochan Kim, Erkan Topal & Michael Hitch (2022) Correlation between COVID-19 cases and gold price fluctuation, International Journal of Mining, Reclamation and Environment, 36:8, 574-586, DOI: 10.1080/17480930.2022.2077542
  
