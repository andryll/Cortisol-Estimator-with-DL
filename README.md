# Cortisol Estimator with Deep Learning

This repository contains the source code and experiments for the automatic estimation of cortisol levels using Time Series Regression models. The project evaluates the performance of different architectures on mass spectrometry data, comparing a baseline model against state-of-the-art neural networks.

## 📄 Overview

The goal of this project is to quantify cortisol levels based on time series data. We implemented and compared three specific models:

1.  **Rocket** (Baseline): A convolution-based model using random kernels.
2.  **FCN** (Fully Convolutional Network): A standard neural network for time series.
3.  **InceptionTime** (State-of-the-art): A deep learning ensemble based on the Inception architecture.

## 🛠️ Technologies & Libraries

This project was built using Python and the **Aeon** library for time series learning.

* [Aeon](https://github.com/aeon-toolkit/aeon)
* NumPy & Pandas
* Scikit-learn
* PyTorch / TensorFlow (depending on the Aeon backend used)

## 🚀 Installation

1.  Clone this repository:
    ```bash
    git clone [https://github.com/andryll/Cortisol-Estimator-with-DL.git](https://github.com/andryll/Cortisol-Estimator-with-DL.git)
    cd Cortisol-Estimator-with-DL
    ```

2.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: Ensure you have `aeon` installed)*

## 📊 Results Summary

The models were evaluated using MSE, RMSE, and Median Error. We also analyzed regulatory compliance based on **ANVISA Resolution RDC No. 27/2012** (acceptable error margin of ±15%).

| Model | RMSE | Median Error | Compliance (RDC 27) |
|-------|------|--------------|---------------------|
| **Rocket** | **8.52** | 28.19 | 27.70% |
| **FCN** | 10.77 | 29.81 | 32.43% |
| **InceptionTime**| 9.21 | **15.95** | **35.14%** |

While **Rocket** achieved the lowest RMSE, **InceptionTime** showed better stability (lower median error) and the highest compliance rate with health regulations.

## 📂 Project Structure

* `data/`: Dataset used for training and testing (if public).
* `notebooks/`: Jupyter notebooks with EDA and training loops.
* `models/`: Saved weights for FCN and InceptionTime.
* `src/`: Utility scripts for data preprocessing and evaluation.

## 📜 Citation

If you use this code or findings in your research, please cite:

> [Your Name/Authors]. "Automatic Cortisol Quantification using Time Series Deep Learning Models." [Year].

## ⚖️ License

Distributed under the MIT License. See `LICENSE` for more information.
