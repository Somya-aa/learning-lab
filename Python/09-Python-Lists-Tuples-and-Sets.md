# Chapter 9: Python Lists, Tuples, and Sets

## 1. Introduction

Lists, tuples, and sets are built-in collection data types in Python. They allow us to store multiple values in a single variable.

Each collection has different properties and uses.

| Feature | List | Tuple | Set |
|---|---|---|---|
| Syntax | `[]` | `()` | `{}` |
| Ordered | Yes | Yes | No |
| Mutable | Yes | No | Yes |
| Allows Duplicates | Yes | Yes | No |
| Indexing | Yes | Yes | No |

## 2. Python Lists

A list is an ordered and mutable collection that can store multiple values of different data types.

### Creating a List

```python
fruits = ["Apple", "Mango", "Banana"]

print(fruits)
```

**Output:**
```text
['Apple', 'Mango', 'Banana']
```

### Accessing List Elements

List elements can be accessed using positive and negative indexing.

```python
fruits = ["Apple", "Mango", "Banana"]

print(fruits[0])
print(fruits[1])
print(fruits[-1])
```

**Output:**
```text
Apple
Mango
Banana
```

### List Slicing

Slicing is used to access a portion of a list.

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
print(numbers[:3])
print(numbers[-2:])
```

**Output:**
```text
[20, 30, 40]
[10, 20, 30]
[40, 50]
```

### Modifying List Elements

Lists are mutable, so their elements can be changed.

```python
fruits = ["Apple", "Mango", "Banana"]

fruits[1] = "Orange"

print(fruits)
```

**Output:**
```text
['Apple', 'Orange', 'Banana']
```

## 3. Common List Methods

Python provides several methods to perform operations on lists.

| Method | Description |
|---|---|
| `append()` | Adds an element at the end |
| `insert()` | Adds an element at a specified position |
| `extend()` | Adds elements from another iterable |
| `remove()` | Removes the first matching element |
| `pop()` | Removes and returns an element |
| `clear()` | Removes all elements |
| `sort()` | Sorts the list |
| `reverse()` | Reverses the list |
| `index()` | Returns the index of an element |
| `count()` | Counts occurrences of an element |
| `copy()` | Creates a shallow copy of the list |

### Example

```python
numbers = [10, 20, 30]

numbers.append(40)
print(numbers)

numbers.insert(1, 15)
print(numbers)

numbers.remove(30)
print(numbers)

numbers.sort()
print(numbers)
```

**Output:**
```text
[10, 20, 30, 40]
[10, 15, 20, 30, 40]
[10, 15, 20, 40]
[10, 15, 20, 40]
```

## 4. Iterating Through a List

A `for` loop can be used to access each element of a list.

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

## 5. Python Tuples

A tuple is an ordered and immutable collection that stores multiple values.

Once created, its elements cannot be changed.

### Creating a Tuple

```python
numbers = (10, 20, 30, 40)

print(numbers)
```

**Output:**
```text
(10, 20, 30, 40)
```

### Accessing Tuple Elements

Tuples support indexing and slicing.

```python
numbers = (10, 20, 30, 40)

print(numbers[0])
print(numbers[-1])
print(numbers[1:3])
```

**Output:**
```text
10
40
(20, 30)
```

### Single-Element Tuple

A single-element tuple requires a trailing comma.

```python
value = (10,)

print(type(value))
```

**Output:**
```text
<class 'tuple'>
```

Without the comma, `(10)` is simply an integer inside parentheses.

## 6. Common Tuple Methods

Since tuples are immutable, they have fewer methods than lists.

| Method | Description |
|---|---|
| `count()` | Counts occurrences of an element |
| `index()` | Returns the index of an element |

Example:

```python
numbers = (10, 20, 30, 20, 40)

print(numbers.count(20))
print(numbers.index(30))
```

**Output:**
```text
2
2
```

## 7. Tuple Packing and Unpacking

### Tuple Packing

Packing means combining multiple values into a tuple.

```python
student = "Somya", 20, "CSE"

print(student)
```

**Output:**
```text
('Somya', 20, 'CSE')
```

### Tuple Unpacking

Unpacking means assigning tuple elements to separate variables.

```python
student = ("Somya", 20, "CSE")

name, age, course = student

print(name)
print(age)
print(course)
```

**Output:**
```text
Somya
20
CSE
```

## 8. Python Sets

A set is an unordered collection of unique elements.

Sets automatically remove duplicate values and do not support indexing.

### Creating a Set

```python
numbers = {10, 20, 30, 10}

print(numbers)
```

**Possible Output:**
```text
{10, 20, 30}
```

The order of elements may vary.

### Creating an Empty Set

```python
my_set = set()

print(type(my_set))
```

**Output:**
```text
<class 'set'>
```

Note: `{}` creates an empty dictionary, not an empty set.

## 9. Common Set Methods

| Method | Description |
|---|---|
| `add()` | Adds an element |
| `update()` | Adds multiple elements |
| `remove()` | Removes an element; raises an error if absent |
| `discard()` | Removes an element without raising an error if absent |
| `pop()` | Removes and returns an arbitrary element |
| `clear()` | Removes all elements |

### Example

```python
numbers = {10, 20, 30}

numbers.add(40)
print(numbers)

numbers.discard(20)
print(numbers)
```

**Possible Output:**
```text
{10, 20, 30, 40}
{10, 30, 40}
```

## 10. Set Operations

Python supports mathematical set operations.

Consider two sets:

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}
```

### A. Union

Union combines all unique elements from both sets.

```python
print(A | B)
```

**Output:**
```text
{1, 2, 3, 4, 5, 6}
```

### B. Intersection

Intersection returns elements common to both sets.

```python
print(A & B)
```

**Output:**
```text
{3, 4}
```

### C. Difference

Difference returns elements present in the first set but not in the second.

```python
print(A - B)
```

**Output:**
```text
{1, 2}
```

### D. Symmetric Difference

Symmetric difference returns elements present in either set, but not in both.

```python
print(A ^ B)
```

**Output:**
```text
{1, 2, 5, 6}
```

## 11. List Comprehension

List comprehension provides a shorter way to create lists using an expression and an iterable.

### Syntax

```python
new_list = [expression for item in iterable]
```

### Example

```python
numbers = [1, 2, 3, 4, 5]

squares = [x ** 2 for x in numbers]

print(squares)
```

**Output:**
```text
[1, 4, 9, 16, 25]
```

A condition can also be included:

```python
numbers = [1, 2, 3, 4, 5, 6]

even_numbers = [x for x in numbers if x % 2 == 0]

print(even_numbers)
```

**Output:**
```text
[2, 4, 6]
```

## 12. Common Mistakes

| Mistake | Explanation |
|---|---|
| Accessing an invalid index | Lists and tuples raise `IndexError` |
| Modifying a tuple | Tuples are immutable |
| Expecting a fixed set order | Sets are unordered |
| Creating an empty set using `{}` | Use `set()` instead |
| Using duplicate set elements | Duplicate values are automatically removed |
| Forgetting the tuple comma | Single-element tuples require a trailing comma |

## 13. What I Learned

After completing this chapter, I understand:

- What lists, tuples, and sets are.
- How to create and access collection elements.
- List indexing, slicing, and modification.
- Common list and tuple methods.
- Tuple packing and unpacking.
- How sets store unique values.
- Union, intersection, difference, and symmetric difference.
- How list comprehension works.
- Differences between lists, tuples, and sets.

## Summary

Lists, tuples, and sets are important Python collection data types. Lists are mutable and ordered, tuples are immutable and ordered, while sets store unique elements without maintaining a fixed order.

Understanding these collections helps in organizing, accessing, and manipulating data efficiently.

---

### Navigation

⬅️ Previous: [Strings and String Methods](08-Strings-and-String-Methods.md)

➡️ Next: [Dictionaries in Python](10-Dictionaries-in-Python.md)