# telecom-customer-churn
Predicting telecom customer churn using logistic regression based on customer tenure, contract type, monthly charges and service usage.

## Setup

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

## Expected output

The notebook displays the dataset summary, EDA plots, the model accuracy, the classification report and the confusion matrix in its output cells.

![Expected output]
