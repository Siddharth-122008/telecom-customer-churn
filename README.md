# Telecom Customer Churn Prediction Using Logistic Regression

Predicting telecom customer churn using Logistic Regression based on customer tenure, contract type, monthly charges and selected service-related features.

## 1. Project Overview

Customer churn refers to a situation in which a customer stops using a company's services. In the telecom industry, identifying customers who are likely to leave is important for improving customer retention.

This project aims to predict telecom customer churn using Logistic Regression, a supervised machine learning classification algorithm. The model uses customer tenure, contract type, monthly charges and selected telecom service-related features to identify patterns associated with customer churn.

The project involves data preprocessing, exploratory data analysis, model training and performance evaluation.

## 2. Project Objectives

- To understand customer churn patterns in the telecom industry.
- To analyse the relationship between customer characteristics and churn.
- To identify features associated with customer churn.
- To develop a Logistic Regression model for predicting customer churn.
- To evaluate the model using appropriate classification metrics.

## 3. Dataset Description

The project uses the **Telco Customer Churn Dataset**, obtained from Kaggle.

**Dataset Source:** [Telco Customer Churn Dataset – Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

The dataset contains customer information such as:

- Customer tenure
- Contract type
- Monthly charges
- Subscribed telecom services
- Customer churn status

The target variable is `Churn`, which indicates whether a customer has left the telecom service.

## 4. Team Members and Roles

| Team Member | Student ID | Role |
|---|---|---|
| Jhanvi Yadav | 2026EEB1356 | Execution Lead |
| Kinjal Khatri | 2026EEB1366 | PPT Lead |
| Siddharth Gangwar | 2026MCB1571 | Documentation Lead |
| Amandeep | 2026AIB1007 | Video Lead |

## 5. Project Structure

The repository contains the following files:

```text
telecom-customer-churn/
│
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── churn_prediction.ipynb
├── requirements.txt
└── README.md
```

| File | Description |
|---|---|
| `WA_Fn-UseC_-Telco-Customer-Churn.csv` | Dataset used for the project |
| `churn_prediction.ipynb` | Jupyter Notebook containing the project implementation |
| `requirements.txt` | Required Python libraries |
| `README.md` | Project documentation |

## 6. Data Loading and Preprocessing

This stage focuses on loading, inspecting and transforming the dataset into a suitable format for analysis and model development.

### 6.1 Data Loading and Inspection

- Loaded the CSV dataset into a Pandas DataFrame using `pd.read_csv()`.
- Displayed the first five records using `head()`.
- Checked the number of rows and columns using `shape`.
- Examined column names and data types using `info()`.

### 6.2 Data Quality Checking

- Checked for missing values using `isnull().sum()`.
- Checked for duplicate records using `duplicated().sum()`.

### 6.3 Removing Unnecessary Columns

The `customerID` column was removed because it is a unique identifier and does not provide useful information for predicting customer churn.

### 6.4 Target Variable Encoding

The target variable `Churn` was converted from categorical values into numerical values.

| Original Value | Encoded Value |
|---|---:|
| Yes | 1 |
| No | 0 |

### 6.5 Feature Selection

The following input features were selected:

**Numerical Features:**
- `tenure`
- `MonthlyCharges`

**Categorical Features:**
- `Contract`
- `PhoneService`
- `MultipleLines`
- `InternetService`
- `OnlineSecurity`
- `OnlineBackup`
- `DeviceProtection`
- `TechSupport`
- `StreamingTV`
- `StreamingMovies`

The target variable selected was `Churn`.

### 6.6 Categorical Feature Encoding

Categorical input features were converted into numerical form using Pandas `get_dummies()`.

The following parameters were used:

- `drop_first=True` to avoid redundant dummy variables.
- `dtype=int` to store encoded values as integers.

### 6.7 Preprocessing Output

After preprocessing, the input features (`X`) and target variable (`y`) were prepared for exploratory data analysis and Logistic Regression model development.

### Setup

Tested on Python 3.14.6 (Windows)

1. Clone the repository:

```bash
git clone https://github.com/Siddharth-122008/telecom-customer-churn.git 
cd telecom-customer-churn
```

2. Create and activate a virtual environment:

```bash
python -m venv venv
```

Windows:
```bash
venv\Scripts\activate
```

macOS / Linux:
```bash
source venv/bin/activate
```

3. Install the required libraries (versions are pinned in `requirements.txt`):

```bash
pip install -r requirements.txt
```

## How to run

1. Start Jupyter Notebook from the project folder:

```bash
jupyter notebook
```

2. In the browser window that opens, click `churn_prediction.ipynb`.
3. Click **Kernel > Restart & Run All**.
4. Wait for all cells to finish (expected runtime: under 1 minute).

The dataset is already included at `data/WA_Fn-UseC_-Telco-Customer-Churn.csv` and is read using a relative path, so no download is needed.

## 7. Project Links

- **Presentation Slides:** Will be added later
- **Project Video:** Will be added later

## 8. AI-Use Disclosure

Will be added later

## 9. Conclusion

To be updated after completing model evaluation and analysing the final results.