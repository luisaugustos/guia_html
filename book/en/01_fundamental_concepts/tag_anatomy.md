# Detailed Anatomy of Tags

Understanding the complete structure of a tag is fundamental for working correctly with HTML.

## Parts of a tag

```html
<p class="important" id="paragraph-1">This is content</p>
```

1. **Opening symbol** (`<`) — marks the start
2. **Tag name** (`p`) — defines what type of element it is
3. **Attributes** (`class="important" id="paragraph-1"`) — additional information
4. **Closing symbol** (`>`) — ends the opening tag
5. **Content** (`This is content`) — what is displayed or processed
6. **Closing tag** (`</p>`) — marks the end of the element

## Common tag types

### Containers
Tags that contain other tags or content:

```html
<div>...</div>    <!-- Generic block -->
<section>...</section>  <!-- Semantic section -->
<article>...</article>  <!-- Article -->
<nav>...</nav>    <!-- Navigation -->
<header>...</header>    <!-- Header -->
<footer>...</footer>    <!-- Footer -->
<main>...</main>   <!-- Main content -->
```

### Text tags
Tags that format text:

```html
<h1>...</h1>  <!-- Heading level 1 -->
<p>...</p>    <!-- Paragraph -->
<strong>...</strong>  <!-- Strong text (important) -->
<em>...</em>  <!-- Emphasis -->
<small>...</small>    <!-- Small text -->
<span>...</span>  <!-- Generic inline text -->
```

### Empty (self-closing)
They don't contain content or a closing tag:

```html
<img src="..." alt="...">
<input type="...">
<br>
<hr>
<meta name="..." content="...">
<link rel="..." href="...">
```

## Hierarchy and correct nesting

Tags must be nested correctly:

```html
<!-- ✓ CORRECT: Elements close in order -->
<div>
  <p>
    <strong>Important text</strong> in a paragraph
  </p>
</div>

<!-- ✗ INCORRECT: Tag overlap -->
<div>
  <p>
    <strong>Important text</p>
  </strong>
</div>
```

## Common attributes in all tags

Some attributes work in almost any tag:

| Attribute | Description | Example |
|---|---|---|
| `id` | Unique element identifier | `id="section-1"` |
| `class` | CSS class for styling | `class="highlighted"` |
| `style` | Inline CSS styles | `style="color: red;"` |
| `title` | Text that appears on hover | `title="See more"` |
| `data-*` | Custom data | `data-number="42"` |

## DOCTYPE and HTML declaration

The **DOCTYPE** is not really a tag, but it's mandatory at the beginning of the document:

```html
<!DOCTYPE html>
```

This tells the browser to use the HTML5 specification. In earlier HTML versions there were several variants, but in HTML5 there's only one.

Immediately after comes the root tag:

```html
<!DOCTYPE html>
<html lang="en">
  ...
</html>
```

The `lang` attribute specifies the main language of the document (important for accessibility and SEO).

## HTML validation

To verify that your HTML is correct, you can use the official W3C validator:

1. Go to [https://validator.w3.org/](https://validator.w3.org/)
2. Enter your code or URL
3. The validator will show you errors and warnings

Keeping HTML valid is important for:
- Browser compatibility
- Accessibility
- SEO (search engine ranking)
- Code maintainability
