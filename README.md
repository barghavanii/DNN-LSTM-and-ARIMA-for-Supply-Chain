# Supply Chain Optimization and Forecasting Models

This project focuses on optimizing delivery schedules and forecasting monthly freight costs using various machine learning models, including DNN, LSTM, and ARIMA. The project involves extensive feature engineering and feature extraction on both structured and unstructured data.

## Project Structure

1. **Data Preparation**:
   - Feature engineering on structured data such as delivery times, freight costs, and schedules.
   - Feature extraction from unstructured data sources.

2. **Model Development**:
   - **DNN (Dense Neural Network)**: Used for optimizing delivery schedules.
   - **LSTM (Long Short-Term Memory Network)**: Used for forecasting monthly freight costs.
   - **ARIMA (AutoRegressive Integrated Moving Average)**: Used for forecasting monthly freight costs.

3. **Model Evaluation**:
   - Performance metrics such as RMSE (Root Mean Squared Error) are used to evaluate the models.

## Summary of Findings

| **Model** | **Objective**                         | **Target Variable**        | **Model Architecture**          | **Performance Metric** | **Training RMSE** | **Test RMSE**      | **Benchmark RMSE** |
|-----------|---------------------------------------|----------------------------|---------------------------------|------------------------|-------------------|--------------------|--------------------|
| DNN       | Optimize delivery schedules           | Schedule v Actual          | Dense Neural Network (4 layers) | RMSE                   | 20.86             | 22.84              | 29.22            |
| LSTM      | Forecast monthly freight costs        | Freight Cost (USD)         | LSTM Network (1 LSTM layer)     | RMSE                   | 292287.38 | 529783.7       | 861773.48        |
| ARIMA     | Forecast monthly freight costs        | Freight Cost (USD)         | ARIMA (2,1,2)                   | RMSE                   | 323737.57         | 565322.23          | 861773.48        |

### Key Points

- **DNN Model**:
  - **Objective**: To predict the deviation between scheduled and actual delivery times and optimize delivery schedules.
  - **Target Variable**: `Schedule v Actual`
  - **Model Performance**: Achieved a training RMSE of 22.86 and a test RMSE of 25.88. The naive benchmark RMSE was 29.22, indicating significant improvement.
  - **Architecture**: The model consists of four dense layers with ReLU activations.

- **LSTM Model**:
  - **Objective**: To forecast monthly freight costs for better financial planning and budgeting.
  - **Target Variable**: `Freight Cost (USD)`
  - **Model Performance**: Achieved a test RMSE of 529783.70. The naive benchmark RMSE was 861773.48, showing better performance than the naive prediction.
  - **Architecture**: The model includes one LSTM layer followed by a dense layer.

- **ARIMA Model**:
  - **Objective**: To forecast monthly freight costs for better financial planning and budgeting.
  - **Target Variable**: `Freight Cost (USD)`
  - **Model Performance**: Achieved a training RMSE of 323737.57 and a test RMSE of 565322.23. The naive benchmark RMSE was 861773.48, indicating improved performance over the naive prediction.
  - **Architecture**: The model is configured with parameters (2,1,2), denoting two autoregressive terms, one differencing term, and two moving average terms.
 
    
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1aYyGQ3PGG7IGqAmz099KTTstmzyr24lk?usp=sharing)

