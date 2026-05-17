# 🐍 Python Cheat Sheet

> Python is a programming language that's easy to read and beginner-friendly. Great for data, automation, web dev, and more.

---

## 🚀 Your First Program

```python
print("Hello, World!")    # Prints text to screen
```

Run it: `python filename.py` or `python3 filename.py`

---

## 📦 Variables & Data Types

```python
# You don't need to specify the type — Python figures it out
name = "Adhithya"          # String (text)
age = 21                   # Integer (whole number)
height = 5.9               # Float (decimal)
is_gamer = True            # Boolean (True/False)
hobbies = ["coding", "gaming", "music"]  # List (array)
```

---

## 📊 Common Data Types

```python
# String
text = "Hello"
text[0]            # 'H'  (index starts at 0)
text[1:4]          # 'ell' (slice)
len(text)          # 5  (length)

# Number
x = 10
y = 3
x + y   # 13
x - y   # 7
x * y   # 30
x / y   # 3.33
x // y  # 3  (integer division)
x % y   # 1  (remainder)
x ** y  # 1000 (power)

# List (ordered, changeable)
items = ["a", "b", "c"]
items.append("d")     # ["a", "b", "c", "d"]
items[0]              # "a"
items[-1]             # "d" (last item)
len(items)            # 4
items.remove("b")     # ["a", "c", "d"]

# Dictionary (key-value pairs)
person = {"name": "Adhithya", "age": 21}
person["name"]        # "Adhithya"
person["age"]         # 21
person["city"] = "Chennai"  # Add new key
```

---

## 🔄 If/Else (Decisions)

```python
age = 18

if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")

# Multiple conditions
if age >= 18 and has_id == True:
    print("Can enter")

if age < 18 or not has_permission:
    print("Cannot enter")
```

---

## 🔁 Loops (Repeating)

```python
# For loop — go through each item
for i in range(5):
    print(i)         # 0, 1, 2, 3, 4

for name in ["Kai", "Sasa", "Helsa"]:
    print(f"Hello, {name}!")   # f-string = embed variables in text

# While loop — repeat until condition is false
count = 0
while count < 5:
    print(count)
    count += 1        # count = count + 1
```

---

## 📦 Functions (Reusable Code)

```python
# Define a function
def greet(name):
    return f"Hello, {name}!"

# Call it
message = greet("Adhithya")
print(message)         # Hello, Adhithya!

# Function with default value
def multiply(a, b=2):
    return a * b

multiply(5)       # 10  (b defaults to 2)
multiply(5, 3)    # 15  (b is 3)
```

---

## 📁 Working with Files

```python
# Read a file
with open("file.txt", "r") as f:
    content = f.read()
    print(content)

# Write to a file
with open("file.txt", "w") as f:
    f.write("Hello, World!")

# Append to a file
with open("file.txt", "a") as f:
    f.write("\nNew line")
```

---

## 📦 Imports (Using Other Code)

```python
import math
print(math.sqrt(16))      # 4.0

import random
print(random.randint(1, 10))  # Random number between 1-10

import os
print(os.listdir("."))    # List files in current folder

from datetime import datetime
print(datetime.now())     # Current date and time
```

---

## 🚨 Common Beginner Mistakes

```python
# Wrong
if name = "Adhithya":    # = is assignment, not comparison!

# Right
if name == "Adhithya":   # == is comparison

# Wrong
for i in range(len(items)):  # Overcomplicated

# Right
for item in items:           # Simpler and cleaner

# Wrong
def my_function():
return value     # Wrong indentation!

# Right
def my_function():
    return value  # Python uses indentation (spaces/tabs) not {}
```

---

## 💡 Pro Tips

- **Indentation matters** — Python uses spaces (or tabs) instead of `{}` to define blocks
- Use **4 spaces** for indentation (PEP 8 standard)
- Use **f-strings** for easy text: `f"My name is {name}"`
- Name variables clearly: `user_age` not `ua`
- Test in the Python REPL: just type `python` in terminal and start coding
- When stuck, `print()` everything — best debugging tool
