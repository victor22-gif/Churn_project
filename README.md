# Customer Churn Prediction Model
## Data Science Portfolio Project

### Overview
This project demonstrates the development of a machine learning model to predict customer churn for a telecommunications company. The model helps identify customers who are likely to discontinue their services, enabling proactive retention strategies.

### Table of Contents
- [Requirements](#requirements)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Methodology](#methodology)
- [Model Performance](#model-performance)
- [Future Improvements](#future-improvements)

### Requirements
```
pandas
numpy
scikit-learn
seaborn
matplotlib
```

### Installation
1. Open Google Colab
2. Create a new notebook
3. Copy the project code
4. Run `!pip install requirements.txt` if any packages are missing
5. The dataset will be automatically downloaded when running the code

### Project Structure
```
├── data_cleaning.py          # Data preprocessing and cleaning functions
├── feature_engineering.py    # Feature creation and transformation
├── model_training.py         # Model training and evaluation
└── predict.py               # Prediction functionality for new customers
```

### Usage

#### Training the Model
```python
# The model will be trained automatically when running the notebook
# Key steps:
1. Data is loaded and cleaned
2. Features are engineered
3. Model is trained and evaluated
```

#### Making Predictions
```python
# Create a DataFrame with new customer data
new_customers = pd.DataFrame({
    'customerID': ['CUST123'],
    'gender': ['Female'],
    'InternetService': ['Fiber optic'],
    'Contract': ['Month-to-month'],
    'PaymentMethod': ['Electronic check'],
    'tenure': [12],
    'MonthlyCharges': [80.0],
    'TotalCharges': [960.0],
    'PhoneService': ['Yes'],
    'OnlineBackup': ['No'],
    'DeviceProtection': ['Yes'],
    'TechSupport': ['No'],
    'Churn': ['No']
})

# Get predictions
churn_probabilities = predict_churn(new_customers)
```

### Methodology

#### Data Preprocessing
- Handling missing values in TotalCharges
- Converting categorical variables to dummy variables
- Feature scaling using StandardScaler

#### Feature Engineering
1. AvgChargePerMonth: Total charges divided by tenure
2. ServiceRatio: Proportion of services subscribed
3. ChargeToTenure: Monthly charges relative to tenure

#### Model Selection
- Algorithm: Random Forest Classifier
- Reasoning: 
  - Handles non-linear relationships
  - Robust to outliers
  - Provides feature importance
  - Good performance with categorical variables

### Model Performance
The model is evaluated using:
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix
- Feature Importance Analysis

### Future Improvements
1. Hyperparameter Tuning
   - Implement GridSearchCV for optimal parameters
   - Cross-validation for more robust evaluation

2. Feature Engineering
   - Create more interaction features
   - Experiment with different feature selection methods

3. Model Enhancements
   - Try other algorithms (XGBoost, LightGBM)
   - Implement model stacking
   - Add feature selection pipeline

4. Production Readiness
   - Add input validation
   - Implement error handling
   - Add logging
   - Create API endpoint

### Contributing
Feel free to fork this project and submit improvements via pull requests.

### License
This project is available under the MIT License.

### Contact
emmanuelvictor039@gmail.com
