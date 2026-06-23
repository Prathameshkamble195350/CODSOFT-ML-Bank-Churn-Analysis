# 🏦 Bank Customer Churn Prediction using Machine Learning | CODSOFT

## 📌 Project Overview

Bank Customer Churn Prediction is a Machine Learning project that predicts whether a customer is likely to leave a bank based on customer demographics, account information, and banking behavior.

The project uses data preprocessing, exploratory data analysis (EDA), feature engineering, and machine learning algorithms to identify customers at risk of churn.

This project was developed as part of the CODSOFT Machine Learning Internship.

---

## 🎯 Objective

The objective of this project is to build a Machine Learning model capable of predicting customer churn and helping banks improve customer retention strategies.

---

## 📂 Dataset

Dataset: Bank Customer Churn Dataset

### Features

| Column | Description |
|----------|-------------|
| CreditScore | Customer Credit Score |
| Geography | Customer Country |
| Gender | Customer Gender |
| Age | Customer Age |
| Tenure | Years with Bank |
| Balance | Account Balance |
| NumOfProducts | Number of Products Used |
| HasCrCard | Credit Card Holder |
| IsActiveMember | Active Member Status |
| EstimatedSalary | Customer Salary |
| Exited | Churn Status |

### Target Variable

- 0 → Customer Stays
- 1 → Customer Leaves (Churn)

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook
- Pickle

---

## 🔄 Project Workflow

### 1️⃣ Data Collection

- Load dataset
- Explore dataset structure
- Understand customer information

### 2️⃣ Data Cleaning

- Check missing values
- Remove unnecessary columns
- Handle categorical variables

### 3️⃣ Exploratory Data Analysis (EDA)

Performed various analyses:

- Churn Distribution
- Gender-wise Churn Analysis
- Geography-wise Churn Analysis
- Age Distribution
- Balance Distribution
- Correlation Analysis

### 4️⃣ Feature Engineering

Convert categorical data into numerical format.

```python
from sklearn.preprocessing import LabelEncoder

encoder = LabelEncoder()
df['Gender'] = encoder.fit_transform(df['Gender'])
```

### 5️⃣ Data Preprocessing

- Feature Selection
- Label Encoding
- One-Hot Encoding
- Feature Scaling

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

### 6️⃣ Train-Test Split

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X_scaled,
    y,
    test_size=0.2,
    random_state=42
)
```

### 7️⃣ Model Training

Machine Learning Algorithm:

- Random Forest Classifier

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=100,
    random_state=42
)

model.fit(X_train, y_train)
```

### 8️⃣ Model Evaluation

Evaluation Metrics:

- Accuracy Score
- Precision Score
- Recall Score
- F1 Score
- Confusion Matrix

```python
from sklearn.metrics import classification_report

predictions = model.predict(X_test)

print(classification_report(y_test, predictions))
```

### 9️⃣ Model Saving

```python
import pickle

pickle.dump(model, open('churn_model.pkl', 'wb'))
```

### 🔟 Customer Churn Prediction

Predict whether a customer will leave the bank.

Example:

```python
sample_customer = [[650, 1, 0, 35, 5, 50000, 2, 1, 1, 60000]]

prediction = model.predict(sample_customer)

print(prediction)
```

---

## 📊 Visualizations Included

✔ Customer Churn Distribution

✔ Gender-wise Churn Analysis

✔ Geography-wise Churn Analysis

✔ Age Distribution Histogram

✔ Balance Distribution Plot

✔ Correlation Heatmap

✔ Feature Importance Analysis

✔ Confusion Matrix

---

## 🚀 How to Run

### Clone Repository

```bash
git clone https://github.com/Prathameshkamble195350/Bank-Customer-Churn-Prediction-CODSOFT.git
```

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Bank customer churn prediction.ipynb
```

---

## 📈 Results

The model successfully predicts whether a customer is likely to leave the bank based on customer information and banking activity.

Evaluation Metrics:

- Accuracy
- Precision
- Recall
- F1 Score

---

## 🔮 Future Improvements

- XGBoost Classifier
- LightGBM
- CatBoost
- Deep Learning Models
- Hyperparameter Tuning
- Streamlit Deployment
- Flask Web Application

---

## 💡 Skills Demonstrated

- Data Cleaning
- Data Analysis
- Data Visualization
- Feature Engineering
- Machine Learning
- Classification Models
- Model Evaluation
- Customer Analytics
- Predictive Modeling

---

## 👨‍💻 Author

**Prathamesh Kamble**

B.Sc. Physics Graduate

Machine Learning Enthusiast

CODSOFT Machine Learning Intern

---

## ⭐ Internship Task

Task: Bank Customer Churn Prediction

Internship: CODSOFT Machine Learning Internship

Domain: Machine Learning & Predictive Analytics

Status: Completed ✅

---

### If you found this project useful, please give it a ⭐ on GitHub!
