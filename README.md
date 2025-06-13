# Gold Price Volatility Prediction in Vietnam

This repository contains a time series forecasting project that aims to predict gold price volatility using a hybrid LSTM-GARCH model. The model combines deep learning (LSTM) and econometrics (GARCH) to improve forecasting accuracy. Data preprocessing, model training, evaluation, and results visualization are all included.

## Background

Gold is widely traded and held in Vietnam as a store of value. Understanding its **volatility** is critical for investors, policymakers, and risk managers. While **GARCH** models effectively capture volatility clustering, they struggle with nonlinear patterns. **LSTM** networks, on the other hand, handle complex temporal dependencies well but lack statistical interpretability. By combining both in a **hybrid LSTM-GARCH** model, this project leverages the strengths of each to improve forecasting accuracy and robustness during volatile market conditions.

## Objective

Our objective is to validate the effectiveness of both standalone and hybrid models in forecasting gold price volatility in Vietnam. To achieve this, we conduct a comprehensive analysis using historical gold price data, which includes features such as date, closing price, and log returns. Leveraging this dataset, we design a series of experiments to evaluate the performance of different models, including GARCH, LSTM, and the proposed LSTM-GARCH hybrid. By comparing the results across these models, we aim to identify the most reliable and accurate approach for volatility forecasting in the Vietnamese gold market.

---

## Framework
![image](https://github.com/user-attachments/assets/f2279d38-095a-4344-bf0c-2fcecd4ecc28)

### 1. **Data Preparation**
- Daily gold price data in Vietnam
- Log returns computed
- Data scaled using `MinMaxScaler`

### 2. **Models**
- **GARCH(1,1)** using `arch` library to model volatility clusters.
- **LSTM** using Keras to model sequences of past volatility.
- **Hybrid LSTM-GARCH** where GARCH forecasts are fed as features into LSTM.

### 3. **Validation**
- Walk-forward (rolling) prediction
- `EarlyStopping` and `Adam` optimizer for LSTM

---

## 📊 Results

| Model           | MSE      | RMSE     |
|----------------|----------|----------|
| GARCH          | 0.00056  | 0.0237   |
| LSTM           | 0.00042  | 0.0205   |
| **LSTM-GARCH** | **0.00031**  | **0.0176**   |

✅ **LSTM-GARCH** outperforms both standalone models by reducing RMSE by ~26%.

- Strong performance during turbulent periods (e.g., 2021 COVID, 2024 inflation shock)
- Better generalization observed in walk-forward testing

---

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
