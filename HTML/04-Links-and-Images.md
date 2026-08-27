# Links and Images

Links and images are important parts of webpages. Links allow users to navigate between pages and websites, while images add visual content to a webpage.

---

## HTML Links

The `<a>` (anchor) element is used to create hyperlinks in HTML.

### Basic Syntax

```html
<a href="https://example.com">Visit Website</a>
```

The `href` (Hypertext REFerence) attribute specifies the destination URL of the link.

---

### Linking to Another HTML Page

You can use links to connect pages within the same website.

**Example:**

```html
<a href="about.html">About Us</a>
<a href="contact.html">Contact</a>
```

A typical multi-page project structure:

```text
website/
├── index.html
├── about.html
└── contact.html
```

---

### Absolute vs. Relative URLs

#### Absolute URLs
An absolute URL contains the complete web address, including protocol (`http://` or `https://`) and domain name. Commonly used when linking to external websites.

```html
<a href="https://www.example.com">Visit Example</a>
```

#### Relative URLs
A relative URL points to a file or resource based on the current file's location.

```html
<!-- Linking to a file in the same directory -->
<a href="about.html">About</a>

<!-- Linking to a file inside a subdirectory -->
<a href="pages/about.html">About</a>
```

---

### Opening Links in a New Tab

The `target` attribute controls where the link opens. Use `target="_blank"` to open in a new tab, along with `rel="noopener"` for security and performance.

```html
<a href="https://example.com" target="_blank" rel="noopener">Open Website</a>
```

---

### Email and Telephone Links

#### Email Links (`mailto:`)
Opens the user's default email client.

```html
<a href="mailto:example@email.com">Send Email</a>
```

#### Telephone Links (`tel:`)
Prompts a phone call on mobile devices or call-enabled applications.

```html
<a href="tel:+1234567890">Call Us</a>
```

---

### Linking to a Section on the Same Page (Anchor Links)

An element can have an `id` attribute that serves as an anchor destination:

```html
<!-- Destination section -->
<h2 id="about">About Us</h2>

<!-- Link jumping to the destination -->
<a href="#about">Go to About Us</a>
```

---

## HTML Images

The `<img>` element is used to embed images into a webpage. It is a **void element** (self-closing), meaning it does not have a closing tag.

### Basic Syntax

```html
<img src="image.jpg" alt="Description of image">
```

---

### The `src` and `alt` Attributes

- **`src` (Source):** Specifies the path/URL to the image file.
- **`alt` (Alternative Text):** Provides text descriptions for accessibility and fallback.

```html
<img src="images/photo.jpg" alt="A sample photo">
<img src="cat.jpg" alt="A cat sitting on a chair">
```

#### Why `alt` text matters:
1. Displayed if the image fails to load.
2. Read aloud by screen readers for visually impaired users.
3. Indexed by search engine crawlers for SEO.

> **Tip:** Write clear, concise, and meaningful descriptions instead of generic filenames like `image123.jpg`.

---

### Image Width and Height

You can specify dimensions directly in HTML attributes:

```html
<img src="photo.jpg" alt="Sample photo" width="400" height="300">
```

*Note: For responsive and scalable designs, controlling image dimensions with CSS is generally preferred.*

---

### Common Image File Formats

| Format | Common Use Cases |
| :--- | :--- |
| **JPEG / JPG** | Photographs and complex realistic images |
| **PNG** | Graphics requiring transparency and lossless detail |
| **GIF** | Simple animations |
| **SVG** | Scalable vector graphics, logos, and UI icons |
| **WebP** | Modern web format offering superior compression |
| **AVIF** | Next-generation efficient image format |

---

### Understanding Image File Paths

#### Same or Sub-directory
Given project structure:

```text
website/
├── index.html
└── images/
    ├── logo.png
    └── photo.jpg
```

To display `photo.jpg` from `index.html`:

```html
<img src="images/photo.jpg" alt="Sample photo">
```

#### Parent Directory (`..` Notation)
Given project structure:

```text
website/
├── index.html
├── images/
│   └── photo.jpg
└── pages/
    └── about.html
```

To display `photo.jpg` from `about.html`, use `../` to navigate up one folder:

```html
<img src="../images/photo.jpg" alt="Sample photo">
```

---

### Linking an Image (Clickable Images)

Wrap an `<img>` element inside an `<a>` element:

```html
<a href="https://example.com">
    <img src="logo.png" alt="Visit Example">
</a>
```

---

### Semantics: `<figure>` and `<figcaption>`

The `<figure>` element groups an image and its associated caption defined by `<figcaption>`.

```html
<figure>
    <img src="mountain.jpg" alt="Mountain landscape">
    <figcaption>A breathtaking view of the mountain landscape at sunset.</figcaption>
</figure>
```

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Links and Images Example</title>
</head>
<body>

    <header>
        <h1>My Website</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <main>
        <h2>My Favorite Image</h2>

        <figure>
            <img src="images/photo.jpg" alt="A beautiful landscape" width="400">
            <figcaption>A beautiful landscape.</figcaption>
        </figure>

        <p>
            Visit 
            <a href="https://example.com" target="_blank" rel="noopener">
                Example Website
            </a> 
            to learn more.
        </p>
    </main>

</body>
</html>
```

---

## Best Practices

- [x] Use meaningful and descriptive link text (avoid generic terms like "click here").
- [x] Use relative paths for local assets and absolute URLs for external links.
- [x] Always include informative `alt` text for images.
- [x] Use `alt=""` (empty alt attribute) for purely decorative images so screen readers skip them.
- [x] Optimize image file sizes to ensure fast page load speeds.
- [x] Select the appropriate image format (e.g., SVG for logos, WebP/JPEG for photos).
- [x] Pair `target="_blank"` with `rel="noopener"` or `rel="noreferrer"` for security.
- [x] Verify link targets and asset paths before deployment.

---

## Common Mistakes to Avoid

### 1. Missing `href` Attribute
```html
<!-- Incorrect -->
<a>About</a>

<!-- Correct -->
<a href="about.html">About</a>
```

### 2. Missing `alt` Attribute
```html
<!-- Incorrect -->
<img src="photo.jpg">

<!-- Correct -->
<img src="photo.jpg" alt="A golden retriever playing in the grass">
```

### 3. Incorrect Relative Paths
If the file is inside an `images/` directory:
```html
<!-- Incorrect -->
<img src="photo.jpg" alt="Photo">

<!-- Correct -->
<img src="images/photo.jpg" alt="Photo">
```

### 4. Non-descriptive Link Text
```html
<!-- Avoid -->
<a href="about.html">Click here</a> to learn about our team.

<!-- Prefer -->
Learn more about our team on our <a href="about.html">About Us page</a>.
```

---

## Summary of Elements & Attributes

| Element / Attribute | Description |
| :--- | :--- |
| `<a>` | Creates a hyperlink |
| `href` | Specifies the URL or destination path |
| `target` | Determines browsing context (e.g., `_blank` for new tab) |
| `rel` | Specifies relationship with linked resource (`noopener`, `noreferrer`) |
| `<img>` | Embeds an image file |
| `src` | Path / URL to image resource |
| `alt` | Fallback alternative text for accessibility |
| `width` / `height` | Dimensions in pixels |
| `<figure>` | Self-contained container for media content |
| `<figcaption>` | Caption / legend for a `<figure>` element |

---

## What I Learned

- How to construct hyperlinks using the `<a>` tag and `href` attribute.
- The differences and use cases between relative and absolute URLs.
- Creating email (`mailto:`) and telephone (`tel:`) action links.
- Building in-page navigation anchors with element IDs.
- Embedding images using `<img>` and configuring `src`, `alt`, and dimensions.
- Directory path traversal techniques (e.g., subdirectories and parent `../` paths).
- Grouping media semantically with `<figure>` and `<figcaption>`.
- Accessibility considerations and writing effective `alt` text.
- Essential best practices and debugging common link/image mistakes.

---

## Summary

Links and images form the backbone of modern interactive web development. A basic link connects documents:

```html
<a href="about.html">About Us</a>
```

While an image provides visual enrichment:

```html
<img src="images/photo.jpg" alt="Sample photo">
```

Writing semantic HTML with proper paths and accessibility attributes ensures your site is fast, usable, and accessible to everyone.

---

## Navigation

⬅️ Previous: [Headings and Paragraphs](03-Headings-and-Paragraphs.md)

➡️ Next: [Lists](05-Lists.md)