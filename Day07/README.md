# 📘 Day 07 – Functions & Recursion in Python

Welcome to Day 7 of the **Python with Machine Learning** course!  
This class focused on building reusable logic with **functions**, handling various types of arguments, and diving into **recursive function calls**.

---

## ✅ Topics Covered

- Function Syntax & Structure
- Function with `return`
- Arbitrary Arguments (`*args`)
- Keyword Arguments
- Arbitrary Keyword Arguments (`**kwargs`)
- Default Parameters
- 6 Practice Problems Based on Functions
- Recursion
  - Recursive Thinking
  - 2 Recursive Function Practices

---

## 🧠 Basic Function Syntax

### 🔹 No Parameters
```python
def sum():
    x = 10 + 20
    print(x)

sum()
````

### 🔹 With Return Value

```python
def sum():
    x = 10 + 20
    return x

print(sum())
```

---

## 🧾 Advanced Function Arguments

### 🔹 Arbitrary Arguments (`*args`)

```python
def my_function(*arif):
    sum = arif[0] + arif[1] + arif[2]
    print(sum)

my_function(1, 2, 3)
```

---

### 🔹 Keyword Arguments

```python
def sum(a, b, c):
    return a - b + c

print(sum(b=10, a=20, c=30))  # ➝ Output: 40
```

---

### 🔹 Arbitrary Keyword Arguments (`**kwargs`)

```python
def sum(**keyword):
    x = keyword["a"] + keyword["b"] - keyword["c"]
    return x

print(sum(b=10, a=20, c=30))  # ➝ Output: 0
```

---

### 🔹 Default Parameters

```python
def sum(a, b=0, c=0, d=0):
    return a + b + c + d

print(sum(10))  # ➝ Output: 10
```

---

## 🧪 Practice Problems

### 🟢 Practice 01 – Count Vowels

```python
def count_vowels(name):
    count = 0
    vowels = "aeiouAEIOU"
    for char in name:
        if char in vowels:
            count += 1
    print(count)

count_vowels("Ariful Islam")
```

---

### 🟢 Practice 02 – Print List

```python
def print_list(a):
    print(*a)

lists = [1, 2, 3, 4]
print_list(lists)
```

---

### 🟢 Practice 03 – Prime Check

```python
def prime(n):
    if n < 2:
        print("Not a prime number")
        return
    for i in range(2, n):
        if n % i == 0:
            print("Not a prime number")
            return
    print("Prime number")

prime(101)
```

---

## 🔁 Recursion

### 🔹 Print Countdown Recursively

```python
def myFunction(num):
    if num <= 0:
        return
    print(num)
    myFunction(num - 1)

myFunction(5)
```

---

### 🔹 Recursive List Printer

```python
def listFunction(list, index=0):
    if index == len(list):
        return
    print(list[index])
    listFunction(list, index + 1)
    print(index)

listFunction([10, 20, 30, 40])
```
