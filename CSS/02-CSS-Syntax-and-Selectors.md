# CSS Syntax and Selectors

CSS selectors are used to select HTML elements that you want to style [cite: 3]. CSS syntax defines how those selectors, properties, and values are written [cite: 3].

Understanding selectors is one of the most important parts of CSS because selectors determine which HTML elements receive a particular style [cite: 3].

---

## Basic CSS Syntax

A CSS rule follows this structure [cite: 3]:

```css
selector {
    property: value;
}
```

**Example:**

```css
p {
    color: blue;
    font-size: 18px;
}
```

**Here [cite: 3]:**
- `p` is the **selector** [cite: 3].
- `color` is a **property** [cite: 3].
- `blue` is the **value** [cite: 3].
- `font-size` is another **property** [cite: 3].
- `18px` is its **value** [cite: 3].

### CSS Declaration
A property and its value together form a **declaration** [cite: 3].

**Example:**
```css
color: blue;
```

Multiple declarations can be written inside the same rule [cite: 3]:

```css
p {
    color: blue;
    font-size: 18px;
    text-align: center;
}
```

Each declaration normally ends with a semicolon [cite: 3].

---

## Selectors Overview

### 1. Universal Selector
The universal selector `*` selects all HTML elements [cite: 3].

```css
* {
    margin: 0;
    padding: 0;
}
```
*This rule applies to all elements on the page [cite: 3].*

### 2. Element Selector
An element selector selects HTML elements by their tag name [cite: 3].

```css
p {
    color: blue;
}
```
*This selects all `<p>` elements [cite: 3].*

```css
h1 {
    font-size: 40px;
}
```
*This selects all `<h1>` elements [cite: 3].*

### 3. Class Selector
A class selector selects elements that have a specific `class` attribute [cite: 3]. A class selector begins with a dot `.` [cite: 3].

**HTML:**
```html
<p class="highlight">Important information.</p>
```

**CSS:**
```css
.highlight {
    color: red;
}
```

Multiple elements can use the same class [cite: 3]:
```html
<p class="highlight">First paragraph.</p>
<p class="highlight">Second paragraph.</p>
```

### 4. ID Selector
An ID selector selects an element using its `id` attribute [cite: 3]. An ID selector begins with `#` [cite: 3].

**HTML:**
```html
<h1 id="main-title">My Website</h1>
```

**CSS:**
```css
#main-title {
    color: purple;
}
```

*An `id` should normally be unique within a webpage [cite: 3].*

### 5. Grouping Selectors
Multiple selectors can be grouped together using commas [cite: 3].

**Instead of:**
```css
h1 {
    color: blue;
}
h2 {
    color: blue;
}
p {
    color: blue;
}
```

**You can write:**
```css
h1, h2, p {
    color: blue;
}
```
*This reduces repeated CSS [cite: 3].*

---

## Combinators and Advanced Selectors

### Descendant Selector
The descendant selector selects elements that are inside another element [cite: 3].

```css
div p {
    color: green;
}
```
*This selects `<p>` elements that are descendants of `<div>` [cite: 3].*

**HTML:**
```html
<div>
    <p>This paragraph is selected.</p>
</div>
```

### Child Selector
The child selector `>` selects elements that are direct children of another element [cite: 3].

```css
div > p {
    color: red;
}
```

**HTML:**
```html
<div>
    <p>Direct child.</p>
    <section>
        <p>Not a direct child of div.</p>
    </section>
</div>
```
*Only the first paragraph is a direct child of the `<div>` [cite: 3].*

### Adjacent Sibling Selector
The `+` selector selects an element that immediately follows another element [cite: 3].

```css
h2 + p {
    color: blue;
}
```

**HTML:**
```html
<h2>About</h2>
<p>This paragraph is immediately after the heading.</p>
```
*The paragraph is selected because it directly follows the `<h2>` [cite: 3].*

### General Sibling Selector
The `~` selector selects sibling elements that appear after another element [cite: 3].

```css
h2 ~ p {
    color: green;
}
```

**HTML:**
```html
<h2>About</h2>
<p>First paragraph.</p>
<p>Second paragraph.</p>
```
*Both paragraphs can be selected because they are siblings that appear after the `<h2>` [cite: 3].*

---

## Attribute Selectors

Attribute selectors select elements based on their attributes [cite: 3].

### Attribute Exists Selector
You can select elements that contain a particular attribute [cite: 3].

```css
input[required] {
    border: 2px solid red;
}
```

**HTML:**
```html
<input type="text" required>
```

### Attribute Value Selector
You can select an element when an attribute has a specific value [cite: 3].

```css
input[type="text"] {
    border: 1px solid black;
}

input[type="email"] {
    background-color: lightblue;
}
```

**HTML:**
```html
<input type="text">
<input type="email">
```

---

## Combining Selectors

### Multiple Classes
An element can have more than one class [cite: 3].

**HTML:**
```html
<p class="text highlight">Important information.</p>
```

**CSS:**
```css
.text {
    font-size: 18px;
}

.highlight {
    color: red;
}
```

### Combining Element and Class Selectors
You can combine an element selector with a class selector [cite: 3].

```css
p.highlight {
    color: red;
}
```
*This selects only `<p>` elements that have the `highlight` class [cite: 3].*

**HTML:**
```html
<p class="highlight">Selected paragraph.</p>
<div class="highlight">This is not selected.</div>
```

### Combining Element and ID Selectors
You can also combine an element with an ID [cite: 3].

```css
h1#main-title {
    color: blue;
}
```
*This selects an `<h1>` element with the ID `main-title` [cite: 3].*

---

## CSS Comments

CSS comments are written using `/* ... */` [cite: 3].

**Example:**
```css
/* Main heading */
h1 {
    color: blue;
}
```
*Comments are ignored by the browser [cite: 3].*

---

## Selector Specificity

When multiple CSS rules target the same element, CSS uses specificity to determine which rule has greater priority [cite: 3].

A simplified order of priority is [cite: 3]:

```text
Inline styles
      ↓
ID selectors
      ↓
Class / attribute / pseudo-class selectors
      ↓
Element selectors
      ↓
Universal selector
```

**Example:**
```css
p {
    color: blue;
}

.text {
    color: green;
}

#intro {
    color: red;
}
```

**HTML:**
```html
<p id="intro" class="text">Hello World</p>
```
*The ID selector has greater specificity than the class and element selectors [cite: 3].*

### The `!important` Rule
The `!important` declaration increases the priority of a CSS declaration [cite: 3].

```css
p {
    color: red !important;
}
```
*It should be used carefully because excessive use can make CSS difficult to maintain [cite: 3]. Avoid using `!important` unless there is a specific reason [cite: 3].*

---

## Common CSS Selectors Table

| Selector | Meaning |
| :--- | :--- |
| `*` | Selects all elements [cite: 3] |
| `p` | Selects all `<p>` elements [cite: 3] |
| `.class` | Selects elements with a class [cite: 3] |
| `#id` | Selects an element with an ID [cite: 3] |
| `div p` | Selects `<p>` inside `<div>` [cite: 3] |
| `div > p` | Selects direct `<p>` children of `<div>` [cite: 3] |
| `h2 + p` | Selects `<p>` immediately after `<h2>` [cite: 3] |
| `h2 ~ p` | Selects sibling `<p>` elements after `<h2>` [cite: 3] |
| `[type]` | Selects elements having the attribute [cite: 3] |
| `[type="text"]` | Selects elements with a specific attribute value [cite: 3] |

---

## Complete Example

**HTML (`index.html`):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>CSS Selectors</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h1 id="main-title">My Learning Lab</h1>

    <p class="intro">I am learning CSS selectors.</p>
    <p class="intro">Selectors are an important part of CSS.</p>

    <section>
        <h2>Topics</h2>
        <p>CSS selectors allow us to target HTML elements.</p>
    </section>

    <form>
        <input type="text" placeholder="Enter your name">
        <input type="email" placeholder="Enter your email">
    </form>

</body>
</html>
```

**CSS (`style.css`):**
```css
/* Universal selector */
* {
    box-sizing: border-box;
}

/* ID selector */
#main-title {
    color: blue;
    text-align: center;
}

/* Class selector */
.intro {
    color: green;
    font-size: 18px;
}

/* Descendant selector */
section p {
    color: purple;
}

/* Attribute selector */
input[type="text"] {
    border: 2px solid black;
}

/* Attribute selector */
input[type="email"] {
    border: 2px solid blue;
}
```

---

## Best Practices

- Use meaningful class names [cite: 3].
- Keep IDs unique [cite: 3].
- Prefer classes for reusable styling [cite: 3].
- Use selectors that are as simple as possible [cite: 3].
- Avoid unnecessarily deep selectors [cite: 3].
- Group selectors when they share the same styles [cite: 3].
- Avoid excessive use of `!important` [cite: 3].
- Keep CSS properly formatted [cite: 3].
- Use comments for important sections [cite: 3].
- Keep specificity manageable [cite: 3].

---

## Common Mistakes

### 1. Forgetting the Dot for Class Selectors
**Incorrect:**
```css
highlight {
    color: red;
}
```

**Correct:**
```css
.highlight {
    color: red;
}
```

### 2. Forgetting the Hash for ID Selectors
**Incorrect:**
```css
main-title {
    color: blue;
}
```

**Correct:**
```css
#main-title {
    color: blue;
}
```

### 3. Using Duplicate IDs
**Avoid:**
```html
<p id="text">First</p>
<p id="text">Second</p>
```

**Use a class if multiple elements need the same styling:**
```html
<p class="text">First</p>
<p class="text">Second</p>
```

### 4. Overusing `!important`
**Avoid:**
```css
p {
    color: red !important;
}
```
*unless there is a specific reason [cite: 3]. Try to solve specificity or CSS organization issues instead [cite: 3].*

---

## What I Learned

In this chapter, I learned:
1. Basic CSS syntax [cite: 3].
2. CSS selectors and declarations [cite: 3].
3. Universal selectors [cite: 3].
4. Element selectors [cite: 3].
5. Class selectors [cite: 3].
6. ID selectors [cite: 3].
7. Grouping selectors [cite: 3].
8. Descendant selectors [cite: 3].
9. Child selectors [cite: 3].
10. Sibling selectors [cite: 3].
11. Attribute selectors [cite: 3].
12. Combining selectors [cite: 3].
13. CSS specificity [cite: 3].
14. The purpose of `!important` [cite: 3].
15. Common selector mistakes and best practices [cite: 3].

---

## Summary

CSS selectors determine which HTML elements receive styles [cite: 3].

**The basic structure is:**
```css
selector {
    property: value;
}
```

**Common selectors include:**
- `*` - Universal selector [cite: 3]
- `p` - Element selector [cite: 3]
- `.class` - Class selector [cite: 3]
- `#id` - ID selector [cite: 3]
- `div p` - Descendant selector [cite: 3]
- `div > p` - Child selector [cite: 3]
- `[type]` - Attribute selector [cite: 3]

Understanding selectors and specificity is essential for writing effective CSS and controlling exactly which elements receive a particular style [cite: 3].

---

## Navigation

⬅️ Previous: [Introduction to CSS](01-Introduction-to-CSS.md)

➡️ Next: [Colors Backgrounds and Opacity](03-Colors-Background-and-Opacity.md)
