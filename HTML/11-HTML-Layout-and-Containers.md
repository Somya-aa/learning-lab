# HTML Layout and Containers

HTML layout is used to organize the content of a webpage into different sections and containers.

HTML provides elements such as `<div>`, `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, and `<footer>` to structure webpages.

---

## What are Containers?

A container is an HTML element used to group and organize other elements.

The most common container is the `<div>` element:

```html
<div>
    <h2>About Me</h2>
    <p>I am learning HTML.</p>
</div>
```

The `<div>` groups the heading and paragraph together.

---

## Generic Containers: `<div>` and `<span>`

### The `<div>` Element
The `<div>` element is a generic block-level container. It does not carry semantic meaning on its own:

```html
<div class="container">
    <h1>My Website</h1>
    <p>Welcome to my website.</p>
</div>
```

Use `<div>` when no suitable semantic element applies.

### The `<span>` Element
The `<span>` element is a generic inline container:

```html
<p>
    I am learning <span>HTML</span> and CSS.
</p>
```

Unlike `<div>`, `<span>` does not start on a new line and is primarily used for targeting small inline text segments with CSS or JavaScript.

---

## Block-Level vs. Inline Elements

### Block-Level Elements
- Begin on a new line.
- Stretch across the full available width of their parent container.
- **Examples:** `<div>`, `<p>`, `<section>`, `<header>`, `<footer>`, `<main>`, `<article>`

```html
<div>First container</div>
<div>Second container</div>
```

### Inline Elements
- Remain within the flow of the same text line.
- Take up only as much width as necessary.
- **Examples:** `<span>`, `<a>`, `<strong>`, `<em>`

```html
<p>This is <span>inline content</span> inside a paragraph.</p>
```

---

## Semantic Layout Elements

### 1. Header (`<header>`)
Represents introductory content, site titles, or header groups:

```html
<header>
    <h1>My Learning Lab</h1>
    <p>Learning Web Development</p>
</header>
```

### 2. Navigation (`<nav>`)
Encloses major site navigation links:

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="projects.html">Projects</a>
    <a href="contact.html">Contact</a>
</nav>
```

### 3. Main (`<main>`)
Represents the central, unique content of the webpage:

```html
<main>
    <h1>My Projects</h1>
    <p>These are my web development projects.</p>
</main>
```

### 4. Section (`<section>`)
Groups related content into a standalone thematic section, typically accompanied by a heading:

```html
<section>
    <h2>About HTML</h2>
    <p>HTML is used to structure webpages.</p>
</section>
```

### 5. Article (`<article>`)
Represents self-contained composition intended for independent distribution or syndication (blog posts, news, tutorials, reviews, forum entries):

```html
<article>
    <h2>Learning HTML</h2>
    <p>HTML is the foundation of web development.</p>
</article>
```

### 6. Aside (`<aside>`)
Contains secondary or related information not part of the primary content flow (e.g., sidebars, callout boxes):

```html
<aside>
    <h2>Related Topics</h2>
    <ul>
        <li>CSS</li>
        <li>JavaScript</li>
    </ul>
</aside>
```

### 7. Footer (`<footer>`)
Defines the footer region containing copyright notices, contact information, or supplementary links:

```html
<footer>
    <p>Copyright 2026 My Learning Lab</p>
</footer>
```

---

## Basic Page Layout Architecture

```text
+-----------------------------+
|           HEADER            |
+-----------------------------+
|           NAVBAR            |
+-----------------------------+
|                             |
|            MAIN             |
|                             |
|  +-----------------------+  |
|  |       SECTION         |  |
|  +-----------------------+  |
|                             |
|  +-----------------------+  |
|  |       ARTICLE         |  |
|  +-----------------------+  |
|                             |
+-----------------------------+
|           FOOTER            |
+-----------------------------+
```

### Underlying Semantic Markup

```html
<header>
    Website Header
</header>

<nav>
    Navigation Links
</nav>

<main>
    <section>
        Main Section
    </section>

    <article>
        Article Content
    </article>
</main>

<footer>
    Footer
</footer>
```

---

## Nesting Containers

Containers can be placed inside other containers to divide complex web layouts into manageable modular sections:

```html
<div class="container">
    <div class="header">
        <h1>My Website</h1>
    </div>

    <div class="content">
        <div class="section">
            <h2>About</h2>
            <p>About my website.</p>
        </div>
    </div>
</div>
```

---

## Semantic Containers vs. `<div>`

Avoid wrapping every section inside generic `<div>` tags.

```html
<!-- Avoid (Overusing div) -->
<div class="header">
    <h1>My Website</h1>
</div>
<div class="navigation">
    <a href="index.html">Home</a>
</div>
<div class="main">
    <p>Main content</p>
</div>

<!-- Prefer (Semantic Structure) -->
<header>
    <h1>My Website</h1>
</header>
<nav>
    <a href="index.html">Home</a>
</nav>
<main>
    <p>Main content</p>
</main>
```

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>HTML Layout</title>
</head>
<body>

    <header>
        <h1>My Learning Lab</h1>
        <p>Learning HTML and Web Development</p>
    </header>

    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
        <a href="projects.html">Projects</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main>
        <section>
            <h2>About HTML</h2>
            <p>HTML is used to create the structure of webpages.</p>
        </section>

        <article>
            <h2>My HTML Project</h2>
            <p>This project contains my HTML learning and practice files.</p>
        </article>

        <aside>
            <h2>Related Topics</h2>
            <ul>
                <li>CSS</li>
                <li>JavaScript</li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>Copyright 2026 My Learning Lab</p>
    </footer>

</body>
</html>
```

---

## Container Reference Table

| Element | Type | Purpose |
| :--- | :--- | :--- |
| `<div>` | Block | Generic block container |
| `<span>` | Inline | Generic inline text wrapper |
| `<header>` | Block | Header / introductory content container |
| `<nav>` | Block | Primary navigation link group |
| `<main>` | Block | Primary page content |
| `<section>` | Block | Thematic grouping of related content |
| `<article>` | Block | Self-contained, syndicatable content |
| `<aside>` | Block | Tangential or sidebar content |
| `<footer>` | Block | Document or section footer content |

---

## Multi-Level Layout Containers

Real-world web layouts combine semantic landmarks with utility containers for styling constraints:

```html
<main>
    <section>
        <div class="container">
            <h2>My Projects</h2>

            <div class="project">
                <h3>HTML Project</h3>
                <p>My first HTML project.</p>
            </div>
        </div>
    </section>
</main>
```

---

## Best Practices

- [x] Use semantic tags whenever they accurately describe the content meaning.
- [x] Use `<div>` only when no fitting semantic tag exists.
- [x] Use `<span>` strictly for targeted inline text segments.
- [x] Keep container nesting shallow and clean.
- [x] Assign descriptive CSS class names to layout containers.
- [x] Maintain a single `<main>` element per document.
- [x] Control positions, alignments, and spacings through CSS (Grid/Flexbox).

---

## Common Mistakes to Avoid

### 1. "Div Soup" (Excessive Generic Containers)

```html
<!-- Incorrect -->
<div>
    <div>
        <div>
            <h1>My Website</h1>
        </div>
    </div>
</div>

<!-- Correct -->
<header>
    <h1>My Website</h1>
</header>
```

### 2. Illogical or Over-Nesting

```html
<!-- Clean and Readable Structure -->
<section>
    <h2>My Projects</h2>
    <div>
        <p>Project information.</p>
    </div>
</section>
```

---

## What I Learned

- The definition and purpose of HTML containers.
- How to use `<div>` for block-level grouping and `<span>` for inline grouping.
- Key differences between block-level and inline display flows.
- Structuring a complete web page with `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, and `<footer>`.
- How to nest containers modularly without over-complicating markup.
- Best practices for layout clarity, maintainability, and accessibility.

---

## Summary

HTML layout organizes page content into semantic landmarks and reusable containers:

```html
<header>
    Header
</header>

<nav>
    Navigation
</nav>

<main>
    <section>
        Main Content
    </section>
    <article>
        Article
    </article>
    <aside>
        Related Content
    </aside>
</main>

<footer>
    Footer
</footer>
```

Semantic elements make the document readable and accessible, while `<div>` and `<span>` serve as generic structural wrappers when custom styling or behavior is required.

---

## Navigation

⬅️ Previous: [HTML Attributes](10-HTML-Attributes.md)

➡️ Next: [HTML Features](12-HTML-Features.md)