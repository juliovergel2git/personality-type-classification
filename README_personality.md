# 🧠 Personality Type Classification — Machine Learning Pipeline

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-F7931E?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## 📋 Project Overview

Can we predict whether a person is an **introvert or an extrovert** based purely on behavioural data?

This project builds a complete supervised machine learning pipeline to classify personality types using features such as time spent alone, stage fright, social event attendance, and posting frequency on social media.

Six classification algorithms are trained, evaluated, and compared — and the best model's hyperparameters are further optimised using `GridSearchCV` with 5-fold cross-validation.

---

## 🎯 Objectives

- Perform EDA to understand feature distributions and class balance
- Preprocess data (missing values, encoding, outlier removal)
- Train and compare 6 classification models
- Analyse feature importance to understand which behaviours are most predictive
- Optimise the best model via hyperparameter tuning

---

## 📊 Dataset

- **Records:** 2,900 rows (2,477 after cleaning)
- **Features:** 7 behavioural variables (time alone, social event attendance, stage fear, etc.)
- **Target:** `Personality` → Binary classification (Introvert / Extrovert)
- **Source:** Public personality classification dataset

---

## 🤖 Models Trained

| Model | Accuracy | F1-score |
|---|---|---|
| Logistic Regression | **92.74%** | **92.74%** |
| Gradient Boosting | **92.74%** | **92.74%** |
| SVM (RBF kernel) | **92.74%** | **92.74%** |
| Neural Network (MLP) | **92.74%** | **92.74%** |
| KNN (k=5) | 92.14% | 92.13% |
| Random Forest | 90.73% | 90.72% |

> Four models tied at ~92.7% — suggesting the problem is largely linearly separable.

---

## 🔍 Key Findings

**Most predictive features (Random Forest importance):**

| Feature | Importance |
|---|---|
| Drained after socializing | 24.1% |
| Time spent alone | 17.5% |
| Stage fear | 17.1% |
| Going outside | 12.6% |
| Post frequency | 11.0% |
| Social event attendance | 10.6% |
| Friends circle size | 7.1% |

**Insight:** Whether someone feels drained after socializing is the single strongest predictor of introversion — more so than how often they actually attend social events.

---

## 🗂️ Repository Structure

```
personality-type-classification/
│
├── personality_type_classification.ipynb   # Full ML pipeline notebook
├── personality_dataset.csv                 # Dataset
├── README.md                               # Project documentation
│
└── charts/                                 # Generated visualisations
    ├── 01_eda_overview.png
    ├── 02_feature_distributions.png
    ├── 03_model_comparison.png
    ├── 04_confusion_matrices.png
    ├── 05_feature_importance.png
    └── 06_optimised_nn_confusion.png
```

---

## 🛠️ Tools & Libraries

- **Python 3.11**
- **Pandas / NumPy** — data manipulation and preprocessing
- **Scikit-learn** — model training, evaluation, GridSearchCV
- **Matplotlib / Seaborn** — visualisation
- **Jupyter Notebook** — interactive analysis

---

## ▶️ How to Run

```bash
# Clone the repository
git clone https://github.com/juliovergel2git/personality-type-classification.git
cd personality-type-classification

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch the notebook
jupyter notebook personality_type_classification.ipynb
```

---

## 🔄 Next Steps

- [ ] Apply feature engineering (interaction terms) to push accuracy further
- [ ] Build a **Streamlit web app** for real-time personality prediction
- [ ] Explore **SHAP values** for deeper model interpretability
- [ ] Test on a larger, real-world dataset

---

## 👤 Author

**Julio Vergel** — Industrial Engineer | Data Science (in progress)  
🔗 [LinkedIn](https://linkedin.com/in/julio-vergel) · [GitHub](https://github.com/juliovergel2git)

---

*Dataset used for educational and portfolio purposes.*
