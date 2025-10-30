## 🧠 Class 18 — Support Vector Machine (SVM) & K-Nearest Neighbors (KNN)

Welcome to **Class 18** of the *Python with Machine Learning* course! 🚀
In this class, we explore two powerful supervised learning algorithms — **Support Vector Machine (SVM)** and **K-Nearest Neighbors (KNN)**.

---

### 🎯 Learning Objectives

By the end of this class, you will understand:

* What SVM and KNN are and how they work
* The mathematical concepts behind both algorithms
* How to implement SVM and KNN using **Scikit-learn**
* How to evaluate classification model performance

---

## 🔹 Support Vector Machine (SVM)

### 🔍 What is SVM?

SVM is a **supervised machine learning algorithm** used for **classification** and **regression** tasks.
It works by finding the **best hyperplane** that separates data points of different classes.

### 📈 Key Concepts

* **Hyperplane:** A decision boundary that separates different classes.
* **Support Vectors:** Data points closest to the hyperplane.
* **Margin:** The distance between the hyperplane and the nearest data points.
* **Kernel Trick:** Allows SVM to work with non-linear data by transforming it into higher dimensions.

### ⚙️ Formula

For a linear SVM,
[
f(x) = w^T x + b
]
SVM tries to find `w` and `b` that maximize the margin between classes.

---

### 💻 Example Code (SVM Implementation)

```python
# Import Libraries
import numpy as np
import pandas as pd
from sklearn import datasets
from sklearn.model_selection import train_test_split
from sklearn.svm import SVC
from sklearn.metrics import classification_report, confusion_matrix, accuracy_score

# Load Dataset
iris = datasets.load_iris()
X = iris.data
y = iris.target

# Split Dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create and Train SVM Model
svm_model = SVC(kernel='linear')
svm_model.fit(X_train, y_train)

# Predict
y_pred = svm_model.predict(X_test)

# Evaluate
print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))
print("Accuracy:", accuracy_score(y_test, y_pred))
```

---

## 🔹 K-Nearest Neighbors (KNN)

### 🔍 What is KNN?

KNN is a **non-parametric supervised learning algorithm** used for classification.
It classifies a new data point based on the **majority class** of its **K nearest neighbors**.

### 📈 Key Concepts

* **Distance Metrics:** Commonly Euclidean or Manhattan distance.
* **K Value:** Number of neighbors to consider.
* **Lazy Learning:** KNN doesn’t train a model; it stores all data points.

### ⚙️ Formula

For **Euclidean Distance**:
[
d(x, y) = \sqrt{\sum_{i=1}^{n} (x_i - y_i)^2}
]

---

### 💻 Example Code (KNN Implementation)

```python
# Import Libraries
from sklearn.neighbors import KNeighborsClassifier

# Create and Train KNN Model
knn_model = KNeighborsClassifier(n_neighbors=5)
knn_model.fit(X_train, y_train)

# Predict
y_pred_knn = knn_model.predict(X_test)

# Evaluate
print("Confusion Matrix:\n", confusion_matrix(y_test, y_pred_knn))
print("\nClassification Report:\n", classification_report(y_test, y_pred_knn))
print("Accuracy:", accuracy_score(y_test, y_pred_knn))
```

---

## ⚖️ Comparison Between SVM and KNN

| Feature         | SVM                                        | KNN                          |
| --------------- | ------------------------------------------ | ---------------------------- |
| Type            | Supervised                                 | Supervised                   |
| Learning Style  | Model-based                                | Instance-based (Lazy)        |
| Works Best For  | Small to medium datasets with clear margin | Large datasets or noisy data |
| Training Time   | High                                       | Low                          |
| Prediction Time | Low                                        | High                         |
| Parameter       | Kernel, C                                  | K value, distance metric     |

---

## 🧩 Model Evaluation Metrics

To assess model performance, we use:

* **Accuracy Score**
* **Confusion Matrix**
* **Precision, Recall, F1-Score**
* **Classification Report**

---

## 📘 Summary

✅ **SVM** separates data with a decision boundary (hyperplane).
✅ **KNN** classifies data based on the closest neighbors.
✅ Both are key classification algorithms in **Machine Learning**.

---

## 📂 Additional Resources

📄 Dataset used: *Iris Dataset (Scikit-learn built-in)*
📚 Library used: `scikit-learn`, `numpy`, `pandas`, `matplotlib`

