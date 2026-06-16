# HTML Semantic Elements

**HTML semantics** means using tags that correctly describe the meaning of their content. It's not just about how it looks in the browser, but about what that content *means*.

## Why does semantics matter?

Using semantic HTML is important for:

1. **Search engines** — understand your content better for SEO
2. **Screen readers** — helps people with visual disabilities
3. **Maintainability** — your code is easier to understand and modify
4. **Accessibility** — you meet important web standards

## Example: Semantic vs. Non-semantic

**Incorrect (non-semantic):**
```html
<div>
  <div><b>My Article</b></div>
  <div>Date: June 15</div>
  <div>The article content goes here...</div>
</div>
```

**Correct (semantic):**
```html
<article>
  <h1>My Article</h1>
  <time datetime="2025-06-15">June 15</time>
  <p>The article content goes here...</p>
</article>
```

## Main semantic tags

### General structure
- `<header>` — header of the page or section
- `<nav>` — navigation menu
- `<main>` — unique main content (only one per page)
- `<section>` — thematic section
- `<article>` — independent content (blog post, news, etc.)
- `<aside>` — sidebar or related content
- `<footer>` — page footer

### Text and content
- `<h1>` to `<h6>` — headings (h1 is most important)
- `<p>` — paragraph
- `<strong>` — important text (not just bold)
- `<em>` — emphasis (not just italic)
- `<mark>` — highlighted text
- `<small>` — small text (notes, copyright)
- `<code>` — programming code
- `<pre>` — preformatted text

### Lists
- `<ul>` — unordered list (bullets)
- `<ol>` — ordered list (numbers)
- `<li>` — list item
- `<dl>` — definition list
- `<dt>` — term to define
- `<dd>` — definition of term

### Quotes and references
- `<blockquote>` — long quote
- `<q>` — short inline quote
- `<cite>` — reference to a work
- `<abbr>` — abbreviation

## Structure of a semantic HTML page

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>My Blog</title>
</head>
<body>
  <header>
    <h1>My Website</h1>
    <nav>
      <a href="/">Home</a>
      <a href="/blog">Blog</a>
      <a href="/contact">Contact</a>
    </nav>
  </header>

  <main>
    <article>
      <h2>My First Article</h2>
      <p>Content...</p>
    </article>
  </main>

  <aside>
    <h3>Recent Articles</h3>
    <ul>
      <li><a href="#">Article 1</a></li>
      <li><a href="#">Article 2</a></li>
    </ul>
  </aside>

  <footer>
    <p>&copy; 2025 My Website</p>
  </footer>
</body>
</html>
```

## Difference between `<strong>` and `<b>`

- `<strong>` — **important** text (semantic)
- `<b>` — **bold** text (presentation only)

Same with `<em>` vs `<i>`.

## Accessibility and semantics

When you use semantic HTML:

- Screen readers understand the structure
- Search engines index your content better
- Your page is easier to maintain
- You comply with WCAG standards

Following chapters will show you how to use each of these tags in detail.
