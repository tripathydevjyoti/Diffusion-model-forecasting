# 📉 Diffusion-model-forecasting

## 📈 Stock Price Forecasting using ARIMA and Diffusion Models

This project presents a comparative analysis of classical ARIMA models and modern Denoising Diffusion Probabilistic Models (DDPMs) for forecasting daily stock prices across multiple economic sectors. We focus on five major companies—**Microsoft, JPMorgan Chase, ExxonMobil, Caterpillar, and Procter & Gamble**—to capture a wide range of volatility and sector-specific dynamics.

---

### 🔍 What the Code Does

- Collects and preprocesses five years of daily closing prices from Stooq.
- Implements **ARIMA** models per stock using `pmdarima.auto_arima()` with optimal parameters selected via AIC.
- Builds a **multivariate diffusion model** using a simple U-Net + LSTM-based DDPM architecture trained on sliding windows of normalized stock data.
- Evaluates both models using standard forecasting metrics:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
- Generates probabilistic forecasts with uncertainty intervals using Monte Carlo sampling from the diffusion model.

---

### 📊 Key Results

- **ARIMA** models perform well in capturing overall price trends, especially for stocks with low complexity.
- The **diffusion model** shows mixed performance:
  - Performs poorly for highly volatile/noisy stocks.
  - Excels when the data has **moderate non-linearity** and **strong signal-to-noise ratios** (e.g., ExxonMobil and Procter & Gamble).
- Diagnostics reveal diffusion models are sensitive to volatility and non-linearity, but show potential for capturing richer dynamics.

---

### 💡 Why It Matters

- Demonstrates the limitations of classical models like ARIMA in modern financial forecasting.
- Shows that **even simplified diffusion models** can learn meaningful structure in certain market regimes.
- Encourages further development of **probabilistic deep generative models** for real-world time series forecasting.

---

### 📁 Files

- `diff_stock_forecast.ipynb`: Full implementation of ARIMA and diffusion-based forecasting pipelines.
- `CMSC_678_Final_Project_Report.pdf`: Full technical report detailing methods, diagnostics, results, and future directions.
