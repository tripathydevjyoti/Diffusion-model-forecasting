# Diffusion-model-forecasting

📈 Stock Price Forecasting using ARIMA and Diffusion Models

This project presents a comparative analysis of classical ARIMA models and modern Denoising Diffusion Probabilistic Models (DDPMs) for forecasting daily stock prices across multiple economic sectors. We focus on five major companies—Microsoft, JPMorgan Chase, ExxonMobil, Caterpillar, and Procter & Gamble—to capture a wide range of volatility and sector-specific dynamics.

🔍 What the Code Does
Collects and preprocesses five years of daily closing prices from Stooq.
Implements ARIMA models per stock using pmdarima.auto_arima() with optimal parameters selected via AIC.
Builds a multivariate diffusion model using a simple U-Net + LSTM-based DDPM architecture trained on sliding windows of normalized stock data.
Evaluates both models using standard forecasting metrics: Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
Generates probabilistic forecasts with uncertainty intervals using Monte Carlo sampling from the diffusion model.
📊 Key Results
ARIMA models perform well in capturing overall price trends, especially for stocks with low complexity.
The diffusion model shows mixed performance: it struggles with highly volatile or noisy data but excels in scenarios with moderate non-linearity and strong signal-to-noise ratios (e.g., ExxonMobil and Procter & Gamble).
Diagnostics reveal that diffusion models are sensitive to volatility and non-linearity, highlighting their potential in capturing richer dynamics where traditional models fall short.
💡 Why It Matters
Demonstrates the limitations of classical models like ARIMA in modern financial forecasting tasks.
Validates that even simplified diffusion models can learn meaningful patterns in specific market regimes.
Paves the way for incorporating probabilistic deep generative models into financial forecasting pipelines, especially in environments with complex, non-linear structure.
📁 Files
diff_stock_forecast.ipynb: Contains full implementation of ARIMA and diffusion-based forecasting pipelines.
Project_Report.pdf: Full technical report detailing methods, diagnostics, results, and future directions.
