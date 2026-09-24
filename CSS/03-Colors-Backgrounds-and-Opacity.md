# CSS Colors, Backgrounds, and Opacity

CSS provides several properties for controlling the colors and backgrounds of HTML elements. These properties help create visual hierarchy and improve the overall appearance of web pages.

In this chapter, you will learn about CSS colors, background properties, gradients, transparency, and opacity.

---

## CSS Colors

The `color` property is used to change the color of text.

```css
p {
    color: blue;
}
```

This changes the text color of all `<p>` elements to blue.

---

### Color Names

CSS supports many predefined color names.

```css
h1 {
    color: red;
}

p {
    color: green;
}

button {
    color: white;
}
```

#### Common Color Names
* `red`
* `blue`
* `green`
* `yellow`
* `black`
* `white`
* `orange`
* `purple`
* `gray`
* `pink`

---

### RGB Colors

RGB stands for **Red, Green, and Blue**. The `rgb()` function allows you to define a color using three primary values.

**Syntax:**
```css
color: rgb(red, green, blue);
```

Each value normally ranges from `0` to `255`.

```css
p {
    color: rgb(255, 0, 0); /* Pure Red */
}
```

#### Examples:
```css
.red {
    color: rgb(255, 0, 0);
}

.green {
    color: rgb(0, 255, 0);
}

.blue {
    color: rgb(0, 0, 255);
}
```

---

### RGBA Colors

RGBA extends RGB by adding an **alpha channel**, which controls the color's transparency.

**Syntax:**
```css
color: rgba(red, green, blue, alpha);
```

The alpha value ranges from `0` (fully transparent) to `1` (fully opaque).

```css
.box {
    background-color: rgba(0, 0, 255, 0.5); /* 50% Opaque Blue */
}
```

---

### HEX Colors

HEX stands for hexadecimal color notation. A HEX color code always begins with `#`.

```css
h1 {
    color: #ff0000; /* Pure Red */
}
```

#### Common HEX Colors
* `#000000` — Black
* `#ffffff` — White
* `#ff0000` — Red
* `#00ff00` — Green
* `#0000ff` — Blue

#### Shorthand HEX Notation
A shorter three-digit notation is possible when pairs repeat:

```css
p {
    color: #fff; /* Equivalent to #ffffff */
}
```

---

### HSL Colors

HSL stands for **Hue**, **Saturation**, and **Lightness**.

```css
h1 {
    color: hsl(240, 100%, 50%);
}
```

* **Hue:** Position on the color wheel (from `0` to `360`). `240` represents blue.
* **Saturation:** Intensity of the color (`0%` is grayscale, `100%` is full color).
* **Lightness:** Lightness level (`0%` is black, `50%` is normal, `100%` is white).

HSL makes it easy to adjust the brightness and saturation of a color scheme systematically.

---

### HSLA Colors

HSLA adds an alpha channel to HSL for transparency control.

```css
.box {
    background-color: hsla(240, 100%, 50%, 0.5);
}
```

---

## Background Properties

### Background Color

The `background-color` property sets the background color of an element.

```css
body {
    background-color: lightgray;
}

.card {
    background-color: white;
}
```

---

### Background Image

The `background-image` property sets an image as an element's background.

```css
body {
    background-image: url("images/background.jpg");
}
```

---

### Background Repeat

By default, background images tile to fill space. The `background-repeat` property controls this behavior.

```css
body {
    background-image: url("images/pattern.png");
    background-repeat: no-repeat;
}
```

#### Common Values
* `repeat` (default)
* `repeat-x` (repeats horizontally only)
* `repeat-y` (repeats vertically only)
* `no-repeat`

---

### Background Size

The `background-size` property controls the dimensions of a background image.

```css
.hero {
    background-image: url("images/banner.jpg");
    background-size: cover;
}
```

#### Common Values
* `cover`: Scales the image so the background area is completely covered (may crop the image).
* `contain`: Scales the image to fit entirely inside the area (may leave blank space).
* `500px 300px`: Explicit dimensions (width and height).

---

### Background Position

The `background-position` property controls where the background image sits within the element.

```css
.hero {
    background-position: center;
}
```

#### Common Values
* Keywords: `center`, `top`, `bottom`, `left`, `right`
* Combination: `background-position: center top;`

---

### Background Attachment

The `background-attachment` property determines whether the background image scrolls with the page or remains fixed.

```css
body {
    background-attachment: fixed;
}
```

#### Common Values
* `scroll` (default)
* `fixed` (fixed relative to viewport)
* `local`

---

### Background Shorthand

Multiple background properties can be defined in a single declaration:

```css
.hero {
    background: url("images/banner.jpg") center / cover no-repeat;
}
```

---

## CSS Gradients

CSS gradients create smooth color transitions without using external image files.

### Linear Gradient

A linear gradient transitions colors along a straight line.

```css
.box {
    background: linear-gradient(to right, blue, purple);
}
```

Using angles:

```css
.box {
    background: linear-gradient(45deg, blue, purple);
}
```

Multiple color stops:

```css
.box {
    background: linear-gradient(to right, red, yellow, green);
}
```

---

### Radial Gradient

A radial gradient radiates outward from a central point.

```css
.box {
    background: radial-gradient(circle, white, blue);
}
```

---

## Opacity and Transparency

### The `opacity` Property

The `opacity` property sets the transparency level for an entire element (including all its child elements and text).

```css
.box {
    opacity: 0.5; /* 50% transparent */
}
```

* `0`: Completely transparent
* `0.5`: 50% visible
* `1`: Completely opaque

---

### Opacity vs. RGBA

It is critical to distinguish between using `opacity` and an alpha color (like `rgba()`):

* **Using `opacity`:**
  ```css
  .box {
      opacity: 0.5;
  }
  ```
  Makes the **entire element and its contents** (text, borders, children) transparent.

* **Using RGBA/HSLA:**
  ```css
  .box {
      background-color: rgba(0, 0, 255, 0.5);
  }
  ```
  Makes **only the background** transparent, keeping child elements and text fully opaque.

---

## CSS Color Variables

CSS Custom Properties (variables) store reusable color values to maintain consistent themes.

```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #111827;
}

h1 {
    color: var(--primary-color);
}

footer {
    background-color: var(--secondary-color);
}
```

---

## Code Example

### HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Colors and Backgrounds</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="hero">
        <h1>My Learning Lab</h1>
        <p>Learning CSS colors and backgrounds.</p>
    </header>

    <main>
        <section class="card">
            <h2>CSS Colors</h2>
            <p>CSS allows us to control text, backgrounds, gradients, and transparency.</p>
        </section>
    </main>

</body>
</html>
```

### CSS (`style.css`)

```css
:root {
    --primary-color: #2563eb;
    --background-color: #f3f4f6;
    --text-color: #111827;
}

body {
    background-color: var(--background-color);
    color: var(--text-color);
}

.hero {
    background: linear-gradient(135deg, #2563eb, #7c3aed);
    color: white;
    text-align: center;
    padding: 60px;
}

.card {
    background-color: white;
    padding: 30px;
    margin: 30px;
    border-radius: 10px;
}
```

---

## Reference Tables

### Color Formats

| Format | Example | Description |
| :--- | :--- | :--- |
| **Color Name** | `red` | Predefined color name |
| **HEX** | `#ff0000` | Hexadecimal color code |
| **RGB** | `rgb(255, 0, 0)` | Red, Green, Blue channel values |
| **RGBA** | `rgba(255, 0, 0, 0.5)` | RGB with an Alpha channel for transparency |
| **HSL** | `hsl(0, 100%, 50%)` | Hue, Saturation, Lightness values |
| **HSLA** | `hsla(0, 100%, 50%, 0.5)` | HSL with an Alpha channel |

### Common Background Properties

| Property | Purpose |
| :--- | :--- |
| `background-color` | Sets background color |
| `background-image` | Adds a background image |
| `background-repeat` | Controls image tiling/repetition |
| `background-size` | Controls image size |
| `background-position` | Controls image placement |
| `background-attachment` | Controls scrolling behavior (`scroll` vs `fixed`) |
| `background` | Shorthand property for combining multiple background options |

---

## Best Practices

1. **Maintain Consistency:** Use custom CSS variables (`var(--...)`) for primary, secondary, and accent colors.
2. **Ensure Contrast:** Choose text and background combinations that meet accessibility contrast guidelines (WCAG).
3. **Use `background-size: cover` Carefully:** Ensure key content in background images isn't cropped out on smaller screens.
4. **Prefer RGBA/HSLA Over Opacity:** When you only want a semi-transparent background, avoid applying `opacity` to the parent container so child text remains readable.
5. **Optimize Images:** Compress background images before serving them on the web to improve loading performance.

---

## Common Mistakes

### 1. Poor Text Contrast
Avoid light gray text on white or bright backgrounds.

```css
/* Good accessibility practice */
body {
    background-color: #ffffff;
    color: #222222;
}
```

### 2. Unexpected Child Transparency
Using `opacity` on a container dims everything inside it:

```css
/* Incorrect if you only want a transparent background */
.card {
    opacity: 0.5; /* Makes text inside .card semi-transparent as well */
}

/* Correct approach */
.card {
    background-color: rgba(255, 255, 255, 0.5); /* Text stays crisp and opaque */
}
```

### 3. Incorrect Relative File Paths
If your file structure looks like this:

```text
project/
│
├── index.html
├── css/
│   └── style.css
└── images/
    └── background.jpg
```

Reference the image from `style.css` by moving up one directory using `..`:

```css
body {
    background-image: url("../images/background.jpg");
}
```

---

## Key Takeaways

* CSS supports color names, HEX, RGB, RGBA, HSL, and HSLA formats.
* Backgrounds can feature colors, images, linear gradients, or radial gradients.
* The `opacity` property affects an element and all of its child content.
* RGBA and HSLA colors allow you to set transparency specifically for background or text colors without affecting child content opacity.
* CSS variables (`:root`) help manage and maintain consistent design systems.

---

⬅️ Previous: [CSS Syntax and Selectors](02-CSS-Syntax-and-Selectors.md)

➡️ Next: [CSS Text and Fonts](04-CSS-Text-and-Fonts.md)