# Gold Price Volatility Prediction in Vietnam

This repository contains a time series forecasting project that aims to predict gold price volatility using a hybrid LSTM-GARCH model. The model combines deep learning (LSTM) and econometrics (GARCH) to improve forecasting accuracy. Data preprocessing, model training, evaluation, and results visualization are all included.

## Project Overview

Gold is a crucial asset class in Vietnam for both investment and savings. Accurately forecasting its **volatility** helps investors manage risk and make informed decisions.

In this project:
- GARCH(1,1) is used to model traditional volatility patterns.
- LSTM is trained on both raw and GARCH-derived features.
- The combination enhances prediction accuracy, especially during high-volatility periods.

---

## 🧠 Model Architecture

- **GARCH(1,1)**: Captures volatility clustering in return series.
- **LSTM**: Learns temporal dependencies in volatility.
- **LSTM-GARCH Hybrid**: Uses GARCH forecast as input to LSTM.

---

## 📊 Key Results

| Model           | MSE      | RMSE     |
|----------------|----------|----------|
| GARCH          | 0.00056  | 0.0237   |
| LSTM           | 0.00042  | 0.0205   |
| **LSTM-GARCH** | **0.00031**  | **0.0176**   |

✅ Hybrid model reduced RMSE by ~26% compared to standalone LSTM.

---

## 📁 Project Structure

