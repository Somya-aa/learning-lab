*Avoid:*
```html
<img src="photo.jpg">
```

*Prefer:*
```html
<img src="photo.jpg" alt="Description of the photo">
```

### 3. Forms Without Labels
Unlabeled inputs are confusing to both screen reader users and touch devices:

*Avoid:*
```html
<input type="text">
```

*Prefer:*
```html
<label for="username">Username:</label>
<input type="text" id="username" name="username">
```

---

## What I Learned

In this chapter, we covered:
- Key features provided by HTML.
- Collecting user inputs with HTML forms.
- Working with diverse form input types.
- Native audio and video multimedia embedding.
- Enhancing document structure and accessibility with semantic tags.
- Structuring tabular data and structured lists.
- Hyperlinks and image management.
- Embedding external resources via `<iframe>`.
- Graphic generation with Canvas and SVG.
- Rendering characters with HTML entities.
- Custom metadata storage with `data-*` attributes.
- Foundational accessibility and client-side form validation.
- Responsive setup via viewport meta configurations.

---

## Summary

HTML provides the foundational structure and semantics for interactive, accessible web applications:
- **Forms & Validation:** Collect, format, and check input data.
- **Media & Graphics:** Native `<audio>`, `<video>`, `<canvas>`, and `<svg>`.
- **Structure:** Semantic tags, structured tables, and ordered/unordered lists.
- **Navigation & Embeds:** Hyperlinks, media embeds, and external frames.
- **Customization & Accessibility:** `data-*` attributes, global attributes, entities, and ARIA/accessibility readiness.

HTML supplies the structure and meaning of a page, CSS handles visual layout and styling, and JavaScript provides dynamic interactivity.

---

## Navigation

⬅️ Previous: [HTML Layout and Containers](11-HTML-Layout-and-Containers.md)

➡️ Next: [HTML Best Practices](13-HTML-Best-Practices.md)