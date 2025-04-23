# 💳 Credit Card Fraud Detection

This project focuses on detecting fraudulent credit card transactions using anomaly detection techniques like **Isolation Forest**. Given the highly imbalanced nature of the data, these models help identify rare fraudulent activities effectively.

---

## 📂 Project Overview

Credit card fraud is a major issue in financial systems, where fraudulent transactions represent a very small fraction of total transactions. This project aims to:
- Explore and visualize the distribution of fraud and normal transactions
- Analyze transaction patterns based on amount and time
- Apply anomaly detection algorithms to detect fraud
- Evaluate model performance using classification metrics and confusion matrix

---

## 📊 Dataset

- **Source**: [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- **Rows**: 284,807
- **Fraudulent transactions**: 492 (~0.172%)
- **Features**:
  - `Time` and `Amount`
  - `V1` to `V28`: Principal Component Analysis (PCA) transformed features
  - `Class`: 0 = Normal, 1 = Fraud

---

## 🛠️ Features Used

Since most original features are PCA-transformed (`V1–V28`), the models use the following variables:
- `V1` to `V28` (PCA components)
- `Amount`
- `Time` *(optionally)*

**Target**:  
- `Class` → 0 (Normal), 1 (Fraud)

---

## 📈 Visualizations

- ✅ Fraud vs Normal bar chart  
- ✅ Histogram of transaction amounts by class  
- ✅ Heatmap of feature correlations  


## 🤖 Models Used

- ✅ **Isolation Forest**: A tree-based model that isolates anomalies instead of profiling normal data points.

---

## ⚙️ How It Works

1. Load the dataset and explore class imbalance
2. Visualize the transaction amount distribution for both fraud and normal classes
3. Preprocess the data (e.g., scale `Amount` and `Time`)
4. Apply `IsolationForest` model
5. Compare predictions with actual labels
6. Evaluate performance using:
   - Accuracy
   - Precision, Recall, F1-Score
   - Confusion Matrix

---

## 🔬 Evaluation Metrics

Due to the class imbalance, **accuracy alone is not a reliable metric**. The focus is on:
- **Precision** → Of all transactions predicted as fraud, how many were correct?
- **Recall** → Of all actual fraudulent transactions, how many were detected?
- **F1-Score** → Harmonic mean of precision and recall

---
