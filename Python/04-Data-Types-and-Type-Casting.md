# Chapter 4: Data Types and Type Casting

## 1. Introduction

Data types define the kind of value a variable can store.

Python provides different built-in data types to store numbers, text, collections, and logical values.

Python is dynamically typed, which means we do not need to declare a variable's data type explicitly.

Example:

```python
x = 10
name = "Somya"

print(x)
print(name)
```

## 2. Types of Data Types in Python

Python has several built-in data types.

| Category | Data Types |
|---|---|
| Numeric | int, float, complex |
| Text | str |
| Boolean | bool |
| Sequence | list, tuple, range |
| Mapping | dict |
| Set | set, frozenset |
| Binary | bytes, bytearray, memoryview |
| None | NoneType |

## 3. Numeric Data Types

Numeric data types are used to store numbers.

### A. Integer (int)

Integer values are whole numbers without decimal points.

```python
age = 20
marks = 85

print(age)
print(marks)
print(type(age))
```

**Output:**
```text
20
85
<class 'int'>
```

### B. Float (float)

Float values contain decimal points.

```python
price = 99.50
percentage = 85.5

print(price)
print(percentage)
print(type(price))
```

**Output:**
```text
99.5
85.5
<class 'float'>
```

### C. Complex (complex)

Complex numbers contain a real part and an imaginary part.

Python uses `j` to represent the imaginary part.

```python
number = 5 + 3j

print(number)
print(type(number))
```

**Output:**
```text
(5+3j)
<class 'complex'>
```

## 4. String Data Type (str)

A string is a sequence of characters enclosed in single quotes, double quotes, or triple quotes.

```python
name = "Somya"
course = 'Computer Science'

print(name)
print(course)
print(type(name))
```

**Output:**
```text
Somya
Computer Science
<class 'str'>
```

Strings are immutable, which means their individual characters cannot be changed after creation.

## 5. Boolean Data Type (bool)

Boolean data types represent two values:

- `True`
- `False`

They are commonly used in conditions and comparisons.

```python
x = 10
y = 20

print(x < y)
print(x > y)
```

**Output:**
```text
True
False
```

## 6. Sequence Data Types

Sequence data types store multiple values in an ordered collection.

### A. List

A list stores multiple values and allows modification.

```python
fruits = ["Apple", "Mango", "Banana"]

print(fruits)
print(type(fruits))
```

**Output:**
```text
['Apple', 'Mango', 'Banana']
<class 'list'>
```

### B. Tuple

A tuple stores multiple values but cannot be modified after creation.

```python
numbers = (10, 20, 30)

print(numbers)
print(type(numbers))
```

**Output:**
```text
(10, 20, 30)
<class 'tuple'>
```

### C. Range

The `range()` function generates a sequence of integers.

```python
numbers = range(1, 5)

print(list(numbers))
```

**Output:**
```text
[1, 2, 3, 4]
```

## 7. Dictionary Data Type (dict)

A dictionary stores data in key-value pairs.

```python
student = {
    "name": "Somya",
    "age": 20,
    "course": "CSE"
}

print(student)
print(type(student))
```

**Output:**
```text
{'name': 'Somya', 'age': 20, 'course': 'CSE'}
<class 'dict'>
```

## 8. Set Data Type (set)

A set stores unique values and does not maintain a fixed order.

```python
numbers = {10, 20, 30, 10}

print(numbers)
print(type(numbers))
```

**Possible Output:**
```text
{10, 20, 30}
<class 'set'>
```

Duplicate values are automatically removed.

## 9. None Data Type (NoneType)

`None` represents the absence of a value.

```python
result = None

print(result)
print(type(result))
```

**Output:**
```text
None
<class 'NoneType'>
```

## 10. Checking Data Types

Python provides the `type()` function to identify the data type of a variable.

Example:

```python
a = 100
b = 10.5
c = "Python"
d = True

print(type(a))
print(type(b))
print(type(c))
print(type(d))
```

**Output:**
```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

Python also provides `isinstance()` to check whether an object belongs to a particular type.

```python
age = 20

print(isinstance(age, int))
```

**Output:**
```text
True
```

## 11. Type Casting in Python

Type casting means converting a value from one data type to another.

Python supports several conversion functions.

| Function | Conversion |
|---|---|
| `int()` | Converts to integer |
| `float()` | Converts to float |
| `str()` | Converts to string |
| `bool()` | Converts to Boolean |
| `complex()` | Converts to complex number |
| `list()` | Converts to list |
| `tuple()` | Converts to tuple |
| `set()` | Converts to set |

### A. Integer Conversion

```python
x = 10.8
y = int(x)

print(y)
```

**Output:**
```text
10
```

Note: `int()` removes the decimal portion; it does not round the number.

### B. Float Conversion

```python
x = 10
y = float(x)

print(y)
```

**Output:**
```text
10.0
```

### C. String Conversion

```python
age = 20
result = str(age)

print(result)
print(type(result))
```

**Output:**
```text
20
<class 'str'>
```

### D. Boolean Conversion

```python
print(bool(1))
print(bool(0))
print(bool(""))
```

**Output:**
```text
True
False
False
```

## 12. Implicit and Explicit Type Conversion

Python supports two main types of conversion.

### A. Implicit Type Conversion

Python automatically converts one data type into another when appropriate.

Example:

```python
a = 10
b = 2.5

result = a + b

print(result)
print(type(result))
```

**Output:**
```text
12.5
<class 'float'>
```

Here, Python automatically converts the integer into a float.

### B. Explicit Type Conversion

Explicit conversion happens when the programmer manually converts a value using functions such as `int()`, `float()`, or `str()`.

Example:

```python
a = "100"
b = int(a)

print(b + 50)
```

**Output:**
```text
150
```

## 13. Mutable and Immutable Data Types

Python data types can also be classified based on whether their values can be changed after creation.

| Mutable | Immutable |
|---|---|
| List | Integer |
| Dictionary | Float |
| Set | String |
| Bytearray | Tuple |
| | Boolean |
| | Frozenset |

**Mutable:** The object can be modified after creation.

**Immutable:** The object cannot be modified after creation.

## 14. Common Type Conversion Errors

Some conversions are not possible and may produce errors.

Example:

```python
value = "Hello"
number = int(value)
```

**Output:**
```text
ValueError: invalid literal for int()
```

This happens because `"Hello"` cannot be converted into an integer.

Always check the input before performing conversions.

## 15. What I Learned

After completing this chapter, I understand:

- Different built-in Python data types.
- Numeric, string, and Boolean data types.
- Lists, tuples, dictionaries, and sets.
- How to use `type()` and `isinstance()`.
- How type casting works.
- Difference between implicit and explicit conversion.
- Difference between mutable and immutable data types.
- Common type conversion errors.

## Summary

Data types determine what kind of values Python variables can store. Type casting allows us to convert values between different data types.

Understanding data types and type conversion is important for writing reliable Python programs and handling different kinds of data.

---

### Navigation

⬅️ Previous: [Python Syntax and Variables](03-Python-Syntax-and-Variables.md)

➡️ Next: [Operators and Expressions](05-Operators-and-Expressions.md)