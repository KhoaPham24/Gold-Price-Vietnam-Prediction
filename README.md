# Gold Price Volatility Prediction in Vietnam

This repository contains a time series forecasting project that aims to predict gold price volatility using a hybrid LSTM-GARCH model. The model combines deep learning (LSTM) and econometrics (GARCH) to improve forecasting accuracy. Data preprocessing, model training, evaluation, and results visualization are all included.

## Background

Gold is widely traded and held in Vietnam as a store of value. Understanding its **volatility** is critical for investors, policymakers, and risk managers. While **GARCH** models effectively capture volatility clustering, they struggle with nonlinear patterns. **LSTM** networks, on the other hand, handle complex temporal dependencies well but lack statistical interpretability. By combining both in a **hybrid LSTM-GARCH** model, this project leverages the strengths of each to improve forecasting accuracy and robustness during volatile market conditions.

## Objective

Our objective is to validate the effectiveness of both standalone and hybrid models in forecasting gold price volatility in Vietnam. To achieve this, we conduct a comprehensive analysis using historical gold price data, which includes features such as date, closing price, and log returns. Leveraging this dataset, we design a series of experiments to evaluate the performance of different models, including GARCH, LSTM, and the proposed LSTM-GARCH hybrid. By comparing the results across these models, we aim to identify the most reliable and accurate approach for volatility forecasting in the Vietnamese gold market.

---

## Framework

![image](https://github.com/user-attachments/assets/82d82349-53d7-4143-912c-3783ddd04ab3)

*The following diagram illustrates the overall architecture of our forecasting framework, including **GARCH, LSTM, LSTM-GARCH** models*

## Results
![image](https://github.com/user-attachments/assets/1fc070fa-1db0-4157-83f9-21ff14426d1c)
*Garch Prediction*

![image](https://github.com/user-attachments/assets/6b80749a-21ce-4dfa-9d05-00dab6a4e415)
*LSTM Prediction*

![image](https://github.com/user-attachments/assets/c9a75d14-23d3-4566-83e2-173a60a54936)
*LSTM-GARCH Prediction*
The research project accomplished the development and evaluation of diverse models for gold price volatility forecasting, encompassing both individual models (GARCH, LSTM) and a hybrid model (LSTM-GARCH). These models were rigorously assessed using key evaluation metrics such as MSE and RMSE. Notably, the hybrid LSTM-GARCH model exhibited improved forecasting accuracy compared to traditional approaches, especially during periods of heightened market volatility. This outcome highlights the potential effectiveness of integrating statistical and deep learning methods to enhance the precision and reliability of volatility prediction in financial markets.

| Model       | MAE       | MAPE       | RMSE       |
|-------------|-----------|------------|------------|
| GARCH       | 0.005594  | 0.355746   | 0.008361   |
| LSTM        | 0.003177  | 0.254695   | 0.003981   |
| **LSTM-GARCH** | **0.002177*** | **0.165544*** | **0.003226*** |

## Requirements
Ensure that you have **Python 3.8** or higher installed, then install the required Python packages: 
```bibtex
# Data manipulation and computation
pandas==1.5.0
numpy==1.25.0

# Plotting
matplotlib==3.7.0

# Machine Learning
scikit-learn==1.2.0

# Deep Learning Framework
tensorflow==2.11.0  # This package includes Keras as well

# For volatility models in finance
arch==5.5.0

# Hyperparameter tuning for Keras models
keras_tuner==1.1.3
```

## Citation
```bibtex
@article{roszyk2024hybrid,
  author={Natalia Roszyk and Robert Ślepaczuk},
  title={The Hybrid Forecast of S&P 500 Volatility ensembled from VIX, GARCH and LSTM models},
  journal={arXiv preprint arXiv:2407.16780},
  year={2024}
}
