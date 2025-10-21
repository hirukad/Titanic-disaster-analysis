# Titanic-disaster-analysis
A machine learning model that can predict whether a passenger on the titanic is survived(1) or not survived(0) based on their features

# Titanic Survival Prediction 🛳️

Predicting passenger survival on the Titanic using machine learning and feature engineering.  

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/) 
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3.0-green)](https://scikit-learn.org/)  
[![Kaggle](https://img.shields.io/badge/Kaggle-Titanic-orange)](https://www.kaggle.com/c/titanic)

---

## 📚 Project Overview
This project explores the Titanic dataset and builds ML models to predict survival.  
It demonstrates:
- Exploratory Data Analysis (EDA)
- Feature engineering
- Preprocessing and encoding
- Model training and evaluation (Logistic Regression, Random Forest)

---

## 🗂 Dataset
**Source:** [Kaggle Titanic](https://www.kaggle.com/c/titanic/data)  

| Dataset | Rows | Features |
|---------|------|---------|
| Training | 891 | 12 |
| Test | 418 | 11 |

**Key Features:** `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`, `Cabin`, `Name`

---

## ⚙️ Feature Engineering
- **FamilySize** = `SibSp + Parch + 1`  
- **IsAlone** = 1 if passenger is alone, else 0  
- **Title** extracted from `Name` (Mr, Mrs, Miss, etc.)  
- **AgeGroup** = binned age categories  
- **Deck** = extracted from `Cabin`  
- **One-hot encoding** for categorical variables  
- Boolean columns converted to 0/1  

---

## 🔧 Data Preprocessing
- Missing `Age` filled with median  
- Missing `Embarked` filled with most common port  
- Scaling numeric features for Logistic Regression  

---

## 🤖 Models
- Logistic Regression (with 5-fold cross-validation)  
- Random Forest Classifier  

**Metrics Used:** Accuracy, F1 Score, Confusion Matrix  

**Example Performance:**
[[93 12]
 [19 55]]
Accuracy: 0.8268156424581006
F1 Score: 0.7801418439716312
