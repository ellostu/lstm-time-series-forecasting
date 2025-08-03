# LSTM Time Series Forecasting on Cloud Infrastructure Metrics

This project demonstrates an end-to-end pipeline for time series forecasting using LSTM (Long Short-Term Memory) models. It is based on real-world cloud infrastructure data, containing high-frequency metrics from containerized services.

> 🎯 **Objective**: Predict service request patterns and resource usage trends in a cloud-native environment using deep learning.

---

## 🔍 Overview

In modern Cloud and AI/ML systems, predictive analytics is crucial for autoscaling, anomaly detection, and reliability. This project simulates such a use case using open-source data from [SIR Lab's data-release](https://github.com/sir-lab/data-release), applying advanced time series preprocessing and deep learning modeling.

---

## 🧠 Skills Demonstrated

### 📊 Data Manipulation & Preprocessing
- Merged multiple CSV files from a directory into a single DataFrame using `pandas`
- Handled missing data and NaNs (`fillna`)
- Renamed and dropped unnecessary columns
- Created meaningful datetime indices from raw `day` and `time` columns

### 🛠️ Feature Engineering for Time Series
- Created time-based input/output sequences using a sliding window (`create_sequences`)
- Applied MinMax scaling without data leakage (fit only on training)
- Built supervised learning data for LSTM using `look_back_window` and `forecast_horizon`

### 📈 Exploratory Data Analysis (EDA)
- Interpreted series structure (rows = time, columns = metrics)
- Detected daily seasonal patterns and upward trends in service requests
- Correctly interpreted NaNs as time periods with 0 requests

### 🤖 Deep Learning Modeling
- Built an LSTM model using `Keras` (`Sequential`, `LSTM`, `Dropout`, `Dense`)
- Configured proper `input_shape` for sequential data
- Used `mean_squared_error` loss and `adam` optimizer
- Trained and validated model chronologically (time-aware split)

### 📉 Evaluation & Forecasting
- Used `model.evaluate()` to assess training and validation performance
- Visualized predicted vs actual series values for multiple metrics
- Analyzed `model.summary()` and total trainable parameters

---

## 📷 Forecasting Example

<img width="1544" height="584" alt="image" src="https://github.com/user-attachments/assets/63da122e-3fff-40fa-9f84-220c0a4f04a8" />

<img width="1546" height="606" alt="image" src="https://github.com/user-attachments/assets/d1d2d441-026f-454e-b4d3-a3e668b5f7f7" />

---

## 📦 Dataset

Data was obtained from:  
**[SIR Lab – data-release repository](https://github.com/sir-lab/data-release)**  
The dataset includes minute-level logs of resource usage and service requests across pods and containers in a simulated cloud environment.

---

## 🚀 How to Run

```bash
# Create a virtual environment
python -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook lstm_time_series_forecasting.ipynb
