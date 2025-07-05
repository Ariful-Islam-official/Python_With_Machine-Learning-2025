# 📘 Day 04 - Lists, Tuples, Dictionaries & Sets in Python

Welcome to Day 4 of the **Python with Machine Learning** course!  
In this session, we explored core Python data structures — mutable and immutable collections — and practiced how to use them effectively in real problems.

---

## ✅ Topics Covered

- Lists (Review)
- Tuples in Python
  - Tuple Characteristics
  - Tuple Methods
- Dictionary in Python
  - Accessing Items
  - Nested Dictionaries
  - Dictionary Methods
- Sets in Python
  - Properties of Sets
  - Set Methods (union, intersection, pop)
- 4 Practice Problems on:
  - List & Tuple
  - Dictionary & Set

---

## 🧪 Code Examples

### 🔹 List (Mutable)
```python
lists = ["Ariful Islam", 27, "IIUC", 3.46]
lists[0] = "Arif"  # Lists are mutable
print(lists)
````

---

### 🔹 Tuple (Immutable)

```python
tuples = ("Ariful Islam", 27, "IIUC", 3.46)
tuples1 = (1,)  # Tuple with one item must have a trailing comma
print(tuples)
print(tuples1)
```

### 🔹 Tuple Methods

```python
tup = (3, 1, 1, 2)
print(tup.index(1))   # Output: 1 (first occurrence)
print(tup.count(0))   # Output: 0
```

---

## 🧪 Practice on List & Tuple

### 🟢 Practice 01 – Favorite Books List

```python
lists = []
book1 = input("Enter your first fav Book: ")
book2 = input("Enter your second fav Book: ")
book3 = input("Enter your third fav Book: ")

lists.append(book1)
lists.append(book2)
lists.append(book3)
print(lists)
```

### 🟢 Practice 02 – Palindrome Check with List

```python
example01 = [4, 1, 6, 5, 4]
copy_example = example01.copy()
copy_example.reverse()

if example01 == copy_example:
    print("Palindrome")
else:
    print("Not Palindrome")
```

---

## 🧾 Dictionary in Python

```python
info = {
    "name": "Ariful islam",
    "age": 27,
    "learning": "Coding",
    "isAdult": True,
    "cgpa": 3.46,
    "subjects": ["Python", "C", "C++", "JS"],
    "topics": ("Dict", "Set")
}

print(info["cgpa"])
print(info["isAdult"])
# print(info["myName"])  # ❌ KeyError if key doesn't exist
```

---

### 🔹 Nested Dictionary

```python
Arif = {
    "name": "Ariful islam",
    "ID": "T181023",
    "Marks": {
        "DC": 75,
        "C Programming": 85,
        "MathI": 90
    }
}

Arif_update = {
    "Group": "A",
    "blood Group": "B+"
}
```

---

## 🧾 Set in Python

### 🔹 Properties & Duplicates

```python
sets = {2, 3, 4, 5.00, "Ariful", "Ariful", None, True, (1, 2, 3, 4)}
print(sets)
```

### 🔹 Set Methods

```python
var = {1, "Ariful", 0.06}
print(var.pop())  # Removes a random item

set1 = {1, 2, 3}
set2 = {3, 4, 5}
print(set1.union(set2))         # Combines sets
print(set1.intersection(set2))  # Common elements
```

---

## 🧪 Practice on Dictionary & Set

### 🟢 Practice – Student Marks Dictionary

```python
marks = {}
phy = int(input("Enter physics marks: "))
math = int(input("Enter math marks: "))
chem = int(input("Enter chemistry marks: "))

marks.update({"phy": phy})
marks.update({"math": math})
marks.update({"chem": chem})
print(marks)
```

### 🟢 Practice – Set with Tuples

```python
set_ = {("int", 9), ("float", "9.0")}
print(set_)
```
