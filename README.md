# Time Series Forecasting Benchmark

This repository presents a consolidated benchmarking study comparing classical, machine learning, and deep learning models for time-series forecasting under limited data conditions.

## Models Evaluated
- ARIMA (statistical baseline)
- XGBoost (tree-based regression with lag features)
- LSTM (recurrent neural network)
- Transformer (attention-based deep learning model)

## Methodology
- Time-series data is split into training, validation, and test sets.
- Hyperparameter tuning is performed for LSTM and Transformer models using validation RMSE.
- Final evaluation is conducted on a held-out test set using RMSE as the primary metric.
- The best-performing model is used for long-horizon forecasting.

## Key Findings
- Deep learning models outperform traditional approaches on this dataset.
- LSTM achieves the lowest test RMSE, showing better generalisation in low-data settings.
- Transformer performs well during validation but shows mild overfitting on the test set.

## Notes
- Results should be interpreted with caution due to the small test size.
- Long-horizon forecasts are generated using a recursive strategy, which may accumulate error.

## Requirements
- Python 3.x
- NumPy
- Pandas
- Scikit-learn
- Statsmodels
- PyTorch
- XGBoost

## Usage
Run the notebook sequentially to reproduce preprocessing, model training, evaluation, and forecasting results.
