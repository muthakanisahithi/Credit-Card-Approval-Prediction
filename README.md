# Loan Approval Prediction System

## Overview

The **Loan Approval Prediction System** is a machine learning-based application that predicts whether a loan application should be approved based on an applicant's personal, employment, and credit history information.

The system stores applicant details, credit history, machine learning model information, and prediction results in a relational database.

---

## Features

- User Management
- Applicant Information Management
- Credit History Management
- Loan Approval Prediction
- Risk Category Classification
- Machine Learning Model Management
- Prediction History

---

# Entity Relationship Diagram

The database consists of five main entities:

- Users
- Applicant_Details
- Credit_History
- ML_Model
- Approval_Prediction

---

# Database Tables

## Users

| Column | Description |
|---------|-------------|
| UserID (PK) | Unique User ID |
| Name | User Name |
| Email | Email Address |
| Password | User Password |
| Role | User Role |

---

## Applicant_Details

| Column | Description |
|---------|-------------|
| ApplicantID (PK) | Applicant ID |
| UserID (FK) | References Users |
| IncomeType | Income Source |
| EducationType | Education Qualification |
| FamilyStatus | Marital Status |
| HousingType | Housing Status |
| EmploymentDays | Employment Duration |

---

## Credit_History

| Column | Description |
|---------|-------------|
| HistoryID (PK) | History ID |
| ApplicantID (FK) | References Applicant_Details |
| MonthsBalance | Balance Months |
| PaymentStatus | Payment Status |
| OverdueStatus | Overdue Status |

---

## ML_Model

| Column | Description |
|---------|-------------|
| ModelID (PK) | Model ID |
| ModelName | Model Name |
| AlgorithmType | ML Algorithm |
| Accuracy | Model Accuracy |
| ModelFile | Saved Model File |

---

## Approval_Prediction

| Column | Description |
|---------|-------------|
| PredictionID (PK) | Prediction ID |
| ApplicantID (FK) | References Applicant_Details |
| ModelID (FK) | References ML_Model |
| ApprovalResult | Approved / Rejected |
| RiskCategory | Low / Medium / High |
| PredictionDate | Prediction Date |

---

# Relationships

| Relationship | Cardinality |
|--------------|-------------|
| Users → Applicant_Details | One-to-Many (1:N) |
| Applicant_Details → Credit_History | One-to-Many (1:N) |
| Applicant_Details → Approval_Prediction | One-to-One (1:1) |
| ML_Model → Approval_Prediction | One-to-Many (1:N) |

---

# Workflow

1. User logs into the system.
2. Applicant details are entered.
3. Credit history is recorded.
4. Applicant data is sent to the ML model.
5. The model predicts loan approval.
6. Prediction results are stored.
7. Users can view previous predictions.

---

# Technologies Used

## Frontend

- HTML
- CSS
- JavaScript
- Bootstrap

## Backend

- Python
- Flask

## Database

- MySQL

## Machine Learning

- Scikit-learn
- Pandas
- NumPy
- Joblib

---

# Project Structure

```text
LoanApprovalPrediction/
│
├── app.py
├── database.sql
├── model.pkl
├── requirements.txt
├── README.md
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
├── templates/
│   ├── index.html
│   ├── login.html
│   ├── dashboard.html
│   └── prediction.html
│
├── dataset/
│   └── loan_dataset.csv
│
└── models/
    └── trained_model.pkl
```

---

# Future Enhancements

- Explainable AI (XAI)
- Real-time Credit Score Integration
- Email Notifications
- Admin Dashboard
- REST API Support
- Model Performance Comparison

---

# Advantages

- Faster Loan Approval
- Reduced Manual Work
- Accurate Predictions
- Better Risk Analysis
- Secure Data Storage
- Easy to Maintain

---

# Conclusion

The Loan Approval Prediction System combines machine learning and database management to automate the loan approval process. It efficiently stores applicant information, credit history, prediction results, and machine learning model details while providing accurate loan approval decisions.

---

## Author

**Shaik Bashirunnisa**

---

## License

This project is developed for educational and academic purposes.
