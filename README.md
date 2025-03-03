# 🚴 Bike Rental Demand Prediction – A Time Series Approach  

## 📌 Project Overview  
This project focuses on predicting **bike rental demand** using historical data and external factors such as weather, seasonality, and working conditions. The goal is to build a **robust time series model** to help businesses optimize bike availability and improve customer satisfaction.  

We utilize **SARIMAX** and other time series forecasting techniques, ensuring accuracy through rigorous data preprocessing, feature engineering, and hyperparameter tuning.  

---

## 📂 Steps in the Project  

### 1️⃣ Data Import and Initial Exploration  
- The dataset is loaded from `hour.csv`.  
- Initial exploration includes:  
  ✅ Displaying first and last rows  
  ✅ Checking data types  
  ✅ Identifying missing values and duplicates  

### 2️⃣ Data Preprocessing  
- **Handling Missing Values**: Forward fill applied for missing timestamps.  
- **Feature Engineering**:  
  ✅ `datetime` conversion for time-based analysis  
  ✅ Extraction of **hour, day, and season** components  
- **Scaling**: Exogenous variables are standardized using `StandardScaler` for model stability.  

### 3️⃣ Exploratory Data Analysis (EDA)  
- Identified **seasonality, trends, and correlations** in the dataset.  
- Key insights:  
  ✅ Demand peaks in **fall** and dips in **spring**.  
  ✅ **Weather conditions** significantly affect rentals.  
  ✅ **Weekends and holidays** show higher rental activity.  
- **Visualizations**: Heatmaps, time series plots, and distribution graphs provide a deep dive into rental patterns.  

### 4️⃣ Model Training and Evaluation  
The project explores multiple forecasting models:  
🔹 **SARIMA** – Captures seasonality and trends.  
🔹 **SARIMAX** – Includes external weather-related factors.  
🔹 **Exponential Smoothing** – Baseline model for comparison.  

- **Hyperparameter Tuning**:  
  ✅ Grid search for optimal `(p, d, q, P, D, Q, S)` values.  
  ✅ Cross-validation to prevent overfitting.  

- **Model Evaluation Metrics**:  
  📌 **Mean Absolute Error (MAE)**  
  📌 **Mean Squared Error (MSE)**  
  📌 **Root Mean Squared Error (RMSE)**  

### 5️⃣ Forecasting and Results  
- Final model successfully **predicts future bike rentals** while accounting for external factors.  
- Forecasted values are plotted against actual data to **validate accuracy**.  

---

## 🛠️ Libraries Used  
🔹 `pandas`, `numpy` – Data manipulation and numerical operations  
🔹 `statsmodels` – SARIMA & SARIMAX implementation  
🔹 `scikit-learn` – Feature scaling and preprocessing  
🔹 `matplotlib`, `seaborn` – Data visualization  
🔹 `XGBoost` – Used for feature importance analysis  

---

## 🚀 Running the Project Locally  

1️⃣ **Clone the Repository:**  
```sh
git clone https://github.com/yourusername/bike-rental-prediction.git
cd bike-rental-prediction
