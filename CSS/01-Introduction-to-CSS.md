
---

## Best Practices

- Prefer external CSS for larger projects.
- Use meaningful class names.
- Keep CSS properly formatted and indented.
- Use comments when they improve understanding.
- Avoid unnecessary inline styles.
- Keep related styles organized.
- Use consistent naming conventions.
- Avoid repeating the same CSS unnecessarily.
- Keep HTML structure separate from presentation.

---

## Common Mistakes

### 1. Forgetting to Link External CSS
**Incorrect:**
```html
<head>
    <title>My Website</title>
</head>
```

**Correct:**
```html
<head>
    <title>My Website</title>
    <link rel="stylesheet" href="style.css">
</head>
```

### 2. Missing Semicolon
**Incorrect:**
```css
p {
    color: blue
    font-size: 18px;
}
```

**Correct:**
```css
p {
    color: blue;
    font-size: 18px;
}
```

### 3. Incorrect CSS File Path
If the CSS file is inside a `css` folder:
```text
website/
├── index.html
└── css/
    └── style.css
```

**The correct link is:**
```html
<link rel="stylesheet" href="css/css/style.css">
```
*(or `href="css/style.css"`, depending on relative structure)*

---

## What I Learned

In this chapter, I learned:

1. What CSS is.
2. Why CSS is used.
3. The difference between HTML and CSS.
4. The three ways to add CSS.
5. How inline CSS works.
6. How internal CSS works.
7. How external CSS works.
8. Basic CSS syntax.
9. Selectors, properties, and values.
10. How CSS connects with HTML.
11. How CSS files are organized.
12. Basic concepts of the CSS cascade.
13. CSS best practices and common mistakes.

---

## Summary

CSS is used to control the appearance and presentation of HTML webpages [cite: 1].

**The basic CSS structure is:**
```css
selector {
    property: value;
}
```

**For example:**
```css
h1 {
    color: blue;
    font-size: 40px;
}
```

**CSS can be added using:**
1. Inline CSS
2. Internal CSS
3. External CSS

For larger projects, external CSS is generally preferred because it keeps styling separate from HTML and allows styles to be reused across multiple pages.