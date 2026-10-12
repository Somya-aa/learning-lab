# CSS Pseudo-Classes and Pseudo-Elements

CSS pseudo-classes and pseudo-elements allow you to style elements based on their state or specific parts of their content.

They are useful for creating hover effects, styling form inputs, highlighting selected elements, and adding decorative content without modifying the HTML structure.

---

## 1. What Are Pseudo-Classes?

A pseudo-class selects an element based on its state or position. Pseudo-classes use a **single colon** (`:`).

**Syntax:**

```css
selector:pseudo-class {
    property: value;
}
```

**Example:**

```css
button:hover {
    background-color: blue;
}
```

*The button changes its background color when the user hovers over it.*

---

## 2. The `:hover` Pseudo-Class

The `:hover` pseudo-class applies styles when the pointer moves over an element.

```css
button {
    background-color: royalblue;
    color: white;
    padding: 10px 20px;
    border: none;
}

button:hover {
    background-color: darkblue;
}
```

**Common uses include:**
- Buttons
- Navigation links
- Cards
- Images
- Interactive menus

---

## 3. The `:active` Pseudo-Class

The `:active` pseudo-class applies styles while an element is being activated, such as while a mouse button is held down over a button.

```css
button:active {
    transform: scale(0.95);
}
```

*This makes the button appear slightly smaller while being pressed.*

---

## 4. The `:focus` Pseudo-Class

The `:focus` pseudo-class selects an element that currently has focus. It is especially useful for form fields and keyboard navigation.

```css
input:focus {
    outline: 2px solid royalblue;
    border-color: royalblue;
}
```

*A visible focus indicator helps users understand which element is currently selected.*

---

## 5. The `:focus-visible` Pseudo-Class

`:focus-visible` styles an element when the browser determines that a visible focus indicator is appropriate.

```css
button:focus-visible {
    outline: 3px solid royalblue;
    outline-offset: 3px;
}
```

*This is useful for improving keyboard accessibility without necessarily showing the same focus indicator after every pointer interaction.*

---

## 6. The `:visited` Pseudo-Class

The `:visited` pseudo-class selects links that the browser recognizes as previously visited.

```css
a:visited {
    color: purple;
}
```

*Note: Browsers restrict which properties can be styled for visited links to protect users' browsing privacy.*

---

## 7. The `:link` Pseudo-Class

The `:link` pseudo-class selects links that have not been visited.

```css
a:link {
    color: blue;
}
```

**Example combining link states (LVHA order):**

```css
a:link {
    color: blue;
}

a:visited {
    color: purple;
}

a:hover {
    color: red;
}

a:active {
    color: orange;
}
```

---

## 8. The `:first-child` and `:last-child` Pseudo-Classes

These pseudo-classes select elements according to their position among their siblings.

### `:first-child`
Selects an element when it is the first child of its parent.

```css
li:first-child {
    color: green;
}
```

### `:last-child`
Selects an element when it is the last child of its parent.

```css
li:last-child {
    color: red;
}
```

---

## 9. The `:nth-child()` Pseudo-Class

`:nth-child()` selects elements according to their position among siblings.

```css
li:nth-child(2) {
    color: blue;
}
```

**Pattern selection examples:**

```css
/* Odd/Even */
li:nth-child(odd) {
    background-color: #f2f2f2;
}

li:nth-child(even) {
    background-color: white;
}

/* Formulas */
li:nth-child(3n) {
    color: red;
}

li:nth-child(3n + 1) {
    font-weight: bold;
}
```

---

## 10. The `:not()` Pseudo-Class

The `:not()` pseudo-class selects elements that do not match a specified selector.

```css
button:not(.primary) {
    background-color: gray;
}

input:not([type="checkbox"]) {
    padding: 8px;
}
```

---

## 11. The `:checked` Pseudo-Class

The `:checked` pseudo-class selects checked checkboxes and selected radio buttons.

```css
input:checked {
    accent-color: green;
}
```

---

## 12. The `:disabled` and `:enabled` Pseudo-Classes

These pseudo-classes select form controls according to whether they are enabled or disabled.

```css
/* Disabled state */
input:disabled {
    background-color: #ddd;
    cursor: not-allowed;
}

/* Enabled state */
input:enabled {
    border: 1px solid gray;
}
```

---

## 13. The `:required` and `:optional` Pseudo-Classes

These pseudo-classes select form fields based on whether they are required.

```css
input:required {
    border-left: 3px solid red;
}

input:optional {
    border-left: 3px solid gray;
}
```

---

## 14. The `:valid` and `:invalid` Pseudo-Classes

These pseudo-classes select form controls according to their validation state.

```css
input:valid {
    border-color: green;
}

input:invalid {
    border-color: red;
}
```

*Note: An empty required field is generally invalid until a valid value is entered.*

---

## 15. What Are Pseudo-Elements?

Pseudo-elements allow you to style a specific part of an element or create generated content. They generally use a **double colon** (`::`).

**Syntax:**

```css
selector::pseudo-element {
    property: value;
}
```

**Example:**

```css
p::first-letter {
    font-size: 30px;
    color: red;
}
```

---

## 16. The `::before` Pseudo-Element

`::before` creates a generated content box before an element's existing content.

```css
h2::before {
    content: "★ ";
    color: orange;
}
```

*The `content` property is required for `::before` to generate content.*

---

## 17. The `::after` Pseudo-Element

`::after` creates a generated content box after an element's existing content.

```css
h2::after {
    content: " ✓";
    color: green;
}
```

*Pseudo-elements are useful for decoration, but important information should remain available in the HTML content.*

---

## 18. The `::first-letter` Pseudo-Element

`::first-letter` styles the first letter of a block container's text.

```css
p::first-letter {
    font-size: 32px;
    font-weight: bold;
    color: royalblue;
}
```

---

## 19. The `::first-line` Pseudo-Element

`::first-line` styles the first formatted line of text.

```css
p::first-line {
    font-weight: bold;
    color: darkblue;
}
```

---

## 20. The `::selection` Pseudo-Element

`::selection` styles the portion of text selected by the user.

```css
::selection {
    background-color: yellow;
    color: black;
}
```

---

## 21. The `::placeholder` Pseudo-Element

`::placeholder` styles placeholder text inside form controls.

```css
input::placeholder {
    color: gray;
    font-style: italic;
}
```

---

## 22. The `::marker` Pseudo-Element

`::marker` styles the marker of list items (bullets or numbers).

```css
li::marker {
    color: royalblue;
    font-size: 20px;
}
```

---

## 23. Pseudo-Class vs Pseudo-Element

| Feature | Pseudo-Class | Pseudo-Element |
| :--- | :--- | :--- |
| **Purpose** | Selects an element based on state or position | Styles a part of an element or generated content |
| **Syntax** | Usually uses `:` | Usually uses `::` |
| **Example** | `button:hover` | `p::first-letter` |
| **Common Use** | Hover, focus, checked states | Decorative content, selected text, placeholders |

---

## 24. Practical Example

**HTML:**

```html
<div class="card">
    <h2>Learning CSS</h2>
    <p>Explore pseudo-classes and pseudo-elements.</p>
    <button class="btn">Learn More</button>
</div>
```

**CSS:**

```css
.card {
    width: 300px;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 10px;
}

.card h2::before {
    content: "★ ";
    color: orange;
}

.card p::first-letter {
    font-size: 24px;
    font-weight: bold;
}

.btn {
    padding: 10px 20px;
    background-color: royalblue;
    color: white;
    border: none;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.btn:hover {
    background-color: darkblue;
}

.btn:focus-visible {
    outline: 3px solid orange;
    outline-offset: 3px;
}
```

---

## 25. Common Pseudo-Classes Summary

| Pseudo-Class | Purpose |
| :--- | :--- |
| `:hover` | Pointer is over an element |
| `:active` | Element is being activated |
| `:focus` | Element has focus |
| `:focus-visible` | Browser determines visible focus is appropriate |
| `:visited` | Link has been visited |
| `:first-child` | Element is the first child |
| `:last-child` | Element is the last child |
| `:nth-child()` | Selects elements by sibling position |
| `:not()` | Excludes matching elements |
| `:checked` | Checkbox or radio button is checked |
| `:disabled` | Form control is disabled |
| `:valid` | Form control satisfies its constraints |
| `:invalid` | Form control fails its constraints |

---

## 26. Common Pseudo-Elements Summary

| Pseudo-Element | Purpose |
| :--- | :--- |
| `::before` | Creates generated content before an element's content |
| `::after` | Creates generated content after an element's content |
| `::first-letter` | Styles the first letter |
| `::first-line` | Styles the first formatted line |
| `::selection` | Styles selected text |
| `::placeholder` | Styles placeholder text |
| `::marker` | Styles list markers |

---

## 27. Best Practices

- Use pseudo-classes for states and structural selection.
- Use pseudo-elements for styling specific parts of elements.
- Use `:focus-visible` to provide clear keyboard focus indicators.
- Keep hover effects consistent across interactive elements.
- Do not rely only on hover for important interactions.
- Use `::before` and `::after` primarily for decorative content.
- Keep essential information in the HTML rather than generated content.
- Test form states such as valid, invalid, checked, and disabled.
- Use pseudo-classes and pseudo-elements to reduce unnecessary HTML.

---

## 28. Common Mistakes

### Mistake 1: Confusing Colons
```css
/* Pseudo-class (single colon) */
button:hover { background-color: blue; }

/* Pseudo-element (double colon) */
p::first-letter { color: red; }
```

### Mistake 2: Forgetting `content`
```css
/* Incorrect - will not display */
h2::before { color: red; }

/* Correct */
h2::before {
    content: "★ ";
    color: red;
}
```

### Mistake 3: Using Placeholder Text as a Label
Placeholder text disappears when users enter a value. Always use a proper HTML `<label>` for form fields.

### Mistake 4: Removing Focus Indicators
Avoid removing focus outlines (`outline: none;`) without providing a clear, accessible alternative indicator for keyboard users.

---

## Key Takeaways

- **Pseudo-classes** (`:`) select elements based on state or position (e.g., `:hover`, `:focus`, `:checked`, `:nth-child()`).
- **Pseudo-elements** (`::`) style specific parts of elements or generate content (e.g., `::before`, `::after`, `::selection`).
- Accessible focus indicators are crucial for keyboard navigation.
- They help keep HTML clean by shifting decorative elements and state handling directly into CSS.

---

➡️ Previous: [CSS Transition and Design](13-CSS-Transition-and-Design.md)

➡️ Next: [CSS Best Practices](14-CSS-Best-Practices.md)