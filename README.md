# 💳 Credit Card Fraud Detection and Customer Profiling

This project involves analyzing two credit card datasets to:
1. Detect fraudulent transactions using anomaly detection techniques.
2. Profile customers using clustering.
3. Predict credit limits using linear regression.

---

## 📁 Datasets Used

1. **Credit Card Fraud Dataset**
   - Contains transactions over two days in 2013.
   - 492 frauds out of 284,807 transactions (highly imbalanced).
   - Features: `Time`, `V1` to `V28` (PCA transformed), `Amount`, `Class` (fraud=1).

2. **Credit Card Customer Dataset**
   - Contains information like:
     - `Avg_Credit_Limit`
     - `Total_Credit_Cards`
     - `Total_visits_bank`
     - `Total_visits_online`
     - `Total_calls_made`

---

## Project Tasks & Approach

### 1. Fraud Detection (Anomaly Detection)
- Used **Isolation Forest** for unsupervised anomaly detection.
- Preprocessed `Time` and `Amount` using StandardScaler.
- Detected anomalies and evaluated using:
  - Confusion Matrix
  - Classification Report
- Visualized normal vs. fraudulent transactions.

### 2. Customer Profiling (Clustering)
- Used **K-Means Clustering** implemented from scratch (no scikit-learn).
- Normalized features.
- Determined optimal clusters using the **Elbow Method**.
- Final clustering done with `k=4`.
- Visualized clusters using **PCA** + **Matplotlib**.

### 3. Transaction Amount Prediction (Linear Regression)
- Built a **Linear Regression** model to predict `Avg_Credit_Limit`.
- Identified key features:
  - `Total_Credit_Cards`
  - `Total_visits_bank`
  - `Total_visits_online`
  - `Total_calls_made`
- Evaluated using:
  - Mean Squared Error (MSE)
  - R² Score
- Displayed learned feature coefficients.

---

## Technologies Used

- Python 
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 📌 Folder Structure

CreditCardFraudDetection/<br>
│<br>
├──creditcard.ipynb # Full project notebook <br>
├── customer.csv # Customer dataset <br>
├── creditcard.csv # Fraud detection dataset<br>
├── README.md # This file<br>


---

## 📈 Results

- **Fraud Detection**: Successfully detected frauds using anomaly detection.
- **Customer Segmentation**: Identified 3 behaviorally distinct customer groups.
- **Regression**: Built a model to estimate avg. credit limit from user activity.

---

