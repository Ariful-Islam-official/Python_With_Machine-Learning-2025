# 📘 Python Class 8 - Lambda Functions, File I/O, and Exception Handling

## 🧠 Topics Covered:
- ✅ Lambda Functions in Python
- ✅ File I/O Operations
- ✅ Exception Handling in Python

---

## 🔹 Lambda Functions

### ➤ Basic Lambda Example:
```python
x = lambda a, b, c: a + b + c
print(x(10, 20, 30))  # Output: 60
````

### ➤ Lambda Inside a Function:

```python
def myfunction(n):
    print("This is a function")
    return lambda a: a**n

var = myfunction(10)
print(var(43))
```

### ➤ Practice Example:

```python
lists = [("Arif", 27), ("Asif", 29), ("Shakil", 23)]
lists.sort(key=lambda x: x[0])
print(lists)
```

---

## 🗃️ File I/O in Python

### ➤ Reading a File:

```python
f = open("demo.txt", "r")
data = f.read()
print(data)
f.close()
```

### ➤ Reading Lines:

```python
f = open("demo.txt", "r")
dataline1 = f.readline()
dataline2 = f.readline()
dataline3 = f.readline()
print(dataline2, end="")
print(dataline1, end="")
print(dataline3)
f.close()
```

### ➤ Creating & Writing Files:

```python
f = open("Documents/createFile.txt", "w")
f.write("Python batch")
f.close()
```

### ➤ Appending to File:

```python
f = open("Documents/createFile.txt", "a")
f.write("\nAdding some line")
f.close()
```

### ➤ Using `with` Statement:

```python
with open("demo.txt", "r") as f:
    data = f.read()
    print(data)
```

### ➤ Deleting a File:

```python
import os
os.remove("Documents")
```

---

## 🔄 File Handling Practice

### ➤ Practice 1 - Write:

```python
with open("notes.txt", "w") as f:
    f.write("Hi everyone, \nwe are learning about File handling \nusing JavaScript \nI enjoy coding in JavaScript")
```

### ➤ Practice 2 - Replace:

```python
with open("notes.txt", "r") as f:
    data = f.read()
    new_data = data.replace("JavaScript", "Python")

with open("notes.txt", "w") as f:
    f.write(new_data)
```

---

## ❗ Exception Handling

### ➤ Basic Try-Except:

```python
try:
    for i in range(1, 6):
        print(j)
except NameError as e:
    print(e)
```

### ➤ Multiple Try Blocks:

```python
try:
    x = 10
    y = 20
    sum = x + y
    print(sum)
except:
    print("Your sum has a problem")
```

### ➤ Multiple Exceptions:

```python
try:
    num = int(input("Enter a number: "))
    a = [6, 3, 9, 12]
    print(a[num])
except IndexError as e:
    print("There is an IndexError", e)
except ValueError as e:
    print("There is a ValueError", e)
```

### ➤ Finally Block:

```python
def function():
    try:
        num = int(input("Enter a number: "))
        a = [6, 3, 9, 12]
        print(a[num])
        return
    except IndexError as e:
        print("There is an IndexError", e)
        return
    except ValueError as e:
        print("There is a ValueError", e)
        return
    finally:
        print("END")

function()
```

### ➤ Raising an Exception:

```python
a = int(input('Enter a value between 5 and 9: '))
if a < 5 or a > 9:
    raise ValueError("Value should be between 5 and 9")
print(a)
```

---

