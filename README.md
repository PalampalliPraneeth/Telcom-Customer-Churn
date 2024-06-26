# Telcom Customer Churn Prediction

This project aims to predict customer churn using various machine learning models. The dataset used is the Telco Customer Churn dataset, which contains information about customers' demographic and service usage.

## Requirements

The following Python libraries are required to run the code:

- numpy
- pandas
- matplotlib
- seaborn
- tensorflow
- imbalanced-learn
- scikit-learn
- xgboost

You can install these dependencies using pip:

```sh
pip install numpy pandas matplotlib seaborn tensorflow imbalanced-learn scikit-learn xgboost
```

## Dataset

The Telco Customer Churn dataset includes the following columns:

- `customerID`: Unique identifier for each customer
- `gender`: Customer's gender
- `SeniorCitizen`: Whether the customer is a senior citizen (1) or not (0)
- `Partner`: Whether the customer has a partner (Yes, No)
- `Dependents`: Whether the customer has dependents (Yes, No)
- `tenure`: Number of months the customer has stayed with the company
- `PhoneService`: Whether the customer has a phone service (Yes, No)
- `MultipleLines`: Whether the customer has multiple lines (Yes, No, No phone service)
- `InternetService`: Customer's internet service provider (DSL, Fiber optic, No)
- `OnlineSecurity`: Whether the customer has online security service (Yes, No, No internet service)
- `OnlineBackup`: Whether the customer has online backup service (Yes, No, No internet service)
- `DeviceProtection`: Whether the customer has device protection service (Yes, No, No internet service)
- `TechSupport`: Whether the customer has tech support service (Yes, No, No internet service)
- `StreamingTV`: Whether the customer has streaming TV service (Yes, No, No internet service)
- `StreamingMovies`: Whether the customer has streaming movies service (Yes, No, No internet service)
- `Contract`: The contract term of the customer (Month-to-month, One year, Two year)
- `PaperlessBilling`: Whether the customer has paperless billing (Yes, No)
- `PaymentMethod`: The customer's payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
- `MonthlyCharges`: The amount charged to the customer monthly
- `TotalCharges`: The total amount charged to the customer

## Data Preprocessing

1. **Drop `customerID`**: Unique identifier not relevant for modeling.
2. **Convert `TotalCharges` to numeric**: Handle errors, coerce to numeric type.
3. **Handle missing values**: Remove rows with missing `TotalCharges`.
4. **Replace categorical values**: Convert 'No internet service' and 'No phone service' to 'No'.
5. **Convert binary categorical columns**: Convert 'Yes'/'No' columns to 1/0.
6. **One-hot encoding**: Apply to categorical columns like `InternetService`, `Contract`, and `PaymentMethod`.
7. **Normalization**: Scale numerical columns (`tenure`, `MonthlyCharges`, `TotalCharges`).

## Model Training

Models trained for churn prediction:

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- K-Nearest Neighbors
- XGBoost

## Evaluation

Evaluate models using:

- **F1 score**: Harmonic mean of precision and recall.
- **Confusion Matrix**: Summarizes predictions vs. actual values.
- **Classification Report**: Precision, recall, F1-score per class.

## Instructions

1. Install required libraries using `pip install -r requirements.txt`.
2. Place the dataset `Telco.csv` in the specified location.
3. Run `CustomerChurnPrediction.ipynb` to preprocess data, train models, and evaluate performance.
