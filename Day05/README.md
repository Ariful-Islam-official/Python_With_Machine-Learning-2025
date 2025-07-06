# 📘 Day 05 - While Loops in Python

Welcome to Day 5 of the **Python with Machine Learning** course!  
In this session, we focused on **looping structures** in Python, particularly the `while` loop — a powerful tool for repeating code based on conditions.

---

## ✅ Topics Covered

- Introduction to Loops
- `while` Loop
- Loop Control Statements:
  - `break`
  - `continue`
- `else` Clause with Loops
- 6 Practice Problems on While Loop

---

## 🧪 Code Examples

### 🔹 Without Loop (Hardcoded Print)
```python
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
print(7)
print(8)
print(9)
print(10)
````

### 🔹 Basic While Loop

```python
i = 0  # Iterator
while i <= 10:  # Condition
    print(i)
    i += 1  # Increment
```

---

## 🧪 Practice Problems

### 🟢 Practice 01 – Countdown from 10 to 1

```python
i = 10
while i >= 1:
    print(i)
    i -= 1
```

---

### 🟢 Practice 02 – Count Digits of a Number

```python
number = int(input("Enter a number: "))
i = 0
while number > 0:
    number = number // 10
    i += 1
print(i)  # Outputs digit count
```

---

### 🟢 Practice 03 – Sum Until 0 is Entered

```python
total = 0
number = int(input("Enter a number (0 to stop): "))
while number != 0:
    total += number
    number = int(input("Enter a number (0 to stop): "))
print(total)
```

---

### 🟢 Practice 04 – Reverse a Number

```python
number = int(input("Enter a number: "))
i = 0
while number != 0:
    digit = number % 10
    i = i * 10 + digit
    number = number // 10
print(i)
```

---

### 🟢 Practice 05 – Traverse a List Using While

```python
lists = [1, 2, 3, 5, 6, 78, 9, 10, 100, 20, 30, 40]
i = 0
while i < len(lists):
    print(lists[i])
    i += 1
```

---

### 🟢 Practice 06 – Search in Tuple

```python
tuples = (23, 46, 7, 89, 94, 1, 1, 13, 1)
number = int(input("Enter a number: "))
i = 0
while i < len(tuples):
    if tuples[i] == number:
        print("Found at index", i)
    i += 1
```

---

## 🧨 Loop Control Statements

### 🔹 break – Stop Loop After Match

```python
tuples = (23, 46, 7, 89, 94, 1, 1, 13)
number = int(input("Enter a number: "))
i = 0
while i < len(tuples):
    if tuples[i] == number:
        print("Found at index", i)
        break
    i += 1
```

---

### 🔹 continue – Skip Current Iteration

```python
i = 0
while i <= 5:
    if i == 3:
        i += 1
        continue
    print(i)
    i += 1
```

---

### 🔹 continue – Print Only Odd Numbers

```python
i = 0
while i <= 10:
    if i % 2 == 0:
        i += 1
        continue
    print(i)
    i += 1
```

---

### 🔹 else with while Loop

```python
i = 0
while i <= 10:
    if i % 2 == 0:
        i += 1
        continue
    print(i)
    i += 1
else:
    print("The program is End")
```
