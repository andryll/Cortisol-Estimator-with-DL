# Cortisol Estimator with Deep Learning

This repository contains the source code and experiments for the automatic estimation of cortisol levels using Time Series Regression models. The project evaluates the performance of different architectures on mass spectrometry data, comparing a baseline model against state-of-the-art neural networks.

##  Overview

The goal of this project is to quantify cortisol levels based on time series data. We implemented and compared three specific models:

1.  **Rocket**: A convolution-based model using random kernels.
2.  **FCN**: A standard neural network for time series.
3.  **InceptionTime**: A deep learning ensemble based on the Inception architecture.

## Results Summary

The models were evaluated using MSE, RMSE, and Median Error. We also analyzed regulatory compliance based on **ANVISA Resolution RDC No. 27/2012** (acceptable error margin of ±15%).

| Model | RMSE | Median Error | Compliance (RDC 27) |
|-------|------|--------------|---------------------|
| **Rocket** | **8.52** | 28.19 | 27.70% |
| **FCN** | 10.77 | 29.81 | 32.43% |
| **InceptionTime**| 9.21 | **15.95** | **35.14%** |
