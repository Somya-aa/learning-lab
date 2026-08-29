
The `<caption>` element provides an accessible title or summary description for the table. It must be placed immediately after the opening `<table>` tag.

```html
<table>
    <caption>Student Marks</caption>
    <tr>
        <th>Name</th>
        <th>Marks</th>
    </tr>
    <tr>
        <td>Somya</td>
        <td>90</td>
    </tr>
</table>
```

---

## Table Semantic Sections

HTML provides semantic container elements to group table rows logically:

- `<thead>` → Header section
- `<tbody>` → Main table body content
- `<tfoot>` → Footer / summary section

```html
<table>
    <thead>
        <tr>
            <th>Subject</th>
            <th>Marks</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>HTML</td>
            <td>90</td>
        </tr>
        <tr>
            <td>CSS</td>
            <td>85</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th>Total</th>
            <th>175</th>
        </tr>
    </tfoot>
</table>
```

---

## Cell Merging Attributes

### 1. `colspan` (Column Span)
The `colspan` attribute allows a single cell to stretch across multiple columns.

```html
<table>
    <tr>
        <th colspan="2">Student Information</th>
    </tr>
    <tr>
        <td>Name</td>
        <td>Somya</td>
    </tr>
</table>
```

### 2. `rowspan` (Row Span)
The `rowspan` attribute allows a single cell to stretch across multiple vertical rows.

```html
<table>
    <tr>
        <th rowspan="2">Name</th>
        <td>HTML</td>
    </tr>
    <tr>
        <td>CSS</td>
    </tr>
</table>
```

---

## Table Accessibility with `scope`

The `scope` attribute explicitly specifies whether a `<th>` header element relates to a column (`scope="col"`) or a row (`scope="row"`). This helps screen readers interpret complex data tables accurately.

```html
<table>
    <tr>
        <th scope="col">Name</th>
        <th scope="col">Course</th>
    </tr>
    <tr>
        <th scope="row">Somya</th>
        <td>HTML</td>
    </tr>
</table>
```

---

## Styling Tables

HTML handles table structure, while CSS should always be used to control visual presentation:

- Borders and border collapse (`border-collapse: collapse;`)
- Padding and cell spacing
- Text alignment
- Background colors and zebra striping
- Width, sizing, and responsive scrolling wrappers

> **Note:** Avoid obsolete HTML presentation attributes such as `border="1"`, `cellpadding`, `cellspacing`, or `bgcolor`.

---

## Complete Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Student Marks</title>
</head>
<body>

    <h1>Student Marks</h1>

    <table>
        <caption>Semester Results</caption>
        <thead>
            <tr>
                <th scope="col">Subject</th>
                <th scope="col">Marks</th>
                <th scope="col">Grade</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>HTML</td>
                <td>90</td>
                <td>A</td>
            </tr>
            <tr>
                <td>CSS</td>
                <td>85</td>
                <td>A</td>
            </tr>
            <tr>
                <td>Programming</td>
                <td>88</td>
                <td>A</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <th scope="row">Average</th>
                <td>87.6</td>
                <td>A</td>
            </tr>
        </tfoot>
    </table>

</body>
</html>
```

---

## Best Practices

- [x] Use tables strictly for tabular data, not for page layout.
- [x] Use `<th>` for header labels and `<td>` for data entries.
- [x] Use `<caption>` to give tables a descriptive, accessible label.
- [x] Structure multi-row tables using `<thead>`, `<tbody>`, and `<tfoot>`.
- [x] Implement the `scope` attribute on `<th>` elements for assistive technologies.
- [x] Rely on CSS for borders, spacing, padding, and alignments.
- [x] Ensure rows and columns remain logically aligned when using `colspan` and `rowspan`.

---

## Common Mistakes

### 1. Using Tables for Page Layout
Do not use `<table>` structures to organize website columns, sidebars, or headers. Use CSS Grid or Flexbox instead.

### 2. Using `<td>` Instead of `<th>` for Headings

```html
<!-- Incorrect -->
<tr>
    <td>Name</td>
    <td>Age</td>
</tr>

<!-- Correct -->
<tr>
    <th>Name</th>
    <th>Age</th>
</tr>
```

### 3. Missing `<tr>` Container Tags

```html
<!-- Incorrect -->
<table>
    <td>HTML</td>
    <td>CSS</td>
</table>

<!-- Correct -->
<table>
    <tr>
        <td>HTML</td>
        <td>CSS</td>
    </tr>
</table>
```

---

## Common Table Elements & Attributes

| Element / Attribute | Description |
| :--- | :--- |
| `<table>` | Root container for table content |
| `<tr>` | Defines a single table row |
| `<th>` | Defines a table header cell |
| `<td>` | Defines a standard table data cell |
| `<caption>` | Defines a title/caption for the table |
| `<thead>` | Groups header content in a table |
| `<tbody>` | Groups the primary body rows of a table |
| `<tfoot>` | Groups summary/footer content in a table |
| `colspan` | Specifies the number of columns a cell should span |
| `rowspan` | Specifies the number of rows a cell should span |
| `scope` | Specifies header relation (`col`, `row`, `colgroup`, `rowgroup`) |

---

## What I Learned

- How to build semantic HTML tables using `<table>`, `<tr>`, `<th>`, and `<td>`.
- How to add meaningful table descriptions using `<caption>`.
- How to segment complex tables into `<thead>`, `<tbody>`, and `<tfoot>`.
- How to merge cells across axes using `colspan` and `rowspan`.
- How to improve accessibility with the `scope` attribute.
- The separation of structural table markup from CSS styling.
- Avoiding common table antipatterns like layout tables and omitted row wrappers.

---

## Summary

HTML tables organize structured datasets into clear, readable rows and columns.

```html
<table>
    <tr>
        <th>Name</th>
        <th>Course</th>
    </tr>
    <tr>
        <td>Somya</td>
        <td>HTML</td>
    </tr>
</table>
```

Combining proper structural elements (`<thead>`, `<tbody>`, `<tfoot>`) with accessible attributes (`scope`, `<caption>`) produces clean, readable, and screen-reader-friendly data presentations.

---

## Navigation

⬅️ Previous: [Tables](05-Tables.md)

➡️ Next: [Forms and Inputs Elements](07-Forms=and-Inputs-Elements.md)