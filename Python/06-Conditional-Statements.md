# Chapter 6: Conditional Statements in Python

## 1. Introduction

Conditional statements are used to make decisions in a Python program.

They allow a program to execute different blocks of code depending on whether a condition is `True` or `False`.

Python provides the following conditional statements:

- `if`
- `if-else`
- `if-elif-else`
- Nested if statements
- Conditional expressions
- `match-case`

## 2. The if Statement

The `if` statement executes a block of code only when the given condition is True.

### Syntax

```python
if condition:
    statement
```

### Example

```python
age = 20

if age >= 18:
    print("You are eligible to vote")
```

**Output:**
```text
You are eligible to vote
```

## 3. The if-else Statement

The `if-else` statement executes one block when the condition is True and another block when it is False.

### Syntax

```python
if condition:
    statement1
else:
    statement2
```

### Example

```python
number = 7

if number % 2 == 0:
    print("Even Number")
else:
    print("Odd Number")
```

**Output:**
```text
Odd Number
```

## 4. The if-elif-else Statement

The `elif` keyword means "else if".

It is used to check multiple conditions in a program.

Python executes the first block whose condition is True. If no condition is True, the `else` block executes.

### Syntax

```python
if condition1:
    statement1
elif condition2:
    statement2
elif condition3:
    statement3
else:
    statement4
```

### Example

```python
marks = 85

if marks >= 90:
    print("Grade A+")
elif marks >= 80:
    print("Grade A")
elif marks >= 70:
    print("Grade B")
else:
    print("Grade C")
```

**Output:**
```text
Grade A
```

## 5. Nested if Statements

A nested if statement means placing one `if` statement inside another `if` statement.

It is useful when a decision depends on multiple conditions.

### Example

```python
age = 20
citizen = True

if age >= 18:
    if citizen:
        print("Eligible to vote")
    else:
        print("Citizenship required")
else:
    print("Not eligible to vote")
```

**Output:**
```text
Eligible to vote
```

## 6. Short-Hand if Statement

Python allows writing a simple `if` statement on a single line.

### Example

```python
age = 20

if age >= 18: print("Adult")
```

**Output:**
```text
Adult
```

This is suitable for simple statements, but normal multi-line conditions are generally easier to read.

## 7. Conditional Expression (Ternary Operator)

A conditional expression allows us to write an if-else decision in a single line.

### Syntax

```python
value_if_true if condition else value_if_false
```

### Example

```python
age = 20

result = "Adult" if age >= 18 else "Minor"

print(result)
```

**Output:**
```text
Adult
```

## 8. The match-case Statement

Python introduced the `match-case` statement in Python 3.10.

It is used to compare a value against different patterns and execute the matching block.

### Syntax

```python
match expression:
    case pattern1:
        statement1
    case pattern2:
        statement2
    case _:
        default_statement
```

The underscore (`_`) acts as a default case.

### Example

```python
day = 3

match day:
    case 1:
        print("Monday")
    case 2:
        print("Tuesday")
    case 3:
        print("Wednesday")
    case _:
        print("Invalid day")
```

**Output:**
```text
Wednesday
```

## 9. The pass Statement

The `pass` statement is used as a placeholder when a statement is syntactically required but no action needs to be performed.

### Example

```python
age = 20

if age >= 18:
    pass
else:
    print("Minor")
```

The program executes without an error even though the `if` block is empty.

## 10. Difference Between if, elif and else

| Statement | Purpose |
|---|---|
| `if` | Checks the first condition |
| `elif` | Checks another condition if previous conditions are False |
| `else` | Executes when all previous conditions are False |

## 11. Common Mistakes

| Mistake | Explanation |
|---|---|
| Missing colon (`:`) | Every conditional header requires a colon |
| Incorrect indentation | Python uses indentation to define blocks |
| Using `=` instead of `==` | `=` assigns a value, while `==` compares values |
| Incorrect condition order | Earlier conditions may prevent later conditions from being checked |
| Missing else handling | Some conditions may not produce the expected output |

## 12. What I Learned

After completing this chapter, I understand:

- How conditional statements work in Python.
- How to use `if` and `if-else`.
- How to check multiple conditions using `elif`.
- How nested if statements work.
- How to write conditional expressions.
- How to use the `match-case` statement.
- The purpose of the `pass` statement.
- Common mistakes in conditional programming.

## Summary

Conditional statements allow Python programs to make decisions based on specific conditions. They are essential for controlling program execution and building logical applications.

Understanding these statements provides the foundation for learning loops and more advanced programming concepts.

---

### Navigation

⬅️ Previous: [Operators and Expressions](05-Operators-and-Expressions.md)

➡️ Next: [Loops in Python](07-Loops-in-Python.md)