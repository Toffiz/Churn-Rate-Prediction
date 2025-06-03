# Churn-Rate-Prediction
Second place in Hackathon from BI group

# 📊 Churn Rate Prediction with LightGBM & Optuna

This project predicts **customer churn** using a supervised classification approach. It leverages **LightGBM** for model training and **Optuna** for automated hyperparameter tuning, optimizing the **Precision-Recall AUC (PR AUC)** — a critical metric when dealing with imbalanced datasets like churn.

---

## 🔧 Project Structure

```
.
├── train.csv               # Training dataset
├── churn_prediction.py     # Model training & evaluation script
├── README.md               # Project documentation
```

---

## 📦 Dependencies

Install the required libraries using pip:

```bash
pip install pandas numpy scikit-learn lightgbm xgboost optuna matplotlib
```

---

## 🚀 How It Works

1. **Data Loading & Preprocessing**
   Load your dataset (`train.csv`) using `pandas`. Encode categorical labels if necessary and split the data into features `X` and target `y`.

2. **Train-Test Split**
   The data is split into training and testing subsets with `train_test_split`.

3. **Model Optimization**

   * Hyperparameters of LightGBM are tuned using `Optuna`.
   * The objective function maximizes **Precision-Recall AUC**, suitable for imbalanced classification problems.

4. **Model Evaluation**

   * The final model is evaluated using **precision**, **recall**, and **PR AUC**.
   * Various threshold values are tested to observe changes in PR AUC performance.

---

## 🧪 Metrics

The key evaluation metric is **Precision-Recall AUC (PR AUC)**, which is more informative than ROC AUC when dealing with imbalanced datasets like churn.

The script prints:

* Optimal hyperparameters found by Optuna
* Final PR AUC score on the test set
* PR AUC at multiple thresholds

---

## 🧠 Model Used

* **LightGBM**: A fast, distributed, high-performance gradient boosting framework.
* **Optuna**: An automatic hyperparameter optimization framework.
* Additional models (RandomForest, XGBoost, etc.) can be added for comparison.

---

## 📂 Data

Ensure your `train.csv` includes:

* Numerical or categorical features (pre-encoded if needed)
* A binary target column (e.g., `Churned`: 1 for churn, 0 for retained)

---

## 📌 Future Work

* Add feature engineering and EDA
* Handle categorical encoding dynamically
* Try ensemble stacking or comparison with other classifiers
* Deploy with a Flask or Streamlit API

---

## 🧑‍💻 Author

Developed by \[Danial Shokobalinov] — for any queries, feel free to reach out!

---
