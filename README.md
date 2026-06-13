# 📉 Customer Churn Classification

A machine learning project to predict customer churn using classification models — built as part of the **InternSpark AI Internship Task 1**.

---

## 📌 Project Overview

Customer churn refers to when a customer stops using a company's service. This project analyzes a telecom customer dataset to:
- Explore and understand the data
- Preprocess and engineer features
- Train and compare multiple ML classification models
- Identify the best model for predicting churn

---

## 📊 Dataset

| Property | Value |
|---|---|
| File | `data/customer_churn_data.csv` |
| Total Customers | 5,880 |
| Features | 19 |
| Churn Rate | 49.29% |

Key features include: `gender`, `tenure`, `Contract`, `MonthlyCharges`, `TotalCharges`, `InternetService`, `PaymentMethod`, and more.

---

## 🧠 Models Trained

Three classification models were trained and evaluated:

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 0.5009 | 0.4926 | 0.4000 | 0.4415 | 0.4748 |
| **Random Forest** ✅ | **0.5119** | **0.5054** | **0.4810** | **0.4929** | **0.4982** |
| Gradient Boosting | 0.4804 | 0.4721 | 0.4517 | 0.4617 | 0.4628 |

🏆 **Best Model: Random Forest** (highest ROC-AUC score)

---

## 🗂️ Project Structure

```
customer-churn-classification/
│
├── data/
│   └── customer_churn_data.csv       # Raw dataset
│
├── notebook/
│   └── Customer_Churn_Classification.ipynb  # Main analysis notebook
│
├── images/
│   ├── models_performance_comparison.png    # Model comparison chart
│   └── Screenshot.png                       # Project screenshot
│
├── requirements.txt                  # Python dependencies
└── README.md                         # Project documentation
```

---

## ⚙️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/customer-churn-classification.git
cd customer-churn-classification
```

### 2. Create and activate a virtual environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```

Then open `notebook/Customer_Churn_Classification.ipynb` and run all cells.

---

## 🔍 Methodology

1. **Data Loading & Exploration** — Understand structure, distributions, and churn rate
2. **Data Preprocessing** — Remove irrelevant columns, encode categoricals, scale numericals
3. **Feature Engineering** — One-Hot Encoding + Standard Scaling via `ColumnTransformer`
4. **Train/Test Split** — 80/20 stratified split to preserve class balance
5. **Model Training** — Logistic Regression, Random Forest, Gradient Boosting
6. **Evaluation** — 5-fold cross-validation + test set metrics + confusion matrices + ROC curves

---

## 📈 Results

![Model Performance Comparison](images/models_performance_comparison.png)

---

## 🛠️ Technologies Used

- Python 3.x
- pandas, numpy
- scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

---

## 👤 Author

Internship Project — InternSpark | Artificial Intelligence Domain
