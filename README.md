📈 Stock Price Prediction using LSTM
This project uses Long Short-Term Memory (LSTM) networks to predict stock prices based on historical data. It fetches stock price data using yfinance, preprocesses it, and trains an LSTM model to predict future prices.

🚀 Features
✅ Fetches stock data using Yahoo Finance (yfinance)
✅ Preprocesses data with log transformation and MinMax scaling
✅ Creates time-series sequences for LSTM training
✅ Trains and saves an LSTM model, reloading it if already trained
✅ Evaluates model accuracy using Mean Absolute Percentage Error (MAPE)
✅ Tunes TIME_STEPS (from 10 to 90) to find the best window size for predictions
✅ Plots actual vs. predicted prices for visualization

🛠️ Installation
1️⃣ Install Dependencies
Run the following command to install required Python libraries:

bash
Copy
Edit
pip install numpy pandas matplotlib yfinance scikit-learn tensorflow
2️⃣ Run the script
bash
Copy
Edit
python stock_prediction.py
You'll be prompted to enter a stock ticker (e.g., ^NSEI for NIFTY).

📊 How It Works
1️⃣ Data Collection

Fetches 10 years of stock data using yfinance
Uses closing prices for analysis
2️⃣ Preprocessing

Converts closing prices using log transformation
Scales data between 0 and 1 using MinMaxScaler
Splits data into training (75%), validation (15%), and test (10%)
3️⃣ Training

Uses a stacked LSTM model (3 LSTM layers + Dropout for regularization)
Implements EarlyStopping to prevent overfitting
Saves the trained model (stock_lstm_model.h5)
4️⃣ Evaluation

Predicts stock prices on train, validation, and test sets
Inverse transforms predictions to original scale
Calculates MAPE (Mean Absolute Percentage Error) for accuracy
5️⃣ Hyperparameter Tuning

Loops through TIME_STEPS values (10-90)
Finds the best time window for price prediction
Plots actual vs. predicted stock prices
📈 Results
The script outputs:
✅ Train, Validation, and Test Accuracy
✅ MAPE for error measurement
✅ Best TIME_STEPS value based on accuracy
✅ Graphs comparing actual vs. predicted price
