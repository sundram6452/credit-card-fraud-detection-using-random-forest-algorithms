# credit-card-fraud-detection-using-random-forest-algorithms

# 💳 Credit Card Fraud Detection using Random Forest

## 📌 Overview
Credit card fraud is a major challenge in the financial industry, causing billions in losses each year.  
This project applies **Random Forest**, a powerful ensemble machine learning algorithm, to detect fraudulent credit card transactions.  

The objective is to classify transactions into two categories:
- **Normal** (legitimate transactions)  
- **Fraudulent** (suspicious/fraud cases)  

---

## 📂 Dataset
- Dataset: [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)  
- **284,807 transactions** in total  
- Only **492 fraud cases** (≈0.172% → highly imbalanced dataset)  
- Features:  
  - 28 anonymized PCA components (`V1` … `V28`)  
  - `Time`  
  - `Amount`  

---

## ⚙️ Tech Stack
- **Language:** Python  
- **Libraries:**
  - `numpy`, `pandas` → data preprocessing  
  - `matplotlib`, `seaborn` → data visualization  
  - `scikit-learn` → machine learning (Random Forest, metrics)  

---

## 🧠 Approach
1. **Data Preprocessing**
   - Standardized/normalized features like `Amount`  
   - Train-test split for model validation  

2. **Class Imbalance Handling**
   - Used techniques such as undersampling or **SMOTE** to balance fraud vs. normal samples  

3. **Model Training**
   - Implemented **Random Forest Classifier**  
   - Tuned hyperparameters (`n_estimators`, `max_depth`, etc.) using GridSearchCV  

4. **Evaluation**
   - Since the dataset is highly imbalanced, accuracy is not enough.  
   - Used metrics:  
     - Precision  
     - Recall  
     - F1-Score  
     - Matthews Correlation Coefficient (MCC)  
     - Confusion Matrix  

---

## 📊 Model Evaluation (Sample Results with Random Forest)

### Confusion Matrix
![Confusion Matrix](conf_matrix.png)

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
   ```
2. Install dependencies
```bash
pip install -r requirements.txt
```
3.Run the training script
```bash
python fraud_detection.py
