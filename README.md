# Traffic-Flow-Prediction
## 🚦 NYC Traffic Volume Prediction 🗽

This project demonstrates a deep learning approach to predict traffic volumes in NYC using a dataset spanning 2006-2008. It includes data preprocessing, manual implementation of an LSTM network, and comparisons with built-in LSTM and MLP models. The manual LSTM showcases a custom implementation of gates and state transitions, offering a foundational understanding of recurrent neural networks.

***

## 📂 Project Structure

#### Data Preprocessing
Parsed raw traffic data to create a time-indexed dataset.
Resampled and interpolated missing values for 15-minute intervals.
Engineered features like Weekday, Hour, Is_Weekend, and traffic volume transformations (Vol_log, Vol_diff).

#### Manual LSTM Implementation
Developed a custom LSTM using matrix multiplications, activation functions (sigmoid, tanh), and weight initializations (Xavier/Glorot uniform).
Designed and trained the LSTM model for regression to predict traffic volumes.

#### Comparative Models
Built and trained an in-built LSTM model using TensorFlow.
Compared performance metrics like MAE, RMSE, and accuracy between the manual and built-in models.

#### Visualization
Plotted training/validation loss and MAE over epochs.
Compared actual vs. predicted traffic volumes using graphical representations.

*** 

## 🛠 Features & Workflow
#### 1. Dataset Information
The dataset contains traffic volume (Vol) recorded for specific NYC segments over three years.
Features include Datetime, SegmentID, Direction, Vol, and more.
#### 2. Preprocessing
Resampling: Aggregated traffic volume to 15-minute intervals.
Feature Engineering: Added temporal features like Hour, Weekday, and Is_Weekend.
Transformation: Applied log transformation for better feature scaling.
Normalization: MinMaxScaler was used to scale the features.
#### 3. Manual LSTM
Fully custom implementation of LSTM gates and states:
Forget Gate: Controls what information to discard.
Input Gate: Decides what new information to store.
Output Gate: Determines the next hidden state.
Integrated Xavier initialization for weight matrices and zero initialization for biases.
#### 4. Evaluation Metrics
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
Model Accuracy
#### 5. Comparisons
Benchmarked the manual LSTM model against TensorFlow’s built-in LSTM.
