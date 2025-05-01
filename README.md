# Gold-Price-Prediction-Model
* Imports Libraries: import necessary libraries: NumPy for numerical operations , Pandas for data manipulation, scikit-learn for model building and evaluation (specifically train_test_split, RandomForestRegressor, and metrics), and pickle for saving the trained model.
 * Loads Data:  load gold price data from the CSV file /content/gld_price_data.csv into a Pandas DataFrame named df.
 * Displays Initial Data: use df.head() to show the first few rows of your DataFrame, giving  a glimpse of the data.
 * Checks for Missing Values: df.isnull().sum() calculates and displays the number of missing values in each column of DataFrame.
 * Drops the 'Date' Column:remove the 'Date' column from the DataFrame using df.drop('Date', axis=1), likely because it's not directly useful for the regression model.
 * Splits Data into Training and Testing Sets:
   *  define your features (x) by dropping the target variable 'GLD' from the DataFrame.
   *  define  target variable (y) as the 'GLD' column.
   * You split your data into training and testing sets using train_test_split with an 80% train and 20% test split (test_size=0.2) and set a random_state of 42 for reproducibility.
 * Trains a Random Forest Regressor Model:
   * create an instance of the RandomForestRegressor called rfr.
   * train the model using your training features (x_train) and training target variable (y_train) with the fit() method.
 * Makes Predictions:  use the trained model (rfr) to make predictions on your test features (x_test) and store these predictions in y_pred.
 * Evaluates the Model: calculate and print the Mean Absolute Error (MAE) and Mean Squared Error (MSE) to assess the performance of your model by comparing the predicted values
