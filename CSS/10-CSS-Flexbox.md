# CSS Flexbox

CSS Flexbox, short for Flexible Box Layout, is a one-dimensional layout system used to arrange elements in rows or columns.

Flexbox makes it easier to align, distribute, and resize elements without relying on complicated positioning techniques.

---

## 1. What is Flexbox?

Flexbox works with two main components:

- **Flex Container** — the parent element.
- **Flex Items** — the direct children of the container.

```css
.container {
    display: flex;
}
```

Example:

```html
<div class="container">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
</div>
```

The three `<div>` elements become flex items.

---

## 2. Main Axis and Cross Axis

Flexbox uses two axes:

```text
Main Axis
──────────────→

Cross Axis
     ↓
```

By default:
- **Main axis** → Horizontal
- **Cross axis** → Vertical

The direction can be changed using `flex-direction`.

---

## 3. flex-direction

The `flex-direction` property determines the direction of flex items.

### Row
```css
.container {
    display: flex;
    flex-direction: row;
}
```
Items are arranged horizontally.

### Row Reverse
```css
.container {
    flex-direction: row-reverse;
}
```
Items are arranged horizontally in the reverse direction.

### Column
```css
.container {
    flex-direction: column;
}
```
Items are arranged vertically.

### Column Reverse
```css
.container {
    flex-direction: column-reverse;
}
```
Items are arranged vertically in the reverse direction.

---

## 4. justify-content

`justify-content` controls the alignment of items along the main axis.

Common values:
- `flex-start`
- `flex-end`
- `center`
- `space-between`
- `space-around`
- `space-evenly`

Example:
```css
.container {
    display: flex;
    justify-content: center;
}
```

Common Behaviors:
```text
flex-start
[1][2][3]

center
    [1][2][3]

flex-end
        [1][2][3]

space-between
[1]       [2]       [3]

space-around
  [1]    [2]    [3]

space-evenly
   [1]   [2]   [3]
```

---

## 5. align-items

`align-items` controls alignment along the cross axis.

Common values:
- `stretch`
- `flex-start`
- `flex-end`
- `center`
- `baseline`

Example:
```css
.container {
    display: flex;
    align-items: center;
}
```
This is commonly used to vertically center items in a horizontal flex container.

---

## 6. gap

The `gap` property creates space between flex items.

```css
.container {
    display: flex;
    gap: 20px;
}
```

You can also use:
```css
.container {
    row-gap: 10px;
    column-gap: 20px;
}
```

`gap` is generally cleaner than adding margins to every flex item.

---

## 7. flex-wrap

By default, flex items try to remain on one line.
Use `flex-wrap` when items should move to another line if there is not enough space.

```css
.container {
    display: flex;
    flex-wrap: wrap;
}
```

Common values:
- `nowrap`
- `wrap`
- `wrap-reverse`

---

## 8. align-content

`align-content` controls the spacing between multiple flex lines when wrapping is enabled.

```css
.container {
    display: flex;
    flex-wrap: wrap;
    align-content: center;
}
```

Common values include:
- `flex-start`
- `flex-end`
- `center`
- `space-between`
- `space-around`
- `space-evenly`
- `stretch`

`align-content` is mainly useful when there are multiple rows or columns of flex items.

---

## 9. flex-flow

`flex-flow` is shorthand for:
- `flex-direction`
- `flex-wrap`

Example:
```css
.container {
    flex-flow: row wrap;
}
```

This means:
- Direction → `row`
- Wrapping → `wrap`

---

## 10. flex-grow

`flex-grow` determines how much an item can grow relative to other flex items.

```css
.item {
    flex-grow: 1;
}
```

Example:
```css
.item1 {
    flex-grow: 1;
}

.item2 {
    flex-grow: 2;
}
```
The second item can receive twice as much available extra space as the first.

---

## 11. flex-shrink

`flex-shrink` determines how much an item can shrink when there is not enough space.

```css
.item {
    flex-shrink: 1;
}
```

The default value is generally `1`.
To prevent an item from shrinking:
```css
.item {
    flex-shrink: 0;
}
```

---

## 12. flex-basis

`flex-basis` defines the initial size of a flex item along the main axis.

```css
.item {
    flex-basis: 200px;
}
```

It can be used instead of directly setting width in many flex layouts.

---

## 13. flex Shorthand

The `flex` property is shorthand for:
- `flex-grow`
- `flex-shrink`
- `flex-basis`

Example:
```css
.item {
    flex: 1;
}
```

A common pattern is:
```css
.item {
    flex: 1 1 200px;
}
```

This means:
- Grow → `1`
- Shrink → `1`
- Basis → `200px`

---

## 14. align-self

`align-self` allows an individual flex item to override the container's `align-items` value.

```css
.item {
    align-self: center;
}
```

Other values include:
- `auto`
- `flex-start`
- `flex-end`
- `center`
- `baseline`
- `stretch`

---

## 15. order

The `order` property changes the visual order of flex items.

```css
.item1 {
    order: 2;
}

.item2 {
    order: 1;
}
```

Items with lower order values appear first.
The default order is:
```css
order: 0;
```

> **Note:** Use `order` carefully because changing visual order can create accessibility and logical reading-order issues.

---

## 16. Centering with Flexbox

One of the most useful Flexbox patterns is centering an element.

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

For a container with a defined height:
```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 300px;
}
```

This centers the child horizontally and vertically.

---

## 17. Flexbox Example

### HTML
```html
<div class="container">
    <div class="card">Card 1</div>
    <div class="card">Card 2</div>
    <div class="card">Card 3</div>
</div>
```

### CSS
```css
.container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.card {
    flex: 1 1 200px;
    padding: 20px;
    border: 1px solid #ccc;
}
```

The cards can:
- Arrange horizontally.
- Wrap onto additional lines.
- Maintain spacing using `gap`.
- Resize according to the available space.

---

## 18. Flex Container vs Flex Item Properties

| Flex Container Properties (Applied to Parent) | Flex Item Properties (Applied to Children) |
| :--- | :--- |
| `display` | `flex-grow` |
| `flex-direction` | `flex-shrink` |
| `flex-wrap` | `flex-basis` |
| `flex-flow` | `flex` |
| `justify-content` | `align-self` |
| `align-items` | `order` |
| `align-content` | |
| `gap` | |

---

## 19. Common Flexbox Properties

| Property | Purpose |
| :--- | :--- |
| `display: flex` | Creates a flex container |
| `flex-direction` | Sets row or column direction |
| `justify-content` | Aligns items on the main axis |
| `align-items` | Aligns items on the cross axis |
| `flex-wrap` | Controls wrapping |
| `gap` | Creates space between items |
| `flex-grow` | Controls item growth |
| `flex-shrink` | Controls item shrinking |
| `flex-basis` | Sets initial item size |
| `flex` | Shorthand for flex sizing |
| `align-self` | Overrides individual alignment |
| `order` | Changes visual order |

---

## 20. Best Practices

- Use Flexbox for **one-dimensional** layouts.
- Use `gap` for consistent spacing.
- Use `flex-wrap` when content may not fit on one line.
- Use `justify-content` for main-axis alignment.
- Use `align-items` for cross-axis alignment.
- Use `flex: 1` when equal flexible sizing is appropriate.
- Avoid excessive use of `order`.
- Keep the HTML reading order logical.
- Use CSS Grid when a two-dimensional row-and-column layout is more appropriate.

---

## 21. Common Mistakes

### Mistake 1: Confusing the Axes
With `flex-direction: row;`, the main axis is horizontal.  
With `flex-direction: column;`, the main axis becomes vertical.

### Mistake 2: Using the Wrong Alignment Property
Remember:
- `justify-content` → Main axis
- `align-items` → Cross axis

### Mistake 3: Forgetting flex-wrap
If items are overflowing, consider adding:
```css
.container {
    flex-wrap: wrap;
}
```

### Mistake 4: Using Flexbox for Everything
Flexbox is excellent for one-dimensional layouts, but CSS Grid is often better for complex two-dimensional layouts.

---

## Summary

Flexbox provides a powerful and flexible way to arrange elements.

```text
Flex Container
      │
      ├── Direction
      ├── Alignment
      ├── Wrapping
      └── Gap
           │
           ↓
      Flex Items
      ├── Grow
      ├── Shrink
      ├── Basis
      ├── Alignment
      └── Order
```

Flexbox is especially useful for navigation bars, cards, buttons, headers, footers, and other one-dimensional layouts.

---

➡️ Next: [CSS Positioning](09-CSS-Positioning.md)

➡️ Next: [CSS Grid](11-CSS-Grid.md)