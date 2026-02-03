# Wine-Quality-Prediction-using-ML
 🍷 Wine Quality Prediction – End-to-End Machine Learning Project

This project demonstrates a complete **end-to-end Machine Learning workflow** using a real-world wine quality dataset.  
The focus is on **understanding the full ML process** — from data exploration to model evaluation and optimization — rather than just achieving high accuracy.

---

## 📌 Project Objective

The goal of this project is to predict whether a wine is **Good** or **Bad** based on its chemical properties.

To achieve this, the project covers:
- Data understanding and inspection
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model training and comparison
- Model evaluation using appropriate metrics
- Pipeline creation and hyperparameter tuning

---

## 📊 Dataset Information

- **Source:** Wine Quality Dataset (`winequality.csv`)
- **Rows:** 1599 wine samples
- **Features:** Chemical properties such as acidity, sulphates, alcohol, pH, etc.
- **Target Variable:** `quality` (score from 3 to 8)

Each row represents a single wine sample.

---

## 🔄 Problem Reformulation

The original problem was transformed into a **binary classification task**:

- **Good Wine (1):** Quality ≥ 7  
- **Bad Wine (0):** Quality < 7  

This makes the problem more practical and closer to real-world decision-making systems.

---

## 🧪 Exploratory Data Analysis (EDA)

Key observations:
- Most wines fall into quality scores **5 and 6**
- High-quality wines are relatively rare
- The dataset is **imbalanced**, with ~14% Good wines

EDA helped guide model selection and evaluation strategy.

---

## ⚙️ Machine Learning Workflow

### 1. Data Preparation
- Checked for missing values (none found)
- Separated features and target
- Performed train–test split (80/20) using **stratification**
- Applied feature scaling where required

### 2. Models Trained
The following models were trained and compared:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)

---

## 📈 Model Evaluation

Models were evaluated using:
- Accuracy
- Confusion Matrix
- Precision, Recall, and F1-score

### Best Performing Model
- **Random Forest Classifier**
- Test Accuracy: **~94%**
- High precision for identifying good-quality wines
- Moderate recall due to class imbalance

---

## 🔁 Pipeline & Hyperparameter Tuning

To demonstrate industry-standard practices:
- A **Pipeline** combining `StandardScaler` and `SVM` was created
- **GridSearchCV** with 5-fold cross-validation was used for tuning
- Best parameters:
  - `kernel = rbf`
  - `C = 100`
- Best cross-validated **F1-score ≈ 0.53**

Pipelines ensured consistent preprocessing and prevented data leakage.

---

## 🧠 Key Learnings

- Importance of EDA before modeling
- Handling imbalanced datasets correctly
- Why accuracy alone can be misleading
- When and why feature scaling is required
- How pipelines and cross-validation prevent data leakage
- How real-world ML systems are structured end-to-end

---

## 🏭 Real-World Relevance

This project closely mirrors real-world ML workflows used in industry:
- Structured data validation
- Model comparison
- Robust evaluation
- Reproducible pipelines
- Honest performance reporting

---

## 📂 Repository Structure

```text
├── data/
│   └── winequality.csv
├── notebook/
│   └── Wine_Quality_ML_Project.ipynb
├── report/
│   └── Wine_Quality_ML_Project_Report.docx
├── README.md
