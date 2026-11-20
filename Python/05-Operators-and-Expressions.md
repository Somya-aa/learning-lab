# Chapter 5: Python Operators and Expressions

## 1. Introduction

Operators are special symbols or keywords used to perform operations on variables and values.

An expression is a combination of values, variables, and operators that produces a result.

Example:

```python
a = 10
b = 5

result = a + b

print(result)
```

**Output:**
```text
15
```

Here, `+` is an operator, and `a + b` is an expression.

## 2. Types of Operators in Python

Python provides the following types of operators:

1. Arithmetic Operators
2. Comparison Operators
3. Assignment Operators
4. Logical Operators
5. Bitwise Operators
6. Membership Operators
7. Identity Operators

## 3. Arithmetic Operators

Arithmetic operators are used to perform mathematical operations.

| Operator | Name | Example | Result |
|---|---|---|---|
| `+` | Addition | `10 + 5` | 15 |
| `-` | Subtraction | `10 - 5` | 5 |
| `*` | Multiplication | `10 * 5` | 50 |
| `/` | Division | `10 / 5` | 2.0 |
| `%` | Modulus | `10 % 3` | 1 |
| `//` | Floor Division | `10 // 3` | 3 |
| `**` | Exponentiation | `2 ** 3` | 8 |

Example:

```python
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a % b)
print(a // b)
print(a ** b)
```

**Output:**
```text
13
7
30
3.3333333333333335
1
3
1000
```

## 4. Comparison Operators

Comparison operators compare two values and return either `True` or `False`.

| Operator | Meaning | Example |
|---|---|---|
| `==` | Equal to | `10 == 10` |
| `!=` | Not equal to | `10 != 5` |
| `>` | Greater than | `10 > 5` |
| `<` | Less than | `5 < 10` |
| `>=` | Greater than or equal to | `10 >= 10` |
| `<=` | Less than or equal to | `5 <= 10` |

Example:

```python
a = 10
b = 5

print(a == b)
print(a != b)
print(a > b)
print(a < b)
```

**Output:**
```text
False
True
True
False
```

## 5. Assignment Operators

Assignment operators are used to assign values to variables and update their values.

| Operator | Example | Equivalent Expression |
|---|---|---|
| `=` | `x = 10` | Assign 10 to x |
| `+=` | `x += 5` | `x = x + 5` |
| `-=` | `x -= 5` | `x = x - 5` |
| `*=` | `x *= 5` | `x = x * 5` |
| `/=` | `x /= 5` | `x = x / 5` |
| `%=` | `x %= 5` | `x = x % 5` |
| `//=` | `x //= 5` | `x = x // 5` |
| `**=` | `x **= 2` | `x = x ** 2` |

Example:

```python
x = 10

x += 5
print(x)

x *= 2
print(x)
```

**Output:**
```text
15
30
```

## 6. Logical Operators

Logical operators are used to combine conditional expressions.

Python provides three logical operators:

| Operator | Meaning | Description |
|---|---|---|
| `and` | Logical AND | True if both conditions are true |
| `or` | Logical OR | True if at least one condition is true |
| `not` | Logical NOT | Reverses the Boolean result |

Example:

```python
a = 10
b = 20

print(a < 15 and b > 15)
print(a > 15 or b > 15)
print(not(a > b))
```

**Output:**
```text
True
True
True
```

## 7. Bitwise Operators

Bitwise operators perform operations on the binary representations of integers.

| Operator | Name |
|---|---|
| `&` | AND |
| `|` | OR |
| `^` | XOR |
| `~` | NOT |
| `<<` | Left Shift |
| `>>` | Right Shift |

Example:

```python
a = 5
b = 3

print(a & b)
print(a | b)
print(a ^ b)
print(~a)
print(a << 1)
print(a >> 1)
```

**Output:**
```text
1
7
6
-6
10
2
```

## 8. Membership Operators

Membership operators check whether a value exists in a sequence or collection.

Python provides two membership operators:

- `in`: Returns True if the value exists.
- `not in`: Returns True if the value does not exist.

Example:

```python
fruits = ["Apple", "Mango", "Banana"]

print("Apple" in fruits)
print("Orange" not in fruits)
```

**Output:**
```text
True
True
```

## 9. Identity Operators

Identity operators check whether two variables refer to the same object in memory.

Python provides two identity operators:

- `is`
- `is not`

Example:

```python
a = [10, 20, 30]
b = a
c = [10, 20, 30]

print(a is b)
print(a is c)
print(a == c)
```

**Output:**
```text
True
False
True
```

Explanation:

- `a is b` is True because both refer to the same object.
- `a is c` is False because they are different objects.
- `a == c` is True because their values are equal.

## 10. Operator Precedence

Operator precedence determines the order in which operators are evaluated in an expression.

Example:

```python
result = 10 + 5 * 2

print(result)
```

**Output:**
```text
20
```

Multiplication is performed before addition.

### Common Operator Precedence (High to Low)

| Priority | Operators |
|---|---|
| 1 | `()` Parentheses |
| 2 | `**` Exponentiation |
| 3 | `+x`, `-x`, `~x` Unary operators |
| 4 | `*`, `/`, `//`, `%` |
| 5 | `+`, `-` |
| 6 | `<<`, `>>` |
| 7 | `&` |
| 8 | `^` |
| 9 | `|` |
| 10 | Comparisons, `in`, `is` |
| 11 | `not` |
| 12 | `and` |
| 13 | `or` |

Parentheses can be used to make expressions easier to understand and control evaluation order.

## 11. What I Learned

After completing this chapter, I understand:

- What operators and expressions are.
- Arithmetic and comparison operators.
- Assignment and logical operators.
- Bitwise operators and their uses.
- Membership and identity operators.
- Difference between `==` and `is`.
- How operator precedence works.

## Summary

Operators are essential building blocks of Python programming. They allow us to perform mathematical calculations, compare values, assign data, evaluate conditions, and work with collections.

Understanding these operators helps in writing logical and efficient Python programs.

---

### Navigation

⬅️ Previous: [Data Types and Type Casting](04-Data-Types-and-Type-Casting.md)

➡️ Next: [Conditional Statements](06-Conditional-Statements.md)