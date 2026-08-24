# HTML Structure and Syntax

HTML documents follow a standard structure that helps browsers understand and display webpage content correctly.

Understanding HTML structure and syntax is important before creating larger webpages.

---

# Basic HTML Structure

A basic HTML document contains:

```html
<!DOCTYPE html>
<html>

<head>
    <title>My Webpage</title>
</head>

<body>

    <h1>Hello World</h1>
    <p>Welcome to my webpage.</p>

</body>

</html>
```

The main parts are:

- `<!DOCTYPE html>`
- `<html>`
- `<head>`
- `<body>`

---

# DOCTYPE Declaration

The `<!DOCTYPE html>` declaration tells the browser that the document uses HTML5.

Example:

```html
<!DOCTYPE html>
```

It should be placed at the beginning of an HTML document.

---

# HTML Root Element

The `<html>` element is the root of an HTML document.

Example:

```html
<html>

    <!-- Other HTML elements -->

</html>
```

All major parts of the webpage are placed inside the `<html>` element.

---

# Head Element

The `<head>` element contains information about the webpage.

Example:

```html
<head>

    <title>My Website</title>

</head>
```

The `<head>` can contain:

- Page title
- Metadata
- Links to CSS files
- Favicons
- Other document information

Most content inside `<head>` is not directly displayed on the webpage.

---

# Body Element

The `<body>` contains the visible content of a webpage.

Example:

```html
<body>

    <h1>Welcome</h1>

    <p>This is my webpage.</p>

</body>
```

Content such as headings, paragraphs, images, links, lists, tables, and forms is normally placed inside the `<body>`.

---

# HTML Tags

HTML uses tags to define elements.

Example:

```html
<p>Hello World</p>
```

The parts are:

```text
<p>            Opening tag
Hello World    Content
</p>           Closing tag
```

The opening and closing tags together define the element.

---

# Opening and Closing Tags

Most HTML elements have an opening tag and a closing tag.

Example:

```html
<h1>My Heading</h1>
```

Here:

```text
<h1>        Opening tag
My Heading  Content
</h1>       Closing tag
```

The closing tag contains a forward slash `/`.

---

# Void Elements

Some HTML elements do not have closing tags.

These are called **void elements**.

Examples:

```html
<br>
<hr>
<img src="image.jpg" alt="Image">
<input type="text">
<meta charset="UTF-8">
<link rel="stylesheet" href="style.css">
```

They perform their function without containing normal content.

---

# Nesting Elements

HTML elements can be placed inside other elements. This is called **nesting**.

Example:

```html
<body>

    <h1>My Website</h1>

    <p>This is my <strong>first</strong> webpage.</p>

</body>
```

Here, `<strong>` is nested inside the `<p>` element.

---

# Proper Nesting

Elements should be properly nested.

Correct:

```html
<p>This is <strong>important</strong>.</p>
```

Incorrect:

```html
<p>This is <strong>important.</p></strong>
```

Always close nested elements in the correct order.

---

# HTML Attributes

Attributes provide additional information about elements.

Example:

```html
<a href="https://example.com">Visit Website</a>
```

Here:

```text
href
```

is an attribute.

Another example:

```html
<img src="photo.jpg" alt="Profile photo">
```

Here:

- `src` specifies the image location.
- `alt` provides alternative text.

---

# Attribute Syntax

Attributes are normally written inside the opening tag.

General syntax:

```text
attribute="value"
```

Example:

```html
<p class="intro">Welcome to my website.</p>
```

Here:

```text
class = attribute
intro = value
```

Multiple attributes can be used:

```html
<img src="photo.jpg" alt="My Photo" width="300">
```

---

# HTML Comments

Comments allow developers to add notes inside HTML code.

Syntax:

```html
<!-- This is a comment -->
```

Example:

```html
<!-- Website header -->

<h1>My Website</h1>
```

Comments are not displayed on the webpage.

They are useful for explaining code and organizing large documents.

---

# HTML Indentation

Indentation makes HTML easier to read.

Example:

```html
<body>

    <header>

        <h1>My Website</h1>

    </header>

    <main>

        <p>Welcome to my website.</p>

    </main>

</body>
```

Good indentation helps developers understand the relationship between elements.

---

# HTML Case

HTML tag names are generally case-insensitive.

For example, browsers can interpret:

```html
<P>Hello</P>
```

However, lowercase tags are recommended:

```html
<p>Hello</p>
```

Using lowercase tags keeps code consistent and readable.

---

# HTML Whitespace

HTML usually ignores extra spaces and line breaks in normal text.

For example:

```html
<p>Hello       World</p>
```

will generally display the text with normal spacing.

For intentional spacing or layout, CSS should normally be used instead of adding many spaces.

---

# Special Characters

Some characters have special meanings in HTML.

For example:

```html
<p>5 &lt; 10</p>
```

The browser displays:

```text
5 < 10
```

Common HTML entities include:

| Entity | Character |
|--------|-----------|
| `&lt;` | `<` |
| `&gt;` | `>` |
| `&amp;` | `&` |
| `&quot;` | `"` |
| `&nbsp;` | Non-breaking space |

---

# HTML File Structure

A typical project may contain multiple HTML files.

Example:

```text
website/
│
├── index.html
├── about.html
├── contact.html
└── services.html
```

`index.html` is commonly used as the main webpage.

---

# Linking HTML Pages

HTML pages can be connected using the `<a>` element.

Example:

```html
<a href="about.html">About Us</a>
```

Another example:

```html
<a href="contact.html">Contact</a>
```

This allows users to navigate between webpages.

---

# Complete HTML Example

```html
<!DOCTYPE html>
<html>

<head>

    <meta charset="UTF-8">

    <meta name="description" content="My Learning Lab website">

    <title>Learning Lab</title>

</head>

<body>

    <header>

        <h1>My Learning Lab</h1>

    </header>

    <main>

        <h2>About Me</h2>

        <p>
            I am learning web development step by step.
        </p>

        <a href="about.html">Learn More</a>

    </main>

</body>

</html>
```

---

# Common Structural Elements

Some commonly used HTML elements for organizing webpages are:

| Element | Purpose |
|---------|---------|
| `<html>` | Root element |
| `<head>` | Document information |
| `<title>` | Page title |
| `<body>` | Visible content |
| `<header>` | Header section |
| `<nav>` | Navigation |
| `<main>` | Main content |
| `<section>` | Section of content |
| `<footer>` | Footer section |

Semantic elements such as `<header>`, `<nav>`, `<main>`, and `<footer>` will be covered in more detail in later chapters.

---

# Best Practices

- Always use `<!DOCTYPE html>`.
- Use lowercase HTML tags.
- Use proper indentation.
- Close elements correctly.
- Use meaningful attribute names and values.
- Use quotes around attribute values.
- Keep HTML structure organized.
- Use comments when they improve readability.
- Use semantic elements where appropriate.
- Separate HTML structure from CSS styling.

---

# Common Mistakes

### Forgetting the DOCTYPE

Incorrect:

```html
<html>
```

Better:

```html
<!DOCTYPE html>
<html>
```

---

### Incorrect Nesting

Incorrect:

```html
<p><strong>Hello</p></strong>
```

Correct:

```html
<p><strong>Hello</strong></p>
```

---

### Missing Quotes Around Attributes

Incorrect:

```html
<a href=about.html>About</a>
```

Correct:

```html
<a href="about.html">About</a>
```

---

### Forgetting to Close Elements

Incorrect:

```html
<p>Hello
```

Correct:

```html
<p>Hello</p>
```

---

# What I Learned

In this chapter, I learned:

- The basic structure of an HTML document.
- The purpose of `<!DOCTYPE html>`.
- The role of `<html>`, `<head>`, and `<body>`.
- Opening and closing tags.
- Void elements.
- HTML nesting.
- HTML attributes.
- HTML comments.
- Proper indentation.
- HTML entities.
- Linking multiple HTML pages.
- Common HTML structure elements.
- Common HTML syntax mistakes.

---

# Summary

HTML follows a structured syntax that allows browsers to understand webpage content.

A basic HTML document follows this structure:

```html
<!DOCTYPE html>
<html>

<head>
    <title>Page Title</title>
</head>

<body>

    <h1>Page Heading</h1>
    <p>Page content.</p>

</body>

</html>
```

Understanding HTML structure and syntax makes it easier to create clean, readable, and maintainable webpages.

---

## Navigation

⬅️ Previous: [Introduction to HTML](01-Introduction-to-HTML.md)

➡️ Next: [Headings and Paragraphs](03-Headings-and-Paragraphs.md)
