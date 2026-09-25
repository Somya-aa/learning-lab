# CSS Text and Fonts

CSS provides many properties for controlling the appearance of text. We can change the font, size, color, alignment, spacing, decoration, and other text-related properties.

---

## Text Color

The `color` property changes the color of text.

**Example:**
```css
p {
    color: #333;
}
```

You can use color names, HEX, RGB, HSL, and other supported color formats.

---

## Text Alignment

The `text-align` property controls the horizontal alignment of text.

**Common values:**
* `left`
* `center`
* `right`
* `justify`

**Example:**
```css
h1 {
    text-align: center;
}

p {
    text-align: justify;
}
```

---

## Text Decoration

The `text-decoration` property adds or removes decorations from text.

**Common values:**
* `none`
* `underline`
* `overline`
* `line-through`

**Example:**
```css
a {
    text-decoration: none;
}

.deleted {
    text-decoration: line-through;
}
```

---

## Text Transform

The `text-transform` property changes the capitalization of text.

**Common values:**
* `uppercase`
* `lowercase`
* `capitalize`
* `none`

**Example:**
```css
h1 {
    text-transform: uppercase;
}

.title {
    text-transform: capitalize;
}
```

---

## Text Indentation

The `text-indent` property specifies the indentation of the first line of a paragraph.

**Example:**
```css
p {
    text-indent: 30px;
}
```

---

## Letter Spacing

The `letter-spacing` property controls the space between characters. Negative values can also be used.

**Example:**
```css
h1 {
    letter-spacing: 2px;
}

h1.condensed {
    letter-spacing: -1px;
}
```

---

## Word Spacing

The `word-spacing` property controls the space between words.

**Example:**
```css
p {
    word-spacing: 5px;
}
```

---

## Line Height

The `line-height` property controls the vertical space between lines of text. A suitable line height improves readability, especially for paragraphs.

**Example:**
```css
p {
    line-height: 1.6;
}
```

---

## Text Shadow

The `text-shadow` property adds a shadow to text.

**Syntax:**
```css
text-shadow: horizontal vertical blur color;
```

**Example:**
```css
h1 {
    text-shadow: 2px 2px 4px gray;
}
```

---

## Text Overflow

The `text-overflow` property controls how overflowing text is displayed. It is commonly used with `overflow` and `white-space`. Long text may be displayed with an ellipsis (`...`).

**Example:**
```css
.title {
    width: 200px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}
```

---

## White Space

The `white-space` property controls how spaces and line breaks are handled.

**Common values:**
* `normal`
* `nowrap`
* `pre`
* `pre-wrap`
* `pre-line`

**Example:**
```css
p {
    white-space: nowrap;
}
```

---

## Font Family

The `font-family` property specifies the typeface used for text. It is common to provide fallback fonts—if the first font is unavailable, the browser tries the next one.

**Example:**
```css
body {
    font-family: "Segoe UI", Arial, sans-serif;
}
```

### Generic Font Families
CSS provides generic font families that can be used as fallbacks:
* `serif`
* `sans-serif`
* `monospace`
* `cursive`
* `fantasy`
* `system-ui`

#### Serif Fonts
Serif fonts have small decorative strokes on letters.
```css
.heading {
    font-family: Georgia, serif;
}
```

#### Sans-Serif Fonts
Sans-serif fonts do not have decorative strokes. They are commonly used for modern interfaces and websites.
```css
body {
    font-family: Arial, sans-serif;
}
```

#### Monospace Fonts
In monospace fonts, each character occupies the same amount of horizontal space. They are commonly used for programming code.
```css
code {
    font-family: "Courier New", monospace;
}
```

---

## Font Size

The `font-size` property controls the size of text.

**Example:**
```css
h1 {
    font-size: 40px;
}

p {
    font-size: 18px;
}
```

CSS supports different units such as `px`, `em`, `rem`, `%`, and `vw`.

---

## Font Weight

The `font-weight` property controls how thick or bold the text appears.

**Common values:** `normal`, `bold`, `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`

* `400` → `normal`
* `700` → `bold`

*Note: The exact available weights depend on the selected font.*

**Example:**
```css
h1 {
    font-weight: 700;
}
```

---

## Font Style

The `font-style` property controls whether text is `normal`, `italic`, or `oblique`.

**Example:**
```css
p {
    font-style: italic;
}
```

---

## Font Variant

The `font-variant` property can control certain variations of a font, such as small caps.

**Example:**
```css
.title {
    font-variant: small-caps;
}
```

---

## Font Shorthand

Several font properties can be combined using the `font` shorthand property. When using shorthand, `font-size` and `font-family` are mandatory components.

**Example:**
```css
p {
    font: italic 600 18px Arial, sans-serif;
}
```

---

## Web Fonts & Custom Fonts

### Google Fonts
Web fonts allow a webpage to use fonts that may not be installed on the user's computer.

**HTML:**
```html
<head>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
</head>
```

**CSS:**
```css
body {
    font-family: "Poppins", sans-serif;
}
```

### Local Fonts with `@font-face`
CSS can load custom font files directly from your project folder.

```css
@font-face {
    font-family: "MyFont";
    src: url("../fonts/myfont.woff2") format("woff2");
}

body {
    font-family: "MyFont", sans-serif;
}
```

---

## Complete Example

### HTML
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Text and Fonts</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <main class="container">
        <h1 class="title">My Learning Lab</h1>
        <h2>CSS Text and Fonts</h2>
        <p class="description">
            CSS allows us to control the appearance, spacing, alignment, and typography of text.
        </p>
        <p class="highlight">
            I am learning CSS step by step.
        </p>
    </main>
</body>
</html>
```

### CSS
```css
body {
    font-family: Arial, sans-serif;
    color: #222;
}

.container {
    max-width: 800px;
    margin: auto;
}

.title {
    text-align: center;
    font-size: 40px;
    font-weight: 700;
    letter-spacing: 1px;
    text-transform: uppercase;
}

h2 {
    font-size: 28px;
    color: #2563eb;
}

.description {
    font-size: 18px;
    line-height: 1.6;
    text-align: justify;
}

.highlight {
    font-weight: bold;
    text-decoration: underline;
}
```

---

## Quick Reference Table

| Property | Purpose |
| :--- | :--- |
| `color` | Sets text color |
| `text-align` | Aligns text |
| `text-decoration` | Adds text decoration |
| `text-transform` | Changes text capitalization |
| `text-indent` | Indents the first line |
| `letter-spacing` | Controls character spacing |
| `word-spacing` | Controls word spacing |
| `line-height` | Controls line spacing |
| `text-shadow` | Adds a shadow |
| `font-family` | Sets the font |
| `font-size` | Sets text size |
| `font-weight` | Controls text thickness |
| `font-style` | Controls italic/normal style |
| `font-variant` | Controls font variants |

---

## Best Practices & Common Mistakes

### Best Practices
1. Choose readable fonts and keep a consistent typography system.
2. Always provide fallback fonts.
3. Use appropriate line height (`1.5`–`1.6` is great for paragraph readability).
4. Maintain sufficient text contrast.
5. Limit decorative text effects to avoid poor readability.
6. Use relative units (`em`, `rem`) for responsive typography.

### Common Mistakes
* **Using Too Many Fonts:** Avoid mixing too many unrelated fonts on a single page.
* **Poor Line Height:** Setting `line-height: 1` can make dense paragraphs hard to read.
* **Poor Text Contrast:** Light grey text on a white background reduces accessibility.
* **Removing Link Underlines Without Alternatives:** If using `text-decoration: none` on `<a>` tags, ensure there is another hover or color signal.

---

## Summary
In this chapter, we covered how to modify text appearance, set up fallback fonts, control spacing, import Google fonts or custom `@font-face` fonts, and apply typography best practices for better visual design and accessibility.

---

⬅️ Previous: [Colors Backgrounds and Opacity](03-Colors-Backgrounds-and-Opacity.md)

➡️ Next: [CSS Box Model](05-CSS-Box-Model.md)