
# Fetal Health Classification using Machine Learning

## Overview

Cardiotocography (CTG) is used during pregnancy to monitor fetal heart rate and uterine contractions. It is monitor fetal well-being and allows early detection of fetal distress.

CTG interpretation helps in determining if the pregnancy is high or low risk. An abnormal CTG may indicate the need for further investigations and potential intervention.


This project focuses on building and deploying a machine learning model to classify fetal health outcomes
(Normal, Suspect, Pathological) using cardiotocography (CTG) data.

An interactive Streamlit web application was developed to allow real-time predictions using clinical input values.

---

## Dataset
- Source: Cardiotocography (CTG) dataset
- Samples: 2,126
- Features: 21 numerical CTG parameters
- Target:
  - 1 → Normal
  - 2 → Suspect
  - 3 → Pathological

---

## Exploratory Data Analysis
Key insights:
- Higher accelerations are associated with healthier fetuses
- Reduced short-term variability indicates fetal distress
- Histogram variance increases for pathological cases
- Some features show weak linear correlation but strong distributional differences

---

## Models Trained
- Logistic Regression
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- Gradient Boosting (Best)

---

## Best Model Performance
**Gradient Boosting Classifier (Tuned)**

- Cross-validation Accuracy: **94.24%**
- Test Accuracy: **91.55%**

### Classification Report
| Class | Precision | Recall | F1-score |
|------|----------|--------|----------|
| Normal | 0.95 | 0.97 | 0.96 |
| Suspect | 0.75 | 0.69 | 0.72 |
| Pathological | 0.84 | 0.74 | 0.79 |

---

## Streamlit Web Application
Features:
- Interactive sliders for all 21 CTG parameters
- Real-time fetal health prediction
- Probability distribution across classes
- Model trained using the same preprocessing pipeline

The application was deployed locally and exposed publicly using **ngrok**.

---

## How to Run Locally

```bash
pip install -r app/requirements.txt
streamlit run app/app.py
