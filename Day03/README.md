# 📘 Day 03 - Conditional Statements & Lists in Python

Welcome to Day 3 of the **Python with Machine Learning** course!  
In this class, we focused on decision-making in Python using conditional statements and introduced lists — one of Python’s most flexible data types.

---

## ✅ Topics Covered

- Conditional Statements
  - `if`, `else`, `elif`
  - Nested `if`
  - Single-line `if-else`
  - Clever `if-else` using expressions
- 3 Practice Problems in Class
- 4 Homework Problems based on Conditions
- Lists in Python
  - List Creation & Access
  - List Slicing
  - Common List Methods

---

## 🧪 Code Examples

### 🔹 Basic Conditional Statement
```python
age = int(input("Enter your age: "))
bangladeshLaw = 18

if age >= bangladeshLaw:
    print("Yes, you can vote!")
else:
    print("No, you can't vote!")
```

### 🔹 Nested if / elif Example

```python
gender = input("Enter your gender (m/f): ")
age = int(input("Enter your age: "))
bangladeshMaleLaw = 21
bangladeshFemaleLaw = 18

if gender == "m":
    if age >= bangladeshMaleLaw:
        print("Yes, You are eligible.")
    else:
        print("No, You are not yet eligible.")
else:
    if age >= bangladeshFemaleLaw:
        print("Yes, You are eligible.")
    else:
        print("No, You are not yet eligible.")
```

### 🔹 Age-Based Ticket System (Using if-elif-else)

```python
age = int(input("Enter your age: "))
if age < 5:
    print("Free Entry")
elif age <= 12:
    print("Child Ticket: 100 TK")
elif age <= 59:
    print("Regular Ticket: 250 TK")
else:
    print("Senior Ticket: 150 TK")
```

### 🔹 Single-line if-else

```python
age = int(input("Enter your age: "))
print("Free Entry") if age < 5 else (
    print("Child Ticket: 100 TK") if age <= 12 else (
        print("Regular Ticket: 250 TK") if age <= 59 else print("Senior Ticket: 150 TK")
    )
)
```

### 🔹 Clever if-else (Advanced)

```python
age = int(input("Enter your age: "))
result = (
    (("Senior Ticket: 150TK", "Regular Ticket: 250TK")[age <= 59], "Child Ticket: 100 TK")[age <= 12],
    "Free Entry"
)[age < 5]
print(result)
```

---

## 🧾 Lists in Python

### 🔹 List Creation & Access

```python
bioData = [2, 4, 4, 5, 1, 2, 6]
```

### 🔹 List Methods

```python
bioData.pop(1)  # Removes value at index 1
print(bioData)  # Output: [2, 4, 5, 1, 2, 6]
```

### 🔹 Example of Immutable String

```python
Name = "Ariful"
# Name[0] = "B"  # ❌ Error: Strings are immutable
```

---

## 🏠 Homework Practice (Based on Conditions)

1. Check if a number is positive, negative, or zero.
2. Ask a user for two numbers and print the greater one.
3. Grade system using marks:

   * 90–100 = A+
   * 80–89 = A
   * ...
4. Check if a year is a leap year.



