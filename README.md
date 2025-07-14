# 🔋 Energy Consumption Prediction Using Ensemble Learning

This project focuses on predicting energy consumption based on various building features using advanced machine learning techniques such as **Random Forest** (Bagging), **XGBoost**, and **Stacking Regressors**. The model is trained and evaluated on the [ENB2012 energy efficiency dataset](https://archive.ics.uci.edu/ml/datasets/energy+efficiency).

--

---

## 📊 Dataset

The project uses the **ENB2012 dataset** which contains 768 samples of building data with 8 input variables:
- Relative Compactness
- Surface Area
- Wall Area
- Roof Area
- Overall Height
- Orientation
- Glazing Area
- Glazing Area Distribution

The output variables are:
- Heating Load
- Cooling Load

> 📌 Only **one of the outputs (last column)** is used as the target (`y`) in this project.

---

## 🚀 Features

- 📉 **Preprocessing**:  
  - Missing value imputation with median
  - Duplicate removal
  - Highly correlated feature elimination (> 0.9)
  - Feature scaling using `StandardScaler`
  - Dimensionality reduction using `PCA` (95% variance retained)

- 🤖 **Models Implemented**:
  - **Bagging** with `RandomForestRegressor`
  - **Stacking** with `RandomForest` and `XGBoost` as base learners, `XGBoost` as meta-learner

- 📈 **Evaluation Metrics**:
  - RMSE (Root Mean Squared Error)
  - R² Score
  - Custom Accuracy Metric (within ±5% tolerance)

---

## 🛠️ Tech Stack

- Python 3.x
- Jupyter Notebook / Google Colab
- Libraries:
  - `scikit-learn`
  - `xgboost`
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`

---

## 🧪 How to Run

### ▶️ On Google Colab

1. Open the notebook: [Colab Link](https://colab.research.google.com/drive/134Z80PIPTanlJM5KEW11FqdOW4O1Oari)
2. Upload the dataset `ENB2012_data.xlsx` when prompted.
3. Run all cells sequentially.

### 💻 Locally (Python)

1. Clone/download the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
