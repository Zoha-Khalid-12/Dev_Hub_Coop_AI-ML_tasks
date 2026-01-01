# Task 3 — Heart Disease Prediction (DevelopersHub Internship)

This project is part of the **AI/ML Engineering DevelopersHub Internship Tasks** — **Task 3: Heart Disease Prediction**.

## Objective
Build a machine learning model to predict whether a person is likely to have **heart disease** based on medical attributes.  
The notebook includes:
- Data cleaning & preprocessing
- Exploratory Data Analysis (EDA)
- Model training (Logistic Regression + Decision Tree)
- Evaluation (Accuracy, Confusion Matrix, ROC Curve, AUC)
- Feature importance analysis
- Threshold tuning (precision/recall tradeoff)

---

## Dataset
This project uses a Heart Disease dataset (UCI-based).  
**Kaggle link:** https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data

> Note: The dataset is not included in this repository by default.  
> You can download it from Kaggle or load it from Google Drive in Colab.

---

## Tech Stack
- Python
- Google Colab
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## Models Used
1. **Logistic Regression**
2. **Decision Tree Classifier**

---

## Evaluation Metrics
- Accuracy
- Confusion Matrix
- ROC Curve
- ROC-AUC Score

Additionally:
- **Threshold tuning** was performed to reduce False Negatives (important in medical prediction tasks).

---

## Project Structure
```text
Task_3/
├── notebooks/
│   └── Task_3.ipynb
├── model/
│   └── heart_disease_model.joblib
├── README.md
├── .gitignore
└── requirements.txt
