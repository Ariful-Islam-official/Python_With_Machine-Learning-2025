# 📘 Day 02 - Expressions, Operators, Input & Strings in Python

Welcome to Day 2 of the **Python with Machine Learning** course!  
In this session, we explored different types of expressions and operators in Python, how to take user input, and how to work with strings.

---

## ✅ Topics Covered

- Types of Operators
- Expressions in Python
  - Constant Expressions
  - Arithmetic Expressions
  - Integral Expressions
  - Floating-point Expressions
  - Relational Expressions
  - Logical Expressions
  - Bitwise Expressions
- Comments in Python
- Taking Input from User
- Practice Problems (based on inputs)
- Strings in Python
  - Indexing & Slicing
  - String Functions
- Practice Problems (based on strings)

---

## 🧪 Code Examples

### 🔹 Arithmetic & Constant Expressions
```python
x = 10
y = 5
print(x + y)

x = 20 + 5  # Constant expression
print(x)
````

### 🔹 Arithmetic with Strings

```python
x = "arif"
res = x * 10
print(res)  # "arif" repeated 10 times
```

### 🔹 Integral Expression (casting float to int)

```python
x = 10
y = 5.5
print(x + int(y))
print(int(x + y))
```

### 🔹 Float Expression

```python
x = 100
y = 20
print(float(x + y))
print(x / y)
```

### 🔹 Relational & Logical Expressions

```python
result = (10 + 13) <= (2 + 3)
print(result)

result = (10 < 13) and (1 == 1)
print(result)

result = (10 > 13) or (1 == 1)
print(result)
```

### 🔹 Bitwise Operation

```python
result = 10 << 2
print(result)  # 40
```

---

## 🧮 User Input Examples

```python
x = float(input("x value = "))
y = 20
print(x + y)
```

```python
x = int(input("Enter number 1: "))
y = int(input("Enter number 2: "))
sum = x + y
print(sum)
```

```python
x = int(input("Enter a side of square: "))
area = x**2
print(area)
```

```python
result = not True and False or True
print(result)
```

---

## 🔤 String Handling

### 🔹 String Concatenation & Length

```python
firstName = "Ariful"
lastName = "Islam"
fullName = firstName + " " + lastName
print(len(fullName))  # Total characters
```

### 🔹 Indexing & Slicing

```python
print(fullName[0])      # First character
print(fullName[11])     # Last character
print(fullName[-3])     # Third from last
print(fullName[3:6])    # Slicing
print(fullName[7:12])   # Slicing
newName = fullName.replace("A", "B")
print(newName)
```

### 🔹 String Functions

```python
str = "i am a coder"

print(str.endswith("coder"))  # True
print(str.find("a"))          # Position of 'a'
print(str.count("a"))         # Count of 'a'
print(str.capitalize())       # Capitalize first letter
```

---

## 📝 Practice Tasks

Try the following:

* Write a program that calculates the area of a rectangle.
* Ask the user for their name and greet them using a message.
* Take two numbers and output both their sum and product.
* Use slicing to print your name in reverse.
* Find how many times the letter 'e' appears in a sentence.

---
