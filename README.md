# LinearRegression_StockPrediction_Research
LQ45 Stock Price Prediction — LR vs SVR vs XGBoost

This repository contains the full dataset, code, and output for the research paper "Machine Learning-Based Medium-Term Stock Price Prediction in the Indonesian LQ45 Stock Market: Integrating Moving Average and RSI via Linear Regression."

The study evaluates Linear Regression against SVR and XGBoost for predicting closing prices 14 trading days ahead across all 45 constituent stocks of the LQ45 index on the Indonesia Stock Exchange (IDX), using MA10, MA20, MA50, and RSI14 as engineered features over a 5-year window (2021–2026).

Contents
data/ — OHLC price data for all 45 LQ45 tickers (sourced via yfinance, also published on Kaggle)
notebook/ — full pipeline: data loading, feature engineering, model training, and evaluation
output/ — per-ticker metrics (MAE, RMSE, R²) and generated figures

Method
Data is chronologically split 80/20 (no shuffling) to prevent look-ahead bias. Features are standardized on the training partition only. Linear Regression is compared against SVR (RBF kernel) and XGBoost under identical conditions, with hyperparameters tuned via time-series cross-validation.

Key Finding
Linear Regression outperformed both non-linear models on most tickers, primarily due to its ability to extrapolate beyond the training price range — a capability SVR and XGBoost structurally lack.

Citation
If you use this work, please cite the associated paper (ICIMCIS 2026).

Links
Dataset on Kaggle: OHLC LQ45 Index 2021–2026
