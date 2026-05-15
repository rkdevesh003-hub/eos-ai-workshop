# 🤖 WEEK-01 — AI Foundations + Python Basics
---

# SESSION 1 · PART A · WORLD OF AI
---

As an aspirant of AI learning I started my journey with excitement and curiosity. My tutors explained the answer for the question "WHY AI?".

AI is becoming a part of our daily life.

Some examples are:
- YouTube recommendations
- Chatbots
- Self driving cars
- Voice assistants
- Face recognition

AI helps machines learn patterns and make smart decisions using data.

---

# 🧠 AI ⊃ Machine Learning ⊃ Deep Learning
---

1. AI  
Machines doing smart tasks.

2. Machine Learning  
AI systems learning from data.

3. Deep Learning  
Machine Learning using neural networks.

---

# SESSION 1 · PART B · GIT & GITHUB
---

After the introduction to AI, my tutors introduced us to Git and GitHub.

Git is mainly used for version control while GitHub helps developers store projects online.

We learned:
- What is Git
- What is GitHub
- Creating repositories
- Uploading files
- Pushing projects
- README.md

Some commands shown during the session:

```bash
git init
git add .
git commit -m "first commit"
git push
```

My tutors also explained how developers work together using GitHub.

Most of this session was practical based, so it cannot be fully explained only using notes.

In fact, the notes and projects I am creating for this workshop are also being uploaded to GitHub.

---

# SESSION 2 · PART A · PYTHON FUNDAMENTALS
---

After learning the basics of AI, my tutors introduced Python programming.

Python is beginner friendly and very easy to understand. It is also one of the most used languages in Artificial Intelligence and Machine Learning.

My tutors suggested us to use Google Colab for coding.

---

# 📘 TOPICS WE LEARNT
---

## 1️⃣ Variables

Variables are like containers used to store values.

```python
name = "Aryan"
age = 16

print(name)
print(age)
print("Hello", name)
```

💡 The = sign means storing a value.

---

## 2️⃣ 🏷️ Data Types

The four main data types are:

- int
- float
- str
- bool

```python
print(type(16))
print(type(9.5))
print(type("Aryan"))
print(type(True))
```

---

## 3️⃣ ✨ f-Strings

f-strings are a clean way to print values.

```python
name = "Aryan"
age = 16

print(f"My name is {name} and I am {age}")
```

---

## 4️⃣ 📋 Lists and Dictionaries

Lists store multiple values.

```python
fruits = ["apple", "banana", "orange"]

print(fruits)
```

Dictionaries store values in key-value pairs.

```python
student = {
    "name": "Aryan",
    "age": 16
}

print(student)
```

---

## 5️⃣ 🔀 if / else

Conditional statements help programs make decisions.

```python
age = 18

if age >= 18:
    print("Eligible")
else:
    print("Not Eligible")
```

---

## 6️⃣ 🔁 Loops

Loops help repeat tasks.

```python
for i in range(5):
    print(i)
```

---

## 7️⃣ 🧩 Functions

Functions help organize code.

```python
def greet(name):
    print(f"Hello {name}")

greet("Aryan")
```

---

## 8️⃣ 🎯 List Comprehension

```python
numbers = [x*x for x in range(5)]

print(numbers)
```

---

# SESSION 2 · PART B · NUMPY
---

After learning Python basics, my tutors introduced NumPy.

NumPy stands for Numerical Python.

It is mainly used for:
- Arrays
- Mathematical operations
- Data processing
- Scientific computing

---

# 🔹 IMPORTING NUMPY
---

```python
import numpy as np
```

---

# 🔹 CREATING ARRAYS
---

```python
import numpy as np

arr = np.array([1, 2, 3, 4])

print(arr)
```

---

# 🔹 2D ARRAYS
---

```python
matrix = np.array([
    [1, 2, 3],
    [4, 5, 6]
])

print(matrix)
```

---

# 🔹 ARRAY ATTRIBUTES
---

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr.shape)
print(arr.ndim)
print(arr.size)
```

---

# 🔹 SPECIAL ARRAYS
---

## Zeros

```python
print(np.zeros((2, 3)))
```

## Ones

```python
print(np.ones((2, 2)))
```

## Identity Matrix

```python
print(np.eye(3))
```

---

# 🔹 INDEXING AND SLICING
---

```python
arr = np.array([10, 20, 30, 40])

print(arr[0])
print(arr[1:3])
```

---

# 🔹 RESHAPING ARRAYS
---

```python
arr = np.array([1, 2, 3, 4, 5, 6])

reshaped = arr.reshape(2, 3)

print(reshaped)
```

---

# 🔹 NUMPY OPERATIONS
---

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

print(a + b)
print(a - b)
print(a * b)
```

---

# 🔹 BROADCASTING
---

Broadcasting is one of the powerful features of NumPy.

```python
arr = np.array([1, 2, 3])

print(arr + 5)
```

---

# 🔹 BOOLEAN MASKING
---

```python
arr = np.array([1, 2, 3, 4, 5, 6])

print(arr[arr > 3])
```

---

# 🔹 RANDOM NUMBERS
---

```python
print(np.random.rand(5))
```

---

# 🧠 FINAL REFLECTION — WEEK 01
---

This week helped me understand:
- Basics of Artificial Intelligence
- Git and GitHub
- Python fundamentals
- NumPy arrays
- Mathematical operations using NumPy

This session increased my interest in AI and coding.
