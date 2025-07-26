# 🧠 Class 9: Object-Oriented Programming (OOP) in Python

## 📝 Topics Covered

- Class & Object in Python
- `__init__` Constructor Function
- Class & Instance Attributes
- Methods and Static Methods
- Abstraction
- Encapsulation
- `del` Keyword
- Inheritance:
  - Single Inheritance
  - Multi-level Inheritance
  - Multiple Inheritance
- `super()` Method
- `@classmethod`
- Polymorphism
- 5 Practice Tasks Based on OOP

---

## 📌 Code Snippets and Practice

### ✅ Class & Object

```python
class Student:
    name = "Ariful Islam"
    ID = "T181023"
    age = 27

student1 = Student()
print(student1.name, student1.ID, student1.age)
````

---

### ✅ Constructor (`__init__`)

```python
class Student:
    def __init__(self, name, ID, age):
        self.name = name
        self.ID = ID
        self.age = age
        print("Adding new student in Database...")

student1 = Student("Ariful Islam", "T181023", 27)
```

---

### ✅ Class vs Instance Attributes

```python
class Student:
    universityName = "IIUC"
    def __init__(self, name, ID):
        self.name = name
        self.ID = ID

student1 = Student("Arif", "T181023")
print(student1.name, Student.universityName)
```

---

### ✅ Instance Methods

```python
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks
    def welcome(self):
        print("Welcome", self.name)
    def get_marks(self):
        print(self.marks)

student1 = Student("Arif", 78)
student1.welcome()
```

---

### ✅ Static Methods

```python
class Student:
    @staticmethod
    def university():
        print("IIUC")

Student.university()
```

---

### ✅ Abstraction (Basic)

```python
class Car:
    def __init__(self):
        self.acc = False
        self.brk = False
        self.clu = False
```

---

### ✅ Encapsulation (Basic)

```python
class Student:
    @staticmethod
    def university():
        print("IIUC")
```

---

### ✅ Deleting Object Attributes

```python
class Student:
    universityName = "IIUC"
    def __init__(self,name, ID):
        self.name = name
        self.ID = ID

student1 = Student("Ariful Islam","T181023")
del student1.name  # Delete instance attribute
del Student.universityName  # Delete class attribute
```

---

### ✅ Single Inheritance

```python
class Car:
    @staticmethod
    def start():
        print("Car started...")

class ToyotaCar(Car):
    def __init__(self, name):
        self.name = name

car1 = ToyotaCar("X-Corolla")
car1.start()
```

---

### ✅ Multi-Level Inheritance

```python
class Car:
    def start(self):
        print("Car started...")

class ToyotaCar(Car):
    pass

class Xcorolla(ToyotaCar):
    pass
```

---

### ✅ Multiple Inheritance

```python
class A():
    variableA = "Welcome to class A"

class B():
    variableB = "Welcome to class B"

class C(A, B):
    variableC = "Welcome to class C"
```

---

### ✅ `super()` Method

```python
class ToyotaCar:
    def __init__(self, name):
        self.name = name

class XCorolla(ToyotaCar):
    def __init__(self, type, name):
        super().__init__(name)
        self.type = type

obj1 = XCorolla("Electric", "Prius")
print(obj1.name, obj1.type)
```

---

### ✅ Class Method

```python
class Person:
    name = "Anonymous"

    @classmethod
    def changeName(cls, name):
        cls.name = name

p1 = Person()
p1.changeName('Ariful Islam')
print(Person.name)
```

---

### ✅ Polymorphism

```python
print(1+2)                  # Output: 3
print("Ariful" + "Islam")  # Output: ArifulIslam
print([1,2,3] + [4,5,6])    # Output: [1, 2, 3, 4, 5, 6]
```

---

### ✅ Operator Overloading – Complex Number Class

```python
class Complex:
    def __init__(self, real, img):
        self.real = real
        self.img = img

    def showNumber(self):
        print(f"{self.real}+{self.img}i")

    def __add__(self, num2):
        print(f"{self.real + num2.real}+{self.img + num2.img}i")

    def __sub__(self, num2):
        print(f"{self.real - num2.real}+{self.img - num2.img}i")

x = Complex(1, 4)
y = Complex(5, 3)
x + y
x - y
```

