# HTML Attributes

HTML attributes provide additional information about HTML elements. They are written inside the opening tag and usually consist of a name and a value.

```html
<p class="intro">Welcome to my website.</p>
```

Here, `class` is the attribute name and `"intro"` is its value.

---

## Syntax of an Attribute

The general syntax is:

```html
<element attribute="value">
```

**Example:**

```html
<img src="image.jpg" alt="A beautiful image">
```

- `src` specifies the file path/URL of the image.
- `alt` provides accessible fallback text for screen readers and broken links.

---

## Core Identification Attributes

### 1. The `id` Attribute
Assigns a unique identifier to a single element on the page.

```html
<p id="intro">Welcome to my website.</p>
```

- Must be unique within the HTML document.
- Extensively targeted by CSS for single-element styling and JavaScript for DOM manipulation.

### 2. The `class` Attribute
Assigns one or more class names to group elements together.

```html
<p class="highlight">First paragraph.</p>
<p class="highlight">Second paragraph.</p>
```

- Multiple elements can share the same class name.
- Multiple classes can be applied to an element separated by spaces (e.g., `class="btn btn-primary"`).

---

## Linking & Resource Embedding Attributes

### The `href` Attribute
Specifies the target destination URL of a hyperlink (`<a>`).

```html
<!-- External destination -->
<a href="https://example.com">Visit Website</a>

<!-- Internal relative destination -->
<a href="about.html">About</a>
```

### The `src` Attribute
Specifies the path/URL to an external resource (used in `<img>`, `<script>`, `<audio>`, `<video>`, `<iframe>`).

```html
<img src="images/photo.jpg" alt="A photo">
```

### The `alt` Attribute
Provides alternative text for an image to assist screen readers and display fallback text if the file fails to load.

```html
<img src="images/logo.png" alt="My Learning Lab logo">
```

---

## Document & Element Metadata Attributes

### The `title` Attribute
Provides advisory tooltip information displayed when a user hovers over the element.

```html
<p title="This is additional information">Move your mouse over this text.</p>
```

### The `lang` Attribute
Declares the natural language of the document or element.

```html
<html lang="en">
```

### The `target` Attribute
Controls the browsing context in which a linked document opens.

```html
<a href="https://example.com" target="_blank" rel="noopener">Visit Website</a>
```

### The `style` Attribute
Applies inline CSS directly to the element.

```html
<p style="color: blue;">This text is blue.</p>
```

> **Note:** Inline styles are harder to maintain. Larger projects should use external CSS stylesheets instead.

### The `width` and `height` Attributes
Specifies display dimensions (in pixels) for elements like `<img>` and `<video>`.

```html
<img src="images/photo.jpg" alt="A photo" width="400" height="300">
```

---

## Boolean Attributes

Boolean attributes do not require an explicit value. Their presence alone represents the `true` state, and omitting them represents `false`.

Common boolean attributes:
- `required`
- `disabled`
- `checked`
- `readonly`
- `multiple`
- `autofocus`

```html
<!-- Field is mandatory -->
<input type="text" required>

<!-- Button is non-clickable and omitted from submission -->
<button type="button" disabled>Unavailable</button>

<!-- Option is selected by default -->
<input type="checkbox" name="terms" checked>

<!-- Value is non-editable but submitted with form -->
<input type="text" value="HTML Course" readonly>
```

---

## Form-Specific Attributes

### The `placeholder` Attribute
Displays a temporary hint inside an input field before user entry.

```html
<input type="text" placeholder="Enter your name">
```

### The `name` and `value` Attributes
- `name`: Acts as the key when sending submitted form data to the server.
- `value`: Defines the current or initial data payload associated with the control.

```html
<input type="text" name="username" value="Somya">
```

---

## Custom Data Attributes (`data-*`)

Custom data attributes store arbitrary private data directly on elements for use with JavaScript or CSS.

```html
<button data-course="html" data-level="beginner">HTML Course</button>
```

---

## Global Attributes Reference

Global attributes can be applied to nearly all HTML elements:

| Attribute | Purpose |
| :--- | :--- |
| `id` | Gives an element a unique identifier |
| `class` | Assigns one or more classes for styling/scripts |
| `title` | Provides advisory tooltip information |
| `lang` | Specifies the language code of the element |
| `style` | Adds inline CSS rules |
| `hidden` | Hides the element visually and from screen readers |
| `data-*` | Stores custom private client data |
| `tabindex` | Controls keyboard navigation tab focus order |

---

## Rules for Writing Attributes

### 1. Attribute Quotation
Always enclose attribute values in straight double (`"..."`) or single (`'...'`) quotes:

```html
<!-- Recommended -->
<p class="intro">Hello World</p>
```

### 2. Attribute Order
Attribute order does not affect functionality. These two declarations are equivalent:

```html
<img src="image.jpg" alt="Photo">
<img alt="Photo" src="image.jpg">
```

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML Attributes</title>
</head>
<body>

    <header id="main-header" class="website-header">
        <h1 title="Welcome to my website">My Learning Lab</h1>
    </header>

    <main>
        <p id="intro" class="highlight">
            Welcome to my HTML project.
        </p>

        <img src="images/logo.png" alt="My Learning Lab logo" width="300">

        <p>
            <a href="about.html" class="nav-link">About</a>
        </p>

        <form>
            <label for="username">Username:</label>
            <input
                type="text"
                id="username"
                name="username"
                placeholder="Enter your username"
                required
            >

            <br><br>

            <button type="submit">Submit</button>
        </form>
    </main>

</body>
</html>
```

---

## Best Practices

- [x] Use descriptive and meaningful attribute values.
- [x] Ensure every `id` on the page is unique.
- [x] Use `class` for styling shared across multiple elements.
- [x] Always supply useful `alt` text for images; use `alt=""` for decorative images.
- [x] Always enclose attribute values in quotation marks.
- [x] Pair `target="_blank"` with `rel="noopener"` for security.
- [x] Do not replace form `<label>` tags with `placeholder` attributes.
- [x] Prefer external CSS over inline `style` attributes.

---

## Common Mistakes to Avoid

### 1. Duplicate IDs

```html
<!-- Incorrect -->
<p id="intro">First paragraph</p>
<p id="intro">Second paragraph</p>

<!-- Correct -->
<p id="intro">First paragraph</p>
<p id="description">Second paragraph</p>
```

### 2. Missing `alt` Text on Images

```html
<!-- Incorrect -->
<img src="logo.png">

<!-- Correct (informative) -->
<img src="logo.png" alt="My website logo">

<!-- Correct (decorative) -->
<img src="decoration.png" alt="">
```

### 3. Using `placeholder` Instead of `<label>`

```html
<!-- Incorrect -->
<input type="email" placeholder="Email">

<!-- Correct -->
<label for="email">Email:</label>
<input type="email" id="email" name="email" placeholder="example@email.com">
```

---

## Common Attributes Reference Table

| Attribute | Common Use Case |
| :--- | :--- |
| `id` | Unique identification for DOM and CSS hooks |
| `class` | Grouping elements for shared styling and scripts |
| `href` | Destination URL for hyperlinks |
| `src` | External file resource location |
| `alt` | Fallback accessible description for media |
| `title` | Advisory hover tooltip text |
| `lang` | Language definition for document or element |
| `style` | Inline CSS declarations |
| `target` | Browsing context window for link navigation |
| `name` | Field key for submitted form payloads |
| `value` | Field value for input controls |
| `placeholder` | Temporary input guidance hint |
| `required` | Mandatory input validation flag |
| `disabled` | Interactive inactivation flag |
| `checked` | Pre-selection flag for checkboxes and radios |
| `readonly` | Immutability flag for editable inputs |
| `data-*` | Custom data storage prefix |

---

## What I Learned

- The purpose, syntax, and placement of HTML attributes.
- Differentiating between unique identifiers (`id`) and shared styles (`class`).
- How `href` and `src` connect external assets and web pages.
- Accessibility standards with `alt` and `lang`.
- How boolean attributes operate without explicit string values.
- How forms leverage `name`, `value`, `placeholder`, and validation attributes.
- Creating custom data properties with `data-*`.
- Global attributes and debugging attribute formatting errors.

---

## Summary

HTML attributes configure, describe, and enhance HTML elements:

```html
<a href="about.html" class="nav-link" title="Learn more about me">About Me</a>
```

In this example, `href`, `class`, and `title` configure destination, styling hooks, and advisory hints. Leveraging attributes properly creates accessible, valid, and interactive web documents.

---

## Navigation

⬅️ Previous: [HTML Media](09-HTML-Media.md)

➡️ Next: [HTML Layout and Containers](11-HTML-Layout-and-Containers.md)