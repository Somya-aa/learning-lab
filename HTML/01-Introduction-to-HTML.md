# Introduction to HTML

HTML stands for **HyperText Markup Language**. It is the standard markup language used to create and structure content on web pages.

---

# What is HTML?

HTML is used to create the basic structure of a webpage.

A webpage can contain:

- Headings
- Paragraphs
- Images
- Links
- Lists
- Tables
- Forms
- Videos
- Audio

HTML provides the structure of a webpage, while CSS is used for styling and JavaScript is used for interaction.

---

# How HTML Works

HTML documents are written using HTML elements.

The browser reads the HTML code and converts it into a webpage.

Example:

```html
<h1>Hello World</h1>
<p>This is my first webpage.</p>
```

---

# Basic HTML Document

A basic HTML document looks like this:

```html
<!DOCTYPE html>
<html>

<head>
    <title>My First Webpage</title>
</head>

<body>

    <h1>Hello World</h1>
    <p>Welcome to my webpage.</p>

</body>

</html>
```

---

# Understanding the Basic Structure

## `<!DOCTYPE html>`

Tells the browser that the document uses HTML5.

```html
<!DOCTYPE html>
```

## `<html>`

The root element of the webpage.

```html
<html>
    ...
</html>
```

## `<head>`

Contains information about the webpage.

```html
<head>
    <title>My Website</title>
</head>
```

## `<title>`

Defines the title displayed in the browser tab.

```html
<title>My Website</title>
```

## `<body>`

Contains the visible content of the webpage.

```html
<body>
    <h1>Welcome</h1>
    <p>This is my website.</p>
</body>
```

---

# HTML Tags

HTML uses tags to define elements.

Example:

```html
<p>Hello World</p>
```

Here:

- `<p>` → Opening tag
- `Hello World` → Content
- `</p>` → Closing tag

---

# HTML Elements

An HTML element generally consists of:

```text
Opening Tag + Content + Closing Tag
```

Example:

```html
<h1>My Website</h1>
```

Some elements do not require a closing tag.

Example:

```html
<br>
```

These are called **void elements**.

---

# HTML Attributes

Attributes provide additional information about an element.

Example:

```html
<a href="https://example.com">Visit Website</a>
```

Here, `href` is an attribute.

Another example:

```html
<img src="image.jpg" alt="Sample image">
```

Here, `src` and `alt` are attributes.

---

# Headings

HTML provides six levels of headings:

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

`<h1>` is the highest-level heading and `<h6>` is the lowest.

---

# Paragraphs

The `<p>` element is used to create paragraphs.

```html
<p>
    HTML is used to structure content on web pages.
</p>
```

Multiple paragraphs can be created using multiple `<p>` elements.

```html
<p>First paragraph.</p>
<p>Second paragraph.</p>
```

---

# Comments

HTML comments are used to add notes inside the code.

```html
<!-- This is an HTML comment -->
```

Comments are not displayed on the webpage.

---

# HTML File Extension

HTML files normally use the `.html` extension.

Examples:

```text
index.html
about.html
contact.html
```

The most common starting page of a website is:

```text
index.html
```

---

# Creating Your First HTML File

Create a file named:

```text
index.html
```

Add:

```html
<!DOCTYPE html>
<html>

<head>
    <title>My First Page</title>
</head>

<body>

    <h1>Hello World!</h1>

    <p>
        This is my first HTML webpage.
    </p>

</body>

</html>
```

Save the file and open it in a web browser.

---

# HTML and Web Development

HTML is one of the core technologies used for web development.

```text
HTML
  ↓
Structure

CSS
  ↓
Style

JavaScript
  ↓
Interaction
```

HTML creates the structure, CSS controls the appearance, and JavaScript adds interaction.

---

# Basic HTML Example

```html
<!DOCTYPE html>
<html>

<head>
    <title>My Learning Lab</title>
</head>

<body>

    <h1>Welcome to My Website</h1>

    <p>
        I am learning HTML as part of my Learning Lab project.
    </p>

    <h2>My Goal</h2>

    <p>
        I want to learn web development step by step.
    </p>

</body>

</html>
```

---

# Best Practices

- Use `<!DOCTYPE html>` at the beginning.
- Use lowercase HTML tags.
- Use proper indentation.
- Use meaningful page titles.
- Close elements properly when required.
- Use comments when necessary.
- Use meaningful file names.
- Keep HTML code clean and organized.

---

# Common HTML Elements

| Element | Purpose |
|---------|---------|
| `<html>` | Root of the HTML document |
| `<head>` | Contains document information |
| `<title>` | Defines the page title |
| `<body>` | Contains visible page content |
| `<h1>` - `<h6>` | Headings |
| `<p>` | Paragraph |
| `<br>` | Line break |
| `<a>` | Link |
| `<img>` | Image |
| `<!-- -->` | Comment |

---

# What I Learned

In this chapter, I learned:

- What HTML is.
- Why HTML is used.
- How HTML works with a browser.
- The basic structure of an HTML document.
- HTML tags and elements.
- HTML attributes.
- Headings and paragraphs.
- HTML comments.
- HTML file extensions.
- How to create my first HTML webpage.
- The difference between HTML, CSS, and JavaScript.

---

# Summary

HTML is the foundation of a webpage. It provides the structure that browsers use to display content.

The basic structure is:

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

Understanding this structure is the first step toward building websites with HTML.

---

## Navigation

⬅️ Previous: [HTML README](README.md)

➡️ Next: [HTML Structure and Syntax](02-HTML-Structure-and-Syntax.md)
