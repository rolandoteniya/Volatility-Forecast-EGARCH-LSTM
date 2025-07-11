# Hybrid EGARCH-LSTM for S&P 500 Volatility Forecasting

A project to forecast daily realised volatility of the S&P 500 index using a hybrid econometric-neural network model. This repository contains the code and analysis for my MSc Data Science & AI dissertation at the University of Liverpool.

## Aim

The primary aim is to develop and evaluate a hybrid EGARCH-LSTM model to achieve a higher level of forecasting accuracy than standalone GARCH or LSTM models, targeting an 18% reduction in RMSE over benchmarks.

## Methodology

1.  **Data Acquisition:** S&P 500 and VIX data are downloaded using the `yfinance` library.
2.  **Econometric Modelling:** A "bake-off" of GARCH-family models is conducted to select the best component for capturing volatility clustering and leverage effects.
3.  **Hybrid Model Construction:** An LSTM is trained on the residuals from the winning EGARCH model and VIX data as an exogenous feature.
4.  **Evaluation:** The model's performance is validated on an unseen test set. Statistical significance is tested with the Diebold-Mariano test and model predictions are interpreted using SHAP.

## How to Run

1.  Clone the repository: `git clone https://github.com/rolandoteniya/Volatility-Forecasting-EGARCH-LSTM.git`
2.  Install dependencies: `pip install -r requirements.txt`
3.  Run the main analysis notebook: `/notebooks/your_notebook_name.ipynb`