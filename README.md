# 🚗 Car Price Prediction - Quikr Predictor

This project is a complete **end-to-end machine learning web application** that predicts the resale price of used cars based on various features. The system uses a **Linear Regression model** trained on real-world data scraped from Quikr. The project combines data preprocessing, model training, saving the model, and serving it via a Flask web interface — making it ideal for ML portfolio and deployment practice.

---

## 📌 Features

- Real-world dataset collected from Quikr
- Data cleaning and preprocessing using pandas
- Model training using scikit-learn’s Linear Regression
- Web deployment using Flask
- Dynamic HTML form with user input and live predictions

---

## 🧠 End-to-End Project Flow

### 🔹 Step 1: Data Collection & Cleaning

- **Input**: `quikr_car (1).csv` (raw data scraped from Quikr)
- **Notebook**: `Quikr_Predictor.ipynb`
- **Steps Performed**:
  - Null value removal, outlier handling
  - Feature extraction (engine, mileage, kms driven)
  - Categorical encoding for fuel type, brand, etc.
  - Final dataset saved as `Cleaned Car.csv`

---

### 🔹 Step 2: Model Training

- **Notebook**: `Quikr_Predictor.ipynb`
- **Algorithm Used**: Linear Regression (`scikit-learn`)
- **Steps Performed**:
  - Load `Cleaned Car.csv`
  - Split into features and target
  - Train-test split
  - Model training and evaluation (R² score, MAE)
  - Model saved as `LinearRegressionModel.pkl`

---

### 🔹 Step 3: Web App Deployment with Flask

- **File**: `application.py`
- **UI File**: `templates/index.html`
- **Frontend Styling**: `static/css/`
- **Workflow**:
  - Flask loads `LinearRegressionModel.pkl`
  - Also loads `Cleaned Car.csv` to fetch dropdown options (company, fuel type)
  - Renders HTML form where users enter:
    - Brand/Company
    - Year
    - Fuel Type
    - KMs Driven
  - Converts form input to model-ready format
  - Predicts car price using the trained model
  - Displays prediction directly on the same page

---

## 🔁 Component Workflow Diagram

Raw Data → Cleaning → Model Training → Saved Model (.pkl)
│ │
└──────> Web Interface <──────────┘
│
User Input Form
│
Prediction Displayed

