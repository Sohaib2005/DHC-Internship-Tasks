# DevelopersHub Corporation — AI/ML Engineering Internship Tasks

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

This repository contains completed AI/ML internship tasks for **DevelopersHub Corporation**.  
**3 out of 6 tasks completed** — covering data visualization, classification, and regression.

---

## Repository Structure

```
DHC-Internship-Tasks/
│
├── Task1-Iris-EDA/
│   ├── iris_eda.ipynb          # Main notebook
│   ├── requirements.txt
│   └── plots/                  # Generated visualizations
│
├── Task3-Heart-Disease/
│   ├── heart_disease_prediction.ipynb
│   ├── requirements.txt
│   └── plots/
│
├── Task6-House-Price/
│   ├── house_price_prediction.ipynb
│   ├── requirements.txt
│   └── plots/
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## Task 1: Exploring and Visualizing the Iris Dataset

### Objective
Load, inspect, and visualize the Iris dataset to understand data trends, distributions, and feature relationships.

### Dataset
**Iris Dataset** — 150 samples, 3 species, 4 features (sepal/petal length & width).  
Loaded directly via `seaborn` — no download required.

### Approach
- Loaded and inspected dataset with pandas (`.head()`, `.info()`, `.describe()`)
- Checked for missing values and class balance
- Created: Pairplot, Scatter plots, Histograms, Box plots, Correlation Heatmap

### Key Results & Findings
| Finding | Detail |
|---|---|
| Dataset quality | 150 samples, no missing values, perfectly balanced |
| Best features | Petal length & petal width (most separable) |
| Strongest correlation | Petal length ↔ Petal width (r = 0.96) |
| Easiest class | *Iris setosa* — completely isolated in petal space |
| Hardest to separate | *Versicolor* vs *Virginica* — slight overlap |

### Libraries
`pandas` · `numpy` · `matplotlib` · `seaborn`

---

## Task 3: Heart Disease Prediction

### Objective
Build a classification model to predict whether a patient is at risk of heart disease from clinical measurements.

### Dataset
**UCI Heart Disease Dataset** — 303 patient records, 13 clinical features, binary target.  
Loaded via public GitHub mirror (no Kaggle login required).

### Models Applied
| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | ~85% | ~0.92 |
| Decision Tree | ~80% | ~0.85 |

### Approach
- Data cleaning: handled missing values, ensured correct dtypes
- EDA: class distribution, age/heart rate distributions, correlation heatmap, box plots
- Trained Logistic Regression (with StandardScaler) and Decision Tree (max_depth=5)
- Evaluated with: Accuracy, Classification Report, Confusion Matrix, ROC Curve
- Visualized feature importance (Decision Tree) and coefficients (Logistic Regression)

### Key Results & Findings
- **Logistic Regression** outperforms Decision Tree on this dataset
- **Top predictive features:** Max heart rate (`thalach`), chest pain type (`cp`), vessel count (`ca`), ST depression (`oldpeak`)
- Higher max heart rate correlates with *no* disease — efficient cardiac function
- Cholesterol alone is a weaker predictor than commonly assumed

### Libraries
`pandas` · `numpy` · `matplotlib` · `seaborn` · `scikit-learn`

---

## Task 6: House Price Prediction

### Objective
Predict median house prices in California using property and demographic features.

### Dataset
**California Housing Dataset** — 20,640 census blocks, 8 features.  
Built into `scikit-learn` — no download required.

### Models Applied
| Metric | Linear Regression | Gradient Boosting |
|---|---|---|
| MAE | ~0.53 | ~0.37 |
| RMSE | ~0.73 | ~0.51 |
| R² | ~0.60 | ~0.80 |

### Approach
- Preprocessing: outlier removal for extreme room/occupancy values, StandardScaler for LR
- EDA: target distribution, feature histograms, correlation heatmap, geographic price map
- Trained Linear Regression and Gradient Boosting Regressor (200 estimators)
- Evaluated with MAE, RMSE, R²
- Visualized: Actual vs Predicted, Residual plot, Feature Importance

### Key Results & Findings
- **Gradient Boosting significantly outperforms Linear Regression** (R² 0.80 vs 0.60)
- **Median Income** is the single strongest predictor of house price
- **Location (Latitude/Longitude)** is the second most important factor — coastal areas are far more expensive
- Linear Regression underfits — house pricing relationships are inherently non-linear
- Residuals for Gradient Boosting are well-centered, indicating no systematic bias

### Libraries
`pandas` · `numpy` · `matplotlib` · `seaborn` · `scikit-learn`

---

## How to Run

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Run a notebook
```bash
cd Task1-Iris-EDA
jupyter notebook iris_eda.ipynb
```

All datasets are loaded programmatically inside the notebooks — **no manual downloads needed**.

---

## Submission Info
- **Internship:** DevelopersHub Corporation — AI/ML Engineering
- **Due Date:** 15th May, 2026
- **Tasks Completed:** 1, 3, 6 (3 of 6 required)
- **Submitted via:** Google Classroom (GitHub link)

---

## License
This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
