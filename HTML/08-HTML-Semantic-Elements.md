### 5. Article (`<article>`)
Represents a self-contained composition intended for independent distribution or reuse (e.g., blog posts, news stories, forum threads, reviews).

```html
<article>
    <h2>Learning HTML</h2>
    <p>HTML is the foundation of web development.</p>
</article>
```

### 6. Aside (`<aside>`)
Contains secondary content tangentially related to the surrounding content (e.g., sidebars, callout boxes, related links).

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
Represents the footer region for its nearest sectioning root or document (e.g., copyright notices, contact details, site maps).

```html
<footer>
    <p>Copyright 2026 My Learning Lab</p>
</footer>
```

---

## Media, Interactive & Formatting Elements

### Media with Figure (`<figure>` and `<figcaption>`)
Encapsulates self-contained media assets (images, diagrams, code listings) alongside a descriptive caption.

```html
<figure>
    <img src="images/logo.png" alt="My Learning Lab logo">
    <figcaption>My Learning Lab logo.</figcaption>
</figure>
```

### Expandable Details (`<details>` and `<summary>`)
Creates native interactive disclosure widgets that toggle content visibility without JavaScript.

```html
<details>
    <summary>What is HTML?</summary>
    <p>HTML is used to structure content on webpages.</p>
</details>
```

### Machine-Readable Time (`<time>`)
Represents specific timestamps or dates with a standardized `datetime` attribute.

```html
<p>
    The project was started on
    <time datetime="2026-09-01">September 1, 2026</time>.
</p>
```

---

## Semantic vs. Non-Semantic Elements

`<div>` and `<span>` are generic container elements used primarily for styling or script hooks when no semantic element applies.

- **`<div>`**: Generic block-level container.
- **`<span>`**: Generic inline container.

```html
<div>
    <p>This is a block with a <span class="highlight">highlighted</span> inline phrase.</p>
</div>
```

---

## Semantic Document Blueprint

```html
<header>
    Website Header
</header>

<nav>
    Navigation Links
</nav>

<main>
    <section>
        Main Section Content
    </section>

    <article>
        Independent Article
    </article>

    <aside>
        Related Sidebar Content
    </aside>
</main>

<footer>
    Footer Information
</footer>
```

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Semantic HTML</title>
</head>
<body>

    <header>
        <h1>My Learning Lab</h1>
        <p>Learning Web Development</p>
    </header>

    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main>
        <section>
            <h2>HTML</h2>
            <p>HTML is used to structure webpages.</p>
        </section>

        <article>
            <h2>Why Learn HTML?</h2>
            <p>HTML provides the foundation for building webpages and web applications.</p>
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

## Reference Tables

### Semantic Elements

| Element | Description / Purpose |
| :--- | :--- |
| `<header>` | Introductory container or navigation header |
| `<nav>` | Container for major site navigation links |
| `<main>` | Dominant, primary content unique to the page |
| `<section>` | Standalone thematic grouping of content |
| `<article>` | Self-contained, independently distributable content |
| `<aside>` | Secondary/tangential content or sidebar |
| `<footer>` | Document or section footer information |
| `<figure>` | Self-contained media container |
| `<figcaption>` | Caption or legend for a `<figure>` |
| `<details>` | Native interactive disclosure toggle |
| `<summary>` | Visible heading/summary for a `<details>` element |
| `<time>` | Machine-readable date/time representation |

### Non-Semantic Elements

| Element | Description / Purpose |
| :--- | :--- |
| `<div>` | Generic block-level container |
| `<span>` | Generic inline container |

---

## Best Practices

- [x] Use semantic elements whenever they accurately describe the content meaning.
- [x] Use a single `<main>` element per document for the central content.
- [x] Reserve `<nav>` for major navigation link collections.
- [x] Give `<section>` and `<article>` elements descriptive headings (`<h2>`–`<h6>`).
- [x] Use `<article>` for content that retains independent meaning out of context.
- [x] Use `<aside>` for secondary context, callouts, or sidebars.
- [x] Fallback to `<div>` and `<span>` only when no meaningful semantic tag fits.

---

## Common Mistakes to Avoid

### 1. "Div Soup" (Overusing Generic Containers)

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

### 2. Multiple `<main>` Tags
Avoid multiple top-level `<main>` elements in a single page document.

```html
<!-- Correct -->
<main>
    <!-- Primary page content goes here -->
</main>
```

### 3. Using `<section>` Without Heading or Purpose
A `<section>` should always encapsulate a distinct thematic topic.

```html
<!-- Correct -->
<section>
    <h2>My Projects</h2>
    <p>These are some of my projects.</p>
</section>
```

---

## What I Learned

- The definition and purpose of semantic HTML tags.
- How semantic markup boosts accessibility, SEO, and maintainability.
- Practical implementation of `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, and `<footer>`.
- How to structure media semantically with `<figure>` and `<figcaption>`.
- Creating native interactive accordions with `<details>` and `<summary>`.
- Using `<time>` with the `datetime` attribute for standard machine parsing.
- Distinguishing between semantic elements and generic wrappers (`<div>` / `<span>`).

---

## Summary

Semantic HTML provides explicit meaning to page layout and content structure:

```html
<header>
    <h1>My Website</h1>
</header>

<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
</nav>

<main>
    <section>
        <h2>About</h2>
        <p>Information about the website.</p>
    </section>
</main>

<footer>
    <p>Copyright 2026</p>
</footer>
```

Structuring documents with semantic tags produces accessible, SEO-friendly, and maintainable web pages.

---

## Navigation

⬅️ Previous: [Forms and Inputs Elements](07-Forms=and-Inputs-Elements.md)

➡️ Next: [HTML Media](09-HTML-Media.md)