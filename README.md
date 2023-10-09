# task-2a
Stock-price prediction
Fetch historical stock price data from Yahoo Finance. The yf.download() function is used to download the closing price for the specified company symbol and date range.
Preprocess the data. The data is first scaled to the range [0, 1] using the MinMaxScaler class from scikit-learn. This is done to make the data easier to train the model on.
Split the data into training and testing sets. The data is split into two sets: a training set and a testing set. The training set is used to train the model, and the testing set is used to evaluate the performance of the model on unseen data.
Create sequences for training and testing. The data is converted into sequences of the specified length. This is done so that the LSTM model can learn the long-term dependencies in the data.
Build the LSTM model. The LSTM model is built using the Sequential class from TensorFlow. The model has two layers: an LSTM layer with 50 units and a dense layer with 1 unit. The dense layer outputs the predicted stock price.
Train the model. The model is trained on the training data using the fit() function. The model is trained for 50 epochs using a batch size of 32.
Make predictions. The model is used to make predictions on the testing data using the predict() function.
Inverse transform the predictions and actual prices to their original scale. The predictions and actual prices are inverse transformed to their original scale using the inverse_transform() function.
Calculate Mean Squared Error. The Mean Squared Error (MSE) is calculated between the predicted prices and the actual prices. The MSE is a measure of how well the model fits the data.
Visualize the results. The predicted prices and actual prices are plotted on a graph.
