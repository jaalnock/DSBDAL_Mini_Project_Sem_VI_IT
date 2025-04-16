# Mini Project: COVID-19 Data Science Analysis

This repository contains a data science mini project analyzing a COVID-19 patient dataset. The project follows the complete data science lifecycle—data cleaning, exploration, feature engineering, modeling, and visualization—to predict ICU admission.

---

## 📁 Project Structure

- `data/`
  - └── `Covid_data.csv` # Raw dataset
- `notebooks/`
  - └── `covid_analysis.ipynb` # Jupyter Notebook with full analysis
- `outputs_with_randomForest/`
  - └── `feature_importance.png` # Visualizations from Random Forest model
- `outputs_with_xgboost/`
  - └── `feature_importance.png` # Visualizations from XGBoost model
- `reports/`
  - └── (optional) # Project report placeholder

---

## ⚙️ Requirements

- Python 3.x
- Required Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`
  - `imbalanced-learn`
  - `xgboost`

### 💻 Installation

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost
```

## 🚀 Usage

1. Place your `Covid_data.csv` in the `data/` folder.
2. Open `notebooks/covid_analysis.ipynb` in Jupyter Notebook and run all cells.
3. Check the following folders for results:
   - `outputs_with_randomForest/` → Results from the **Random Forest** model
   - `outputs_with_xgboost/` → Results from the **XGBoost** model

## 🎯 Objective

- Explore the data science project lifecycle
- Analyze COVID-19 patient data to predict ICU admission
- Visualize insights using **Matplotlib** and **Seaborn**
- Compare different algorithms to identify the best-performing model

## 🔍 Methodology

### 1️⃣ Initial Model: Random Forest

- Started with a Random Forest classifier using RandomizedSearchCV for hyperparameter tuning.
- Despite offering good interpretability, the model had suboptimal accuracy and AUC-ROC.
- All related plots and outputs are stored in the `outputs_with_randomForest/` directory.

### 2️⃣ Improved Model: XGBoost

- Switched to XGBoost, which better handles imbalanced datasets and provides fine control over model complexity.
- Performed RandomizedSearchCV again for tuning hyperparameters.
- Achieved significantly better performance:
  - Higher Accuracy
  - Higher AUC-ROC
- Outputs and visualizations are in `outputs_with_xgboost/`.

## 📊 Results

### ✅ Random Forest Model

- Limitations in ICU prediction performance led to the transition to XGBoost.
- Outputs in: `outputs_with_randomForest/`

### ✅ XGBoost Model

- Improved metrics:
  - Better Accuracy
  - Stronger AUC-ROC
  - Effective with imbalanced dataset
- Outputs in: `outputs_with_xgboost/`

## 💡 Insights

### Top Features influencing ICU admission:

- AGE
- PNEUMONIA
- OBESITY
- CARDIOVASCULAR

Feature importance and EDA plots reveal actionable insights for healthcare-focused decision-making.
