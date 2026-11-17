# Chapter 3: Python Syntax and Variables

## 1. Introduction

Python syntax refers to the rules used to write Python programs. Python has a simple and readable syntax, making it easier to understand and maintain code.

Variables are used to store data that can be accessed and modified during program execution.

## 2. Python Statements

A statement is an instruction executed by Python.

Example:

```python
print("Hello Python")
x = 10
y = 20
print(x + y)
```

**Output:**
```text
Hello Python
30
```

Python generally uses a new line to separate statements. Semicolons can separate multiple simple statements, but using separate lines is recommended.

## 3. Python Indentation

Indentation means spaces at the beginning of a line.

Python uses indentation to define blocks of code.

Example:

```python
age = 20

if age >= 18:
    print("You are eligible to vote")
```

**Output:**
```text
You are eligible to vote
```

Incorrect indentation can cause an `IndentationError`.

**Best Practice:** Use four spaces for each indentation level.

## 4. Variables in Python

A variable is a name that refers to a value stored in memory.

Example:

```python
name = "Somya"
age = 20
marks = 85.5

print(name)
print(age)
print(marks)
```

**Output:**
```text
Somya
20
85.5
```

In Python, variables do not need an explicit data type declaration.

## 5. Variable Assignment

The assignment operator (`=`) is used to assign a value to a variable.

Example:

```python
x = 10
y = 20

print(x)
print(y)
```

**Output:**
```text
10
20
```

The value of a variable can be changed during program execution.

```python
number = 10
number = 25

print(number)
```

**Output:**
```text
25
```

## 6. Rules for Naming Variables

Python follows certain rules when naming variables:

1. A variable name must begin with a letter or underscore.
2. It cannot begin with a number.
3. It can contain letters, numbers, and underscores.
4. Spaces are not allowed.
5. Variable names are case-sensitive.
6. Python keywords cannot be used as variable names.

Valid variable names:

```python
name = "Somya"
age = 20
student_marks = 90
_total = 500
```

Invalid variable names:

```python
# 2name = "Somya"
# student name = "Somya"
# class = "CSE"
```

## 7. Multiple Variable Assignment

Python allows assigning values to multiple variables in a single statement.

### Assigning Different Values

```python
name, age, marks = "Somya", 20, 90

print(name)
print(age)
print(marks)
```

**Output:**
```text
Somya
20
90
```

### Assigning the Same Value

```python
a = b = c = 10

print(a, b, c)
```

**Output:**
```text
10 10 10
```

## 8. Constants in Python

A constant is a value that is intended to remain unchanged throughout a program.

Python does not have a special keyword to declare constants.

By convention, constant names are written in uppercase letters.

Example:

```python
PI = 3.14159
MAX_USERS = 100

print(PI)
print(MAX_USERS)
```

**Output:**
```text
3.14159
100
```

Uppercase naming indicates that these values should not be changed.

## 9. Taking User Input

The `input()` function is used to accept information from the user.

Example:

```python
name = input("Enter your name: ")

print("Hello", name)
```

**Sample Output:**
```text
Enter your name: Somya
Hello Somya
```

By default, `input()` returns data as a string.

To accept numeric input, use type conversion.

```python
age = int(input("Enter your age: "))

print("Your age is", age)
```

**Sample Output:**
```text
Enter your age: 20
Your age is 20
```

## 10. Displaying Output

The `print()` function is used to display information.

Example:

```python
name = "Somya"
age = 20

print("Name:", name)
print("Age:", age)
```

**Output:**
```text
Name: Somya
Age: 20
```

Python also supports formatted output using f-strings.

```python
name = "Somya"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

**Output:**
```text
My name is Somya and I am 20 years old.
```

## 11. Python Keywords

Keywords are reserved words that have special meanings in Python.

Examples include:

```text
if       else       elif
for      while      break
continue return     def
class    try        except
finally  import     from
True     False      None
and      or         not
```

Keywords cannot be used as variable names.

To display all Python keywords:

```python
import keyword

print(keyword.kwlist)
```

## 12. What I Learned

After completing this chapter, I understand:

- Basic Python syntax and statements.
- The importance of indentation.
- How to create and assign variables.
- Rules for naming variables.
- Multiple variable assignment.
- Constants and naming conventions.
- How to accept input using `input()`.
- How to display output using `print()`.
- How to use f-strings.
- What Python keywords are.

## Summary

Python syntax provides a simple way to write programs. Variables help store and manage data, while input and output functions allow interaction with users.

Understanding statements, indentation, variable assignment, and naming rules is essential before moving to more advanced Python concepts.

---

### Navigation

⬅️ Previous: [Python Installation and Setup](02-Python-Installation-and-Setup.md)

➡️ Next: [Data Types and Type Casting](04-Data-Types-and-Type-Casting.md)