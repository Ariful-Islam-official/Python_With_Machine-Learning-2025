# 📘 Class 16 – Linear Regression & Gradient Descent  

In **Class 16**, we explored one of the most fundamental algorithms in Machine Learning: **Linear Regression**.  
We also implemented **Gradient Descent** manually to optimize the model parameters.  

---

## 🔹 Topics Covered  

### 📌 Linear Regression  
- What is Linear Regression?  
- Linear Regression Formula:  
  \[
  y = mx + c
  \]  
- One example of Linear Regression  

### 📌 Multiple Linear Regression  
- What is Multiple Linear Regression?  
- Multiple Linear Regression Formula:  
  \[
  y = b_0 + b_1x_1 + b_2x_2 + ... + b_nx_n
  \]  
- One example of Multiple Linear Regression  

### 📌 Linear Regression in Practice  
- Advantages & Disadvantages of Linear Regression  
- Loss Function Calculation (Mean Squared Error):  
  \[
  L = \frac{1}{n}\sum (y_{pred} - y_{true})^2
  \]  

### 📌 Gradient Descent for Linear Regression  
- Concept of minimizing the loss function  
- Updating weights & bias:  
  \[
  w = w - \alpha \cdot \frac{\partial L}{\partial w}
  \]  
  \[
  b = b - \alpha \cdot \frac{\partial L}{\partial b}
  \]  

---

## 🧪 Hands-On Code  

We implemented Linear Regression **from scratch** in Python using NumPy, Pandas, and Matplotlib.  
The model was trained on the **Salary Dataset**.  

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split

class LinearRegression():
    def __init__(self, learningRate, numberOfIterations):
        self.learningRate = learningRate
        self.numberOfIterations = numberOfIterations

    def fit(self, x, y):
        self.n, self.p = x.shape
        self.w = np.zeros(self.p)
        self.b = 0
        self.x = x
        self.y = y
        for i in range(self.numberOfIterations):
            self.update()

    def update(self):
        y_pred = self.predict(self.x)
        dw = -(2 * (self.x.T).dot(self.y - y_pred)) / self.n
        db = -2 * np.sum(self.y - y_pred) / self.n
        # updating
        self.w = self.w - self.learningRate * dw
        self.b = self.b - self.learningRate * db

    def predict(self, x):
        return x.dot(self.w) + self.b  # y = mx + c

salary_data = pd.read_csv("/content/drive/MyDrive/DataSet/salary_data.csv")
salary_data.isnull().sum()

x = salary_data.iloc[:, :-1].values
y = salary_data.iloc[:, 1].values

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.33, random_state=2)

model = LinearRegression(learningRate=0.02, numberOfIterations=2000)
model.fit(x_train, y_train)

print("w =", model.w[0])
print("b =", model.b)

