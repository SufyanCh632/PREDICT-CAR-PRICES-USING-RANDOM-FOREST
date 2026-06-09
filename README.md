# PREDICT-CAR-PRICES-USING-RANDOM-FOREST

## Overview

This project builds a **Car Price Prediction System** using **Python** and **Machine Learning**. The model uses a **Random Forest Regressor** to predict the price of a car based on features such as make, model, year, and mileage.

The dataset is first converted into a Pandas DataFrame, categorical features are encoded using one-hot encoding, and then the model is trained and evaluated.

---

## Features

* Loads car data into a Pandas DataFrame.
* Converts categorical data into numerical format using One-Hot Encoding.
* Splits data into training and testing sets.
* Trains a Random Forest Regression model.
* Predicts car prices.
* Evaluates model performance using:

  * Mean Squared Error (MSE)
  * R² Score

---

## Technologies Used

* Python
* Pandas
* Scikit-learn

---

## Required Libraries

Install the required libraries using:

```bash
pip install pandas scikit-learn
```

---

## Project Structure

```text
car-price-prediction/
│
├── car_price_prediction.py
├── README.md
└── dataset.csv (optional)
```

---

## Dataset

Sample dataset fields:

| Column  | Description                 |
| ------- | --------------------------- |
| make    | Car manufacturer            |
| model   | Car model                   |
| year    | Manufacturing year          |
| mileage | Distance driven             |
| price   | Car price (target variable) |

Example:

```python
{
    'make': 'Toyota',
    'model': 'Corolla',
    'year': 2015,
    'mileage': 50000,
    'price': 15000
}
```

---

## How It Works

### 1. Load Data

The dataset is loaded into a Pandas DataFrame.

```python
df = pd.DataFrame(data)
```

### 2. Encode Categorical Features

```python
df_encoded = pd.get_dummies(df, columns=['make', 'model'])
```

### 3. Split Data

```python
train_test_split(X, y, test_size=0.2, random_state=42)
```

### 4. Train Model

```python
model = RandomForestRegressor(
    n_estimators=100,
    random_state=42
)
```

### 5. Make Predictions

```python
y_pred = model.predict(X_test)
```

### 6. Evaluate Model

```python
mean_squared_error(y_test, y_pred)
r2_score(y_test, y_pred)
```

---

## Sample Output

```text
Dataset:
      make     model  year  mileage  price
0   Toyota  Corolla  2015    50000  15000
1    Honda    Civic  2017    30000  17000
...

Mean Squared Error: 1250000.0
R-Squared Error: 0.92
```

*(Results may vary because of dataset size and randomness.)*

---

## Future Improvements

* Use a larger real-world dataset.
* Add more features such as:

  * Fuel Type
  * Transmission
  * Engine Size
  * Condition
* Hyperparameter tuning.
* Deploy as a web application using Flask or Django.
* Create a user-friendly interface.

---

## Author

**Muhammad Suffiyan Rafi**
Computer Science Student | Python & Machine Learning Enthusiast

---

## License

This project is open-source and available for educational purposes.
