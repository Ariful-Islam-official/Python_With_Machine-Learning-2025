# 📘 Day 06 – For Loops, Range, Nested Loops, and Functions in Python

Welcome to Day 6 of the **Python with Machine Learning** course!  
In this session, we covered the most commonly used looping structure – the `for` loop – and introduced basic **function creation** in Python.

---

## ✅ Topics Covered

- `for` Loop in Python
- `for-else` Statement
- `range()` Function
  - with one, two, and three arguments
- Nested `for` Loops
- `pass` Statement
- Comparison between `while` and `for`
- 2 Practices based on `for` loops
- 3 Practices based on `for` + `range()`
- 2 Practices using both `while` and `for` loops
- Basic Function Syntax
- Using a Function to Reduce Code Repetition

---

## 🧪 Code Examples

### 🔹 While Loop over a List
```python
numbers = [1, 2, 3, 4, 5]
i = 0
while i < len(numbers):
    print(numbers[i])
    i += 1
````

### 🔹 For Loop over a List

```python
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)

veggis = ["potato", "Tomato", "cucumber"]
for i in veggis:
    print(i)
```

---

### 🔹 For-Else Loop

```python
name = "Ariful islam"
inputs = input("Enter a char: ")

for i in name:
    if i == inputs:
        print("Found")
        break
else:
    print("Not found")

print("Program END")
```

---

### 🔹 Using `range()` Function

```python
for i in range(5):
    print(i)  # 0 to 4

for i in range(1, 10):
    print(i)  # 1 to 9

for i in range(1, 10, 2):
    print(i)  # 1, 3, 5, 7, 9
```

---

### 🔹 Nested For Loop

```python
a = [1, 2, 3]
b = [6, 9, 12]

for i in a:
    for j in b:
        print(i, j)
```

---

### 🔹 pass Statement

```python
name = "Ariful islam"
inputs = input("Enter a char: ")

for i in name:
    if i == inputs:
        print("Found")
        break
    if name != inputs:
        pass
else:
    print("Not found")
```

---

## 🧪 Practice Problems

### 🟢 Practice 01 – Factorial Using `for` Loop

```python
num = int(input("Enter a Factorial number: "))
fact = 1
for i in range(1, num + 1):
    fact *= i
print(fact)
```

---

### 🟢 Practice 02 – Factorial Using `while` Loop

```python
num = int(input("Enter a Factorial number: "))
fact = 1
while num >= 1:
    fact *= num
    num -= 1
print(fact)
```

---

## 🧮 Before Using Functions (Repeated Code Example)

```python
x = 5
y = 4
sum = x + y
print(sum)

# 500 lines later...
x = 10
y = 20
sum = x + y
print(sum)

# More repetition
x = 50
y = 40
sum = x + y
print(sum)
```

---

## 🧠 Using a Function Instead

### 🔹 Basic Function Definition

```python
def sumValues(x, y):
    sum = x + y
    print(sum)

sumValues(5, 4)
sumValues(10, 20)
sumValues(50, 40)
sumValues(100, 200)
```
