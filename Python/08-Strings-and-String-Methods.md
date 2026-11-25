# Chapter 8: Strings and String Methods

## 1. Introduction

A string is a sequence of characters enclosed in single quotes, double quotes, or triple quotes.

Strings are used to store and manipulate text in Python.

Example:

```python
name = "Somya"
language = 'Python'

print(name)
print(language)
```

**Output:**
```text
Somya
Python
```

## 2. Creating Strings

Python supports three common ways to create strings.

### A. Single Quotes

```python
text = 'Hello Python'
print(text)
```

### B. Double Quotes

```python
text = "Hello Python"
print(text)
```

### C. Triple Quotes

Triple quotes are used for multi-line strings.

```python
text = """Welcome
to Python
Programming"""

print(text)
```

**Output:**
```text
Welcome
to Python
Programming
```

## 3. String Indexing

Indexing is used to access individual characters from a string.

Python supports:

- Positive indexing: Starts from `0`.
- Negative indexing: Starts from `-1` from the end.

Example:

```python
name = "Python"

print(name[0])
print(name[2])
print(name[-1])
```

**Output:**
```text
P
t
n
```

## 4. String Slicing

Slicing is used to extract a portion of a string.

### Syntax

```python
string[start:stop:step]
```

- `start`: Starting index (included).
- `stop`: Ending index (excluded).
- `step`: Number of positions to move.

Example:

```python
text = "Python Programming"

print(text[0:6])
print(text[7:18])
print(text[:6])
print(text[::2])
```

**Output:**
```text
Python
Programming
Python
Pto rgamn
```

## 5. Strings are Immutable

Strings are immutable, which means their characters cannot be changed directly after creation.

Example:

```python
name = "Python"

# This will cause an error:
# name[0] = "J"
```

To create a modified string, assign a new value.

```python
name = "Python"
name = "J" + name[1:]

print(name)
```

**Output:**
```text
Jython
```

## 6. String Concatenation

Concatenation means joining two or more strings using the `+` operator.

Example:

```python
first = "Hello"
second = "World"

result = first + " " + second

print(result)
```

**Output:**
```text
Hello World
```

## 7. String Repetition

The `*` operator repeats a string a specified number of times.

Example:

```python
text = "Python "

print(text * 3)
```

**Output:**
```text
Python Python Python
```

## 8. Common String Methods

Python provides several built-in string methods.

| Method | Description |
|---|---|
| `upper()` | Converts characters to uppercase |
| `lower()` | Converts characters to lowercase |
| `capitalize()` | Capitalizes the first character |
| `title()` | Capitalizes the first character of each word |
| `strip()` | Removes leading and trailing whitespace |
| `replace()` | Replaces a specified substring |
| `split()` | Splits a string into a list |
| `join()` | Joins elements of an iterable into a string |
| `find()` | Returns the first position of a substring |
| `count()` | Counts occurrences of a substring |
| `startswith()` | Checks whether a string starts with a value |
| `endswith()` | Checks whether a string ends with a value |

### Example

```python
text = "hello python"

print(text.upper())
print(text.lower())
print(text.capitalize())
print(text.title())
```

**Output:**
```text
HELLO PYTHON
hello python
Hello python
Hello Python
```

### Using replace()

```python
text = "I like Java"

result = text.replace("Java", "Python")

print(result)
```

**Output:**
```text
I like Python
```

### Using split()

```python
text = "Python is easy"

result = text.split()

print(result)
```

**Output:**
```text
['Python', 'is', 'easy']
```

### Using join()

```python
words = ["Python", "is", "easy"]

result = " ".join(words)

print(result)
```

**Output:**
```text
Python is easy
```

## 9. String Formatting

String formatting allows us to insert variables and expressions into strings.

### A. f-Strings

F-strings provide a convenient way to format strings.

```python
name = "Somya"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

**Output:**
```text
My name is Somya and I am 20 years old.
```

### B. format() Method

```python
name = "Somya"
age = 20

print("My name is {} and I am {} years old.".format(name, age))
```

**Output:**
```text
My name is Somya and I am 20 years old.
```

## 10. Escape Characters

Escape characters are special sequences used to represent characters that cannot be easily typed directly.

| Escape Character | Meaning |
|---|---|
| `\n` | New line |
| `\t` | Horizontal tab |
| `\\` | Backslash |
| `\'` | Single quote |
| `\"` | Double quote |

Example:

```python
print("Hello\nPython")
print("Hello\tPython")
```

**Output:**
```text
Hello
Python
Hello    Python
```

## 11. Checking String Content

Python provides methods to check the content of a string.

| Method | Description |
|---|---|
| `isalpha()` | Checks whether all characters are alphabetic |
| `isdigit()` | Checks whether all characters are digits |
| `isalnum()` | Checks whether all characters are letters or digits |
| `isspace()` | Checks whether all characters are whitespace |
| `islower()` | Checks whether all cased characters are lowercase |
| `isupper()` | Checks whether all cased characters are uppercase |

Example:

```python
text = "Python123"

print(text.isalpha())
print(text.isdigit())
print(text.isalnum())
```

**Output:**
```text
False
False
True
```

## 12. Common String Mistakes

| Mistake | Explanation |
|---|---|
| Incorrect indexing | String indexing starts from 0 |
| Index out of range | Accessing an invalid position causes an error |
| Modifying a string directly | Strings are immutable |
| Incorrect slicing | The stop index is excluded |
| Forgetting quotes | String values must be enclosed in quotes |
| Confusing `find()` and `index()` | `find()` returns -1 when not found, while `index()` raises an error |

## 13. What I Learned

After completing this chapter, I understand:

- How to create strings in Python.
- Positive and negative string indexing.
- How string slicing works.
- Why strings are immutable.
- String concatenation and repetition.
- Common built-in string methods.
- How to format strings using f-strings and `format()`.
- How to use escape characters.
- How to check string content.

## Summary

Strings are an important data type in Python used to store and manipulate text. Python provides indexing, slicing, formatting, and several built-in methods to perform string operations.

Understanding strings is essential for handling text-based data in Python applications.

---

### Navigation

⬅️ Previous: [Loops in Python](07-Loops-in-Python.md)

➡️ Next: [Lists, Tuples, and Sets](09-Python-Lists-Tuples-and-Sets.md)