# Chapter 7: Loops in Python

## 1. Introduction

Loops are used to execute a block of code repeatedly as long as a particular condition is satisfied or until a sequence is exhausted.

Loops help reduce code repetition and make programs more efficient.

Python provides two main types of loops:

1. `for` loop
2. `while` loop

Python also supports loop control statements such as `break`, `continue`, and `pass`.

## 2. The for Loop

The `for` loop is used to iterate over a sequence such as a list, tuple, string, or range.

### Syntax

```python
for variable in sequence:
    statements
```

### Example

```python
fruits = ["Apple", "Mango", "Banana"]

for fruit in fruits:
    print(fruit)
```

**Output:**
```text
Apple
Mango
Banana
```

## 3. The range() Function

The `range()` function generates a sequence of numbers. It is commonly used with `for` loops.

### Syntax

```python
range(start, stop, step)
```

- `start`: Starting value (default is 0).
- `stop`: Ending limit (excluded from the sequence).
- `step`: Difference between consecutive values (default is 1).

### Example 1: Using range()

```python
for i in range(5):
    print(i)
```

**Output:**
```text
0
1
2
3
4
```

### Example 2: Specifying Start and Stop

```python
for i in range(1, 6):
    print(i)
```

**Output:**
```text
1
2
3
4
5
```

### Example 3: Using Step

```python
for i in range(2, 11, 2):
    print(i)
```

**Output:**
```text
2
4
6
8
10
```

## 4. The while Loop

The `while` loop repeatedly executes a block of code as long as its condition remains True.

### Syntax

```python
while condition:
    statements
```

### Example

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

**Output:**
```text
1
2
3
4
5
```

**Important:** Always ensure that the loop condition eventually becomes False. Otherwise, an infinite loop may occur.

## 5. Nested Loops

A loop inside another loop is called a nested loop.

The inner loop executes completely for every iteration of the outer loop.

### Example

```python
for i in range(1, 4):
    for j in range(1, 3):
        print(i, j)
```

**Output:**
```text
1 1
1 2
2 1
2 2
3 1
3 2
```

## 6. The break Statement

The `break` statement immediately terminates the nearest enclosing loop.

### Example

```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```

**Output:**
```text
1
2
3
```

The loop stops when `i` becomes 4.

## 7. The continue Statement

The `continue` statement skips the remaining statements in the current iteration and moves to the next iteration.

### Example

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

**Output:**
```text
1
2
4
5
```

The number 3 is skipped.

## 8. The pass Statement

The `pass` statement is a placeholder that performs no operation.

It is useful when a loop or code block must exist but its implementation is not ready.

### Example

```python
for i in range(5):
    if i == 2:
        pass
    print(i)
```

**Output:**
```text
0
1
2
3
4
```

Unlike `break` and `continue`, `pass` does not change the normal flow of the loop.

## 9. The else Clause in Loops

Python allows an `else` block to be used with both `for` and `while` loops.

The `else` block executes when the loop finishes normally, without being terminated by a `break` statement.

### Example

```python
for i in range(1, 4):
    print(i)
else:
    print("Loop completed")
```

**Output:**
```text
1
2
3
Loop completed
```

If the loop terminates using `break`, its `else` block does not execute.

## 10. Difference Between for and while Loops

| for Loop | while Loop |
|---|---|
| Iterates over a sequence or iterable | Repeats while a condition is True |
| Commonly used when iterating over collections | Commonly used when repetition depends on a condition |
| Automatically moves to the next item | Requires condition management |
| Often used with `range()` | Uses a Boolean condition |

## 11. Common Loop Mistakes

| Mistake | Explanation |
|---|---|
| Infinite loop | The condition never becomes False |
| Missing indentation | Loop statements must be indented |
| Incorrect range limit | The stop value is excluded |
| Missing counter update | A while loop may never terminate |
| Incorrect use of break | It terminates the nearest enclosing loop |
| Incorrect use of continue | It skips the current iteration |

## 12. What I Learned

After completing this chapter, I understand:

- What loops are and why they are used.
- How to use `for` and `while` loops.
- How the `range()` function works.
- How nested loops operate.
- How to control loops using `break`, `continue`, and `pass`.
- How the `else` clause works with loops.
- Differences between `for` and `while` loops.
- How to identify common loop errors.

## Summary

Loops are important control structures in Python that allow repetitive execution of code. The `for` loop is commonly used to iterate over sequences, while the `while` loop repeats as long as a condition is True.

Understanding loops and their control statements is essential for developing efficient programs.

---

### Navigation

⬅️ Previous: [Conditional Statements](06-Conditional-Statements.md)

➡️ Next: [Strings and String Methods](08-Strings-and-String-Methods.md)