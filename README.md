# Cryptocurrency-Price-Forecasting-using-LSTM

This project uses Long Short-Term Memory (LSTM) networks to forecast Bitcoin (BTC-USD) prices. It leverages over a decade of historical data from Yahoo Finance (`yfinance`) and is deployed via a Flask web app that supports dynamic user interaction and visualizations.

## 📁 Project Structure

```
project-folder/
│
├── templates/
│   ├── index.html              # User input form
│   ├── result.html             # Displays prediction results
|   ├── base.html
│
├── CryptoCurrency(Bitcoin) Price Prediction.ipynb   # Model training notebook
├── README.md                   # Project documentation
├── app.py                      # Flask web application
├── model.keras                 # Trained LSTM model
```

## 📦 Dependencies

- `yfinance`, `pandas`, `numpy`, `matplotlib`
- `scikit-learn`, `keras`, `flask`

Install all dependencies with:

```bash
pip install -r requirements.txt
```

## 🔍 Overview

### 📊 Data Collection & Preprocessing
- Historical BTC-USD data fetched using `yfinance`.
- Applied MinMax scaling.
- Used sliding windows to convert time series into supervised learning format.

### 🧠 Model Training
- Deep LSTM model with:
  - 2 LSTM layers (128 & 64 units)
  - Dense output layer
- Trained using Adam optimizer & Mean Squared Error loss.
- Achieved over 85% prediction accuracy on test data.

### 🌐 Web Application (Flask)
- User inputs: stock symbol (default: BTC-USD) & prediction window (1–10 days).
- Displays:
  - Current vs predicted trend (dynamic plot using Matplotlib)
  - Future price forecast

### 📈 Dynamic Visualizations
- Matplotlib is used for real-time plotting of price trends and predictions.
- Visual comparison of actual vs forecasted values.

## 🚀 How to Run

### Step 1: Clone the repository
```bash
git clone https://github.com/ssarthak0/Cryptocurrency-Price-Forecasting-using-LSTM
cd Cryptocurrency-Price-Forecasting-using-LSTM
```

### Step 2: Install dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Launch the Flask app
```bash
python app.py
```

Then go to `http://127.0.0.1:5000/` in your browser.

## ⚙️ Model Architecture Summary

- LSTM(128, return_sequences=True) → LSTM(64) → Dense(1)
- Optimizer: Adam
- Loss: Mean Squared Error (MSE)

## 📊 Performance

- Low RMSE indicating reliable forecasts.
- Plots show strong correlation between predicted and actual values.

## 📄 License

MIT License – see `LICENSE` file for details.
