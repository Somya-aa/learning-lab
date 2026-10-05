# CSS Grid Master Reference

CSS Grid is a powerful two-dimensional layout system used to arrange elements simultaneously into rows and columns. While Flexbox is primarily designed for one-dimensional layouts (a single row or column), Grid gives you full control over both axes.

---

## Visual Model

```text
Grid Container
 ├── Rows
 ├── Columns
 ├── Gaps
 ├── Grid Areas
 └── Grid Items
```

---

## 1. What is CSS Grid?

CSS Grid operates on the interaction between a parent container and child items:

- **Grid Container:** The parent element where `display: grid` is applied.
- **Grid Items:** The direct children of the container.
- **Rows & Columns:** The horizontal and vertical tracks.
- **Gaps:** Spaces separating grid items.
- **Grid Lines:** Numbered lines demarcating tracks.
- **Grid Areas:** Named regions occupying space defined by grid lines.

### Defining a Grid Container

```css
.container {
    display: grid;
}
```

```html
<div class="container">
    <div>Item 1</div>
    <div>Item 2</div>
    <div>Item 3</div>
    <div>Item 4</div>
</div>
```

---

## 2. Defining Columns & Rows

### Columns (`grid-template-columns`)

Defines track sizes for grid columns using fixed or flexible units:

```css
/* Three explicit columns of 200px each */
.container {
    display: grid;
    grid-template-columns: 200px 200px 200px;
}

/* Three flexible columns using fractional units */
.container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
}
```

### Rows (`grid-template-rows`)

Explicitly defines track heights for grid rows:

```css
.container {
    display: grid;
    grid-template-rows: 100px 150px;
}
```

---

## 3. Core Grid Functions & Units

### The `fr` Unit

The `fr` (fraction) unit represents a portion of the remaining available space inside the container.

```css
.container {
    grid-template-columns: 1fr 2fr;
}
```
* **Column 1:** Takes 1 fraction ($1/3$) of available space.
* **Column 2:** Takes 2 fractions ($2/3$) of available space (twice as wide).

### The `repeat()` Function

Simplifies track lists by repeating a specified pattern:

```css
/* Instead of: 1fr 1fr 1fr */
grid-template-columns: repeat(3, 1fr);

/* Creates 4 columns of 200px each */
grid-template-columns: repeat(4, 200px);
```

### The `minmax()` Function

Sets minimum and maximum track dimensions:

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, minmax(200px, 1fr));
}
```
*Columns will shrink to no less than `200px` and grow up to `1fr` of the container space.*

---

## 4. Spacing (Gaps)

The `gap` property sets gutter spacing between grid items without affecting the outer edges.

```css
/* Unified gap */
.container {
    display: grid;
    gap: 20px;
}

/* Specific row and column gaps */
.container {
    row-gap: 10px;
    column-gap: 20px;
}

/* Shorthand: gap: <row-gap> <column-gap> */
.container {
    gap: 10px 20px;
}
```

---

## 5. Grid Item Placement

### Explicit Line Numbers

Grid tracks are bordered by numbered lines starting at `1`.

```text
|       |       |       |       |
1       2       3       4       5
```

Position items across specific lines:

```css
.item {
    grid-column: 1 / 3; /* Starts at line 1, ends at line 3 (spans 2 columns) */
    grid-row: 1 / 3;    /* Starts at line 1, ends at line 3 (spans 2 rows) */
}
```

### The `span` Keyword

Specifies how many tracks an item should span relative to its current auto-placement:

```css
.item {
    grid-column: span 2;
    grid-row: span 2;
}
```

---

## 6. Grid Template Areas

Assign visual names to regions of your layout for explicit structural placement.

### Defining Areas on the Container

```css
.container {
    display: grid;
    grid-template-areas:
        "header  header"
        "sidebar main"
        "footer  footer";
}
```

### Assigning Items to Areas

```css
.header  { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main    { grid-area: main; }
.footer  { grid-area: footer; }
```

### Practical Page Layout Example

```html
<div class="layout">
    <header>Header</header>
    <aside>Sidebar</aside>
    <main>Main Content</main>
    <footer>Footer</footer>
</div>
```

```css
.layout {
    display: grid;
    grid-template-columns: 200px 1fr;
    grid-template-areas:
        "header  header"
        "sidebar main"
        "footer  footer";
    gap: 20px;
}

header { grid-area: header; }
aside  { grid-area: sidebar; }
main   { grid-area: main; }
footer { grid-area: footer; }
```

---

## 7. Responsive Auto-Fitting Grids

Grid can build responsive layouts dynamically without media queries using `auto-fit` or `auto-fill` combined with `minmax()`.

```css
.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
}
```

- **`auto-fit`:** Fits as many columns as possible and expands existing items to fill any remaining space.
- **`auto-fill`:** Creates empty tracks to fill space even if there are no items to occupy them.

---

## 8. Alignment & Positioning

### Item Alignment inside Grid Areas

Controls how items align within their designated grid cell:

| Property | Axis | Common Values |
| :--- | :--- | :--- |
| `justify-items` | Horizontal (Inline Axis) | `start`, `end`, `center`, `stretch` |
| `align-items` | Vertical (Block Axis) | `start`, `end`, `center`, `stretch` |
| `place-items` | Shorthand (`<align>` / `<justify>`) | `center`, `stretch stretch` |

```css
.container {
    place-items: center; /* Centers content horizontally AND vertically */
}
```

### Content Alignment for the Entire Grid

Controls how the total grid tracks align within a larger container when the grid is smaller than its parent bounds:

```css
.container {
    justify-content: center;
    align-content: center;
}
```

---

## 9. Grid vs Flexbox Comparison

| Feature | Flexbox | CSS Grid |
| :--- | :--- | :--- |
| **Layout Dimension** | One-dimensional (Row OR Column) | Two-dimensional (Rows AND Columns) |
| **Alignment Basis** | Content-driven | Layout-driven |
| **Primary Use Cases** | Navigation bars, UI components, simple stacks | Page structures, card grids, dashboards |

> **Note:** Flexbox and Grid are complementary tools. Flexbox works well for micro-layouts (e.g., button groups, header links), while Grid manages macro-layouts (e.g., overall page structure, gallery systems).

---

## 10. Summary Reference Table

| Property | Description |
| :--- | :--- |
| `display: grid` | Establishes a grid formatting context. |
| `grid-template-columns` | Sets explicit column track sizes. |
| `grid-template-rows` | Sets explicit row track sizes. |
| `grid-template-areas` | Defines layout grid using named strings. |
| `grid-column` | Shorthand for start/end column line placements. |
| `grid-row` | Shorthand for start/end row line placements. |
| `grid-area` | Assigns an item to a named grid template area. |
| `gap` | Sets spacing between grid rows and columns. |
| `justify-items` | Aligns item contents along the inline (horizontal) axis. |
| `align-items` | Aligns item contents along the block (vertical) axis. |
| `place-items` | Shorthand for setting `align-items` and `justify-items`. |
| `minmax()` | Constrains track sizing within a minimum and maximum range. |

---

## 11. Best Practices & Pitfalls

### Best Practices
- **Use `fr` units** to create fluid layouts that adapt to viewport sizing.
- **Utilize `gap`** instead of margins on individual items for consistent track spacing.
- **Leverage `repeat(auto-fit, minmax(...))`** to handle basic responsive grids cleanly.
- **Keep markup logical** to preserve document outline clarity and accessibility.

### Common Pitfalls
- ❌ **Over-reliance on fixed pixels:** Hardcoding track widths (`px`) breaks mobile responsiveness.
- ❌ **Misapplying Grid for 1D tasks:** Avoid using complex Grid code when a single Flexbox row/column suffices.
- ❌ **Overcomplicating Grid Areas:** Stick to simple area names; overly nested strings quickly become hard to maintain.

---

➡️ Next: [CSS Flexbox](10-CSS-Flexbox.md)

➡️ Next: [CSS Responsive Design](12-CSS-Responsive-Design.md)