# Concrete Strength Prediction Using XGBoost and GridSearchCV

This project demonstrates how to apply **XGBoost Regressor** to predict the strength of concrete based on various material components. It also includes the implementation of **GridSearchCV** to optimize the hyperparameters of the model, ensuring the best possible performance.

## Project Structure

- **data loading**: Reads a CSV file containing concrete composition data with features such as cement, fly ash, water, etc.
- **feature and target split**: Splits the dataset into features (X) and the target variable (y).
- **train-test split**: Divides the dataset into training and testing sets.
- **model definition**: Uses the XGBoost Regressor for regression tasks.
- **hyperparameter tuning**: Utilizes GridSearchCV to perform cross-validated hyperparameter tuning, optimizing for R² and negative root mean squared error.

## Main Components

- **XGBoost Regressor**: A high-performance gradient boosting model.
- **GridSearchCV**: A technique for hyperparameter tuning by testing multiple values across predefined search spaces.
- **Performance Metrics**: The model is optimized using the R² score and root mean squared error (RMSE).

### Hyperparameters Considered

- `n_estimators`: Number of trees in the model (100, 200, 500)
- `max_depth`: Maximum depth of a tree (3, 6, 9)
- `gamma`: Minimum loss reduction required to make a further partition on a leaf node (0.01, 0.1)
- `learning_rate`: Shrinks feature weights to prevent overfitting (0.001, 0.01, 0.1, 1)

### Steps

1. **Data Loading**: Reads the concrete dataset from a CSV file.
2. **Data Preparation**: Splits the data into features and target.
3. **Train-Test Split**: Uses an 80/20 split for training and testing data.
4. **GridSearchCV**: Searches for the best hyperparameter values using 5-fold cross-validation.
5. **Model Evaluation**: Evaluates and prints the best estimator, parameters, and the corresponding score.

## How to Run the Project

1. Clone the repository.
2. Install the required Python packages.
   ```bash
   pip install -r requirements.txt
