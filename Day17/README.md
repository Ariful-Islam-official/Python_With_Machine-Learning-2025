# 📘 Class 17 – Logistic Regression  

In **Class 17**, we extended our study of regression by exploring **Logistic Regression**, one of the most important algorithms for **classification problems**.  

---

## 🔹 Topics Covered  

### 📌 Linear Regression (Recap)  
- Review of Linear Regression concepts  
- Formula and intuition behind regression  

### 📌 Logistic Regression  
- Introduction to Logistic Regression  
- Differences between Linear & Logistic Regression  
- Logistic Function (Sigmoid):  
  \[
  f(x) = \frac{1}{1 + e^{-x}}
  \]  

### 📌 Logistic Regression Workflow  
1. **Data Collection & Preparation**  
   - Cleaning, handling missing values, feature selection  
2. **Model Setup**  
   - Choosing Logistic Regression for classification tasks  
3. **Training (Fitting)**  
   - Using dataset to fit the model  
4. **Cost Function**  
   - Log Loss (Cross-Entropy Loss)  
5. **Prediction**  
   - Class probabilities → 0 or 1 classification  
6. **Model Evaluation**  
   - Accuracy, Precision, Recall, F1-score, ROC-AUC  

---

## ✅ Advantages of Logistic Regression  
- Simple and easy to implement  
- Works well for binary classification problems  
- Provides probability estimates  
- Interpretable coefficients  

## ❌ Disadvantages of Logistic Regression  
- Not suitable for non-linear problems without feature engineering  
- Assumes linear relationship between features and log-odds  
- Sensitive to outliers and multicollinearity  

---

## 🧪 Hands-On Code (Example)  

```python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report

# Example dataset (diabetes dataset)
data = pd.read_csv("/content/drive/MyDrive/DataSet/diabetes.csv")

# Features & Target
x = data.drop("Outcome", axis=1)
y = data["Outcome"]

# Split data
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=42)

# Model setup
model = LogisticRegression(max_iter=200)
model.fit(x_train, y_train)

# Prediction
y_pred = model.predict(x_test)

# Evaluation
print("Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))
````

