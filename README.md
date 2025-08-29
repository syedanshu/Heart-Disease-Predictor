

---

# 🫀 Heart Disease Predictor

This project predicts the likelihood of **heart disease** using **Machine Learning models**.
It uses the [Kaggle Heart Disease dataset](https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data).

## 📂 Project Structure

```
heart_disease_predictor.ipynb   # Main notebook with training + evaluation
README.md                       # Documentation
```
⚙️ Installation

Clone the repository: git clone (https://github.com/syedanshu/Heart-Disease-Predictor) cd Disease_Detector

Create and activate a virtual environment (recommended): python -m venv venv source venv/bin/activate # On Linux/Mac venv\Scripts\activate # On Windows

Install dependencies: pip install -r requirements.txt
--- 

## ⚙️ Models Implemented

1. **Logistic Regression**

   * Baseline interpretable model.
   * Achieved \~**84.2% accuracy**.
   * Provides coefficients to show how each feature increases/decreases risk.

2. **Random Forest**

   * Ensemble model capturing non-linear feature interactions.
   * Achieved \~**88.6% accuracy**.
   * Provides feature importance rankings.

---

## 📊 Feature Importance & Comparison

### 🔹 Random Forest Feature Importances

```python
importances = rf_model.feature_importances_
features = X_train.columns
```

Visualizes which features contribute most to predictions.

### 🔹 Logistic Regression Coefficients

```python
coefficients = log_reg.coef_[0]
features = X_train.columns
```

Shows direction (positive = higher risk, negative = protective).

### 🔹 Combined Comparison

```python
comparison_df.set_index("Feature")[["RandomForest","LogisticRegression"]].plot(kind="bar")
```

* **Green bars:** Random Forest importance.
* **Blue bars:** Logistic Regression coefficients.
* Lets you compare both models side by side.

---

## 📈 Results

* **Random Forest outperformed Logistic Regression** in overall accuracy.
* Both models highlight features such as:

  * **Chest pain type (cp)**
  * **Max heart rate (thalach)**
  * **ST depression (oldpeak)**
  * **Number of major vessels (ca)**
  * **Thalassemia type (thal)**

These are strong indicators of heart disease.

---

## 🚀 How to Run

1. Clone this repository or download the notebook.
2. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Run the notebook:

   ```bash
   jupyter notebook heart_disease_predictor.ipynb
   ```
4. Explore results and feature importance charts.

---








