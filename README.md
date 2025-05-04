# 🧠 Crypto AML Detection using Elliptic Dataset

This project demonstrates the use of graph analytics and machine learning to identify illicit transactions on the Bitcoin blockchain, using the [Elliptic Bitcoin Dataset](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set).

---

## 📌 Project Objective

To develop a reproducible workflow to:
- Load and preprocess blockchain transaction data.
- Engineer features from both transactional and graph-based signals.
- Train a classification model to detect illicit activity.
- Generate a risk score and risk level classification.
- Provide model explainability using SHAP.

---

## 🗂️ Project Structure

```
📁 crypto-aml-detection/
├── FULL_ANALYSIS.ipynb               # Final notebook with end-to-end pipeline
├── predictor.py                      # Script for loading/scoring new transactions
├── xgb_illicit_model.pkl             # Trained XGBoost model
├── scaler.pkl                        # RobustScaler used on selected features
├── xgb_feature_list.json            # Ordered feature list for prediction
├── new_data.csv                      # Example input for prediction
└── README.md                         # This file
```

---

## ⚙️ Requirements

```bash
pip install pandas numpy networkx shap xgboost scikit-learn matplotlib joblib
```

---

## 🚀 How to Use

### 🔎 Run Full Analysis
1. Open `FULL_ANALYSIS.ipynb`
2. Run all cells sequentially

### 🔁 Predict New Transactions
1. Save new transaction data in `new_data.csv`
2. Run:
```bash
python predictor.py
```
3. Output will include prediction, risk score, risk level, and top explanatory features

---

## 📊 Outputs

- **Risk Score (0 to 1):** Probability of a transaction being illicit
- **Risk Level:** Categorized as `Low`, `Medium`, or `High`
- **Top Features:** Most influential variables (SHAP-based)
- **Model Metrics:**
  - Accuracy: 99%
  - F1-Score (Illicit class): 0.95
  - AUC: ~0.99

---

## 🔎 Model Explainability
- SHAP summary plots
- Top 5 influential features per node
- Justification for risk scoring per prediction

---

## 📈 Tools Used
- Python (pandas, sklearn, xgboost, shap)
- NetworkX (graph metrics)
- Jupyter Notebook

---

## ✍️ Author
**[Tu Nombre Aquí]**  
Data Science & AML Specialist  
[LinkedIn profile / GitHub link opcional]

---

## 📬 Contact
If you have any questions or suggestions, feel free to open an issue or reach out!

---

## 📚 Acknowledgments
Elliptic dataset provided under license for research purposes. Full metadata and labels available on [Kaggle](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set).
