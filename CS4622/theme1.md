# Python Programming (1)

## Table of Contents
- [Lecture 2: Data Types in Python](#lecture-2-data-types-in-python)
- [Lecture 3: Statements and Files](#lecture-3-statements-and-files)
- [Lecture 4: Functions and Iterators](#lecture-4-functions-and-iterators)
- [Lecture 5: OOP, Modules, and Packages](#lecture-5-oop-modules-and-packages)

---

# Lecture 2: Data Types in Python

## Numeric Types
- **int**: Integer values (e.g., `5`, `-3`)
- **float**: Floating-point values (e.g., `3.14`, `-0.5`)
- **complex**: Complex numbers (e.g., `2+3j`)

```python
x = 5        # int
y = 3.14     # float
z = 2 + 3j   # complex
```

## Boolean Type
- **bool**: `True` or `False`

```python
flag = True
if flag:
    print("It is True")
```

## Strings
- Immutable sequences of characters
- Can use single `'`, double `"`, or triple `'''`/`"""` quotes
- Supports slicing, indexing, and concatenation

```python
s = "Hello"
print(s[0])    # 'H'
print(s[-1])   # 'o'
print(s + " World")  # "Hello World"
```

## Lists
- Ordered, mutable collections
- Can hold mixed data types

```python
lst = [1, 2, "three"]
lst.append(4)
print(lst[2])  # "three"
```

## Tuples
- Ordered, immutable collections

```python
t = (1, 2, 3)
print(t[0])   # 1
```

## Sets
- Unordered collections of unique elements

```python
s = {1, 2, 2, 3}
print(s)  # {1, 2, 3}
```

## Dictionaries
- Key-value pairs, mutable

```python
d = {"a": 1, "b": 2}
print(d["a"])  # 1
d["c"] = 3
```

---

# Lecture 3: Statements and Files

## Statements
- **Assignment**: `x = 5`
- **Conditionals**: `if`, `elif`, `else`
- **Loops**: `for`, `while`
- **Control**: `break`, `continue`, `pass`

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

## File Handling
- `open(filename, mode)` with modes `'r'`, `'w'`, `'a'`, `'rb'`, `'wb'`
- `with` automatically closes files

```python
with open("data.txt", "r") as f:
    content = f.read()

with open("output.txt", "w") as f:
    f.write("Hello")
```

---

# Lecture 4: Functions and Iterators

## Functions
- Encapsulate logic, return values

```python
def square(x):
    return x*x

print(square(5))  # 25
```

## Lambda Functions
- Anonymous, single-expression

```python
f = lambda x, y: x + y
print(f(3, 4))  # 7
```

## Iterators
- Objects with `__iter__()` and `__next__()`

```python
lst = [1, 2, 3]
it = iter(lst)
print(next(it))  # 1
```

## Generators
- Use `yield`, lazy evaluation

```python
def gen_nums(n):
    for i in range(n):
        yield i

for val in gen_nums(3):
    print(val)
```

## Comprehensions
- List, Dict, Set comprehensions

```python
[x*x for x in range(5)]
{x: x*x for x in range(5)}
{x*x for x in range(5)}
```

---

# Lecture 5: OOP, Modules, and Packages

## Classes and Objects

```python
class Dog:
    def __init__(self, name):
        self.name = name
    
    def bark(self):
        print(f"{self.name} says woof")

d = Dog("Buddy")
d.bark()
```

## Inheritance

```python
class Animal:
    def eat(self):
        print("Eating")

class Cat(Animal):
    def meow(self):
        print("Meow")

c = Cat()
c.eat()
```

## Modules and Packages
- **Module**: single `.py` file
- **Package**: directory with `__init__.py`

```python
import math
print(math.sqrt(16))
```

```text
my_package/
    __init__.py
    module1.py
    module2.py
```

---

**End of Theme 1 Notes**
