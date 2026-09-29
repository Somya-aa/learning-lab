# CSS Units and Measurements

CSS units are used to define the size of elements, spacing, typography, and layout properties. Choosing the right unit is essential for building responsive, maintainable, and scalable web pages across various screen sizes.

---

## 1. Types of CSS Units

CSS units are broadly categorized into two main types:

### Absolute Units
Absolute units have a fixed size and do not scale based on parent or root settings.

* `px` — Pixels
* `pt` — Points
* `cm` — Centimeters
* `mm` — Millimeters
* `in` — Inches

### Relative Units
Relative units depend on another reference value, such as a parent element, the root font size, or the dimensions of the viewport.

* `%` — Percentage relative to the parent element
* `em` — Relative to element or inherited font size
* `rem` — Relative to root (`<html>`) font size
* `vw` — Viewport Width (1% of viewport width)
* `vh` — Viewport Height (1% of viewport height)
* `vmin` — 1% of the viewport's smaller dimension
* `vmax` — 1% of the viewport's larger dimension

---

## 2. Pixels (`px`)

`px` is one of the most common absolute units. It provides precise control over layout dimensions.

```css
.box {
    width: 300px;
    height: 150px;
    padding: 20px;
}
```

* **Best For:** Borders, fixed icons, or precise pixel-perfect elements.
* **Drawback:** Overusing fixed pixel values can hinder fluid, responsive design.

---

## 3. Percentage (`%`)

Percentages are calculated relative to the parent element's dimensions.

```css
.container {
    width: 80%;
}
```

* **Example:** If the parent container is `1000px` wide, an `80%` width equals `800px`.
* **Best For:** Flexible layouts and responsive grid containers.

---

## 4. `em`

`em` is relative to the font size of the immediate element or its inherited context.

```css
.parent {
    font-size: 20px;
}

.child {
    font-size: 2em; /* Evaluates to 40px */
}
```

* **Note:** `em` can compound quickly when elements are deeply nested, making sizing harder to predict.

---

## 5. `rem` (Root `em`)

`rem` stands for "root em" and is always relative to the font size of the root (`<html>`) element.

```css
html {
    font-size: 16px;
}

.heading {
    font-size: 2rem; /* Evaluates to 32px */
}
```

* **Best For:** Scalable typography, padding, and margins across the entire document.

---

## 6. Comparison: `em` vs `rem`

| Unit | Relative To | Common Use Case |
| :--- | :--- | :--- |
| **`em`** | Current/Parent element's font size | Component-scoped scalability |
| **`rem`** | Root (`<html>`) font size | Global typography, margins, padding |

```css
.parent {
    font-size: 20px;
}

.child {
    font-size: 2em;  /* 40px (relative to parent) */
}

.title {
    font-size: 2rem; /* 32px (relative to html root, default 16px) */
}
```

---

## 7. Viewport Units

Viewport units scale according to the size of the browser window.

### `vw` (Viewport Width)
```css
.container {
    width: 50vw; /* 50% of total browser width */
}
```

### `vh` (Viewport Height)
```css
.hero {
    height: 100vh; /* 100% of total browser height */
}
```

---

## 8. `vmin` and `vmax`

### `vmin`
Evaluates based on the smaller viewport dimension (width or height).
```css
.box {
    width: 50vmin;
}
```

### `vmax`
Evaluates based on the larger viewport dimension (width or height).
```css
.box {
    width: 50vmax;
}
```

---

## 9. Other Absolute Units

Physical measurement units are primarily used for print stylesheets (`@media print`):

* `cm` → Centimeters
* `mm` → Millimeters
* `in` → Inches
* `pt` → Points ($1\text{ pt} = \frac{1}{72}\text{ in}$)
* `pc` → Picas ($1\text{ pc} = 12\text{ pt}$)

---

## 10. Practical Applications

### Controlling Typography
```css
h1 {
    font-size: 2rem;
}

p {
    font-size: 1rem;
}
```

### Layout and Spacing
```css
.card {
    padding: 1.5rem;
    margin: 2rem;
    gap: 1rem;
}
```

### Combining Layout Constraints
```css
.container {
    width: 90%;
    max-width: 1200px;
    padding: 2rem;
}
```

---

## 11. CSS Mathematical Functions

### `calc()`
Performs mathematical calculations combining different units.
```css
.container {
    width: calc(100% - 40px);
}

.box {
    width: calc(100vw - 2rem);
}
```

### `min()` and `max()`
Selects the minimum or maximum calculated value from a set of parameters.
```css
/* Selects whichever value is smaller */
.box {
    width: min(90%, 1000px);
}

/* Selects whichever value is larger */
.container {
    width: max(300px, 50%);
}
```

### `clamp()`
Sets a flexible range with minimum, preferred, and maximum limits: `clamp(minimum, preferred, maximum)`.

```css
h1 {
    font-size: clamp(2rem, 5vw, 4rem);
}
```

---

## 12. Quick Reference Table

| Unit | Type | Reference Base | Primary Application |
| :--- | :--- | :--- | :--- |
| `px` | Absolute | Screen pixel | Fixed borders, fine details |
| `%` | Relative | Parent element | Layout column widths |
| `em` | Relative | Element/Inherited font size | Context-dependent spacing |
| `rem` | Relative | Root (`<html>`) font size | Typography, consistent margins/

---

⬅️ Previous: [CSS Box Model](05-CSS-Box-Model.md)

➡️ Next: [CSS Margin Padding and Borders](07-CSS-Margin-Padding-and-Borders.md)