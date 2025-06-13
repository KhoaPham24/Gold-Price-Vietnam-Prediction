# Gold Price Volatility Prediction in Vietnam

This repository contains a time series forecasting project that aims to predict gold price volatility using a hybrid LSTM-GARCH model. The model combines deep learning (LSTM) and econometrics (GARCH) to improve forecasting accuracy. Data preprocessing, model training, evaluation, and results visualization are all included.

## Background

Gold is widely traded and held in Vietnam as a store of value. Understanding its **volatility** is critical for investors, policymakers, and risk managers. While **GARCH** models effectively capture volatility clustering, they struggle with nonlinear patterns. **LSTM** networks, on the other hand, handle complex temporal dependencies well but lack statistical interpretability. By combining both in a **hybrid LSTM-GARCH** model, this project leverages the strengths of each to improve forecasting accuracy and robustness during volatile market conditions.

## Objective

Our objective is to validate the effectiveness of both standalone and hybrid models in forecasting gold price volatility in Vietnam. To achieve this, we conduct a comprehensive analysis using historical gold price data, which includes features such as date, closing price, and log returns. Leveraging this dataset, we design a series of experiments to evaluate the performance of different models, including GARCH, LSTM, and the proposed LSTM-GARCH hybrid. By comparing the results across these models, we aim to identify the most reliable and accurate approach for volatility forecasting in the Vietnamese gold market.

---

## Framework

![image](https://github.com/user-attachments/assets/7dd8a1ad-a726-469e-bd19-12b6061edae8)

*The following diagram illustrates the overall architecture of our forecasting framework, including **GARCH, LSTM, LSTM-GARCH** models*

## 📊 Results

The research project accomplished the development and evaluation of diverse models for gold price volatility forecasting, encompassing both individual models (GARCH, LSTM) and a hybrid model (LSTM-GARCH). These models were rigorously assessed using key evaluation metrics such as MSE and RMSE. Notably, the hybrid LSTM-GARCH model exhibited improved forecasting accuracy compared to traditional approaches, especially during periods of heightened market volatility. This outcome highlights the potential effectiveness of integrating statistical and deep learning methods to enhance the precision and reliability of volatility prediction in financial markets.

| Model       | MAE       | MAPE       | RMSE       |
|-------------|-----------|------------|------------|
| GARCH       | 0.005594  | 0.355746   | 0.008361   |
| LSTM        | 0.003177  | 0.254695   | 0.003981   |
| **LSTM-GARCH** | **0.002177*** | **0.165544*** | **0.003226*** |

## 🔧 Requirements

- Python ≥ 3.8  
- numpy  
- pandas  
- keras  
- tensorflow  
- arch  
- matplotlib  
- scikit-learn

Install all dependencies:
```bash
pip install -r requirements.txt
🚀 Usage
bash
Copy
Edit
# Step 1: Run GARCH model to extract volatility
python garch_model.py

# Step 2: Train LSTM model
python lstm_model.py

# Step 3: Combine GARCH output with LSTM (Hybrid)
python hybrid_model.py

# Optional: Visualize results
python plot_results.py
