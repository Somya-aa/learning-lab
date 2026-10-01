# CSS Display and Visibility

The `display` and `visibility` properties control how HTML elements appear and behave in a webpage layout.

Understanding these properties is essential for creating flexible, responsive layouts and controlling element visibility.

---

## 1. The `display` Property

The `display` property defines how an element participates in the page flow and layout.

```css
.box {
    display: block;
}
```

**Common values include:**
* `block`
* `inline`
* `inline-block`
* `none`
* `flex`
* `grid`

---

## 2. Block Elements

A block-level element:
* Starts on a **new line** by default.
* Occupies the **full available width** of its parent container.
* Accepts custom `width` and `height` properties.

### Example

```html
<div>First Box</div>
<div>Second Box</div>
```

```css
div {
    display: block;
}
```

### Common Block Elements
* `<div>`
* `<p>`
* `<h1>` – `<h6>`
* `<section>`
* `<header>`
* `<footer>`

---

## 3. Inline Elements

An inline element:
* Does **not** start on a new line; sits inline with adjacent content.
* Takes up only as much width as its content requires.
* Ignores top/bottom `margin` and `height` properties.

### Example

```html
<span>Hello</span> <span>World</span>
```

### Common Inline Elements
* `<span>`
* `<a>`
* `<strong>`
* `<em>`

---

## 4. Inline-Block (`inline-block`)

`inline-block` combines the key features of inline and block elements:
* Placed inline on the same line as neighboring elements.
* Respects custom `width`, `height`, padding, and margins.

```css
.box {
    display: inline-block;
    width: 150px;
    height: 100px;
}
```

This is useful for creating horizontal component layouts like button bars or navigation items without using floats.

---

## 5. `display: none`

`display: none` completely hides an element and removes it from the document flow.

```css
.hidden {
    display: none;
}
```

**Key behaviors:**
* The element becomes completely invisible.
* It **occupies no space** in the layout.
* Surrounding elements collapse into the freed space.

```html
<p class="hidden">This text is hidden and takes up no space.</p>
```

---

## 6. `visibility: hidden`

`visibility: hidden` hides an element visually while preserving its footprint in the document flow.

```css
.hidden {
    visibility: hidden;
}
```

**Difference:**
* `display: none` $\rightarrow$ Hidden + **No layout space taken**.
* `visibility: hidden` $\rightarrow$ Hidden + **Layout space preserved**.

---

## 7. `display` vs. `visibility` Comparison

| Property | Visible? | Occupies Space? | Triggers Reflow? |
| :--- | :---: | :---: | :---: |
| `display: block` | Yes | Yes | N/A |
| `display: inline` | Yes | Yes | N/A |
| `display: none` | **No** | **No** | Yes |
| `visibility: hidden` | **No** | **Yes** | No |

---

## 8. Changing Default Display Behavior

You can override an HTML element's natural display behavior with CSS:

```css
/* Converts inline anchor tags into full-width block elements */
a {
    display: block;
}

/* Places list items horizontally inline */
li {
    display: inline-block;
}
```

---

## 9. `display: flex`

The `flex` value converts an element into a Flexbox container, creating a 1D layout context for its direct children.

```css
.container {
    display: flex;
    gap: 20px;
}
```

Flexbox simplifies aligning items horizontally or vertically and distributing extra space along rows or columns.

---

## 10. `display: grid`

The `grid` value converts an element into a CSS Grid container, enabling 2D column-and-row layouts.

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```

---

## 11. `display: contents`

`display: contents` causes an element's outer container box to vanish from the DOM layout tree, leaving its child elements to act as direct children of the parent element above it.

```css
.wrapper {
    display: contents;
}
```

> ⚠️ **Note:** Use with caution, as `display: contents` can affect accessibility semantics for screen readers on certain HTML elements.

---

## 12. Visibility Property Values

The `visibility` property controls visual rendering with three primary values:

* `visible`: Default value; renders the element normally.
* `hidden`: Hides the element while keeping layout space.
* `collapse`: Removes table rows/columns or behaves like `hidden` on non-table elements.

```css
.box {
    visibility: visible;
}

.box.invisible {
    visibility: hidden;
}
```

---

## 13. Opacity vs. Visibility

| Feature | `opacity: 0` | `visibility: hidden` |
| :--- | :--- | :--- |
| **Visual State** | Fully transparent | Completely invisible |
| **Space Taken** | Yes | Yes |
| **Interactivity** | Can still click/hover | Cannot receive click events |
| **Transitions** | Animatable / smooth | Discrete state change |

---

## 14. Practical Example

### HTML
```html
<div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box hidden">Box 3</div>
</div>
```

### CSS
```css
.container {
    display: flex;
    gap: 20px;
}

.box {
    padding: 20px;
    border: 1px solid black;
}

.hidden {
    display: none;
}
```

**Result:** `Box 3` is completely omitted, allowing `Box 1` and `Box 2` to sit side-by-side without leaving a blank gap for the 3rd box.

---

## 15. Summary of Common Display Values

| Value | Purpose |
| :--- | :--- |
| `block` | Creates a block box (new line, full width). |
| `inline` | Creates an inline box (flows with text). |
| `inline-block` | Flow inline while supporting width & height. |
| `none` | Removes element and space from document flow. |
| `flex` | Activates Flexbox container. |
| `grid` | Activates Grid container. |
| `contents` | Strips container box; keeps children in layout. |

---

## 16. Best Practices

1. **Choose appropriate layout display modes:** Use `flex` or `grid` for major layout blocks instead of relying heavily on legacy `inline-block` hacks.
2. **Use `display: none`** when removing elements completely from view (e.g., collapsed dropdown menus).
3. **Use `visibility: hidden`** when reserved layout dimensions must be preserved to prevent sudden visual layout shifts (CLS).
4. **Consider Accessibility:** Hiding elements via CSS also hides them from assistive technology like screen readers unless targeted specifically.

---

## 17. Common Mistakes

* ❌ **Confusing `display: none` and `visibility: hidden`:** `display: none` strips layout space; `visibility: hidden` keeps it.
* ❌ **Overusing `inline-block` for page layouts:** `inline-block` introduces whitespace margin issues between elements; use `flex` or `grid` instead.
* ❌ **Hiding critical elements improperly:** Hiding form labels or key context blocks without providing accessible screen reader alternatives (`sr-only` patterns).

---

## Key Takeaways

```
  DISPLAY VALUES AT A GLANCE:

  [ block ]         Starts on new line, fills container width
  [ inline ]        Stays inline, fits content width
  [ inline-block ]  Stays inline, respects width/height
  [ none ]          Hidden & removed from document layout flow
  [ flex / grid ]   Modern container layout engines
```

---

➡️ Next: [CSS Margin Padding and Borders](07-CSS-Margin-Padding-and-Borders.md)

➡️ Next: [CSS Positioning](09-CSS-Positioning.md)