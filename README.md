# 🌫️ Air Quality Forecasting - PM2.5 Prediction with LSTM

This repository contains my submission for the graded assignment in **Machine Learning Techniques I**, focused on predicting PM2.5 pollution levels in Beijing using Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models.

## 📌 Objective

To forecast PM2.5 air pollution levels using time-series data from weather and air quality sensors, with a goal to achieve a **Root Mean Squared Error (RMSE) < 4000** on the Kaggle leaderboard.

## 📊 Dataset

- `train.csv` – historical data with pollution and weather features
- `test.csv` – test data for forecasting
- `sample_submission.csv` – format for predictions

## 🔧 Preprocessing

- Extracted `hour`, `dayofweek`, and `month` from the datetime column
- Normalized features and target using `MinMaxScaler`
- Generated sequences using sliding window approach (48–72 hours)

## 🤖 Model Architectures Tested

We experimented with four different deep learning architectures:

1. **Simple Bidirectional LSTM** – one BiLSTM layer
2. **Stacked BiLSTM** – deeper LSTM stack
3. **BiLSTM + Dense** – additional dense layers for learning capacity
4. **Deep BiLSTM (Best)** – 3-layer deep Bidirectional LSTM with dropout

## 🏆 Results (Kaggle Scores)

| Architecture         | RMSE         |
|----------------------|--------------|
| Baseline LSTM        | 9,392.93     |
| Simple BiLSTM        | 12,283.78    |
| Stacked BiLSTM       | 13,795.49    |
| BiLSTM + Dense       | 12,646.24    |
| **Deep BiLSTM** ✅   | **10,548.51** |

> While the target RMSE was <4000, our **Deep BiLSTM** was the most effective.

## 📁 Files

- `notebooks/` – all model architectures and experiments
- `submission.csv` – best predictions for Kaggle
- `report.pdf` – detailed analysis and results

## 🚀 Future Work

- Integrate attention mechanisms
- Use external meteorological data
- Try GRU or Transformer models

---

## 📬 Author

**[Steven SHYAKA]** – [s.shyaka1@alustudent.com](mailto:s.shyaka1@alustudent.com)

