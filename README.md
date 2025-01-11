
# Credit Card Fraud Detection System

A machine learning-based solution for detecting fraudulent credit card transactions. This project leverages a Random Forest Classifier trained on a synthetic dataset and provides an intuitive user interface built with Streamlit for real-time predictions.

## Key Features
- **Streamlit Frontend**: A simple and interactive UI for entering transaction details and predicting fraud.
- **Random Forest Classifier**: A robust ML model for binary classification (fraudulent or non-fraudulent transactions).
- **SMOTE Implementation**: Balances the dataset to address class imbalance, ensuring reliable model performance.
- **Feature Engineering**: Extracted features like transaction date, time, and category to enhance model accuracy.
- **Joblib Model Serialization**: Ensures the model can be reused without retraining.
  
---

## Project Structure

```plaintext
credit_card_fraud_detection/
├── Final.ipynb           # Jupyter notebook for data preprocessing, model training, and evaluation
├── main.py               # Streamlit app script for fraud prediction
├── model.joblib          # Pre-trained Random Forest model
├── credit_card_transactions.csv  # Dataset used for model training
└── README.md             # Project documentation
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/credit_card_fraud_detection.git
   cd credit_card_fraud_detection
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Streamlit app:
   ```bash
   streamlit run main.py
   ```

## Dataset

The model was trained on a synthetic dataset (`credit_card_transactions.csv`) containing the following features:
- **Category**: Type of transaction (e.g., gas, grocery, shopping).
- **Amount**: Transaction amount in USD.
- **Gender**: Customer's gender.
- **City Population**: Population of the city where the transaction occurred.
- **Merchant Location**: Latitude and longitude of the merchant.
- **Transaction Time Details**: Year, month, day, hour, minute, and second of the transaction.
- **Fraud Label**: Binary label indicating if the transaction is fraudulent.

## Model Overview

- **Algorithm**: Random Forest Classifier.
- **Data Balancing**: SMOTE (Synthetic Minority Oversampling Technique) to address class imbalance.
- **Feature Scaling**: StandardScaler for normalizing numerical features.
- **Evaluation Metrics**:
  - Classification Report (Precision, Recall, F1-Score).
  - ROC AUC Score.

## Usage

1. Launch the app using Streamlit:
   ```bash
   streamlit run main.py
   ```
2. Input transaction details:
   - Select transaction category, amount, gender, city population, and merchant's location.
   - Specify transaction time (year, month, day, hour, minute, second).
3. Click on **Predict** to determine if the transaction is fraudulent.

## Example Prediction

### Input
- **Category**: shopping_net  
- **Amount**: 350.00  
- **Gender**: Female  
- **City Population**: 500000  
- **Merchant Latitude**: 40.712776  
- **Merchant Longitude**: -74.005974  
- **Transaction Time**: 2019-12-15 14:30:45  

### Output
- **Result**: This transaction is not fraudulent.

## Dependencies

- Python 3.7+
- pandas  
- numpy  
- seaborn  
- scikit-learn  
- imbalanced-learn  
- joblib  
- streamlit  

Install dependencies using:
```bash
pip install -r requirements.txt
```

## How It Works

1. **Preprocessing**: The dataset undergoes cleaning and feature extraction.
2. **Model Training**: A Random Forest model is trained using balanced data (SMOTE).
3. **Frontend**: The Streamlit app allows users to input transaction details and view predictions in real-time.
