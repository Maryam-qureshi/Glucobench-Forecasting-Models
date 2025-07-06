<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
</head>
<body>

<h1>🩺 GlucoBench Forecasting Models</h1>

<p>This project implements time series forecasting models using the <a href="https://openreview.net/forum?id=xSpf1l72gX">GlucoBench</a> benchmark dataset for personalized blood glucose prediction. It focuses on understanding and reproducing forecasting architectures under standardized data preprocessing and evaluation metrics.</p>

<hr>

<h2>📌 Project Overview</h2>
<p>The objective is to forecast patient-specific glucose levels using a wide range of models, from statistical to deep learning approaches, and evaluate them under:</p>
<ul>
  <li><strong>In-Distribution (ID)</strong> scenarios</li>
  <li><strong>Out-of-Distribution (OOD)</strong> generalization</li>
</ul>

<hr>

<h2>📊 Key Components</h2>

<h3>✅ Data Preprocessing</h3>
<ul>
  <li>Based on <code>DataFormatter</code> (in <code>data_formatter/base.py</code>)</li>
  <li>Handles:
    <ul>
      <li>Column configuration</li>
      <li>NA handling</li>
      <li>Interpolation</li>
      <li>Scaling</li>
      <li>Splitting into train/val/test/OOD</li>
    </ul>
  </li>
  <li>Configured via YAML files (in <code>config/</code>)</li>
</ul>

<h3>✅ Models Implemented</h3>
<p>Located in <code>lib/</code>:</p>
<ul>
  <li><code>arima.py</code>: ARIMA using <code>statsforecast</code></li>
  <li><code>linreg.py</code>: Linear Regression using <code>darts</code></li>
  <li><code>transformer.py</code>: Transformer model</li>
  <li><code>tft.py</code>: Temporal Fusion Transformer</li>
  <li><code>latentode.py</code>: Latent ODE</li>
  <li><code>gluformer.py</code>: Gluformer model</li>
  <li><code>nhits.py</code>: N-HiTS model</li>
  <li><code>xgbtree.py</code>: XGBoost regression</li>
</ul>

<h3>✅ Evaluation</h3>
<ul>
  <li><strong>Metrics:</strong>
    <ul>
      <li>MSE (Mean Squared Error)</li>
      <li>MAE (Mean Absolute Error)</li>
    </ul>
  </li>
  <li>Results reported for ID and OOD separately</li>
  <li>Logs saved in <code>output/</code> directory</li>
</ul>

<hr>


