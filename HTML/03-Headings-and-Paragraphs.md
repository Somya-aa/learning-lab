# Headings and Paragraphs

Headings and paragraphs are some of the most basic and important elements in HTML. They help organize webpage content and make it easier for users to read and understand.

---

# HTML Headings

HTML provides six levels of headings:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

`<h1>` is the highest-level heading, while `<h6>` is the lowest-level heading.

---

# Using h1

The `<h1>` element is normally used for the main heading of a webpage.

Example:

```html
<h1>My Learning Lab</h1>
```

A page should generally have a clear main heading that describes its primary content.

---

# Using h2 to h6

Lower-level headings are used to organize sections and subsections.

Example:

```html
<h1>Web Development</h1>

<h2>HTML</h2>

<h3>Headings</h3>

<h3>Paragraphs</h3>

<h2>CSS</h2>

<h3>Selectors</h3>
```

This creates a clear content hierarchy.

---

# Heading Hierarchy

Headings should normally follow a logical order.

Good structure:

```text
h1
 ├── h2
 │    ├── h3
 │    └── h3
 └── h2
      └── h3
```

Avoid choosing headings only because of their visual size. CSS should be used to control appearance.

---

# HTML Paragraphs

The `<p>` element is used to create paragraphs.

Example:

```html
<p>
    HTML is used to structure content on webpages.
</p>
```

Each `<p>` element represents a separate paragraph.

---

# Multiple Paragraphs

Multiple paragraphs can be written using separate `<p>` elements.

Example:

```html
<p>
    HTML provides the structure of a webpage.
</p>

<p>
    CSS is used to style the webpage.
</p>

<p>
    JavaScript can add interaction.
</p>
```

Using separate paragraph elements makes the content structure clear.

---

# Line Breaks

The `<br>` element creates a line break.

Example:

```html
<p>
    Hello World!<br>
    Welcome to my webpage.
</p>
```

The output appears on two lines.

`<br>` is a void element, so it does not need a closing tag.

Use `<br>` for meaningful line breaks, not for creating large spaces between sections.

---

# Horizontal Rules

The `<hr>` element represents a thematic break between sections.

Example:

```html
<h2>HTML</h2>

<p>HTML is used to structure webpages.</p>

<hr>

<h2>CSS</h2>

<p>CSS is used to style webpages.</p>
```

Like `<br>`, `<hr>` is a void element.

---

# Paragraph Formatting

HTML provides elements that can give meaning or emphasis to text.

Strong text:

```html
<strong>Important information</strong>
```

Emphasized text:

```html
<em>Important point</em>
```

Marked text:

```html
<mark>Highlighted text</mark>
```

Small text:

```html
<small>Additional information</small>
```

---

# Bold and Italic Text

The `<b>` element draws attention to text without adding strong importance.

```html
<b>Bold text</b>
```

The `<i>` element represents text set apart from normal text.

```html
<i>Italic text</i>
```

For meaningful emphasis, `<strong>` and `<em>` are generally preferred.

---

# Deleted and Inserted Text

Deleted text:

```html
<del>Old price</del>
```

Inserted text:

```html
<ins>New price</ins>
```

Example:

```html
<p>
    Price: <del>$50</del> <ins>$35</ins>
</p>
```

---

# Subscript and Superscript

The `<sub>` element creates subscript text.

```html
H<sub>2</sub>O
```

The `<sup>` element creates superscript text.

```html
x<sup>2</sup>
```

These are useful for chemical and mathematical expressions.

---

# Quotations

The `<blockquote>` element is used for longer quotations.

Example:

```html
<blockquote>
    Learning never stops.
</blockquote>
```

For short quotations, use `<q>`:

```html
<p>
    He said, <q>Practice makes progress.</q>
</p>
```

---

# Abbreviations

The `<abbr>` element can provide additional information about an abbreviation.

Example:

```html
<p>
    <abbr title="HyperText Markup Language">HTML</abbr>
    is used to create webpages.
</p>
```

The `title` attribute provides the full meaning.

---

# Combining Headings and Paragraphs

Headings and paragraphs are commonly used together.

Example:

```html
<h1>My Website</h1>

<p>
    Welcome to my website.
</p>

<h2>About Me</h2>

<p>
    I am learning web development.
</p>

<h2>My Goals</h2>

<p>
    I want to improve my HTML and CSS skills.
</p>
```

This creates a simple and readable document structure.

---

# Complete Example

```html
<!DOCTYPE html>
<html>

<head>
    <title>Headings and Paragraphs</title>
</head>

<body>

    <h1>My Learning Lab</h1>

    <p>
        Welcome to my HTML learning journey.
    </p>

    <hr>

    <h2>What I Am Learning</h2>

    <p>
        I am learning <strong>HTML</strong> to understand
        how webpages are structured.
    </p>

    <h3>My Goal</h3>

    <p>
        My goal is to build clean and accessible webpages.
    </p>

</body>

</html>
```

---

# Best Practices

- Use headings to create a logical content hierarchy.
- Use `<h1>` for the main heading.
- Use `<h2>` and lower levels for sections.
- Use `<p>` for paragraphs.
- Use `<br>` only when a real line break is needed.
- Use `<strong>` and `<em>` when the meaning requires importance or emphasis.
- Do not use headings only to make text look bigger.
- Use CSS for visual styling.
- Keep content organized and readable.

---

# Common Mistakes

### Using Headings Only for Size

Avoid:

```html
<h1>Small Text</h1>
<h4>Very Large Text</h4>
```

Choose headings based on their meaning and structure.

---

### Using Multiple br Tags for Spacing

Avoid:

```html
<p>Hello</p>
<br>
<br>
<br>
<p>World</p>
```

Use CSS to control spacing instead.

---

### Using Empty Paragraphs for Spacing

Avoid:

```html
<p></p>
<p></p>
```

Use CSS for layout and spacing.

---

# Common Elements

| Element | Purpose |
|---------|---------|
| `<h1>` - `<h6>` | Headings |
| `<p>` | Paragraph |
| `<br>` | Line break |
| `<hr>` | Thematic break |
| `<strong>` | Strong importance |
| `<em>` | Emphasis |
| `<mark>` | Highlighted text |
| `<small>` | Smaller text |
| `<del>` | Deleted text |
| `<ins>` | Inserted text |
| `<sub>` | Subscript |
| `<sup>` | Superscript |
| `<blockquote>` | Long quotation |
| `<q>` | Short quotation |
| `<abbr>` | Abbreviation |

---

# What I Learned

In this chapter, I learned:

- How to create headings using `<h1>` to `<h6>`.
- How to create paragraphs using `<p>`.
- How to organize content using heading hierarchy.
- How to create line breaks using `<br>`.
- How to create thematic breaks using `<hr>`.
- How to emphasize and highlight text.
- How to use subscript and superscript.
- How to create quotations.
- How to use abbreviations.
- Common mistakes when working with headings and paragraphs.
- How to create clean and readable webpage content.

---

# Summary

Headings and paragraphs are fundamental HTML elements used to organize webpage content.

A simple structure can look like:

```html
<h1>Main Heading</h1>

<p>
    Introduction to the webpage.
</p>

<h2>First Section</h2>

<p>
    Content for the first section.
</p>

<h2>Second Section</h2>

<p>
    Content for the second section.
</p>
```

Using headings and paragraphs correctly creates a clear structure that is easier for users, browsers, and assistive technologies to understand.

---

## Navigation

⬅️ Previous: [HTML Structure and Syntax](02-HTML-Structure-and-Syntax.md)

➡️ Next: [Links and Images](04-Links-and-Images.md)
